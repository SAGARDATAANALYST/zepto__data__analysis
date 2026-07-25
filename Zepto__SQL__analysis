/*==============================================================
 Project: Zepto E-Commerce Inventory Analysis using SQL
 Database: PostgreSQL
 Author: Sagar Prasad

 Description:
 This project performs data exploration, data cleaning, and
 business analysis on Zepto's inventory dataset using SQL.

==============================================================*/


/*==============================================================
DROP EXISTING TABLE
==============================================================*/

DROP TABLE IF EXISTS zepto;


/*==============================================================
CREATE TABLE
==============================================================*/

CREATE TABLE zepto (
    sku_id SERIAL PRIMARY KEY,
    category VARCHAR(120),
    name VARCHAR(150) NOT NULL,
    mrp NUMERIC(8,2),
    discountPercent NUMERIC(5,2),
    availableQuantity INTEGER,
    discountedSellingPrice NUMERIC(8,2),
    weightInGms INTEGER,
    outOfStock BOOLEAN,
    quantity INTEGER
);


/*==============================================================
DATA EXPLORATION
==============================================================*/

---------------------------------------------------------------
-- 1. Total Number of Records
---------------------------------------------------------------

SELECT COUNT(*) AS total_records
FROM zepto;


---------------------------------------------------------------
-- 2. Preview Dataset
---------------------------------------------------------------

SELECT *
FROM zepto
LIMIT 10;


---------------------------------------------------------------
-- 3. Check for Missing Values
---------------------------------------------------------------

SELECT *
FROM zepto
WHERE name IS NULL
   OR category IS NULL
   OR mrp IS NULL
   OR discountPercent IS NULL
   OR discountedSellingPrice IS NULL
   OR weightInGms IS NULL
   OR availableQuantity IS NULL
   OR outOfStock IS NULL
   OR quantity IS NULL;


---------------------------------------------------------------
-- 4. List All Product Categories
---------------------------------------------------------------

SELECT DISTINCT category
FROM zepto
ORDER BY category;


---------------------------------------------------------------
-- 5. Products In Stock vs Out of Stock
---------------------------------------------------------------

SELECT
    outOfStock,
    COUNT(*) AS total_products
FROM zepto
GROUP BY outOfStock;


---------------------------------------------------------------
-- 6. Products Appearing Multiple Times
---------------------------------------------------------------

SELECT
    name,
    COUNT(sku_id) AS number_of_skus
FROM zepto
GROUP BY name
HAVING COUNT(sku_id) > 1
ORDER BY number_of_skus DESC;



/*==============================================================
DATA CLEANING
==============================================================*/

---------------------------------------------------------------
-- 7. Find Products with Invalid Price
---------------------------------------------------------------

SELECT *
FROM zepto
WHERE mrp = 0
   OR discountedSellingPrice = 0;


---------------------------------------------------------------
-- 8. Remove Invalid Records
---------------------------------------------------------------

DELETE FROM zepto
WHERE mrp = 0;


---------------------------------------------------------------
-- 9. Convert Price from Paise to Rupees
---------------------------------------------------------------

UPDATE zepto
SET
    mrp = mrp / 100.0,
    discountedSellingPrice = discountedSellingPrice / 100.0;


---------------------------------------------------------------
-- 10. Verify Updated Prices
---------------------------------------------------------------

SELECT
    mrp,
    discountedSellingPrice
FROM zepto;



/*==============================================================
BUSINESS ANALYSIS
==============================================================*/

---------------------------------------------------------------
-- Q1. Top 10 Products with Highest Discount Percentage
---------------------------------------------------------------

SELECT DISTINCT
    name,
    mrp,
    discountPercent
FROM zepto
ORDER BY discountPercent DESC
LIMIT 10;



---------------------------------------------------------------
-- Q2. High MRP Products Currently Out of Stock
---------------------------------------------------------------

SELECT DISTINCT
    name,
    mrp
FROM zepto
WHERE outOfStock = TRUE
  AND mrp > 300
ORDER BY mrp DESC;



---------------------------------------------------------------
-- Q3. Estimated Revenue by Product Category
---------------------------------------------------------------

SELECT
    category,
    SUM(discountedSellingPrice * availableQuantity) AS estimated_revenue
FROM zepto
GROUP BY category
ORDER BY estimated_revenue DESC;



---------------------------------------------------------------
-- Q4. Products with MRP Greater than ₹500
--     and Discount Less than 10%
---------------------------------------------------------------

SELECT DISTINCT
    name,
    mrp,
    discountPercent
FROM zepto
WHERE mrp > 500
  AND discountPercent < 10
ORDER BY mrp DESC,
         discountPercent DESC;



---------------------------------------------------------------
-- Q5. Top 5 Categories with Highest Average Discount
---------------------------------------------------------------

SELECT
    category,
    ROUND(AVG(discountPercent),2) AS average_discount
FROM zepto
GROUP BY category
ORDER BY average_discount DESC
LIMIT 5;



---------------------------------------------------------------
-- Q6. Best Value Products (Price Per Gram)
---------------------------------------------------------------

SELECT DISTINCT
    name,
    weightInGms,
    discountedSellingPrice,
    ROUND(discountedSellingPrice / weightInGms,2) AS price_per_gram
FROM zepto
WHERE weightInGms >= 100
ORDER BY price_per_gram ASC;



---------------------------------------------------------------
-- Q7. Categorize Products by Weight
---------------------------------------------------------------

SELECT DISTINCT
    name,
    weightInGms,
    CASE
        WHEN weightInGms < 1000 THEN 'Low'
        WHEN weightInGms < 5000 THEN 'Medium'
        ELSE 'Bulk'
    END AS weight_category
FROM zepto;



---------------------------------------------------------------
-- Q8. Total Inventory Weight by Category
---------------------------------------------------------------

SELECT
    category,
    SUM(weightInGms * availableQuantity) AS total_inventory_weight
FROM zepto
GROUP BY category
ORDER BY total_inventory_weight DESC;



/*==============================================================
END OF PROJECT
==============================================================*/
