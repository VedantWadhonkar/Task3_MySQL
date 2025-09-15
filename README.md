# Task3_MySQL
Inventory Management System
Description

This project is a simple Inventory Management System implemented in MySQL. It allows you to manage products in a store by adding new products, updating stock, and retrieving product details using stored procedures.

Database
Database Name: Inventorydb
Table: product
| Column Name | Data Type     | Description                   |
| ----------- | ------------- | ----------------------------- |
| product\_id | INT           | Primary Key, Auto Increment   |
| name        | VARCHAR(50)   | Name of the product           |
| quantity    | INT           | Quantity in stock (default 0) |
| price       | DECIMAL(10,2) | Price of the product          |

Stored Procedures

AddProduct

Adds a new product to the inventory.

Parameters:

p_name (VARCHAR) – Product name

p_qty (INT) – Quantity

p_price (DECIMAL) – Price

UpdateStock

Updates the quantity of an existing product.

Parameters:

p_id (INT) – Product ID

p_qty_change (INT) – Quantity change (+ to add, - to reduce)

GetProduct

Retrieves product details by ID.

Parameters:

p_id (INT) – Product ID
Features

Add new products to the inventory

Update stock quantity easily

Retrieve product details by ID

Simple, clean SQL-based implementation
