17. Can an immutable object become mutable?
18. Relationship between immutability and thread safety
4. Saga Pattern vs @Transactional

Integer Caching.
16. Sort a HashMap by Key using Streams

4. Database query suddenly becomes slow — how identify bottleneck?
6. Kafka consumers are lagging — how investigate?

Functional Interface Predicate, Consumer add them.

SOLID Principle Example Of All of them 


2. Youngest employee in each department
1. Count employees department-wise
3. Second-highest salary with duplicates


OAuth 2.0 vs JWT

HATEOAS Hypermedia as the Engine of Application State.

Department-wise employee count

1. ArrayList vs LinkedList



3. How do you handle Time Zones in Java?
6. Orders in last 12 months from customers with ≥3 orders


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



Working of HashMap and ConcurrentHashMap



3. How make a Java class thread-safe?

Approaches:

Immutability
synchronized
Lock
Atomic classes
Concurrent collections
Avoid shared mutable state

7. Serialize and deserialize an object


ClassLoader Hierarchy, You need to understand it.

12. Internal working of JVM


31. Sealed Classes
Sealed Interface 
How this is different from Interface
I need to understand in term of ASCII.



RetranctLock : WriteCode for it 


Caching can hurt when:

Data changes frequently
Cache hit rate is low
Objects are large
Invalidation is expensive
Memory pressure increases
Stale data is unacceptabl



🔥 20. p99 latency: 80ms → 2 seconds





ACID vs BASE vs Eventual Consistency


2. How identify whether issue is Application, DB, Kafka, or downstream?


8. Functional and non-functional requirements for REST API

12. 100 records, only 8 threads — process all and wait

Future.get() vs CompletableFuture

15. Why custom ExecutorService with CompletableFuture?

16. What makes FinTech technically different?

17. Prevent duplicate transaction when client retries


24. Should DB Connection be Singleton?


1. BufferedInputStream vs BufferedOutputStream


3. What are Filter Streams?

BufferedInputStream
BufferedOutputStream
DataInputStream
DataOutputStream

8. Encryption vs Decryption


9. What is RSA and where used?


CSRF Example 


13. OAuth vs OAuth 2.0


15. Configure multiple databases in Spring Boot



10. Generics — extends vs super
PECS


27. Database Indexes


28. Composite Key

30. Employees earning more than their manager


☕ Java Streams
3️⃣1️⃣ Given a list of integers:
👉 Reverse the order
👉 Keep distinct values
👉 Place odd numbers first
👉 Place even numbers after them
💻 Coding Round






1️⃣ 10% hike for employees who joined after 2024

HashMap vs IdentityHashMap


HashMap        → logical equality
IdentityHashMap → object identity


Memory Leak Common Reason

Common causes:

Static collections
Unbounded caches
Listeners not removed
ThreadLocal misuse
Resources not closed


1️⃣3️⃣ Access private fields/methods in tests


How to enable Caching in SpringBoot ?


1️⃣6️⃣ Can Spring create a bean for abstract class?



5️⃣ Why Kafka for asynchronous operations?


Kafka 1️⃣4️⃣ Cluster Metadata


1️⃣5️⃣ How Kafka supports scalability?


1️⃣6️⃣ Kafka broker goes down?

1️⃣8️⃣ How Kafka ensures data consistency?


1️⃣9️⃣ Kafka retention


2. Top 3 salaries per department


6. Kafka consumer crashes before offset commit


7️⃣ API latency suddenly increases
Use a measurement-first approach:


1️⃣1️⃣ Can outside classes access hidden data?




6️⃣ IoC vs Dependency Injection


3️⃣ Second-highest number



3️⃣ Exception Handling + Advisor


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



11. Query Optimization Techniques

GC Roots


8. Dependency and Artifact


Java 8 → Java 17

20. How do you call an external API?