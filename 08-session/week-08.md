# Week 08 – T-SQL, ETL Processes, and Multidimensional Data Concepts

## 📚 Topics Covered
- Deep dive into T-SQL for querying and manipulating data  
- Understanding ETL workflows (Extract, Transform, Load)  
- Designing SQL-based data pipelines  
- Introduction to multidimensional data modeling (OLAP cubes)  
- Differences between star schema, snowflake schema, and relational models  
- How multidimensional structures support analytics and BI tools  

## 🧰 Tools & Setup
- SQL Server + SQL Server Management Studio (SSMS)  
- T-SQL scripts for tables, queries, transformations  
- Basic ETL implementation using SQL procedures and staging tables  
- Exposure to SSIS / theoretical ETL pipeline concepts  
- Diagram tools for multidimensional model visualization  

## 🧑‍💻 Code / Example
```sql
-- Example of a staging table load
INSERT INTO Sales_Staging (OrderID, ProductID, Quantity, Price)
SELECT OrderID, ProductID, Quantity, Price
FROM Raw_Sales;

-- Basic transformation step
UPDATE Sales_Staging
SET Total = Quantity * Price;

-- Loading into fact table
INSERT INTO FactSales (OrderID, ProductID, Total, DateKey)
SELECT OrderID, ProductID, Total, CONVERT(INT, REPLACE(CONVERT(VARCHAR(10), OrderDate, 120), '-', ''))
FROM Sales_Staging;

-- Sample T-SQL slice of multidimensional logic
SELECT ProductCategory, SUM(Total) AS TotalRevenue
FROM FactSales fs
JOIN DimProduct dp ON fs.ProductID = dp.ProductID
GROUP BY ProductCategory;
```
ase Studies / Exercises

Built simple staging and cleaning tables for ETL simulation

Practiced T-SQL queries using JOINs, GROUP BY, CASE, and subqueries

Designed a small star schema with Fact and Dimension tables

Explored how OLAP cubes support slicing, dicing, roll-up, and drill-down

Mapped real business questions to multidimensional structures

💡 Insights

ETL is the backbone of any data warehouse or analytics pipeline

T-SQL is powerful when combining transformations and loading logic

Multidimensional models (facts + dimensions) make analytics faster and easier

Star schema simplifies reporting; snowflake adds more normalization

Well-structured dimensional models prepare the ground for advanced AI/ML use cases

🚀 Next Steps

Build a small ETL pipeline from raw data → staging → cleaned → fact/dim tables

Practice more advanced T-SQL (window functions, ranking, CTEs)

Experiment with a simple OLAP cube or Power BI star schema

Connect multidimensional modeling with future BI and AI projects
