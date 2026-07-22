# SQL-DATABASE-DESIGNS-AND-ANALYSIS
# 🗄️ SQL Project – Employee Database Analysis

## 📌 Overview

This project demonstrates my ability to query and analyse relational databases using SQL.

I worked with an employee database containing information about employees, departments, and projects.

---

## 🎯 Objectives

* Retrieve employee and department data
* Combine multiple tables using JOIN operations
* Analyse relationships between employees, departments, and projects
* Handle missing or unmatched data

---

## 🛠️ Tools Used

* MySQL
* SQL (Joins, Aliases, Filtering)

---

## 📊 Key SQL Queries

### 🔹 1. Retrieve all employees

```sql
SELECT * FROM employees;
```

---

### 🔹 2. Employees with their departments (INNER JOIN)

```sql
SELECT e.first_name, e.last_name, d.Department_Name
FROM Employees AS e
INNER JOIN Departments AS d
ON e.Department_id = d.Department_id;
```

---

### 🔹 3. Departments with projects

```sql
SELECT d.Department_Name, p.Project_Name, p.Start_Date
FROM Departments AS d
INNER JOIN Projects AS p
ON d.Department_id = p.DepartmentID;
```

---

### 🔹 4. Departments with manager names

```sql
SELECT d.department_name,
CONCAT(e.first_name, ' ', e.last_name) AS Manager_Name
FROM Departments AS d
LEFT JOIN Employees AS e
ON d.department_manager_id = e.employee_id;
```

---

### 🔹 5. All employees (including those without departments)

```sql
SELECT e.first_name, e.last_name, e.role, d.department_name
FROM Employees AS e
LEFT JOIN Departments AS d
ON e.department_id = d.department_id;
```

---

## 📈 Key Insights

* INNER JOIN returns only matched records between tables
* LEFT JOIN includes unmatched records (useful for identifying missing relationships)
* Aliases improve query readability and structure
* SQL joins are essential for real-world data analysis

---

## 🧠 What I Learned

* How to combine multiple tables using JOINs
* How to structure clean and readable SQL queries
* How relational databases store and connect data

---

## 📷 Project Preview

<img width="1920" height="1020" alt="Employee sql preview" src="https://github.com/user-attachments/assets/f6d8b2b4-9578-483d-a9a1-7b1e33c45807" />


---

✨ This project demonstrates practical SQL skills used in real-world data analysis.

