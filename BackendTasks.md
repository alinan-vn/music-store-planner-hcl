- Tables
    - Customer
    - Billing Info
    - Receipt
    - Shopping Cart
    - Cart Product Items
    - Product
    - Category
    - Condition
    - Cart Song Items
    - Song
    - Album
    - Format Type
    - Genre
    - Admin

^^ Each of these needs a Entity, Rest Crud Repository, and Controller (Services included later to handle business logic)

^^ Controllers contain CRUD functionalities that vary on the entity (refer to README.md)

File structure
Java Application.java
- Entities
    - Customer
- controllers
    - Customer
- CrudRepositories
    - Customer