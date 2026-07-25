# 🛒 Zepto E-Commerce Inventory Analysis using SQL

## 📌 Project Overview

This project analyzes Zepto's e-commerce inventory dataset using PostgreSQL to extract meaningful business insights. It demonstrates how SQL can be used for data exploration, cleaning, and business analysis on a real-world retail dataset.

The objective of this project is to transform raw inventory data into actionable insights that support pricing, inventory management, and product performance analysis.

---

## 🎯 Objectives

- Perform Exploratory Data Analysis (EDA)
- Clean and prepare raw inventory data
- Analyze pricing and discount strategies
- Evaluate inventory availability
- Generate business insights using SQL
- Practice real-world SQL queries used by Data Analysts

---

## 📂 Dataset

**Source:** Kaggle

The dataset contains inventory information for products listed on Zepto, including pricing, discounts, stock availability, product categories, and product weight.

### Dataset Columns

- SKU ID
- Product Name
- Category
- MRP
- Discount Percentage
- Discounted Selling Price
- Available Quantity
- Weight (grams)
- Stock Status
- Package Quantity

---

## 🛠️ Tools & Technologies

- PostgreSQL
- pgAdmin
- SQL

---

## 📊 Project Workflow

### 1. Database Creation

- Created database
- Designed table schema
- Defined appropriate data types
- Imported CSV dataset

---

### 2. Data Exploration

- Counted total records
- Checked data structure
- Identified null values
- Explored unique categories
- Compared in-stock and out-of-stock products
- Identified duplicate product entries

---

### 3. Data Cleaning

- Removed invalid records
- Converted pricing from paise to rupees
- Standardized data for analysis
- Verified cleaned dataset

---

### 4. Business Analysis

Performed SQL analysis to answer business questions such as:

- Top products with the highest discounts
- High-value products currently out of stock
- Estimated revenue by category
- Products with MRP above ₹500
- Categories offering the highest average discounts
- Best value products based on price per gram
- Inventory distribution by category
- Product weight segmentation
- Stock availability analysis

---

## 📈 SQL Concepts Used

- SELECT
- WHERE
- ORDER BY
- GROUP BY
- HAVING
- Aggregate Functions
- CASE WHEN
- Joins
- Common Table Expressions (CTEs)
- Subqueries
- Window Functions
- Data Cleaning Techniques

---

## 📁 Repository Structure

```
├── Dataset/
│   └── zepto_inventory.csv
│
├── SQL Queries/
│   └── zepto_inventory_analysis.sql
│
├── README.md
```

---

## 💼 Business Insights

Some key insights generated from the analysis include:

- Product categories with the highest inventory value
- Categories providing the largest discounts
- Products offering the best value for money
- Inventory shortages across premium products
- Pricing patterns across different categories
- Overall inventory distribution

---

## 🚀 Skills Demonstrated

- SQL Query Writing
- Data Cleaning
- Exploratory Data Analysis (EDA)
- Business Problem Solving
- Retail & E-Commerce Analytics
- Inventory Analysis
- Pricing Analysis
- Data Interpretation

---

## ⭐ Project Highlights

- Real-world E-commerce Dataset
- End-to-End SQL Analysis
- Business-Oriented Insights
- Interview-Level SQL Queries
- Portfolio-Ready Project
