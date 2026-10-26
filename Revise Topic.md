## 19. `thenApply()` vs `thenCompose()` vs `thenCombine()` 🤔🤔🤔

## 15. CopyOnWriteArrayList: When to use it? 🤔🤔🤔

## 8. Correct use and misuse of `Optional` 🤔🤔🤔

## 9. Reflection API and performance trade-offs 🤔🤔🤔

## 11. How can inheritance instead of composition break design? 🤔🤔🤔

---

- Can a record extend another class?
- Does a record compare objects using `==`?
- Are records suitable for DTOs?
- Can we override `equals()` and `hashCode()`?

---

| Feature                      | Inheritance                   | Composition                                       |
| ---------------------------- | ----------------------------- | ------------------------------------------------- |
| Relationship                 | IS-A                          | HAS-A                                             |
| Java mechanism               | `extends`                     | Object field/reference                            |
| Code reuse                   | Inherits accessible behavior  | Delegates to another object                       |
| Coupling                     | Often tighter                 | Often more flexible                               |
| Runtime flexibility          | Limited by class hierarchy    | Dependencies can often be replaced                |
| Multiple reuse relationships | Single class inheritance      | Can combine multiple objects                      |
| Best suited for              | Genuine subtype relationships | Building functionality from collaborating objects |

Multiple Catch + Pipe Operator 

```
Map<String, Integer> map = new HashMap<>();

map.put(null, 100);
map.put(null, 200);

System.out.println(map.size()); // 1
System.out.println(map.get(null)); // 200
```

Chaining and Duplicate Key 

8. What is Prototype Scope?
    * How is it different from Singleton?
    * When would you use prototype-scoped beans?
9. ApplicationContext vs BeanFactory
    * What is ApplicationContext?
    * What is BeanFactory?
    * What are their differences and use cases?

---

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

Note: Java does not provide a standard `AtomicFloat` class. For floating-point values, alternatives include `AtomicReference<Float>` or `DoubleAdder` for appropriate use cases.

- What are the other things does it support ?

---

8. What is distributionManagement in pom.xml? 🤔
Does it mean nexus Repo ?

9. Java 17 Features
- Records — concise data carrier classes.
- Sealed classes — restrict permitted subclasses.
- Pattern matching for instanceof — simplifies type checks.
- Text blocks — multiline strings.
- Switch expressions — return values from switch.
- Helpful NullPointerExceptions — clearer NPE messages.
- Strong encapsulation of JDK internals — improved platform integrity.

Can `var` be used as a generic type? No.

- Return only required fields using DTOs or projections.

2. DSA: Print yes if 5 consecutive vowels exist; otherwise no

```
Function<String, Integer> f = s -> s.length();
System.out.println(f.apply("Java")); // 4

Supplier<Double> s = () -> Math.random();
System.out.println(s.get());
```

## 9. Print `NA` if employee address is null
```
employees.stream()
    .forEach(e -> System.out.println(
        e.getName() + " : " +
        Objects.toString(e.getAddress(), "NA")
    ));
```

### What are TDD and BDD?

- TDD (Test-Driven Development): Write a failing test, implement the code, then refactor — red, green, refactor.
- BDD (Behavior-Driven Development): Define and test expected behavior using scenarios, often written as Given–When–Then.

### 15. Can HashMap keys be mutable?

### 17. Run code before a Spring bean is used

### 9. What happens when an exception occurs during a transaction?

“By default, Spring rolls back for unchecked exceptions and `Error`, but not checked exceptions. We can customize this using `rollbackFor`.”

15. Generics: `extends` vs `super`

- `? extends T`: suitable when reading values as type `T`.
- `? super T`: suitable when adding values of type `T`.

## 1. `Optional.of()` vs `Optional.ofNullable()`

## 1. `isPresent()` vs `ifPresent()`

### 3. `orElse()` vs `orElseGet()` 🤔

- `orElse()` evaluates `getDefault()` even when the value exists.    
- `orElseGet()` evaluates the supplier only when the Optional is empty.
Remember: `orElse` = eager; `orElseGet` = lazy.

### A. Reverse order, distinct integers, odd first then even
```
List<Integer> result = numbers.stream()
    .distinct()
    .sorted(Comparator.reverseOrder())
    .sorted(Comparator.comparingInt(n -> n % 2 == 0 ? 1 : 0))
    .toList();
```

3. ISO 8583

Find a file in a subdirectory
```
try (var paths = Files.walk(Path.of("rootDirectory"))) {
    paths.filter(Files::isRegularFile)
         .filter(p -> p.getFileName().toString().equals("target.txt"))
         .forEach(System.out::println);
}
```

```
@GetMapping("/employees")
public Page<Employee> getEmployees(
        @RequestParam(defaultValue = "0") int page,
        @RequestParam(defaultValue = "10") int size,
        @RequestParam(defaultValue = "name") String sortBy) {

    Pageable pageable = PageRequest.of(
        page, size, Sort.by(sortBy).ascending()
    );

    return employeeRepository.findAll(pageable);
}
```

---

