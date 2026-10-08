JavaOOPS

OOPS 
Basic Question

Microservice 
Drawaback Able to tell 2 

SpringBoot 
Starteweb Dependency Expalin
Java8 Stream API Code 

Comparator Code 
I really need to pratice it.


---


JWT 

Claim Explain 


---

Does JWT Recreated at Server Side ?

How Does Validation Happen ?


If we change exp time how this will impact it ?

What if change something ?

Access or refresh Token



---

Respon


---
Set 

---


There are 2 types of user admin and regular user. We have CRUD APIs for getting list of products. Product will have category and price. Admin can do all operations and regular user can only view products

Product 
ProductId

ADMIN - ALL OPERATION 
REGULAR : VIEW OPERATION

VIEW Operation : All products 
/products /@PreAuthorize(hasAnyRole('ADMIN','USER'))

VIEW By Categoty : By Categoty 
/products?category='Item' /@PreAuthorize(hasAnyRole('ADMIN','USER'))

VIEW Categoty , By price Range 
/products?minprice=1000&maxprice=2000
/@PreAuthorize(hasAnyRole('ADMIN','USER'))

CREATE
@PostMapping
/products

UPDATE 
@PatchMapping
/products/{id}
Use PathVariabele
