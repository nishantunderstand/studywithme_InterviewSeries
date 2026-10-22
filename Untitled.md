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