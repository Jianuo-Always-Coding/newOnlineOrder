# Repository
Definite some interface which will accomplish in service.
Though the interface is empty, it's definite the data type of RestaurantRepository.
Provide super function which service can use like findall().
Also can add @Repository, but not necessary.
For the functions, if it change the data in database, should add the annotation @Modifying and @Query(...), 
... should be the query sentence shows how to change data.

## RestaurantRepository
**An empty Interface.** 

## MenuItemRepository
Definite a function **getByRestaurantId**.

## OrderItemRepository
Definite 3 functions **getAllByCartId, findByCartIdAndMenuItemId, deleteByCartId**

## CartRepository
Definite 2 functions **getByCustomerId, updateTotalPrice**.

## CustomerRepository
Definite 4 functions **findByFirstName, findByLastName, findByEmail, updateNameByEmail**.




 
# Entity
Define the data structure of different objects in the database. Use **@Table** and **@ID**.

We have **cartEntity, customerEntity, MenuItemEntity, OrderItemEntity, RestaurentEntity**.



# Model
## DTOs
Create new object structure which can obtain all the data from different entities once.
## Body


# Service

It is necessary to use @Service to guide Spring Boot to create service
## CartService
## CustomerService
## MenuItemService
## RestaurantService