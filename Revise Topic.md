Q4. What is Schema Registry? 🤔🤔🤔

| Interview question                                    | Key point to answer                                                         |
| ----------------------------------------------------- | --------------------------------------------------------------------------- |
| How do you prevent duplicate Kafka processing?        | Idempotency keys, deduplication, and correct offset handling                |
| How do you handle a downstream service failure?       | Timeouts, retries with backoff, circuit breaker, fallback where appropriate |
| How do you maintain consistency across microservices? | SAGA, compensating transactions, and eventual consistency                   |
| How do you prevent stale cache data?                  | TTL, cache invalidation, and update strategies                              |
| How do you troubleshoot high JVM memory usage?        | Heap dump, GC logs, Java Flight Recorder, and memory-leak analysis          |
| How do you secure APIs?                               | TLS, token validation, authorization checks, and least privilege            |
| How do you improve a slow database query?             | Execution plan, indexing, query optimization, and connection-pool analysis  |


What is difference between BDD and TDD

I knew few questions, 
What is difference between Spy and Mock.

What difference between MockBean and Mock

What are the tools we use for load and stress testing

What is difference between BDD and TDD



---


| `findById(id)`                                         | `getReferenceById(id)`                                                      |
| ------------------------------------------------------ | --------------------------------------------------------------------------- |
| Returns `Optional<Employee>`                           | Returns `Employee`                                                          |
| Fetches the entity from DB immediately (if not cached) | Usually fetches the entity *lazily* when accessed                           |
| Returns `Optional.empty()` if not found                | May throw `EntityNotFoundException` when the proxy is accessed if not found |
| Best for checking whether an employee exists           | Best when you need a reference, e.g. setting a relationship                 |


---
No, `ReentrantLock` cannot be directly used with try-with-resources because it does not implement `AutoCloseable`.




1.3 Java Memory Model
The Java Memory Model (JMM) defines how threads interact through memory and which writes are guaranteed to be visible to other threads.

Key concepts:
- Visibility: Whether one thread sees another thread's changes.
- Atomicity: Whether an operation happens indivisibly.
- Ordering: Which operations are guaranteed to occur before others.
- Happens-before: A relationship that guarantees visibility and ordering.




Weakly consistent iterators

---

12. How do you call an external API from your application? 🤔

For a synchronous Spring Boot application, `RestClient` is a straightforward option.

```
@Service
public class ExternalUserService {

    private final RestClient client;

    public ExternalUserService(RestClient.Builder builder) {
        this.client = builder
                .baseUrl("https://api.example.com")
                .build();
    }

    public ExternalUser getUser(Long id) {
        return client.get()
                .uri("/users/{id}", id)
                .retrieve()
                .body(ExternalUser.class);
    }
}
```

Internal flow:

```
Controller
    ↓
Service
    ↓
RestClient
    ↓ HTTP Request
External API
    ↓ HTTP Response / JSON
Message Converter
    ↓
ExternalUser Java Object
```





```
String s = "HelloWorld";
System.out.println(s.substring(5, 3));
```



### 3. How does React.js communicate with Spring Boot? 🤔

React sends HTTP requests to Spring Boot using `fetch()` or Axios. Spring Boot exposes REST APIs that return JSON


### 4.2 Can a record extend another class? 🤔

No. A record implicitly extends `java.lang.Record`, so it cannot extend another class.

### 4.3 Can a record implement an interface? 🤔

Yes.


### 4.4 Are record classes immutable? 🤔

Record components are final, so they cannot be reassigned after construction. However, records are only shallowly immutable.

```
record Employee(List<String> skills) {}
```

The `skills` reference cannot be reassigned, but the referenced list can still be modified unless you make a defensive copy, such as with `List.copyOf(skills)`.


### 2.10 Application health check vs downstream system smoke check 🤔


## 2. How do we post a message to a REST API? `HttpClient` vs `RestTemplate` 🤔

- Retry only transient failures.  🤔🤔🤔 

## 7. Database commit succeeds, but publishing to Kafka fails. How do you roll back? 🤔


This is a dual-write problem:


## 24. How does Spring Boot manage dependency versions internally? 🤔

bom (bill of material)


---



List.stream().sorted().forEach(System.out::println);
1. Odd 
2. Then Even 



Use streams to sort an array which has odd and even numbers odd should come in first and then even numbers and odd should be sorted and even should be sorted.  🤔🤔🤔 



Use streams to provide an output array which has no negatives or 0s he mentioned to use partitioning by.
list.stream().filter(n-> n>0 ).forEach();

Map<List<Integer,Boolen>> map =  List.stream().collect(PartitioningBy(n->n>0));



---



Write one sql to find all the orders placed in the last 12months by the customer where the customer made at least 3 orders sorted in description order( order and customer table was give) 

Order 
Custumer 

I need to join them 
Left or inner 

inner => 




[Eclipse MAT | jvmperf: JVM Performance Workshop](https://jvmperf.net/docs/memory/mat/)



Stream qn was for annagrams 

TDD vs BDD 


JVM ClassLoader reposbility

In reetrant lock we use try with finally 
Cannot we use try with resource ?


Stream qn was for annagrams 

Interview trap: Is `ConcurrentHashMap` thread-safe for every sequence of operations?

✅ **Takeaway:** Always link tools with metrics like _latency_, _throughput_, or _error rate_ — it shows awareness of SLAs.




Q10. What is database indexing and how does it improve query performance?  
Q11. What is a composite index and when should it be used?   🤔🤔🤔 
Key and Index
Key : Identify the row 
Index : What does it do ?

Q12. What is the difference between optimistic locking and pessimistic locking?   🤔🤔🤔
Add Example 
Word Eytmology 


Q13. How do you handle database transactions across microservices?  




---
