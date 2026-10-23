Does Column Order Matter ?
Key vs Index ?
Why Do we need Index ? Does Key Solve all the Problem ?
---
11. How do you investigate high GC activity?
12. What happens when the database connection pool is exhausted?
13. How do you troubleshoot a slow API?
14. What happens when an external service goes down?
15. How do you prevent cascading failures in microservices?
16. What happens when Kafka consumers stop processing messages?
17. How do you handle duplicate messages?
18. What happens when a transaction partially succeeds?
19. How do you troubleshoot intermittent production failures?
20. Why might an application work locally but fail in production?
For every scenario, prepare your answer using:
Symptoms → Root Cause → Investigation → Fix → Prevention → Monitoring 
---
https://www.instagram.com/reels/DeRwpkdIZ0O/
---
1. How does HashMap work internally in Java?
2. What is the difference between HashMap and ConcurrentHashMap?
3. How does Java handle multithreading and concurrency?
4. What is the difference between synchronized, volatile, and AtomicInteger?
5. How do Java Streams work internally?
6. How would you troubleshoot high CPU usage in a Java application?
7. How would you investigate a Java memory leak?
8. How does Spring Boot auto-configuration work?
9. How does Spring Boot handle dependency injection?
10. How does @Transactional work internally?
11. Why might @Transactional fail to roll back a transaction?
12. How would you optimize a slow Spring Boot API?
13. How would you troubleshoot HikariCP connection pool exhaustion?
14. How would you solve an N+1 query problem in Spring Data JPA?
15. How would you secure a Spring Boot REST API using JWT?
16. How would you implement OAuth2 authentication in Spring Boot?
17. How would you design communication between microservices?
18. REST vs Kafka — when would you choose each?
19. How would you prevent cascading failures between microservices?
20. How would you implement Retry, Circuit Breaker, and Bulkhead?
21. How would you design idempotent APIs in microservices?
22. How would you handle distributed transactions using the Saga pattern?
23. How would you maintain data consistency between microservices?
24. How would you handle duplicate Kafka messages?
25. How would you troubleshoot increasing Kafka consumer lag?
26. How would you design service discovery in a microservices architecture?
27. How would you design an API Gateway for microservices?
28. How would you deploy Spring Boot microservices on AWS?
29. ECS vs EKS — when would you choose each for Java microservices?
30. How would you design high availability across AWS Availability Zones?
31. How would you use AWS RDS for a highly available Spring Boot application?
32. How would you use ElastiCache to improve microservice performance?
33. How would you monitor Java microservices using CloudWatch, metrics, and distributed tracing?
34. A production microservice suddenly becomes slow. How would you troubleshoot Java, Spring Boot, AWS, database, and network issues?
35. Design a highly scalable e-commerce system using Java, Spring Boot, Microservices, Kafka, AWS, caching, and a relational database. How would you handle failures, traffic spikes, and data consistency? 

---

A few questions that stood out:
Design a simple GET API and explain the flow.
Difference between @Controller and @RestController.
Dependency injection in Spring Boot.
Microservices communication and saga pattern.
Functional interface, Stream API, exception handling.
Coding: move all zeroes to the right while preserving order.
Overall, it was a good reminder that strong fundamentals still matter a lot in backend interviews.

---
Some of the key questions asked:
🔹 1. New feature integration
“Your architect asks you to integrate a new feature into an existing application. How would you handle the end-to-end pipeline?”
🔹 2. Handling disagreements with a senior architect
“Your architect is more experienced than you and disagrees with the way you implemented something, saying you shouldn’t use a particular approach or overly fancy functions. How would you handle the situation?”
🔹 3. Code conflicts with another developer
“You are working on Feature 1 while another teammate is working on Feature 2. They push their code first, and now there are conflicts with your changes. How would you resolve it?”
🔹 4. Explaining your work
“How would you present and explain a new feature to technical team members as well as a non-technical client?”
🔹 5. SDLC
“How does SDLC work in your organisation?”
🔹 6. Feedback process
“Who gives you feedback on your work and how do you act on it?”
🔹 7. Bugs after deployment
“You deployed your code and QA finds multiple bugs. How would you handle, debug and optimise the implementation?”
My key takeaway
The round was less about simply knowing a technology and more about understanding how you work as an engineer in a real team.
They were evaluating things like:
• Problem-solving approach
• Code quality and maintainability
• Handling disagreements professionally
• Git/merge-conflict awareness
• Communication with technical & non-technical stakeholders
• SDLC understanding
• Debugging and ownership
• Ability to take feedback and improve
EY (Ernst & Young) TECHNICAL INTERVIEW QUESTIONS & ANSWERS  scrummaster Interview Question & Answer

---

Service Discovery vs Service Registration

---


Here are the exact questions asked:
🔹 Microservices & Architecture 
1️⃣ How do you handle fault tolerance in microservices? 
2️⃣ What are the design patterns used in microservices architecture? 
3️⃣ What is the Circuit Breaker Design Pattern, and how have you implemented it using Resilience4 j? 
4️⃣ What is CQRS (Command Query Responsibility Segregation) pattern? 
5️⃣ What messaging queue have you worked on? Kafka or RabbitMQ?
🔹 Spring Boot & Security 
6️⃣ Have you implemented Role-Based Access Control (RBAC) using Spring Security? 
7️⃣ What is the difference between @Qualifier and @Primary? 
8️⃣ What annotation is used in application.properties / application.yaml to inject values into the service layer?
👉 How do you use those constant values inside your Business Service class?
🔹 Java & Multithreading
9️⃣ Difference between Thread and Runnable 
🔟 If two threads are using shared resources, how do wait() and run() differ?
🔹 Coding Round (Java 8 / Brute Force) Write a Java 8 or normal Java program to print combinations that sum to 6. 
💻 Input: nums = [2, 4, 3, 3, 5, 7] target = 6 💻 Output: [[2,4], [3,3]]
🔹 SQL 
1️⃣1️⃣ Write a query to find employees earning more than the average salary of their department. 
1️⃣2️⃣ Difference between Primary Key vs Unique Key