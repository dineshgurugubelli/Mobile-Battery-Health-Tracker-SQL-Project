  # Mobile-Battery-Health-Tracker-SQL-Project
================================================================================
# 📱 Mobile Battery Health Tracking & Analysis System

A SQL-based database project designed to **track, manage, and analyze smartphone battery performance** using real-world battery usage, charging, application usage, battery health, and battery issue data.

The project uses **MySQL** to store structured data and perform analytical queries to identify battery performance patterns, charging behavior, battery degradation, and application-level battery consumption.

---

## 📌 Project Overview

Smartphone battery performance changes over time due to factors such as charging cycles, screen usage, application usage, and charging behavior.

This project provides a centralized database system to track these factors and analyze the overall health and performance of mobile batteries.

The system can answer questions such as:

* Which mobile has the best battery health?
* Which application consumes the most battery?
* Which phone has the highest charging cycles?
* Which devices have battery health below the average?
* Which mobile has the most battery-related issues?
* Does high charging-cycle usage relate to battery degradation?
* Which device has the highest overall battery consumption?

---

## 🎯 Objectives

* Store mobile device and user information.
* Track daily battery consumption.
* Record charging sessions.
* Monitor battery health over time.
* Track application-level battery consumption.
* Record battery-related issues.
* Analyze battery performance using SQL.
* Identify devices showing signs of battery degradation.
* Generate meaningful battery performance insights.

---

## 🗂️ Database Structure

The project contains **7 main tables**:

```text
┌──────────────┐
│    USERS     │
└──────┬───────┘
       │
       │ 1 : N
       ▼
┌──────────────────┐
│ MOBILE_DEVICES   │
└────┬─────┬───────┘
     │     │
     │     ├─────────────────────┐
     │     │                     │
     ▼     ▼                     ▼
┌───────────────┐       ┌──────────────────┐
│ BATTERY_USAGE │       │ CHARGING_SESSIONS│
└───────────────┘       └──────────────────┘
     │
     │
     ├───────────────────┐
     ▼                   ▼
┌────────────────┐   ┌───────────────┐
│ BATTERY_HEALTH │   │  APP_USAGE    │
└────────────────┘   └───────────────┘
     │
     ▼
┌──────────────────┐
│ BATTERY_ISSUES  │
└──────────────────┘
```

### Tables

| Table               | Description                                          |
| ------------------- | ---------------------------------------------------- |
| `users`             | Stores user information                              |
| `mobile_devices`    | Stores mobile device details                         |
| `battery_usage`     | Tracks daily battery consumption                     |
| `charging_sessions` | Records charging activity                            |
| `battery_health`    | Stores battery health and charging-cycle information |
| `app_usage`         | Tracks application usage and battery consumption     |
| `battery_issues`    | Records battery-related problems                     |

---

## 🛠️ Technologies Used

* **Database:** MySQL
* **Language:** SQL
* **Version Control:** Git & GitHub
* **Development Environment:** MySQL Workbench / MySQL Command Line

---

## 🔑 SQL Concepts Used

### Basic SQL

* `CREATE DATABASE`
* `CREATE TABLE`
* `INSERT`
* `SELECT`
* `WHERE`
* `ORDER BY`
* `LIMIT`

### Intermediate SQL

* `INNER JOIN`
* `LEFT JOIN`
* `GROUP BY`
* `HAVING`
* `COUNT()`
* `SUM()`
* `AVG()`
* `MAX()`
* `MIN()`
* `ROUND()`

### Advanced SQL

* Subqueries
* Common Table Expressions (`CTE`)
* `CASE`
* Window Functions
* `RANK()`
* `DENSE_RANK()`
* Multiple-table joins
* Aggregation and analytical queries

---

## 📊 Project Analysis

The project performs three levels of SQL analysis.

### 🟢 Basic Analysis

Examples:

* Display all users.
* Display all mobile devices.
* Find phones with battery health below 90%.
* Find the highest and lowest battery health.
* Calculate average screen time.
* Count charging sessions.
* Find high battery-consuming applications.

