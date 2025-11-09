# Week 04 – Data Modeling, SQL Server, and NoSQL Foundations .

## 📚 Topics Covered
- Understanding data modeling concepts and their role in analytics and AI  
- Conceptual data model (MCD) and logical data model (MLD) design  
- Translating models into relational databases using SQL Server  
- Introduction to T-SQL for querying, data manipulation, and schema management  
- Overview of NoSQL and document-based storage with MongoDB  
- Discussion on the importance of well-structured and consistent data in building reliable AI solutions  

## 🧰 Tools & Setup
- SQL Server Management Studio (SSMS) for database design and queries  
- MongoDB Atlas for cloud-based NoSQL database practice  
- Draw.io / Lucidchart for creating MCD and MLD diagrams  
- Visual Studio Code for writing and testing T-SQL scripts  
- GitHub for storing scripts, diagrams, and notes  

## 🧑‍💻 Code / Example
```sql 
-- Create a sample table and insert data
CREATE TABLE Employees (
    EmployeeID INT PRIMARY KEY IDENTITY,
    Name NVARCHAR(100),
    Department NVARCHAR(50),
    Salary DECIMAL(10,2)
);

INSERT INTO Employees (Name, Department, Salary)
VALUES ('Amine', 'Data Analytics', 12000.00),
       ('Sara', 'AI Research', 15000.00);
```
-- Example T-SQL query
```
SELECT Department, AVG(Salary) AS AverageSalary
FROM Employees
GROUP BY Department;
// MongoDB equivalent (document-based)
db.employees.insertMany([
  { name: "Amine", department: "Data Analytics", salary: 12000 },
  { name: "Sara", department: "AI Research", salary: 15000 }
]);

db.employees.aggregate([
  { $group: { _id: "$department", avgSalary: { $avg: "$salary" } } }
]);
```
🔍 Case Studies / Exercises

Designed an MCD and MLD for a simple HR or retail database scenario

Implemented tables and relationships in SQL Server based on the models

Practiced key SQL operations: SELECT, JOIN, GROUP BY, and aggregate functions

Compared relational (SQL Server) and document-based (MongoDB) approaches

Discussed data normalization and its trade-offs in AI pipelines

💡 Insights

Data modeling is the foundation of any reliable analytical or AI system

MCD and MLD help clarify relationships before implementation

SQL databases enforce structure, while NoSQL offers flexibility for semi-structured data

Well-structured data reduces noise and bias in machine learning models

Balancing relational and NoSQL systems is key for hybrid analytics environments
