# Tata 1mg - SQL Data Analysis

An end-to-end SQL data analytics project focused on analyzing Tata 1mg's pharmacy, diagnostics, and online consultation operations using MySQL. The project explores business performance, order trends, delivery efficiency, regional sales, inventory challenges, laboratory operations, and customer savings through business-driven SQL queries.

## Project Overview

This project simulates a real-world data analyst's role at Tata 1mg, investigating business problems across its three major business segments:

- **Pharmacy:** Order performance, revenue, delivery efficiency, product availability, and generic substitutions.
- **Diagnostics:** Lab test booking trends, seasonal demand, and phlebotomist performance.
- **Consultations:** Online doctor consultation operations.

The project uses a simulated relational database covering January 2025 to October 2026, designed to replicate realistic business scenarios and support data-driven decision-making.

## Tools & Technologies

- **MySQL 8.0+:** Database management and execution of SQL queries.
- **SQL:** Data extraction, transformation, aggregation, and business analysis.
- **MySQL Workbench:** Database exploration, query execution, and result analysis.

## Dataset Overview

The project uses a simulated dataset containing 15 cities and multiple interconnected business tables.

The database consists of 10 relational tables:

| Table | Description |
|---|---|
| cities | City, state, region, and express delivery availability |
| customers | Customer demographics, location, and acquisition details |
| products | Product information, categories, brands, and pricing |
| orders | Order details, delivery information, payment mode, and order value |
| order_items | Individual products purchased, quantities, and item status |
| lab_tests | Diagnostic test information, categories, and prices |
| phlebotomists | Phlebotomist details and assigned cities |
| lab_bookings | Lab booking details and sample collection status |
| consultations | Doctor consultation details, fees, and completion status |

**Database Name:** `tata1mg_db`

**Data Period:** January 2025 - October 2026

**Note:** All data is simulated for educational and analytical purposes. This project is not affiliated with or based on actual internal Tata 1mg business data.

## Entity Relationship Diagram

The following diagram illustrates the database schema, including the tables, key fields, and relationships used throughout the project.

!(EER DIAGRAM.png)

## Project Workflow

### 1. Database Creation & Design

- Created the `tata1mg_db` database using MySQL.
- Designed a relational database consisting of 10 interconnected tables.
- Established primary keys and foreign key relationships.
- Implemented constraints to maintain data integrity.
- Loaded simulated records into the respective tables.

### 2. Data Exploration

- Explored individual tables to understand the database structure.
- Examined customer, product, order, and operational records.
- Identified relationships between different business segments.
- Used JOIN operations to combine data across multiple tables.

### 3. SQL Analysis

Performed 8 business-driven analytical exercises covering:

1. **Order Performance Analysis:** Calculated total orders, delivered orders, revenue, and Average Order Value (AOV) for October 2026.

2. **City-wise Order Analysis:** Identified the top 10 cities by order volume and calculated their percentage contribution to total orders.

3. **Express Delivery Performance:** Evaluated express delivery efficiency by identifying the percentage of orders delivered after 60 minutes across different cities.

4. **Regional Sales Comparison:** Compared Fever & Cold category sales between September-October 2025 and September-October 2026 to calculate Year-over-Year (YoY) growth.

5. **Diagnostics Demand Analysis:** Tracked weekly Fever Panel bookings across cities since August 2026 and identified significant Week-over-Week (WoW) growth.

6. **Inventory & Stock Analysis:** Identified Fever & Cold products marked Out of Stock during September-October 2026, calculating affected orders and units lost by city.

7. **Phlebotomist Performance:** Ranked phlebotomists within each city based on completed sample collections, including ties.

8. **Generic Medicine Analysis:** Analyzed generic product substitutions, switching percentages, and customer savings across product categories.

### 4. SQL Concepts Used

The project demonstrates practical applications of:

- SELECT, WHERE, ORDER BY, and GROUP BY
- Aggregate Functions (COUNT, SUM, AVG)
- INNER JOIN and LEFT JOIN
- Common Table Expressions (CTEs)
- Subqueries
- CASE Statements
- Conditional Aggregation
- Date and Time Functions
- TIMESTAMPDIFF()
- YEARWEEK()
- Window Functions
- LAG()
- DENSE_RANK()
- HAVING Clause
- Percentage and Growth Calculations

## Key Business Insights

The analysis highlights several important findings from the simulated dataset:

- **Order Performance:** October 2026 recorded 1,800 orders, of which 1,658 were delivered, generating revenue of ₹18,97,452.
- **City Contribution:** Delhi, Bengaluru, and Mumbai collectively contributed approximately 45% of total orders.
- **Delivery Efficiency:** Pune recorded a 28.22% express delivery breach rate, significantly higher than other cities.
- **Regional Growth:** North India recorded 98.5% Year-over-Year growth in Fever & Cold sales.
- **Diagnostics Demand:** Weekly Fever Panel booking spikes indicated a dengue demand wave moving across Delhi, Jaipur, and Lucknow.
- **Inventory Challenges:** Fever & Cold products experienced stock shortages in Delhi and Gurugram during the seasonal demand period.
- **Customer Savings:** Generic substitutions generated approximately ₹7,77,909 in customer savings.

*All figures represent the simulated project dataset and its analytical outputs.*

## Project Structure

```text
Tata-1mg-SQL-Data-Analysis/
│
├── tata1mg_db.sql
│
├── Healthops_Analytics.sql
│
├── README.md
│
├── eer-diagram.png
│
└── .gitignore
```

## How to Run the Project

1. Install MySQL Server 8.0 or above.
2. Open MySQL Workbench and connect to your MySQL server.
3. Open `tata1mg_db.sql`.
4. Execute the SQL script to create the database, tables, relationships, and populate the simulated dataset.
5. Open `Healthops_Analytics.sql`.
6. Execute the analysis queries to explore the business questions and generate insights.

**Important:** The database creation script contains `DROP DATABASE IF EXISTS tata1mg_db`. Running it again will delete and recreate the existing database.

## Future Improvements

- Develop an interactive Power BI dashboard for business performance monitoring.
- Expand analysis to include consultation performance and revenue.
- Introduce customer retention and purchasing behaviour analysis.
- Perform deeper inventory forecasting and demand analysis.
- Explore additional operational KPIs across pharmacy and diagnostics.
