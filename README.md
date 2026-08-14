# 🎓 University Course Management System

<p align="center">
  <img src="https://img.shields.io/badge/SQL-MySQL-blue?style=for-the-badge&logo=mysql" alt="SQL">
  <img src="https://img.shields.io/badge/Database-Relational-green?style=for-the-badge" alt="Database">
  <img src="https://img.shields.io/badge/Project-Completed-success?style=for-the-badge" alt="Project Status">
</p>

<p align="center">
  <b>A complete SQL-based University Course Management System designed to efficiently manage students, courses, departments, instructors, enrollments, and academic performance.</b>
</p>

---

## 📌 Project Overview

The **University Course Management System** is a relational database project developed using **SQL and MySQL**.

The project is designed to manage and organize university academic information in a structured and efficient way. It demonstrates how a real-world university database can be designed using tables, relationships, constraints, joins, aggregate functions, and SQL queries.

The system manages important university data such as:

* 👨‍🎓 Student Information
* 🏫 Department Information
* 📚 Course Information
* 👨‍🏫 Instructor Information
* 📝 Student Enrollments
* 📊 Student Grades and Marks
* 🔗 Relationships between different entities

---

# 🎯 Project Objectives

The main objectives of this project are:

* Create a structured relational database for a university
* Store and manage student information
* Manage university departments
* Store and manage course details
* Manage instructor information
* Track student course enrollments
* Store student grades and marks
* Establish relationships between different tables
* Practice real-world SQL queries
* Retrieve meaningful information from the database
* Perform basic academic data analysis
* Demonstrate database design and SQL concepts

---

# 🏗️ Database Structure

The project contains the following main entities:

| Entity            | Description                                      |
| ----------------- | ------------------------------------------------ |
| 👨‍🎓 Students    | Stores student personal and academic information |
| 🏫 Departments    | Stores university department information         |
| 📚 Courses        | Stores available university courses              |
| 👨‍🏫 Instructors | Stores instructor information                    |
| 📝 Enrollments    | Stores student course registration information   |
| 📊 Grades         | Stores student academic performance              |

---

# 🔗 Database Relationships

The database uses **Primary Keys (PK)** and **Foreign Keys (FK)** to establish relationships between tables.

### Relationship Overview

```text
                    ┌─────────────────┐
                    │   Departments   │
                    └────────┬────────┘
                             │
             ┌───────────────┼───────────────┐
             │               │               │
             ▼               ▼               ▼
      ┌────────────┐  ┌────────────┐  ┌──────────────┐
      │  Students  │  │  Courses   │  │ Instructors  │
      └─────┬──────┘  └─────┬──────┘  └──────────────┘
            │               │
            │               │
            └───────┬───────┘
                    ▼
             ┌──────────────┐
             │ Enrollments  │
             └───────┬──────┘



### Main Relationships

* One Department → Many Students
* One Department → Many Courses
* One Department → Many Instructors
* One Student → Many Enrollments
* One Course → Many Enrollments


---

# 🛠️ Technologies Used

| Technology              | Purpose                                |
| ----------------------- | -------------------------------------- |
| 🐬 MySQL                | Database Management System             |
| 💻 SQL                  | Database Queries                       |
| 🗃️ Relational Database | Data Organization                      |
| 🔑 Primary Key          | Unique identification of records       |
| 🔗 Foreign Key          | Establish relationships between tables |
| 📊 Aggregate Functions  | Data analysis and calculations         |

---

# 🗂️ Project Folder Structure

```text
University-Course-Management-System/
│
├── 📄 README.md
│
├── 📂 SQL/
│   ├── database.sql
│   └── queries.sql
│
└── 📂 outputs


# 📋 Database Tables

## 👨‍🎓 Students

The `Students` table stores information about university students.

### Example Fields

```text
student_id
first_name
last_name
email
phone
date_of_birth
department_id
```

---

## 🏫 Departments

The `Departments` table stores information about university departments.

### Example Fields

```text
department_id
department_name
location
```

---

## 📚 Courses

The `Courses` table stores information about courses offered by the university.

