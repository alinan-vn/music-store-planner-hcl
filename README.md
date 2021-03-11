# Files
- FSD Java Capstone pdf is original capstone pdf with the writing prompt, diagrams, and wireframes.
- Visual Schema Diagram is a PNG screen shot of a schema mocked up in dbdiagram.io 
- Schema Code.txt is the code I wrote in dbdiagram.io to make the schema representation
- Sprint Planning excel sheet: https://docs.google.com/spreadsheets/d/15uhL3pNxoAOg25szR9ukARcExOL7Yn87bO-1ZHlk2N8/edit?usp=sharing

# Tables

## Customer
- Not a fixed ammount
- Email must be unique, another account cannot have the same email
- Username must be unique, another account cannot have the same email
- Password must be unique, another account cannot have the same email
- 1-to-1: Billing Info
- 1-to-many: Shopping Cart, Purchase Info

#### Crud Functionalities
- Create: Register a customer
- Read: Get customer info
- Update: Change customer info
- Delete: delete account

## Billing Info
- 1-to-1: Customer
- Join Table (Seperate from customer details for simplicity -> Can also just be a part of Customer table)

#### Crud Functionalities
- Create: User inputs billing info
- Read: User can view their current billing info
- Update: User can change their billing info
- Delete: User can delete their billing info (?) (OUTSIDE THE MVP)

## Shopping Cart
- 1-to-1: Purchase Info
- 1-to-many: Cart Product Items, Cart Song Items
- many-to-1: Customer
- Join Table (That can be referred to any items being purchased by one user)

#### Crud Functionalities
- Create: Created when user adds items to their shopping cart
- Read: User can see their shopping cart

## Receipt
- 1-to-1: Shopping Cart
- many-to-1: Customer
- Join Table (also serves to show when a Shopping Cart is no longer active by Purchase Info's existence)

#### Crud Functionalities
- Create: Created when shopping cart gets bought
- Read: Customer can read receipt

## Cart Product Items
- 1-to-1: Product
- mant-to-1: Shopping Cart
- Join Table

#### Crud Functionalities
- Create: Created when User adds a product to the shopping cart
- Read: User will want to see what's in the shopping cart

## Cart Song Items
- 1-to-1: Song
- mant-to-1: Shopping Cart
- Join Table

#### Crud Functionalities
- Create: Created when User adds a song to the shopping cart
- Read: User will want to see what's in the shopping cart

## Product
- 1-to-1: Cart Product Items, Category, Condition

#### Crud Functionalities
- Create: [ADMIN] Admin can add products
- Read: Customer (and admin) can view products and product info
- Update: [ADMIN] Admin can update product information
- Delete: [ADMIN] Admin can delete products from catalog

## Song
- 1-to-1: Cart Song Items, Format Type, Genre

#### Crud Functionalities
- Create: [ADMIN] Admin can add songs
- Read: Customer (and admin) can view songs and song info
- Update: [ADMIN] Admin can update song information
- Delete: [ADMIN] Admin can delete songs from catalog

## Category
- 1-to-many: Product 

#### Crud Functionalities
- Create: [Admin] Admin can add categories
- Read: Customers (and admins) can view categories
- Update: [Admin] Admin can change categories
- Delete: [Admin] Admin can delete categories

## Condition
- 1-to-many: Product

#### Crud Functionalities
- Create: [Admin] Admin can add condition types
- Read: Customers (and admins) can view condition types
- Update: [Admin] Admin can change condition types
- Delete: [Admin] Admin can delete condition types

## Format Type
- 1-to-many: Song

#### Crud Functionalities
- Create: [Admin] Admin can add condition format types
- Read: Customers (and admins) can view format types
- Update: [Admin] Admin can change format types
- Delete: [Admin] Admin can delete format types

## Genre
- 1-to-many: Song

#### Crud Functionalities
- Create: [Admin] Admin can add genres
- Read: Customers (and admins) can view genres
- Update: [Admin] Admin can change genres
- Delete: [Admin] Admin can delete genres

# Frontend
- Login
- Register
- View Customer bio page

# Backend