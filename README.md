# ecommerce-business-analysis-SQL
End-to-end E-commerce sales analysis using SQL | Revenue, Profit, Customer &amp; Time-series insights with advanced queries

## 📌 Project Overview

This project focuses on performing end-to-end sales analytics on an E-commerce dataset using SQL.

The goal is to analyze customer purchases, product performance, and order trends to generate meaningful business insights and KPIs that help in decision-making.

Instead of just writing basic queries, this project simulates how a Data Analyst works with real transactional data to answer practical business questions.

## 🎯 Objectives

The analysis aims to:

- Measure total revenue and sales performance

- Identify top customers and repeat buyers

- Analyze product and category performance

- Track monthly sales and growth trends

- Calculate business KPIs like AOV and MoM growth

- Extract insights that can help improve business strategy

## 📂 Dataset Description

The dataset contains 4 relational CSV files, directly imported into the database:


Tables Used:
#### 🧑 Customers

Customer demographic details
(customer_id, name, gender, age_group, country, signup_date)

#### 📦 Products

Product information with pricing
(product_id, product_name, category, unit_price, cost)

#### 🧾 Orders

Order-level transactions
(order_id, customer_id, order_date, status, payment_method, shipping_country)

#### 🛍️ Order_Items

Line-level purchase details
(order_item_id, order_id, product_id, quantity)


## 🔗 Data Model
Customers → Orders → Order_Items ← Products

One customer → many orders

One order → many products

One product → many sales

This structure follows a star schema, commonly used in Business Intelligence systems.


## 🔍 Data Exploration

Initial exploration included:

- Checking row counts of each table

- Understanding relationships between tables

- Identifying primary & foreign keys

- Reviewing data types (dates, numeric fields)

- Verifying missing/null values

- Validating pricing and quantity fields

#### Example checks:

SELECT COUNT(*)
FROM orders;

SELECT DISTINCT category
FROM products;

SELECT MIN(order_date), MAX(order_date)
FROM orders; 


## 🧹 Data Cleaning

- Basic cleaning steps performed:

- Converted date columns to proper DATE format

- Verified numeric columns (price, cost, quantity)

- Removed inconsistencies in joins

- Ensured no duplicate IDs

- Validated null values

Since the dataset was mostly clean, minimal preprocessing was required.

## 📊 Data Analysis

SQL queries were written to generate business insights using:

Techniques Used

- Joins (INNER, LEFT)

- Aggregations (SUM, COUNT, AVG)

- GROUP BY

- CTEs

- Window Functions

- Date-based grouping

- Ranking & growth analysis

## Key Metrics Calculated

### 📈 Sales Metrics

- Total Revenue

- Total Orders

- Units Sold

- Average Order Value (AOV)

### 👥 Customer Metrics

- Top spending customers

- Repeat customers

- Customers with no orders

### 🛍️ Product Metrics

- Top selling products

- Category-wise revenue

- Best product in each category

- Profit calculation

### 📅 Time-based Metrics

- Monthly revenue trend

- Monthly order trend

- Running revenue total

- Month-over-Month growth %

## 🔎 Findings / Insights

Some important insights discovered:

- Few products contribute majority of revenue (Pareto effect)

- Repeat customers generate higher overall sales

- Certain categories outperform others consistently

- Revenue shows clear monthly growth trend

- Window functions helped identify ranking & growth patterns efficiently

These insights can help businesses optimize:

- marketing strategies

- inventory planning

- customer retention

- pricing decisions

## 📑 Reports 

The following analytical reports were created using SQL:

- Sales Summary 

- Customer Ranking 

- Category Performance 

- Monthly Revenue Trend 

- Running Total Revenue 

- MoM Growth 

## 🛠️ SQL Concepts Demonstrated

✔ Complex Joins
✔ Aggregations
✔ Subqueries & CTEs
✔ Window Functions (RANK, LAG, Running Total)
✔ Date Functions
✔ Business KPI calculations

## ▶️ How to Run

- Import CSV files into MySQL/PostgreSQL

- Load data into tables

- Execute ecommerce_sql_queries.sql

- Run queries to reproduce insights

## 🎯 Conclusion

This project demonstrates how SQL can be used to transform raw transactional data into actionable business insights.

It highlights skills in:

- data exploration

- analytical thinking

- SQL querying

- business KPI design

The workflow closely resembles tasks performed by Data Analysts and Business Intelligence professionals in real organizations.

## 👨‍💻 Author

#### Saurabh Verma
#### Data Analytics | SQL | Python | Power BI
