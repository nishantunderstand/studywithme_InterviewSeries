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
