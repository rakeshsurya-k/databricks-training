# databricks-training

Employee Database SQL Queries

This project contains SQL queries for practicing database concepts using three tables:

Department
Employee
Project

The queries cover:

Basic SELECT Queries
String Matching Queries
Date Queries
Aggregate Functions
GROUP BY Queries
HAVING Clause Queries
ORDER BY Queries
JOIN Queries
Nested and Correlated Queries
Moderate Combined Queries
Database Schema
Department Table
CREATE TABLE Department (
    department_id INT PRIMARY KEY,
    name VARCHAR(50)
);
Employee Table
CREATE TABLE Employee (
    emp_id INT PRIMARY KEY,
    name VARCHAR(100),
    age INT,
    salary DECIMAL(10,2),
    department_id INT,
    hire_date DATE,
    FOREIGN KEY (department_id) REFERENCES Department(department_id)
);
Project Table
CREATE TABLE Project (
    project_id INT PRIMARY KEY,
    name VARCHAR(100),
    department_id INT,
    FOREIGN KEY (department_id) REFERENCES Department(department_id)
);
Insert Sample Data
Department Data
INSERT INTO Department VALUES
(1, 'IT'),
(2, 'HR'),
(3, 'Finance'),
(4, 'Marketing');
Employee Data
INSERT INTO Employee VALUES
(1, 'John Doe', 28, 50000, 1, '2020-01-15'),
(2, 'Jane Smith', 34, 60000, 2, '2019-07-23'),
(3, 'Bob Brown', 45, 80000, 1, '2018-02-12'),
(4, 'Alice Blue', 25, 45000, 3, '2021-03-22'),
(5, 'Charlie P.', 29, 50000, 2, '2019-12-01');
Project Data
INSERT INTO Project VALUES
(1, 'Project Alpha', 1),
(2, 'Project Beta', 2),
(3, 'Project Gamma', 1),
(4, 'Project Delta', 3),
(5, 'Project Epsilon', 4);
Topics Covered
Basic Queries
Selecting columns
Filtering rows
Using WHERE clause
String Functions
LIKE operator
Pattern matching
Date Functions
YEAR()
MONTH()
DATE comparisons
Aggregate Functions
SUM()
AVG()
MIN()
MAX()
COUNT()
GROUP BY and HAVING
Department-wise analysis
Aggregate filtering
ORDER BY
Sorting records
JOIN Operations
INNER JOIN
LEFT JOIN
Nested Queries
Subqueries
Correlated subqueries
Software Requirements
MySQL
MySQL Workbench / phpMyAdmin / VS Code SQL Extension
How to Run
Create a database
CREATE DATABASE company_db;
USE company_db;
Run table creation queries
Insert sample data
Execute practice queries
Learning Outcomes

After completing these queries, you will understand:

Database schema creation
Data insertion
SQL filtering techniques
Aggregate functions
Joins and relationships
Nested queries
Data analysis using SQL
Author

SQL Practice Project for Database Learning.
