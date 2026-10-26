🚀 EPAM Java Developer Interview Experience | 💻  
Sharing questions from a recent EPAM Java interview, covering DSA, Java Internals, Spring Boot, Multithreading, Security & Microservices.  
🔥 Questions Asked  
💻 Coding & Java Streams  
DSA: Arrange elements around a given threshold — smaller elements first, larger elements after.  
Java Streams: Convert "I love Java" → "[hashtag#ILoveJava](https://www.linkedin.com/search/results/all/?keywords=%23ilovejava&origin=HASH_TAG_FROM_FEED)"  
Streams: Find anagrams using Java Streams.  
☕ Core Java  
HashMap & HashSet internals  
Treeification  
wait() vs sleep() vs yield()  
Thread vs Runnable  
Thread & Multithreading  
ReentrantLock vs synchronized  
Java Memory Model (JMM)  
Garbage Collection basics  
Design a Thread Pool  
🌱 Spring Boot & Security  
@Configuration, @Service, @SpringBootApplication — output-based questions  
How do Spring Boot annotations work internally?  
Global Exception Handling  
Spring Security  
Authentication vs Authorization  
🏗️ Microservices  
Microservices Design  
Designing scalable and reliable services  
🎯 Key Areas  
DSA | Java Internals | Streams | Concurrency | Spring Boot | Security | Microservices



---

🚀 EPAM L1 Coding Round – Java Questions You Should Practice  
  
Here are two practical Java coding questions that test problem-solving fundamentals and your understanding of Java Streams.  
  
1️⃣ Reverse an Array In-Place  
  
Input:  
  
["h", "e", "l", "l", "o"]  
  
Expected Output:  
  
["o", "l", "l", "e", "h"]  
  
Requirements:  
  
* No Java Streams  
* No additional array or collection  
* Reverse the array in-place  
  
Solution — Two-Pointer Approach:  
  
public static void reverse(String[] arr) {  
int left = 0;  
int right = arr.length - 1;  
while (left < right) {  
String temp = arr[left];  
arr[left] = arr[right];  
arr[right] = temp;  
left++;  
right--;  
}  
}  
  
Complexity:  
  
* ⏱️ Time: O(n)  
* 💾 Auxiliary Space: O(1)  
  
⸻  
  
2️⃣ Java Streams — Find Distinct Skills of Certified Trainers  
  
Given a list of trainers, each containing:  
  
* Skill  
* Certification status  
  
Sample Data:  
  
Skill Certified  
Java true  
Spring Boot true  
Java true  
Kafka false  
Kafka true  
  
Expected Output:  
  
Java, Spring Boot, Kafka  
  
Solution:  
  
String result = [trainers.stream](http://trainers.stream/)()  
.filter(Trainer::isCertified)  
.map(Trainer::getSkill)  
.distinct()  
.collect(Collectors.joining(", "));  
  
How the Stream pipeline works:  
  
* filter() → Keeps only certified trainers.  
* map() → Extracts each trainer’s skill.  
* distinct() → Removes duplicate skills.  
* joining() → Combines the skills into a comma-separated string.  
  
⸻  
  
💡 Interview Tip  
  
Don’t just write the code. Be prepared to explain your approach:  
  
👉 Why did you choose this solution?  
👉 What are the time and space complexities?  
👉 Can you solve the problem without using extra space?  
👉 Why is distinct() required?  
👉 How would you handle duplicate or null values?  
  
Strong fundamentals and clear communication matter just as much as writing working code.




---


EPAM Systems | Java Backend Developer Interview Experience  
  
Recently, Jagdish Khetre shared his Java Backend Developer interview experience at EPAM Systems.  
  
The interview covered a wide range of topics — from Core Java and Spring Boot to Microservices, Distributed Systems, Kubernetes, AI and System Design.  
  
☕ Java & Concurrency  
  
🔹 Stream vs Collection  
🔹 Java Streams — filtering, sorting & finding top elements  
🔹 How to make LinkedList synchronized  
🔹 synchronized vs Lock  
🔹 Optimistic vs Pessimistic Locking  
  
🌱 Spring Boot & JPA  
  
🔹 Purpose of Interceptors  
🔹 Commit & Rollback in Spring  
🔹 Identifying and solving the N+1 problem  
🔹 Skipping a field from JPA persistence  
  
🔗 Microservices & Distributed Systems  
  
🔹 Transactions in distributed systems  
🔹 Outbox Design Pattern  
🔹 Saga Design Pattern  
🔹 2-Phase Commit (2PC)  
🔹 Circuit Breaker Pattern  
🔹 Securing 100+ microservices  
🔹 API Gateway  
🔹 JWT authentication flow  
  
☸️ Kubernetes  
  
🔹 Liveness Probe  
🔹 Readiness Probe  
  
🤖 AI  
  
🔹 Basics of prompting  
🔹 Effective token usage in AI applications  
  
💼 Project Discussion  
  
🔹 Current project & architecture  
🔹 Roles and responsibilities  
🔹 Key technical challenges  
🔹 Real-world problem-solving  
  
📌 Key takeaway:  
For experienced Java developers, interview preparation is no longer just about memorizing definitions.  
  
You should be able to explain why you chose a particular approach, how you would troubleshoot production issues, and how you would design systems for reliability, scalability and security.  
  
If you’re preparing for a Java / Spring Boot / Microservices interview, save this list for your revision. 📚  
  
And if you’ve recently appeared for an interview, share your interview experience and questions — your experience might help another developer prepare better. 🤝






---

Had all, AI virtual(2coding) then 1 technical and 1 technomanager

- Coding had 1 DSA(threshold) 
where need to arrange elements in such order where less than threshold elements must be at start and more at the end
1 stream, “I love Java” is input and expected output is “#ILoveJava”

Technical
- Hashset internals
- Hashmap internals
- Treefication
- Wait sleep yield
- Authentication and authorization
- Spring security
- 2D array
- 1D array
- Output based questions(@Configuration, @Service, @SpringBotApp) 
- Thread
- Multithread
- Runnable
- Thread vs runnable
- Design thread pool

Technimanager
- Can we reused streams? Why? 
- Global exception handler? 
- How Spring boot annotation work? 
- JMM
- GC(basics) 
- Thread and multithread
- Stream qn was for annagrams 
- Dsa qn not sure, will share soon
- Reeentrant lock vs Synchronized
- Microservices design