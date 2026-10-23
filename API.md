- Response Time
- Latency 
- p95
- p99
- Data Relic
- Data Dog 
- APM 


---

- p95: 95% of API requests complete within this response time; 5% take longer.
- p99: 99% of API requests complete within this response time; 1% take longer

Interview tip: *Average response time can hide slow requests*. 
p95 and p99 help us understand how the slowest portion of requests performs.


APM : Application Performance Monitoring 

| Approach       | Tool                          | Purpose                                                          |
| -------------- | ----------------------------- | ---------------------------------------------------------------- |
| Manual testing | Postman                       | Check an individual API's response time                          |
| Load testing   | JMeter, k6                    | Measure response time under concurrent traffic                   |
| APM monitoring | Datadog, New Relic, Dynatrace | Monitor live application performance and investigate bottlenecks |

---

https://www.instagram.com/reels/DbbLjV0oC1e/
- Latency : Time for one request to make a round trip.
- Throughput : How many requests get handled per second
- Bandwidth  : The max Data Capacity of the link itself
- Jitter :  Variation in Delay B/W Consecutitve Packet 

---

| Area             | What to verify                                             |
| ---------------- | ---------------------------------------------------------- |
| Request body     | Required fields, null values, invalid data types           |
| HTTP status code | 400, 401, 403, 404, 405, 415, 500, 503                     |
| Endpoint         | Correct URL, path variables, query parameters              |
| Headers          | Authorization, Content-Type, Accept                        |
| Environment      | Local, QA, UAT, Production; configuration and dependencies |

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


---
Slow Response Time 
- Database
- SQL Query | Explain


---
