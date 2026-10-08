CompletableFuture+Record 
How they are fitted ?

Record Class 
How to access it 🤔🤔🤔 

During Migration 
What will you consider ?

Spring Security 
Need to Rethink and Plan Properly.


---

Collections


List<Integer> list = Arrays.asList(10,11,12,13,14);
list.stream().reversed().findFirst().ifPresent(System.out::println);



--

Employee record
	EmpID 

Address record
		AddressID		
		Employee 

Extract the Data

In Record : we don't need to have get

employee.name();
employee.address().city();
employee.address().state();
	


---


Synchronized and Lock 

---

synchronized
	

Disadvatange
		1. faireness
		2. Retry
		3. timeout 



Lock Interface

1. Reentrackt Lock
2. ReentrantReadWrite Lock
3. StampedLock
		long 


---


HashSet 

HashMap
Key - Value
10,PRESENT 
Uniquness 

---

Object

hashcode and equals 
1. Value Equal , HashCode Equal
2. HashCode Equal, Value Not Equal
3. Should Generate Constient HashCode


---



Design a SpringBoot Architecture 

InputRequest

CDN
DNS


APIGateWay
/user/incident => incident
/user/proces => process

SPOF 
APIGateWay + LoadBalancer 


Spring Security : Authentication

Spring MVC : 
Controller 
/v1/incidet/askClarification

Controller
ServiceLayer
Repostirty
DB

@Tranasaction Annotation

Checked Exception : Explict rollbackFor 
UnChecked Exception / Runtime 




---



Spring Securtity 


---


SpringBoot 2x : META_INF/Spring.factories

Conditional Annotation
ConditionalOnBean 

SpringBoot 3x : META_INF/org.springframework....imports.





---




REST API

6 Guiding 

1. Cacheable 
2. Client_Server
3. Code of demand 
4. 
5. 
6. uniform 

Roy Fielding 


---



Spring Secure

Authentication

Authorziation

Authorization Model 
RBAC
ABAC
ReBAC

@PreAuthroize






---



DI 
1. Contr
2. Fiel
3 

DI + lomobok

private 


---


SpringBootAPI 
100ms 


latencey
More 


---



KAFKA 
Topic : Logical 
Partition : Physcial 
OFFSET : 




---


Kafka Scenarion



---


DLT DLQ
isoloate 

---
