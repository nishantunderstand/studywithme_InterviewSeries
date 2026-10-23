
# Production Monitoring & Troubleshooting — Interview Notes

## 1. Response Time vs Latency vs p95 vs p99

|Term|Meaning|
|---|---|
|Response Time|Total time taken by the server to return a response.|
|Latency|Time taken for a request to travel through a system and receive a response, depending on how it's measured.|
|p95|95% of requests complete within this time; 5% take longer.|
|p99|99% of requests complete within this time; 1% take longer.|

Example: If p95 = 500 ms and p99 = 2 seconds, most requests are fast, but a small number are significantly slower.

## 2. Datadog vs New Relic

- Datadog — monitors application performance, infrastructure, logs, metrics, traces, and alerts.
    
- New Relic — helps track application response times, errors, distributed traces, and database performance.
    

Real-world scenario: Your Spring Boot API takes 5 seconds to respond. Use APM traces to identify whether the delay comes from Java code, SQL queries, another microservice, or an external API.

## 3. Web Service Troubleshooting Scenarios

When an API fails, check these areas:

|Area|What to verify|
|---|---|
|Request body|Required fields, null values, invalid data types|
|HTTP status code|400, 401, 403, 404, 405, 415, 500, 503|
|Endpoint|Correct URL, path variables, query parameters|
|Headers|Authorization, Content-Type, Accept|
|Environment|Local, QA, UAT, Production; configuration and dependencies|

### Why does HTTP 400 occur?

400 Bad Request usually means the server cannot process the request because its input is invalid.

Example:

```
{
  "name": "",
  "age": -5,
  "email": "invalid-email"
}
```

If the API requires a non-empty name, positive age, and valid email, validation can reject this request.

In Spring Boot:

```
@PostMapping("/employees")
public ResponseEntity<String> createEmployee(
        @Valid @RequestBody EmployeeRequest request) {
    return ResponseEntity.ok("Employee created");
}
```

Common reasons for a 400:

- Missing or malformed JSON.
    
- Invalid field type, such as sending a string instead of a number.
    
- Validation failure using `@NotBlank`, `@Min`, or `@Email`.
    
- Missing required request parameters.
    
- Incorrect date or enum format.
    

Debugging approach: Check the request payload, headers, API logs, validation errors, and exception details.

## 4. Common HTTP Status Codes

| Code | Meaning                | Example                           |
| ---- | ---------------------- | --------------------------------- |
| 200  | OK                     | Data fetched successfully         |
| 201  | Created                | Employee created                  |
| 400  | Bad Request            | Invalid request body              |
| 401  | Unauthorized           | Missing or invalid authentication |
| 403  | Forbidden              | User lacks permission             |
| 404  | Not Found              | Employee or endpoint not found    |
| 405  | Method Not Allowed     | POST sent to a GET-only endpoint  |
| 415  | Unsupported Media Type | Incorrect `Content-Type`          |
| 429  | Too Many Requests      | Rate limit exceeded               |
| 500  | Internal Server Error  | Unhandled server exception        |
| 502  | Bad Gateway            | Invalid upstream response         |
| 503  | Service Unavailable    | Service overloaded or unavailable |
| 504  | Gateway Timeout        | Upstream service timed out        |

## 5. Slow Response Time — Database and SQL

Suppose `GET /employees` normally responds in 200 ms but suddenly takes 4 seconds.

Client Request

Spring Boot API

Check application logs and APM traces

Database / SQL Query

Check query execution time and execution plan

Identify Bottleneck

Slow query, missing index, locks, connection pool exhaustion, or excessive data

### Common reasons SQL queries are slow

1. Missing index: Full table scan instead of efficient index lookup.
    
2. Inefficient SQL: Unnecessary joins, subqueries, or expensive operations.
    
3. Too much data: Fetching thousands of rows without pagination.
    
4. Lock contention: Another transaction holds locks needed by the query.
    
5. N+1 queries: Hibernate executes one query for the parent and additional queries for each child.
    
6. Connection pool exhaustion: Requests wait for an available database connection.
    
7. Database resource pressure: High CPU, memory pressure, or disk I/O.
    

### How to troubleshoot

- Check APM traces to identify which SQL statement is slow.
    
- Run `EXPLAIN` to inspect the execution plan.
    
- Check indexes and whether the database performs a full table scan.
    
- Check database locks, connection pool metrics, and query logs.
    
- Optimize the query and measure performance again.
    

Interview answer: “I first identify whether the latency comes from the application or database using APM traces. If SQL is the bottleneck, I inspect the execution plan using `EXPLAIN`, check indexes, joins, locks, and connection pool utilization, then optimize and compare the response time.”