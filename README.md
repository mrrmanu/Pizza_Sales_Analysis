#🍕 Pizza Sales Analysis (SQL)

## 📌 Project Overview

A SQL-based data analysis project that explores pizza sales data to uncover business insights related to revenue, customer demand, ordering patterns, and product performance.

The project focuses on writing optimized SQL queries, joining multiple tables, and applying aggregation, window functions, and ranking techniques.

## 🧠 Business Questions Answered

How many total orders were placed?

What is the total revenue generated?

Which pizza is the highest priced?

What pizza size is ordered the most?

Which pizza types generate the highest revenue?

How does demand vary by hour of the day?

What is the category-wise contribution to total revenue?

How does cumulative revenue grow over time?

## 🗂️ Dataset Schema

orders – order date & time

order_details – pizza quantities per order

pizzas – size & price information

pizza_types – name & category

## 🔍 Key SQL Concepts Used

JOIN (INNER JOIN across multiple tables)

Aggregations: SUM(), COUNT(), AVG()

Date & time functions (HOUR())

Subqueries

Window functions (RANK(), SUM() OVER)

Sorting & limiting (ORDER BY, LIMIT)

Revenue & percentage contribution analysis

## 📊 Key Insights

Identified top-selling pizza types and categories

Analyzed hourly order distribution to understand peak demand

Calculated category-wise revenue contribution (%)

Tracked cumulative revenue trends over time

Ranked top 3 pizzas per category by revenue

## 🛠️ Tools & Technologies

SQL (MySQL compatible)

Relational Data Modeling

Analytical Query Writing

## 🚀 Example Analysis
SELECT pizza_types.name,
       SUM(order_details.quantity * pizzas.price) AS revenue
FROM pizza_types
JOIN pizzas ON pizza_types.pizza_type_id = pizzas.pizza_type_id
JOIN order_details ON order_details.pizza_id = pizzas.pizza_id
GROUP BY pizza_types.name
ORDER BY revenue DESC
LIMIT 3;

## 🎯 Why This Project Matters

Demonstrates real-world SQL analytics skills

Shows ability to translate business questions → data insights

Uses advanced SQL features expected in Data Analyst / Data Scientist roles

Clean, readable, and interview-ready query structure

## 📌 Possible Extensions

Sales forecasting using Python

Dashboard creation (Power BI / Tableau)

Customer segmentation

Time-series trend analysis
