# Spring RESTful Routing & Static Files
## Spring Data Repositories
- CrudRepository
- PagingAndSortingRepository
- JpaRepository

### JpaRepository
JpaRepository provides JPA related methods such as flushing the persistence context and delete records

### CrudRepository
the CRUD functionality:

- save(…) 
- findOne(…) 
- findAll() 
- count() 
- delete(…) 
- exists(…) 

![CRUD](../assets/class12/crud.png)

### PagingAndSortingRepository
When using Pageable, we create a Pageable object with certain properties and we've to specify at least:

- Page size
- Current page number
- Sorting