### Example Fields

```text
course_id
course_name
course_code
credits
department_id
instructor_id
```

---

## 👨‍🏫 Instructors

The `Instructors` table stores information about university instructors.

### Example Fields

```text
instructor_id
first_name
last_name
email
department_id
```

---

## 📝 Enrollments

The `Enrollments` table stores information about students registered for courses.

### Example Fields

```text
enrollment_id
student_id
course_id
enrollment_date
```

---

### Example Fields

```text
grade_id
enrollment_id
grade
marks
```

---

# 🔑 SQL Concepts Used

This project demonstrates several important SQL concepts.

## Database Operations

* `CREATE DATABASE`
* `CREATE TABLE`
* `INSERT`
* `UPDATE`
* `DELETE`
* `SELECT`

## Constraints

* `PRIMARY KEY`
* `FOREIGN KEY`
* `NOT NULL`
* `UNIQUE`
* `CHECK`
* `DEFAULT`

## Filtering & Sorting

* `WHERE`
* `ORDER BY`
* `DISTINCT`
* `LIMIT`

## Grouping

* `GROUP BY`
* `HAVING`

## Aggregate Functions

* `COUNT()`
* `SUM()`
* `AVG()`
* `MIN()`
* `MAX()`

## Joins

* `INNER JOIN`
* `LEFT JOIN`
* `RIGHT JOIN`

## Advanced SQL

* Subqueries
* Multiple Table Joins
* Conditional Logic
* Data Aggregation
* Data Filtering
* Data Analysis

---

# 🚀 How to Run the Project

Follow these steps to run the project using MySQL.

## 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/University-Course-Management-System.git
```

## 2️⃣ Open MySQL

You can use any MySQL-compatible environment such as:

* MySQL Workbench
* MySQL Command Line
* phpMyAdmin
* Other MySQL database tools

## 3️⃣ Create the Database

Run the following file:

```sql
SOURCE SQL/database.sql;
```

## 4️⃣ Create the Tables

Run:

```sql
SOURCE SQL/tables.sql;
```

## 5️⃣ Insert Sample Data

Run:

```sql
SOURCE SQL/sample_data.sql;
```

## 6️⃣ Run the Queries

Run:

```sql
SOURCE SQL/queries.sql;
```

---

# 💻 Example SQL Queries

## 🔍 1. Display All Students

```sql
SELECT *
FROM Students;
```

---

## 📚 2. Display All Courses

```sql
SELECT *
FROM Courses;
```

---

## 🏫 3. Display Students with Their Departments

```sql
SELECT
    s.student_id,
    s.first_name,
    s.last_name,
    d.department_name
FROM Students s
JOIN Departments d
    ON s.department_id = d.department_id;
```

---

## 📝 4. Display Students and Their Courses

```sql
SELECT
    s.first_name,
    s.last_name,
    c.course_name
FROM Students s
JOIN Enrollments e
    ON s.student_id = e.student_id
JOIN Courses c
    ON e.course_id = c.course_id;
```

---

## 📊 5. Calculate Average Marks

```sql
SELECT
    AVG(marks) AS average_marks
FROM Grades;
```

---

## 🏆 6. Find the Highest Marks

```sql
SELECT
    MAX(marks) AS highest_marks
FROM Grades;
```

---

## 📈 7. Count Students in Each Department

```sql
SELECT
    d.department_name,
    COUNT(s.student_id) AS total_students
FROM Departments d
LEFT JOIN Students s
    ON d.department_id = s.department_id
