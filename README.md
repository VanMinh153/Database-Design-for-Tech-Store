# Design Database
<img align="left" alt="NodeJS" width="30px" style="padding-right:10px;" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postgresql/postgresql-original-wordmark.svg" />
<br />

## Introduction
* This is a project for the database lab course
* Purpose: To design a database to store and interact with data from an online electronics store
* Relational database management system : **PostgreSQL**

## Design
> Overview of design
* The database consists of 4 entities – customers, products, categories and orders. Each customer has a shopping cart (cartlines) containing product codes and intended purchase quantities. Customers also have multiple orders (orders), details of each order are stored in the orderlines table. Customer feedback on purchased products is stored in the feedback table. 

* The database is comprised of 7 tables. There are 4 tables corresponding to the 4 entities: customers, products, categories, orders and 3 associative entity tables to model many-to-many relationships: cartlines, orderlines, feedback.
### ER Diagram
> Visualizes the logical structure and relationships between different entities my system.
![ERD](https://github.com/nvq29Apr/Ecommerce/assets/119597631/6a1381a6-49ab-4ec2-bc7c-684f51a2128a)

## Relational Schema
> Shows the detailed logical schema design for implementation as relational tables in RDBMS.
![RS](https://github.com/nvq29Apr/Ecommerce/assets/119597631/3ab3291d-8c5e-461f-b01b-a0e518658f5e)

## Object Descriptions and Necessity Level
### 1. Product Management (products table)
Includes information about products.

### 2. Order Management (orders table)
Helps track order status, order details including purchased products, customers, purchase dates, etc.

### 3. Customer Management
Stores customer information such as personal details, registered accounts and passwords. Also indicates customer loyalty via join date, total spending amount.

### 4. Category Management (categories table)
Product categories being sold, facilitating management for sellers and search for buyers.

### 5. Shopping Cart Management (cartlines table)
Manages products that customers are interested in but have not decided to purchase yet, can be added to cart in advance.

### 6. Product Review Management (feedback table)
Stores customer reviews after purchasing a product, helping other customers reference experiences from past buyers. Also allows the seller to acknowledge and improve quality.

## Demo
> _Some CRUD on my Database_
### Create table and initial data
> CREATE, INSERT, UPDATE
![createdata-ezgif com-video-to-gif-converter](https://github.com/nvq29Apr/Ecommerce/assets/119597631/de0869fe-f134-4d99-abac-1e79d759e666)
### Querying and Filtering data
* _Select laptops which price is less than 20m VND, display size is 15.6inch, and 8GB of RAM_ ![image](https://github.com/nvq29Apr/Ecommerce/assets/119597631/1e3cbcc6-10bc-4068-b8d7-4f1e30e13de8)
* _Show laptop list by Price low to high_ ![image](https://github.com/nvq29Apr/Ecommerce/assets/119597631/44560186-26f8-4822-9c31-3d1ba5ac5edf)

> [!NOTE]
> See more about **query and trigger, function** included at [select-function-trigger.sql](https://github.com/VanMinh153/Database-Design-for-Tech-Store/blob/main/Function-Trigger-Query.sql)
