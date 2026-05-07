# databricks-training
# Employee Database SQL Practice

This project contains SQL practice queries using the following tables:

- Department
- Employee
- Project

The queries cover:

1. Basic SELECT Queries
2. String Matching Queries
3. Date Queries
4. Aggregate Functions
5. GROUP BY Queries
6. HAVING Queries
7. ORDER BY Queries
8. JOIN Queries
9. Nested and Correlated Queries
10. Combined Moderate Queries

---

# Database Schema

## Create Department Table

```sql
CREATE TABLE Department (
    department_id INT PRIMARY KEY,
    name VARCHAR(50)
);
```

## Create Employee Table

```sql
CREATE TABLE Employee (
    emp_id INT PRIMARY KEY,
    name VARCHAR(100),
    age INT,
    salary DECIMAL(10,2),
    department_id INT,
    hire_date DATE,
    FOREIGN KEY (department_id) REFERENCES Department(department_id)
);
```

## Create Project Table

```sql
CREATE TABLE Project (
    project_id INT PRIMARY KEY,
    name VARCHAR(100),
    department_id INT,
    FOREIGN KEY (department_id) REFERENCES Department(department_id)
);
```

---

# Insert Sample Data

## Department Table Data

```sql
INSERT INTO Department VALUES
(1, 'IT'),
(2, 'HR'),
(3, 'Finance'),
(4, 'Marketing');
```

## Employee Table Data

```sql
INSERT INTO Employee VALUES
(1, 'John Doe', 28, 50000, 1, '2020-01-15'),
(2, 'Jane Smith', 34, 60000, 2, '2019-07-23'),
(3, 'Bob Brown', 45, 80000, 1, '2018-02-12'),
(4, 'Alice Blue', 25, 45000, 3, '2021-03-22'),
(5, 'Charlie P.', 29, 50000, 2, '2019-12-01');
```

## Project Table Data

```sql
INSERT INTO Project VALUES
(1, 'Project Alpha', 1),
(2, 'Project Beta', 2),
(3, 'Project Gamma', 1),
(4, 'Project Delta', 3),
(5, 'Project Epsilon', 4);
```

---

# Topics Covered

## Basic Queries
- SELECT
- WHERE
- Filtering records

## String Matching
- LIKE operator
- Pattern matching

## Date Queries
- YEAR()
- MONTH()
- Date filtering

## Aggregate Functions
- SUM()
- AVG()
- MIN()
- MAX()
- COUNT()

## GROUP BY and HAVING
- Grouping records
- Aggregate filtering

## ORDER BY
- Sorting records

## JOIN Operations
- INNER JOIN
- LEFT JOIN

## Nested Queries
- Subqueries
- Correlated subqueries

---

# Software Requirements

- MySQL
- MySQL Workbench
- phpMyAdmin
- VS Code SQL Extension

---

# How to Run

## Step 1: Create Database

```sql
CREATE DATABASE company_db;
USE company_db;
```

## Step 2: Run Table Creation Queries

Execute all CREATE TABLE statements.

## Step 3: Insert Sample Data

Execute all INSERT statements.

## Step 4: Run Practice Queries

Execute the SQL queries one by one for practice.

---

# Learning Outcomes

After completing this project, you will understand:

- Database schema creation
- Table relationships
- Data insertion
- SQL filtering
- Aggregate functions
- GROUP BY and HAVING
- JOIN operations
- Nested queries
- SQL data analysis

---

# Author

rakeshsurya-k
