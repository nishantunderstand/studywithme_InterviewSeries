Interview HCLTech 20260905



Suppose a delete Api
Sometime 201 sometime 204




Absolutely. Here are all the questions we've covered in this interview sequence so far, in order:

Java / JUnit / Design Principles

1. Optimistic Locking
Might @Version fail to prevent lost updates in a given JPA mapping, and how would you correct it to ensure optimistic locking works reliably across updates?


2. JUnit 5 Exception Testing
What is the correct way to test that a method throws an exception in JUnit 5?


3. Mockito Retry Testing
How would you stub a mock so a dependency fails on the first two calls and succeeds on the third, and how would you verify the number of invocations?


4. Liskov Substitution Principle
What precise, actionable rules can you use during code review to detect LSP violations? Consider method signatures, exceptions, and state changes.


5. Interface Segregation Principle
How do you identify an interface that forces implementers to provide methods they don't need, and how would you refactor it?


6. Java Cloneable
What are the problems with Cloneable and super.clone(), and what are robust alternatives for object copying in modern Java?


7. Prototype / Mutable Fields
What correctness issue occurs when cloning objects containing mutable fields, and what is a robust cloning strategy?



Kafka / Avro / Schema Registry

8. Schema Compatibility
Explain backward, forward, and full compatibility in Schema Registry and when to use each.


9. Multi-Tenant Schema Registry
How would you implement operational practices and access controls to prevent incompatible schema registration while allowing team autonomy?


10. Kafka Message Key
What purpose does a key attached to each Kafka record serve?


11. Avro Schema Evolution
A producer already publishes customer events using Avro. How would you add an optional loyaltyTier field without breaking older consumers?


12. Custom Kafka Partitioner
Review a custom partitioner that distributes messages using userId % partitionCount. Identify bugs, race conditions, and corrections.


13. Avro Deserialization During Rolling Deployments
Why does a hardcoded SpecificDatumReader cause schema-version-skew failures, and how should the consumer safely support schema evolution?



REST / Security / Microservices

14. Public vs Private REST Endpoints
What criteria determine whether an endpoint requires authentication, and how should rate limiting and monitoring differ?


15. Multi-Tenant REST Authorization
An API returns resources containing tenantId, while the frontend filters unauthorized records. What's wrong, what attacks are possible, and how should authorization be implemented server-side?


16. Okta OIDC Rolling Deployment
Mobile API calls suddenly return 401 because resource servers see missing scopes while web clients work. How would you diagnose and fix the cross-team OAuth/OIDC contract while minimizing user impact?


17. Gateway JWT + X-User Header
What security issues arise when a gateway validates JWTs and forwards identity using a custom X-User header, and what is a safer identity-propagation strategy?


18. JWT Roles / Authorization
A service extracts roles from a JWT but some endpoints use only authenticated() while others use hasRole("ADMIN"). Identify the authorization flaw, exploitation scenario, and how to standardize authorization.



Earlier questions from the same interview sequence

19. Lazy initialization of a complex object graph


20. Java sealed classes/interfaces


21. Spring @Bean factory methods vs direct instantiation


22. Spring circular dependencies


23. Designing an internal Spring Boot starter


24. Spring @Bean helper constructor dependency becoming null


25. REST API evolution and versioning


26. PATCH vs PUT semantics


27. DELETE response semantics and idempotency


28. Manually setting SecurityContextHolder


29. Bidirectional JPA @OneToMany / @ManyToOne ownership


30. JPA field access vs property access


31. Purpose and limitations of Spring Data JPA repositories


32. Optimistic locking with @Version


33. Migrating JPA @NamedQuery to repository @Query


Here are all the interview questions we've covered in this conversation, cleaned up and consolidated:

Java / Collections / Streams

1. HashMap Collision Handling
In an in-memory cache using HashMap, where keys have poor hash distribution, propose a strategy to reduce collision impact and explain the implications for performance and memory.


2. LinkedList First and Last Elements
Given this linked-list usage, what are the first and last elements printed?


3. noneMatch() vs anyMatch()
Are noneMatch(predicate) and anyMatch(predicate) equivalent? Why might you choose one over the other?


4. Grouping Files by Extension
You need to group files by extension and, for each extension, keep the largest file. Which Collectors combination yields a map of the largest files per extension?


5. Static Helper Methods on an Interface
When providing static helper methods on an interface used across modules, discuss versioning and class-loader concerns and how to ensure stable behavior across releases.



Short interview-ready answers

#	Topic	Key answer

1	HashMap collisions	Improve hashCode() distribution; resizing helps load factor but doesn't fix a fundamentally poor hash
2	LinkedList	Determine from the actual addFirst/addLast/iteration operations
3	noneMatch vs anyMatch	noneMatch(p) == !anyMatch(p); choose based on readability/intent
4	Largest file per extension	groupingBy(File::extension, maxBy(comparingLong(File::size)))
5	Interface static helpers	Treat as public API; maintain binary compatibility, consistent dependency versions, and avoid class-loader conflicts



Interview Question

Using Java 21, write a function that takes a List<Interval> where each interval has a start and end, merges all overlapping intervals, and returns the merged intervals as a TreeMap<Integer, Integer> sorted by start time.

Requirements:

Use a lambda to sort the intervals by start.

Overlapping intervals should be merged.

Return a TreeMap, so the result remains sorted by start.

Handle null or empty input.

Example:


Input:
[1,3], [2,6], [8,10], [9,12]

Output:
{1=6, 8=12}

Bonus: What are the time and space complexities?


