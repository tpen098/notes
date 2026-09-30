---
aliases: []
tags: []
date created: Monday, September 28th 2026, 9:05:38 pm
date modified: Monday, September 28th 2026, 9:19:12 pm
---

# Lab Exercise 04: Basic SQL Queries

This is the PDF submission required for the fourth optional lab exercise in CS 197 FZZQ, submitted by Stephen Singer on September 28, 2026.

## Database Setup

The SQL file uses the north wind database. However, the link provided in the modules is broken. Therefore, the original database is used. Because of this, there are missing fields needed for the exercise such as the `ListPrice`. Kindly run the following to generate dummy values to formally test the queries in the succeeding sections.

```sql
USE northwind;

-- Add missing columns (ignore error if they already exist)
ALTER TABLE Products ADD COLUMN ListPrice DECIMAL(10,2);
ALTER TABLE Products ADD COLUMN UnitCost DECIMAL(10,2);

-- Populate values
SET SQL_SAFE_UPDATES = 0;

UPDATE Products 
SET 
    ListPrice = UnitPrice
WHERE
    ListPrice IS NULL;
UPDATE Products 
SET 
    UnitCost = 19.75
WHERE
    ProductID = 17;
UPDATE Products 
SET 
    UnitCost = 6.00
WHERE
    ProductID = 3;
UPDATE Products 
SET 
    UnitCost = ROUND(ListPrice * 0.50, 2)
WHERE
    UnitCost IS NULL;

SET SQL_SAFE_UPDATES = 1;


```

## Employee Contact Sheet

> [!example] First Instruction
> We need an Employee Contact sheet. Show their First Name, Last Name and Phone Number, and sort by First name.

```sql
-- Query 1: Employee Contact Sheet
SELECT 
    FirstName, 
    LastName, 
    HomePhone
FROM 
    Employees
ORDER BY 
    FirstName ASC;
```

## Suppliers

> [!example] Second Instruction
> Show the Company Name, Country, and City of the suppliers. Sort by Country first, City next, then Company Name.

```sql
-- Query 2: Suppliers
SELECT 
    CompanyName, 
    Country, 
    City
FROM 
    Suppliers
ORDER BY 
    Country ASC, 
    City ASC, 
    CompanyName ASC;
```

## July Birthday Celebrants

> [!example] Third Instruction
> Show the Employee Name (First, Last) and Birthday of all employees that will celebrate their birthday this July.

```sql
-- Query 3: Employees with July Birthday
SELECT 
    FirstName, 
    LastName, 
    BirthDate
FROM 
    Employees
WHERE 
    MONTH(BirthDate) = 7
ORDER BY 
    BirthDate ASC;
```

## Profit per Product

> [!example] Fourth Instruction
> Show the Product Id, Product Name, List Price, Unit Cost, and Profit (calculated) of the products, sorted by Product Name.

```sql
-- Query 4: Profit per product
SELECT 
    ProductID, 
    ProductName, 
    ListPrice, 
    UnitCost, 
    (ListPrice - UnitCost) AS Profit
FROM 
    Products
ORDER BY 
    ProductName ASC;

```

## Profitable Products

> [!example] Final Instruction
> Show the Product ID, Product Name, and Profit per product, sorted by profit in descending order.

```sql
-- Query 5: Profitable Products
SELECT 
    ProductID, 
    ProductName, 
    (ListPrice - UnitCost) AS Profit
FROM 
    Products
WHERE 
    (ListPrice - UnitCost) > 0
ORDER BY 
    Profit DESC;
```
