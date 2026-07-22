# SQL-DATABASE-DESIGNS-AND-ANALYSIS PROJECTS

** 🗄️ SQL Project – Employee Database Analysis**

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



**Global Population & Economic Analysis using MySQL**

**📌 Project Overview**

This project demonstrates SQL data analysis skills using the MySQL World Sample Database.

The objective is to analyse global demographic and economic data by querying countries, cities, and languages to uncover meaningful insights.

The project showcases intermediate to advanced SQL techniques including joins, subqueries, aggregate functions, calculated fields, sorting, filtering, and data exploration.

**🎯 Objectives**

The project aims to:

- Explore the MySQL World database
- Analyse global population statistics
- Compare GDP and GDP per capita across countries
- Identify the world's largest cities
- Investigate country demographics
- Demonstrate SQL querying and analytical skills
  
🗂 Database

The project uses the MySQL World Database, which contains three main tables:

**Country**

Contains information including:

Country Name
Population
Surface Area
GNP
Life Expectancy
Government Form
Region
Continent

**City**

Contains:

City Name
Country Code
Population
District

**CountryLanguage**

Contains:

Country Code
Language
Percentage Spoken
Official Language Indicator

🛠 SQL Concepts Demonstrated

This project includes practical use of:

- SELECT statements
- WHERE clauses
- ORDER BY
- LIMIT
- INNER JOIN
- Aggregate Functions
- AVG()
- COUNT()
- SUM()
- MAX()
- MIN()
- Aliases
- Arithmetic Calculations
- Subqueries
- Data Filtering
- Sorting Results
- 
** 📊 Analysis Performed**
1. Country Analysis

Analysed:

Country populations
GDP
GDP per capita
Surface area
Continents
Regions

2. City Analysis

Explored:

Largest cities by population
City distributions
Population rankings
Country-city relationships

Example:

SELECT Name,
CountryCode,
District,
Population
FROM City
ORDER BY Population DESC;
3. GDP Per Capita Analysis

Calculated GDP per capita using:

GNP / Population

Example:

SELECT
ci.Name AS City,
co.Name AS Country,
(co.GNP / co.Population) AS GDP_Per_Capita
FROM City ci
JOIN Country co
ON ci.CountryCode = co.Code;

4. Average GDP Comparison

Used a subquery to compare countries whose GDP per capita is above the global average.

Example:

SELECT
ci.Name,
co.Name,
(co.GNP / co.Population) AS GDP_Per_Capita
FROM City ci
JOIN Country co
ON ci.CountryCode = co.Code
WHERE
(co.GNP / co.Population) >
(
SELECT AVG(GNP / Population)
FROM Country
);5. Population Ranking

Retrieved the most populated cities worldwide.

Used:

ORDER BY
DESC
LIMIT

Example:

SELECT
Name,
CountryCode,
District,
Population
FROM City
ORDER BY Population DESC
LIMIT 30;
💡 Key Insights

**The analysis revealed several notable patterns:**

Major cities in Asia dominate the list of the world's most populated urban areas.
GDP per capita varies significantly between countries, reflecting substantial economic disparities.
Countries with higher GDP per capita generally exceed the global average, though high total GDP does not always correspond to high GDP per capita.
SQL calculations and subqueries enable meaningful comparisons across multiple economic and demographic indicators.

**🖥 Tools Used**
MySQL Workbench
MySQL 8.0
MySQL World Database

**📈 Skills Demonstrated**
SQL Query Writing
Data Exploration
Data Analysis
Database Management
Table Joins
Aggregate Functions
Subqueries
Calculated Columns
Sorting & Filtering
Query Optimisation
Relational Database Concepts

📷 Project Preview
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/8508b1f4-2cc4-471a-bdeb-1579fc56ac77" />

**🚀 Learning Outcomes**

Through this project, I strengthened my ability to:

Write efficient SQL queries for data analysis.
Perform multi-table joins to combine related datasets.
Use aggregate functions and subqueries to generate business insights.
Calculate custom metrics such as GDP per capita.
Analyse and rank demographic and economic data.
Present query results in a structured and meaningful way.

**📌 Conclusion**

This project demonstrates my practical SQL skills applied to a real-world relational database. By analysing population and economic indicators from the MySQL World dataset, the project highlights how SQL can be used to transform raw data into actionable insights. It showcases proficiency in querying, joining, aggregating, and analysing data, making it a strong portfolio project for data analyst, business intelligence, and SQL-focused roles.
---

✨ This project demonstrates practical SQL skills used in real-world data analysis.

