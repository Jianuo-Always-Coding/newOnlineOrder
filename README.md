# OnlineOrderImprovement

## Gradle
Using Gradle to add dependences, different from maven, is much more simple.


## Entities (@Table -- Spring creates tables automatically)
Create different eneties and their fields in the folder 'entity'. Each entity is an object according rules in the file 'database-init.sql'.

Totally 5 entities: Restaurant, Menu, Customer, Order, Cart

## Repository
This is the logic how services can deal with the data in the database, according to the query sentences that Spring Data JDBC created by itself.

## Model

### DTO -- Data Transfer Object
Use DTO to Wrap the corresponding data required by the page to reduce the times of HTTP requests.

There are 4 DTOs: restaurantDTO, orderDTO, menuDTO, cartDTO

### AddToCartBody(@ JsonProperty)

## Controller (@RestController -- for Spring framework, @PathVariable -- for special entity)
### MenuController

## Service(@Service -- Spring creates class automatically)
Add repositories to different services

### RestautentService
Func1: Find all restaurants and their menu, then return all restaurantDTOs.

### MenuService
Func1: Find restaurant menu by restaurant ID.

Func2: Find a dish by menu ID(primary key).

### CustomerServide
Func1: Find Customer by email.

### CartService (@Transactional: 对数据库进行操作有效)
Func1: Add orderItem to cart. If not exist, creat a new one. If exists, quantity + 1.

Func2: Clear cart.

Func3: Get cart. Return cartDTO.

# DoorDashDemo