Q9. How would you design a scalable REST API in Spring Boot for high traffic?
I would focus on performance, scalability, reliability, and maintainability.
1. Stateless design: Use REST principles and JWT or OAuth2 for authentication.
2. Database optimization: Use proper indexing, connection pooling, and optimized queries.
3. Caching: Use Redis to reduce repeated database calls.
4. Pagination: Avoid returning large datasets in a single response.
5. Asynchronous processing: Use Kafka or RabbitMQ for background tasks.
6. Horizontal scaling: Deploy multiple instances behind a load balancer.
7. Resilience: Apply timeouts, retries with backoff, and circuit breakers.
8. Monitoring: Use Actuator, Micrometer, and centralized logging.

---

17. Can an immutable object become mutable?
18. Relationship between immutability and thread safety
19. Saga Pattern vs @Transactional

- Integer Caching.
16. Sort a HashMap by Key using Streams

17. Database query suddenly becomes slow — how identify bottleneck?
18. Kafka consumers are lagging — how investigate?

- Functional Interface Predicate, Consumer add them.

- SOLID Principle Example Of All of them 

2. Youngest employee in each department
3. Count employees department-wise
4. Second-highest salary with duplicates

- OAuth 2.0 vs JWT

- HATEOAS Hypermedia as the Engine of Application State.

- Department-wise employee count

1. ArrayList vs LinkedList

2. How do you handle Time Zones in Java?
3. Orders in last 12 months from customers with ≥3 orders

REQUIRED
→ Join existing transaction
→ Otherwise create one

REQUIRES_NEW
→ Suspend existing transaction
→ Create new transaction

SUPPORTS
→ Join if one exists
→ Otherwise execute without transaction

MANDATORY
→ Existing transaction required

NOT_SUPPORTED
→ Execute without transaction

- Working of HashMap and ConcurrentHashMap

3. How make a Java class thread-safe?

Approaches:

- Immutability
- synchronized
- Lock
- Atomic classes
- Concurrent collections
- Avoid shared mutable state

7. Serialize and deserialize an object

- ClassLoader Hierarchy, You need to understand it.

12. Internal working of JVM

13. Sealed Classes
14. Sealed Interface 
15. How this is different from Interface
16. I need to understand in term of ASCII.

- RetranctLock : WriteCode for it 

- Caching can hurt when:
- Data changes frequently
- Cache hit rate is low
- Objects are large
- Invalidation is expensive
- Memory pressure increases
- Stale data is unacceptabl

- 🔥 20. p99 latency: 80ms → 2 seconds

- ACID vs BASE vs Eventual Consistency

2. How identify whether issue is Application, DB, Kafka, or downstream?

3. Functional and non-functional requirements for REST API

4. 100 records, only 8 threads — process all and wait

- Future.get() vs CompletableFuture

15. Why custom ExecutorService with CompletableFuture?

16. What makes FinTech technically different?

17. Prevent duplicate transaction when client retries

18. Should DB Connection be Singleton?

19. BufferedInputStream vs BufferedOutputStream

20. What are Filter Streams?
- BufferedInputStream
- BufferedOutputStream
- DataInputStream
- DataOutputStream

7. Encryption vs Decryption
8. What is RSA and where used?
- CSRF Example 
7. OAuth vs OAuth 2.0
8. Configure multiple databases in Spring Boot
9. Generics — extends vs super
- PECS
7. Database Indexes
8. Composite Key
9. Employees earning more than their manager

☕ Java Streams
3️⃣1️⃣ Given a list of integers:
- 👉 Reverse the order
- 👉 Keep distinct values
- 👉 Place odd numbers first
- 👉 Place even numbers after them

💻 Coding Round
- 1️⃣ 10% hike for employees who joined after 2024

- HashMap vs IdentityHashMap
HashMap        → logical equality
IdentityHashMap → object identity

- Memory Leak Common Reason
Common causes:
- Static collections
- Unbounded caches
- Listeners not removed
- ThreadLocal misuse
- Resources not closed

- 1️⃣3️⃣ Access private fields/methods in tests
- How to enable Caching in SpringBoot ?
- 1️⃣6️⃣ Can Spring create a bean for abstract class?
- 5️⃣ Why Kafka for asynchronous operations?
- Kafka 1️⃣4️⃣ Cluster Metadata
- 1️⃣5️⃣ How Kafka supports scalability?
- 1️⃣6️⃣ Kafka broker goes down?
- 1️⃣8️⃣ How Kafka ensures data consistency?
- 1️⃣9️⃣ Kafka retention
2. Top 3 salaries per department
3. Kafka consumer crashes before offset commit

- 7️⃣ API latency suddenly increases Use a measurement-first approach:
- 1️⃣1️⃣ Can outside classes access hidden data?
- 6️⃣ IoC vs Dependency Injection
- 3️⃣ Second-highest number
- 3️⃣ Exception Handling + Advisor

Advisor in Spring AOP is related to combining:
Pointcut → where advice applies
Advice → what action to perform
Advisor
├── Pointcut → WHERE
└── Advice   → WHAT

Spring 9️⃣ Scheduling
11. Why service names instead of IPs?
Use API Gateway/BFF or an aggregator service.
Coding — City With Highest Repeated Character Count
Find the city whose single character occurs the maximum number of times.
12. Query Optimization Techniques
GC Roots
13. Dependency and Artifact
Java 8 → Java 17
14. How do you call an external API?