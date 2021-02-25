# Files
- FSD Java Capstone pdf is original capstone pdf with the writing prompt, diagrams, and wireframes.
- Visual Schema Diagram is a PNG screen shot of a schema mocked up in dbdiagram.io 
- Schema Code.txt is the code I wrote in dbdiagram.io to make the schema representation

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
- 

## Shopping Cart
- 1-to-1: Purchase Info
- 1-to-many: Cart Product Items, Cart Song Items
- many-to-1: Customer
- Join Table (That can be referred to any items being purchased by one user)

#### Crud Functionalities
- 

## Purchase Info
- 1-to-1: Shopping Cart
- many-to-1: Customer
- Join Table (also serves to show when a Shopping Cart is no longer active by Purchase Info's existence)

#### Crud Functionalities
-

## Cart Product Items
- 1-to-1: Product
- mant-to-1: Shopping Cart
- Join Table

#### Crud Functionalities
-

## Cart Song Items
- 1-to-1: Song
- mant-to-1: Shopping Cart
- Join Table

#### Crud Functionalities
-

## Product
- 1-to-1: Cart Product Items, Category, Condition

#### Crud Functionalities
-

## Song
- 1-to-1: Cart Song Items, Format Type, Genre

#### Crud Functionalities
-

## Category
- 1-to-many: Product 
- Fixed Set: [Accessory, Amp, Instrument, etc]

#### Crud Functionalities
-

## Condition
- 1-to-many: Product
- Fixed Set: [New, Like New, Used, Worn, etc]

#### Crud Functionalities
-

## Format Type
- 1-to-many: Song
- Fixed Set: [CD, Digital, Vinyl, etc]

#### Crud Functionalities
-

## Genre
- 1-to-many: Song
- Fixed Set: [Rock, Blues, Jazz, Ska, Funk, etc]

#### Crud Functionalities
-