GROUP BY d.department_name;
```

---

# 📊 Business & Academic Questions Answered

This database can be used to answer important academic management questions such as:

1. How many students are enrolled in each department?
2. Which courses have the highest number of students?
3. What is the average student score?
4. Which student has the highest marks?
5. Which instructors teach specific courses?
6. How many courses are offered by each department?
7. Which students are enrolled in a particular course?
8. What grades did a particular student receive?
9. Which courses have the highest enrollment?
10. What is the overall academic performance?
11. How many students belong to each department?
12. Which courses are offered by a particular department?
13. Which instructor belongs to a particular department?
14. What is the number of enrollments for each course?
15. Which students have achieved the highest grades?

---

# 📁 Project Files

## `database.sql`

Contains the commands required to create the university database.

## `tables.sql`

Contains table creation scripts, primary keys, foreign keys, and other constraints.

## `sample_data.sql`

Contains sample records used to populate the database for testing and analysis.

## `queries.sql`

Contains SQL queries used for data retrieval, filtering, joining, aggregation, and analysis.

## `project_documentation.md`

Contains detailed documentation of the project, database design, table descriptions, relationships, SQL concepts, and project explanation.

---

# 📸 Project Screenshots

Add screenshots of your project here to make the GitHub repository more attractive.

Recommended screenshots:

* 🗄️ Database creation
* 📋 Table structures
* 💻 SQL queries
* 📊 Query results
* 🔗 ER Diagram
* 🐬 MySQL Workbench

Example:

```text
📸 Database Tables
📸 SQL Queries
📸 Query Results
📸 ER Diagram
```

---

# 🎓 Learning Outcomes

Through this project, I practiced and demonstrated:

* ✅ Relational Database Design
* ✅ SQL Database Creation
* ✅ Table Creation
* ✅ Data Insertion
* ✅ Data Updating
* ✅ Data Deletion
* ✅ Primary Keys
* ✅ Foreign Keys
* ✅ Database Constraints
* ✅ SQL Joins
* ✅ Aggregate Functions
* ✅ GROUP BY
* ✅ HAVING
* ✅ Subqueries
* ✅ Data Filtering
* ✅ Data Sorting
* ✅ Data Aggregation
* ✅ Database Relationships
* ✅ Real-world SQL Problem Solving

---

# 🧠 Skills Demonstrated

```text
SQL
MySQL
Database Management
Database Design
Relational Database
DBMS
Data Manipulation
Data Retrieval
SQL Joins
Aggregate Functions
Subqueries
Data Analysis
Problem Solving
```

---

# 🔮 Future Improvements

This project can be further improved by adding:

* 🔐 Student Login System
* 👨‍🏫 Instructor Login System
* 📊 Student Performance Dashboard
* 📈 Power BI Integration
* 🌐 Web Application
* 📱 Mobile Application
* 📧 Email Notifications
* 📅 Attendance Management
* 💰 Fee Management
* 📝 Examination Management
* 📚 Library Management
* 🎓 Student Result Management

---

# 💼 Portfolio Value

This project is suitable as a **SQL / Database portfolio project** for demonstrating practical database knowledge.

It can help showcase skills for entry-level roles such as:

* 📊 Data Analyst
* 🗄️ SQL Developer
* 💻 Database Developer
* 📈 Business Analyst
* 🧑‍💻 Junior Data Professional

---

# ⭐ Why This Project?

A University Course Management System is a practical real-world example of how relational databases are used to organize large amounts of interconnected information.

This project demonstrates the ability to:

> **Design → Create → Populate → Query → Analyze**

a relational database using SQL.

---

# 👨‍💻 Author

## Rakesh pedduri

**SQL & Data Analytics Learner**

### Technical Skills

`SQL` • `MySQL` • `Excel` • `Power BI` • `Python`

---

# 📌 Project Status

🟢 **Completed**

This project was created for **learning, practice, and portfolio purposes**.

---

# 🤝 Contributing

Contributions, suggestions, and improvements are welcome.

If you would like to improve this project:

1. Fork the repository
2. Create a new branch
3. Make your changes
4. Commit your changes
5. Push to the branch
6. Create a Pull Request

---

# ⭐ Support

If you find this project useful, please consider giving the repository a ⭐ on GitHub.

It helps support the project and encourages further development.

---

# 📜 License

This project is created for **educational and portfolio purposes**.

---

<div align="center">

## 🚀 Keep Learning • Keep Building • Keep Growing

### 💻 SQL | 📊 Data Analytics | 🗄️ Database | 🚀 Career

**Thank you for visiting this project! ❤️**

</div>