### 🟡 Medium Analysis

Examples:

* Display users with their mobile details.
* Calculate average battery health by brand.
* Find total charging sessions for each mobile.
* Find applications consuming more than 10% battery.
* Identify phones with more than 200 charging cycles.

### 🔴 Advanced Analysis

Examples:

* Find phones whose battery health is below the overall average.
* Rank phones based on battery health.
* Identify devices with high charging cycles and low battery health.
* Find the most battery-consuming application.
* Identify the device with the highest overall battery consumption.

---

## ⭐ Final Battery Performance Analysis

The project includes a final analysis query that combines multiple tables to evaluate overall battery performance.

The analysis considers:

* Battery health percentage
* Charging cycles
* Total battery consumption
* Number of battery-related issues

The system categorizes devices into:

```text
Excellent
Good
Average
Poor
```

This provides a simple way to identify devices that may require battery maintenance or replacement.

---

## 📁 Project Structure

```text
Mobile-Battery-Health-Tracking-System/
│
├── README.md
│
├── Mobile_Battery_Health.sql
│
├── ER_Diagram/
│   └── Mobile_Battery_Health_ER_Diagram.png
│
└── Screenshots/
    ├── database.png
    ├── tables.png
    └── queries.png
```

---

## 🚀 How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/your-username/mobile-battery-health-tracking-system.git
```

### 2. Open MySQL

You can use:

* MySQL Workbench
* MySQL Command Line
* phpMyAdmin

### 3. Open the SQL file

Open:

```text
Mobile_Battery_Health.sql
```

### 4. Execute the script

The SQL script will:

```text
Create Database
      ↓
Create Tables
      ↓
Create Relationships
      ↓
Insert Sample Data
      ↓
Run Analysis Queries
```

### 5. Select the database

```sql
USE mobile_battery_health;
```

### 6. Check the tables

```sql
SHOW TABLES;
```

---

## 🔗 Entity Relationship Diagram

The ER diagram represents the relationships between users, mobile devices, battery usage, charging sessions, battery health, application usage, and battery issues.

![Mobile Battery Health ER Diagram](ER_Diagram/Mobile_Battery_Health_ER_Diagram.png)

---

## 💡 Sample Business Questions

This database can be used to answer real-world questions such as:

1. Which phone has the highest battery health?
2. Which phone has the lowest battery health?
3. Which application consumes the most battery?
4. Which phone has the highest charging-cycle count?
5. Which brand has the best average battery health?
6. Which phone has the highest battery consumption?
7. Which devices have battery health below the average?
8. Which phone has the highest number of battery issues?
9. Which phones show signs of battery degradation?
10. How does charging behavior relate to battery performance?

---

## 🔮 Future Improvements

The project can be extended in the future by adding:

* 📊 Power BI dashboard for battery analytics
* 📈 Battery health trend visualization
* 🤖 Machine learning for battery-life prediction
* 🔔 Automatic low-battery-health alerts
* 📱 Mobile application interface
* ☁️ Cloud database integration
* 📅 Long-term battery degradation tracking
* 🔋 Battery replacement recommendations

---

## 🎓 Learning Outcomes

Through this project, I practiced:

* Relational database design
* Primary and foreign keys
* Database normalization
* SQL joins
* Aggregate functions
* Subqueries
* CTEs
* Window functions
* Data analysis using SQL
* Real-world database problem solving

---

## 👨‍💻 Author

**Dinesh**

B.Sc. Computer Science

This project was developed as a practical SQL database project to demonstrate database design, SQL querying, and data analysis skills.

---

## ⭐ Project Highlights

```text
📱 Real-world Problem
🗄️ Relational Database
🔗 7 Related Tables
🔑 Primary & Foreign Keys
📊 20+ SQL Queries
🟢 Basic SQL
🟡 Intermediate SQL
🔴 Advanced SQL
📈 Battery Performance Analysis
```

---

## 📜 License

This project is created for **educational and portfolio purposes**.
