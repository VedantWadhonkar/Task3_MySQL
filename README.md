# Task3_MySQL
# Inventory Management System

## Description
This project is a simple **Inventory Management System** using **MySQL**.  
It allows you to manage products by adding new items, updating stock, and retrieving product details using **stored procedures**.

---

## Database

**Database Name:** `Inventorydb`  

**Table:** `product`  

| Column Name | Data Type     | Description                  |
| ----------- | ------------ | ---------------------------- |
| product_id  | INT          | Primary Key, Auto Increment  |
| name        | VARCHAR(50)  | Name of the product          |
| quantity    | INT          | Quantity in stock (default 0)|
| price       | DECIMAL(10,2)| Price of the product         |

---

## Stored Procedures

### 1. AddProduct
- Adds a new product to the inventory.  
- **Parameters:**  
  - `p_name` (VARCHAR) – Product name  
  - `p_qty` (INT) – Quantity  
  - `p_price` (DECIMAL) – Price  

### 2. UpdateStock
- Updates the quantity of an existing product.  
- **Parameters:**  
  - `p_id` (INT) – Product ID  
  - `p_qty_change` (INT) – Quantity change (+ to add, - to reduce)  

### 3. GetProduct
- Retrieves product details by ID.  
- **Parameters:**  
  - `p_id` (INT) – Product ID  

---

## Sample Usage

```sql
-- Add products
CALL AddProduct('Laptop', 10, 55000.00);
CALL AddProduct('Mouse', 50, 500.00);
CALL AddProduct('Keyboard', 20, 1200.00);

-- View all products
SELECT * FROM product;

-- Update stock
CALL UpdateStock(1, 5);  -- Add 5 laptops
CALL UpdateStock(2, -2); -- Reduce 2 mice

-- Get product details
CALL GetProduct(1);  -- Laptop
CALL GetProduct(2);  -- Mouse
