🛒 Zepto Inventory Data Analysis using SQL (MySQL)
This project performs data cleaning, exploration, and business analysis on a retail inventory dataset inspired by a quick-commerce platform (Zepto).
The goal is to extract business insights from raw product data using pure SQL in MySQL Workbench.
It demonstrates how SQL can be used not just for querying data, but for real-world data preparation and analytical decision-making.
________________________________________
📌 Problem Statement
Retail and quick-commerce platforms manage thousands of SKUs across categories.
To make pricing, inventory, and discount decisions, businesses need answers like:
•	Which products offer the best value?
•	Which expensive items are out of stock?
•	Which categories generate the highest revenue?
•	How does discount strategy vary across categories?
•	What is the inventory weight distribution?
This project answers these questions using structured SQL analysis.
________________________________________
🗂️ Database Schema
Table: zepto
Column	                  Type	         Description
sku_id	                SERIAL (PK)	     Unique SKU identifier
category	              VARCHAR(120)	   Product category
name	                  VARCHAR(150)	   Product name
mrp	                    NUMERIC(8,2)	   Maximum retail price
discountPercent	        NUMERIC(5,2)	   Discount offered
availableQuantity	      INTEGER	         Units available
discountedSellingPrice	NUMERIC(8,2)	   Selling price after discount
weightInGms	            INTEGER	         Product weight
outOfStock	            BOOLEAN	         Stock status
quantity								INTEGER				   Pack quantity
________________________________________
⚙️ Tools Used
•	MySQL Workbench
•	SQL (DDL, DML, Aggregations, CASE, GROUP BY, HAVING, ORDER BY)
________________________________________
🧹 Data Cleaning Steps
•	Identified and removed products with invalid price (MRP = 0)
•	Converted price values from paise to rupees
•	Checked for NULL values
•	Identified duplicate product names across SKUs
•	Validated stock availability data
________________________________________
🔍 Data Exploration
•	Total number of records
•	Sample data inspection
•	Distinct product categories
•	Stock vs Out-of-stock distribution
•	Duplicate product detection
________________________________________
📊 Business Analysis Queries
1. Top 10 Best-Value Products (Highest Discount)
Identifies products offering the highest discount percentage.
2. High MRP Products That Are Out of Stock
Highlights expensive items currently unavailable.
3. Estimated Revenue Per Category
SUM(discountedSellingPrice × availableQuantity)
Estimates revenue potential by category.
4. Premium Products with Low Discount
MRP > ₹500 and discount < 10%.
5. Categories with Highest Average Discount
Shows discount strategy across categories.
6. Best Price Per Gram (Value Analysis)
Finds products offering best cost per gram for items above 100g.
7. Weight-Based Product Segmentation
Products grouped into:
•	Low (< 1kg)
•	Medium (< 5kg)
•	Bulk (> 5kg)
8. Total Inventory Weight Per Category
Measures warehouse load and storage distribution.
________________________________________
💡 Key Insights This Project Can Reveal
•	Discount strategy effectiveness
•	Inventory risk (high-value out-of-stock items)
•	Revenue-driving categories
•	Value-for-money product identification
•	Storage and logistics insights from weight analysis
________________________________________
▶️ How to Run
1.	Open MySQL Workbench
2.	Create a new schema/database
3.	Run the table creation script
4.	Import the dataset into the zepto table
5.	Execute the queries step by step
________________________________________
📁 Project Structure
zepto-sql-analysis/
│
├── zepto_SQL_Data_analysis       # Table creation + all queries
├── zepto_v2      # Product dataset
└── README.md
________________________________________
🎯 Learning Outcomes
This project demonstrates:
•	Practical SQL for data cleaning
•	Writing analytical SQL queries for business use-cases
•	Translating raw inventory data into actionable insights
•	Real-world retail analytics using only SQL
________________________________________
🚀 Future Improvements
•	Create indexes for performance optimization
•	Build Power BI / Tableau dashboard on top of this dataset
•	Add stored procedures for reusable reports
•	Automate data validation checks
________________________________________
📌 Author
Sheru Rohith
Aspiring Data Analyst | SQL | Power BI | Python

