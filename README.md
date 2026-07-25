# 🛒 Zepto E-Commerce Inventory Analysis using SQL

## 📌 Project Overview

This project analyzes Zepto's e-commerce inventory dataset using PostgreSQL to uncover meaningful business insights through SQL. The project demonstrates the complete data analysis workflow, including data exploration, data cleaning, and business analysis on a real-world retail inventory dataset.

The objective is to transform raw inventory data into actionable insights that can support pricing strategies, inventory management, and business decision-making.

---

## 🎯 Objectives

- Perform Exploratory Data Analysis (EDA)
- Clean and preprocess raw inventory data
- Analyze product pricing and discount strategies
- Evaluate stock availability and inventory distribution
- Generate business insights using SQL
- Strengthen SQL skills through real-world business scenarios

---

## 📂 Dataset

**Source:** Kaggle

The dataset contains inventory information for products listed on Zepto, including product details, pricing, discounts, stock availability, and inventory quantities.

### Dataset Columns

| Column | Description |
|---------|-------------|
| sku_id | Unique product identifier |
| category | Product category |
| name | Product name |
| mrp | Maximum Retail Price |
| discountPercent | Discount percentage |
| discountedSellingPrice | Final selling price after discount |
| availableQuantity | Available inventory quantity |
| weightInGms | Product weight in grams |
| outOfStock | Stock availability status |
| quantity | Units per package |

---

## 🛠️ Tools & Technologies

- PostgreSQL
- pgAdmin
- SQL

---

## 📊 Project Workflow

### 1. Database Setup

- Created database table
- Defined appropriate data types
- Imported CSV dataset into PostgreSQL

### 2. Data Exploration

- Counted total records
- Explored dataset structure
- Identified missing values
- Examined unique product categories
- Compared in-stock and out-of-stock products
- Identified duplicate product listings

### 3. Data Cleaning

- Removed invalid records
- Converted prices from paise to rupees
- Standardized data for analysis

### 4. Business Analysis

Performed SQL analysis to answer key business questions such as:

- Top 10 products with the highest discounts
- High-value products currently out of stock
- Estimated revenue by product category
- Premium products with low discounts
- Categories offering the highest average discounts
- Best value products based on price per gram
- Product segmentation by weight
- Total inventory weight by category

---

## 📈 SQL Concepts Used

- SELECT
- WHERE
- ORDER BY
- GROUP BY
- HAVING
- Aggregate Functions
- CASE WHEN
- Data Cleaning
- DISTINCT
- DELETE
- UPDATE

---

## 📁 Repository Structure

```
zepto-sql-data-analysis/
│
├── README.md
├── zepto_inventory_analysis.sql
└── zepto_v2.csv
```

---

## 💼 Key Business Insights

- Identified categories generating the highest estimated inventory value.
- Analyzed products offering the highest discounts.
- Detected premium products that were unavailable in stock.
- Compared inventory availability across different product categories.
- Calculated price per gram to identify value-for-money products.
- Categorized products based on weight for inventory segmentation.

---

## 🚀 Skills Demonstrated

- SQL Query Writing
- Data Cleaning
- Exploratory Data Analysis (EDA)
- Retail & E-Commerce Analytics
- Inventory Analysis
- Pricing Analysis
- Business Problem Solving
- Data Interpretation

---

## ⭐ Project Highlights

- Real-world E-Commerce Dataset
- End-to-End SQL Analysis
- Business-Oriented Insights
- Portfolio-Ready Project
- Beginner to Intermediate SQL Concepts
