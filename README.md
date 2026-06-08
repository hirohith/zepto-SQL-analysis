# 🛒 Zepto Inventory Data Analysis using SQL (MySQL)

## 📖 Project Overview

This project performs **data cleaning, exploratory analysis, and business intelligence reporting** on a retail inventory dataset inspired by a quick-commerce platform like Zepto.

Using **MySQL Workbench** and **SQL**, the project transforms raw inventory data into actionable business insights related to pricing, discounts, inventory management, revenue estimation, and product value analysis.

The objective is to demonstrate how SQL can be used for:

* Data cleaning and validation
* Exploratory data analysis (EDA)
* Business performance reporting
* Retail inventory decision-making
* Revenue and pricing analytics

---

## 🎯 Problem Statement

Retail and quick-commerce platforms manage thousands of products across multiple categories. Business teams need data-driven answers to questions such as:

* Which products provide the highest discounts?
* Which expensive products are currently out of stock?
* Which categories generate the highest revenue?
* How do discount strategies vary across categories?
* Which products offer the best value for money?
* How is inventory weight distributed across categories?

This project answers these questions using SQL-based analytical techniques.

---

## 🛠️ Technologies Used

* MySQL Workbench
* SQL

  * DDL (Data Definition Language)
  * DML (Data Manipulation Language)
  * Aggregate Functions
  * CASE Statements
  * GROUP BY
  * HAVING
  * ORDER BY
  * Subqueries

---

## 🗂️ Database Schema

### Table: `zepto`

| Column Name            | Data Type    | Description                  |
| ---------------------- | ------------ | ---------------------------- |
| sku_id                 | SERIAL (PK)  | Unique SKU identifier        |
| category               | VARCHAR(120) | Product category             |
| name                   | VARCHAR(150) | Product name                 |
| mrp                    | NUMERIC(8,2) | Maximum Retail Price         |
| discountPercent        | NUMERIC(5,2) | Discount percentage          |
| availableQuantity      | INTEGER      | Available stock quantity     |
| discountedSellingPrice | NUMERIC(8,2) | Selling price after discount |
| weightInGms            | INTEGER      | Product weight in grams      |
| outOfStock             | BOOLEAN      | Stock availability status    |
| quantity               | INTEGER      | Pack quantity                |

---

## 🧹 Data Cleaning Process

Before analysis, the dataset was cleaned and validated using SQL.

### Cleaning Steps

✅ Removed products with invalid prices (`MRP = 0`)

✅ Converted prices from paise to rupees

✅ Checked for NULL values

✅ Identified duplicate product names

✅ Validated inventory availability records

✅ Verified consistency between stock quantity and out-of-stock status

---

## 🔍 Exploratory Data Analysis (EDA)

The following exploratory analyses were performed:

* Total number of products
* Sample data inspection
* Distinct product categories
* Stock availability distribution
* Out-of-stock product analysis
* Duplicate product identification
* Category-level inventory overview

---

# 📊 Business Analysis

## 1️⃣ Top 10 Best-Value Products

Identifies products with the highest discount percentages.

### Business Value

* Highlights promotional products
* Helps understand aggressive discount strategies

---

## 2️⃣ High MRP Products Currently Out of Stock

Finds premium products that are unavailable.

### Business Value

* Identifies potential revenue loss
* Supports inventory replenishment decisions

---

## 3️⃣ Estimated Revenue by Category

Calculates:

Revenue = Discounted Selling Price × Available Quantity

### Business Value

* Reveals revenue-driving categories
* Helps prioritize inventory investment

---

## 4️⃣ Premium Products with Low Discounts

Filters products where:

* MRP > ₹500
* Discount < 10%

### Business Value

* Identifies premium pricing strategy
* Highlights products maintaining strong margins

---

## 5️⃣ Categories with Highest Average Discount

Computes average discounts across categories.

### Business Value

* Evaluates category-wise promotional strategy
* Supports pricing optimization

---

## 6️⃣ Best Price per Gram Analysis

Identifies products offering maximum quantity for minimum cost.

### Business Value

* Measures customer value
* Helps compare products fairly across package sizes

---

## 7️⃣ Weight-Based Product Segmentation

Products are categorized as:

| Segment       | Weight |
| ------------- | ------ |
| Low Weight    | < 1 kg |
| Medium Weight | 1–5 kg |
| Bulk Products | > 5 kg |

### Business Value

* Supports logistics planning
* Improves warehouse organization

---

## 8️⃣ Total Inventory Weight by Category

Calculates cumulative inventory weight per category.

### Business Value

* Measures storage requirements
* Supports warehouse capacity planning

---

# 💡 Key Insights Generated

This analysis helps uncover:

* Discount effectiveness
* High-value stock risks
* Revenue-generating categories
* Value-for-money products
* Inventory distribution trends
* Storage and logistics considerations

---

# 📁 Project Structure

```text
zepto-sql-analysis/
│
├── zepto_SQL_Data_analysis.sql
│   ├── Table Creation
│   ├── Data Cleaning Queries
│   ├── Exploratory Analysis
│   └── Business Analysis Queries
│
├── zepto_v2.csv
│   └── Product Inventory Dataset
│
├── README.md
│
└── LICENSE
```

---

# ▶️ How to Run the Project

### Step 1: Create Database

```sql
CREATE DATABASE zepto_analysis;
USE zepto_analysis;
```

### Step 2: Create Table

Run the table creation script included in:

```text
zepto_SQL_Data_analysis.sql
```

### Step 3: Import Dataset

Import:

```text
zepto_v2.csv
```

into the `zepto` table using MySQL Workbench.

### Step 4: Execute Queries

Run the SQL file section by section:

1. Data Cleaning
2. Exploratory Analysis
3. Business Analysis

---

# 📚 Skills Demonstrated

### SQL

* Data Cleaning
* Data Validation
* Aggregations
* Filtering
* Sorting
* Grouping
* Conditional Logic
* Business Analytics

### Data Analysis

* Revenue Analysis
* Inventory Analytics
* Discount Analysis
* Product Segmentation
* Value Analysis

### Business Intelligence

* KPI Reporting
* Retail Analytics
* Decision Support
* Inventory Insights

---

# 🚀 Future Enhancements

* Add SQL Indexing for query optimization
* Create Stored Procedures for automated reporting
* Develop Power BI dashboard
* Develop Tableau dashboard
* Build automated data quality checks
* Add inventory forecasting using Python

---

# 🎓 Learning Outcomes

Through this project, I gained experience in:

* Cleaning real-world retail data
* Writing analytical SQL queries
* Performing business-oriented data analysis
* Extracting actionable insights from inventory datasets
* Applying SQL to solve practical business problems

---

## 👨‍💻 Author

**Sheru Rohith**

Aspiring Data Analyst | SQL | Python | Power BI | Machine Learning

### Connect With Me

* GitHub: https://github.com/hirohith
* LinkedIn: linkedin.com/in/sheru-rohith-535b5432b


