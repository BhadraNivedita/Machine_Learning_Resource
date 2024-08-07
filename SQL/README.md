# Roadmap to learn SQL for Data science career

## Why Learn SQL for a Data Science Career?

Learning SQL is crucial for a career in data science, especially across various industries. Simply downloading or loading data isn't enough for the complex tasks that data science jobs demand.

SQL, or Structured Query Language, is the standard for interacting with relational databases. It allows data scientists to efficiently retrieve, manipulate, and analyze large volumes of structured data, which is essential in fields like finance, healthcare, retail, and technology.

In a professional setting, data scientists need to filter large datasets, join tables, aggregate results, and create complex queries to gain meaningful insights. These tasks require the ability to directly manipulate data within databases, going beyond basic data handling.

Additionally, SQL skills are critical for cleaning and preprocessing data, which are fundamental for building accurate predictive models and robust analyses. Clean data is essential, and without SQL, managing messy and unstructured data would be challenging.

Strong SQL skills are also vital for passing job interviews in data science. Many technical interviews include SQL-based questions to evaluate a candidate's ability to work with databases. Employers seek candidates who can write efficient queries, optimize database performance, and solve real-world data problems.

Learning SQL is possible with effort and practice. By dedicating time to practice and understanding errors, you can develop the SQL proficiency needed to excel in data science.


### **1. Understand the Basics**

#### **1.1. What is SQL?**
SQL is a standard language for accessing and manipulating databases. It's essential for retrieving and managing data stored in relational databases, which are commonly used in data science.

#### **1.2. Key Concepts**
- **Database**: A collection of organized data.
- **Table**: A collection of related data entries consisting of rows and columns.
- **Row**: A single record in a table.
- **Column**: A set of data values of a particular type in a table.

### **2. Core SQL Syntax and Commands**

#### **2.1. Data Retrieval**
- **SELECT**: Retrieve data from one or more tables.
- **FROM**: Specify the table(s) to query data from.
- **WHERE**: Filter records based on specific conditions.
- **ORDER BY**: Sort the results.


#### SELECT Statement

The `SELECT` statement is used to retrieve data from one or more tables in a database. It is one of the most commonly used SQL commands.

#### Example Table: Employees

| ID  | Name       | Department | Salary |
|-----|------------|------------|--------|
| 1   | John Doe   | Sales      | 60000  |
| 2   | Jane Smith | HR         | 65000  |
| 3   | Mike Brown | IT         | 70000  |
| 4   | Lisa White | Marketing  | 62000  |

##### Basic Syntax
```sql
SELECT column1, column2, ...
FROM table_name;
```

##### Example Command
To retrieve all columns from the Employees table:

```sql
SELECT * FROM Employees;
```
| ID  | Name       | Department | Salary |
|-----|------------|------------|--------|
| 1   | John Doe   | Sales      | 60000  |
| 2   | Jane Smith | HR         | 65000  |
| 3   | Mike Brown | IT         | 70000  |
| 4   | Lisa White | Marketing  | 62000  |


#### WHERE Clause
The `WHERE` clause is used to filter records that meet certain conditions.

##### Basic Syntax
```sql
SELECT column1, column2, ...
FROM table_name
WHERE condition;
```
##### Example Command
To retrieve employees from the Sales department:
```sql
SELECT * FROM Employees
WHERE Department = 'Sales';
```

##### Example Output

| ID  | Name       | Department | Salary |
|-----|------------|------------|--------|
| 1   | John Doe   | Sales      | 60000  |


#### ORDER BY Clause
The `ORDER BY` clause is used to sort the result set in either ascending or descending order.

##### Basic Syntax

```sql
SELECT column1, column2, ...
FROM table_name
ORDER BY column1 [ASC|DESC], column2 [ASC|DESC], ...;
```
##### Example Command
To retrieve all employees and sort them by Salary in descending order:

```sql
SELECT * FROM Employees
ORDER BY Salary DESC;
```
##### Example Output
| ID  | Name       | Department | Salary |
|-----|------------|------------|--------|
| 3   | Mike Brown | IT         | 70000  |
| 2   | Jane Smith | HR         | 65000  |
| 4   | Lisa White | Marketing  | 62000  |
| 1   | John Doe   | Sales      | 60000  |

Following are some additional important SQL commands one should learn.

#### DISTINCT Keyword
The `DISTINCT` keyword is used to return only distinct (different) values.

##### Basic Syntax

```sql
SELECT DISTINCT column1, column2, ...
FROM table_name;
```
##### Example Command
To retrieve distinct departments from the Employees table:

```sql
SELECT DISTINCT Department FROM Employees;
```

##### Example Output

| Department |
|------------|
| Sales      |
| HR         |
| IT         |
| Marketing  |


#### LIMIT Clause
The `LIMIT` clause is used to specify the number of records to return.

##### Basic Syntax
```sql
SELECT column1, column2, ...
FROM table_name
LIMIT number;
```
##### Example Command
To retrieve the first 2 records from the Employees table:
```sql
SELECT * FROM Employees
LIMIT 2;
```
#### Example Output

| ID  | Name       | Department | Salary |
|-----|------------|------------|--------|
| 1   | John Doe   | Sales      | 60000  |
| 2   | Jane Smith | HR         | 65000  |



#### LIKE Operator
The `LIKE` operator is used to search for a specified pattern in a column.

##### Basic Syntax
```sql
SELECT column1, column2, ...
FROM table_name
WHERE column1 LIKE pattern;
```
##### Example Command
To retrieve employees whose names start with 'J':
```sql
SELECT * FROM Employees
WHERE Name LIKE 'J%';
```

#### Example Output
| ID  | Name       | Department | Salary |
|-----|------------|------------|--------|
| 1   | John Doe   | Sales      | 60000  |
| 2   | Jane Smith | HR         | 65000  |



#### IN Operator
The `IN` operator allows you to specify multiple values in a WHERE clause.

##### Basic Syntax
```sql
SELECT column1, column2, ...
FROM table_name
WHERE column1 IN (value1, value2, ...);
```

##### Example Command
To retrieve employees from the IT and HR departments:
```sql
SELECT * FROM Employees
WHERE Department IN ('IT', 'HR');
```

##### Example Command
To retrieve employees from the IT and HR departments:
```sql
SELECT * FROM Employees
WHERE Department IN ('IT', 'HR');
```

##### Example Output

| ID  | Name       | Department | Salary |
|-----|------------|------------|--------|
| 2   | Jane Smith | HR         | 65000  |
| 3   | Mike Brown | IT         | 70000  |


#### BETWEEN Operator
The `BETWEEN` operator selects values within a given range.

##### Basic Syntax

```sql
SELECT column1, column2, ...
FROM table_name
WHERE column1 BETWEEN value1 AND value2;
```
##### Example Command
To retrieve employees with salaries between 60000 and 65000:

```sql
SELECT * FROM Employees
WHERE Salary BETWEEN 60000 AND 65000;
```
#### **2.2. Data Manipulation**
- **INSERT INTO**: Add new records to a table.
- **UPDATE**: Modify existing records.
- **DELETE**: Remove records from a table.

Example:
```sql
INSERT INTO employees (first_name, last_name, department) VALUES ('John', 'Doe', 'HR');
```

### INSERT INTO

The `INSERT INTO` command is used to add new records to a table.

#### Basic Syntax
```sql
INSERT INTO table_name (column1, column2, ...)
VALUES (value1, value2, ...);
```
##### Example Command
To add a new employee to the Employees table:
```sql
INSERT INTO Employees (EmployeeID, Name, DepartmentID, Salary)
VALUES (5, 'Anna Green', 2, 68000);
```
#### UPDATE
The UPDATE command is used to modify existing records in a table.

##### Basic Syntax
```sql
UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;
```
##### Example Command
To update the salary of an employee in the Employees table:
```sql
UPDATE Employees
SET Salary = 72000
WHERE EmployeeID = 1;
```


#### DELETE
The DELETE command is used to remove records from a table.

##### Basic Syntax
```sql
DELETE FROM table_name
WHERE condition;
```

##### Example Command
To delete an employee from the Employees table:
```sql
DELETE FROM Employees
WHERE EmployeeID = 3;
```

#### **2.3. Aggregation and Grouping**
- **COUNT, SUM, AVG, MAX, MIN**: Perform calculations on data.
- **GROUP BY**: Group rows sharing a property so that an aggregate function can be applied.

#### COUNT

The `COUNT` function returns the number of rows that match a specified condition.

#### Basic Syntax
```sql
SELECT COUNT(column_name)
FROM table_name
WHERE condition;
```
##### Example Command
To count the number of employees in the Employees table:
```sql
SELECT COUNT(EmployeeID) AS NumberOfEmployees
FROM Employees;
```

#### SUM
The SUM function returns the total sum of a numeric column.

##### Basic Syntax
```sql
SELECT SUM(Salary) AS TotalSalary
FROM Employees;
```

#### AVG

The AVG function returns the average value of a numeric column.

##### Basic Syntax
```sql
SELECT AVG(column_name)
FROM table_name
WHERE condition;
```

##### Example Command
To calculate the average salary of employees:
```sql
SELECT AVG(Salary) AS AverageSalary
FROM Employees;
```

#### MAX
The MAX function returns the maximum value in a set of values.

##### Basic Syntax
```sql
SELECT MAX(column_name)
FROM table_name
WHERE condition;

```

##### Example Command
To find the highest salary among employees:
```sql
SELECT MAX(Salary) AS HighestSalary
FROM Employees;
```

#### MIN
The MIN function returns the minimum value in a set of values.

##### Basic Syntax
```sql
SELECT MIN(column_name)
FROM table_name
WHERE condition;
```

##### Example Command
To find the lowest salary among employees:
```sql
SELECT MIN(Salary) AS LowestSalary
FROM Employees;
```



#### GROUP BY
The GROUP BY statement groups rows that have the same values into summary rows, like "find the number of employees in each department". It is often used with aggregate functions (COUNT, MAX, MIN, SUM, AVG) to perform operations on each group of data.

##### Basic Syntax
```sql
SELECT column1, aggregate_function(column2)
FROM table_name
WHERE condition
GROUP BY column1;
```

##### Example Command
To find the number of employees in each department:

```sql
SELECT DepartmentID, COUNT(EmployeeID) AS NumberOfEmployees
FROM Employees
GROUP BY DepartmentID;
```



### **3. Advanced SQL Concepts**

##### JOIN Commands
- **INNER JOIN**: Returns records with matching values in both tables.
- **LEFT JOIN**: Returns all records from the left table, and matched records from the right table.
- **RIGHT JOIN**: Returns all records from the right table, and matched records from the left table.
- **FULL JOIN**: Returns records when there is a match in either table.

Example:
```sql
SELECT employees.first_name, departments.department_name
FROM employees
INNER JOIN departments ON employees.department_id = departments.id;
```
#### INNER JOIN

The `INNER JOIN` command returns records with matching values in both tables.

##### Basic Syntax
```sql
SELECT columns
FROM table1
INNER JOIN table2
ON table1.common_column = table2.common_column;
```
##### Example Command
To retrieve employees along with their corresponding department names:

```sql
SELECT Employees.Name, Departments.Department
FROM Employees
INNER JOIN Departments
ON Employees.DepartmentID = Departments.DepartmentID;
```
#### LEFT JOIN
The LEFT JOIN command returns all records from the left table, and the matched records from the right table. If no match is found, NULL values are returned for columns from the right table.

##### Basic Syntax
```sql
SELECT columns
FROM table1
LEFT JOIN table2
ON table1.common_column = table2.common_column;
```

##### Example Command
To retrieve all employees and their corresponding department names, including those without a department:

```sql
SELECT Employees.Name, Departments.Department
FROM Employees
LEFT JOIN Departments
ON Employees.DepartmentID = Departments.DepartmentID;
```

#### RIGHT JOIN
The RIGHT JOIN command returns all records from the right table, and the matched records from the left table. If no match is found, NULL values are returned for columns from the left table.

##### Basic Syntax
```sql
SELECT columns
FROM table1
RIGHT JOIN table2
ON table1.common_column = table2.common_column;
```

##### Example Command
To retrieve all departments and their corresponding employees, including departments without employees:
```sql
SELECT Employees.Name, Departments.Department
FROM Employees
RIGHT JOIN Departments
ON Employees.DepartmentID = Departments.DepartmentID;
```

#### FULL JOIN
The FULL JOIN command returns records when there is a match in either table. It returns all records from both tables, with NULLs in place where the join condition is not met.

##### Basic Syntax
```sql
SELECT columns
FROM table1
FULL JOIN table2
ON table1.common_column = table2.common_column;
```

##### Example Command
To retrieve all employees and departments, including those without matches:
```sql
SELECT Employees.Name, Departments.Department
FROM Employees
FULL JOIN Departments
ON Employees.DepartmentID = Departments.DepartmentID;
```
## Example Outputs

### INNER JOIN Output
| Name       | Department |
|------------|------------|
| John Doe   | Sales      |
| Jane Smith | HR         |
| Lisa White | IT         |

### LEFT JOIN Output
| Name       | Department |
|------------|------------|
| John Doe   | Sales      |
| Jane Smith | HR         |
| Mike Brown | NULL       |
| Lisa White | IT         |

### RIGHT JOIN Output
| Name       | Department |
|------------|------------|
| John Doe   | Sales      |
| Jane Smith | HR         |
| Lisa White | IT         |
| NULL       | Marketing  |

### FULL JOIN Output
| Name       | Department |
|------------|------------|
| John Doe   | Sales      |
| Jane Smith | HR         |
| Mike Brown | NULL       |
| Lisa White | IT         |
| NULL       | Marketing  |




#### **3.2. Subqueries**
A query nested inside another query.

Example:
```sql
SELECT first_name, last_name
FROM employees
WHERE department_id = (SELECT id FROM departments WHERE department_name = 'Sales');
```

#### **3.3. Indexes**
Enhance the speed of data retrieval operations on a database table.

Example:
```sql
CREATE INDEX idx_employee_department ON employees(department_id);
```

### **4. SQL for Data Analysis**

#### **4.1. Window Functions**
Perform calculations across a set of table rows related to the current row.

Example:
```sql
SELECT employee_id, department_id, salary,
       RANK() OVER (PARTITION BY department_id ORDER BY salary DESC) as rank
FROM employees;
```

#### **4.2. Common Table Expressions (CTEs)**
Simplify complex queries with temporary result sets.

Example:
```sql
WITH department_sales AS (
    SELECT department_id, SUM(sales) as total_sales
    FROM sales
    GROUP BY department_id
)
SELECT departments.department_name, department_sales.total_sales
FROM departments
JOIN department_sales ON departments.id = department_sales.department_id;
```

I have learnt SQL from various online resources which are free. I am providing some of the top resources I consider to be comprehensive and easy to follow. Check these out and chose your own favourite to start with.

## Top 5 Free Resources for Learning SQL for Data Science

Learning SQL is a crucial skill for data science. Here are the top 5 free resources to help you get started:

### 1. Codecademy
[Codecademy](https://www.codecademy.com/learn/learn-sql) offers a comprehensive and interactive SQL course that covers basic to advanced SQL concepts, including data manipulation and querying techniques.

### 2. W3Schools
[W3Schools](https://www.w3schools.com/sql/) provides a detailed SQL tutorial with numerous examples and interactive exercises. It’s a great place to understand the basics and practice writing SQL queries.

### 3. Khan Academy
[Khan Academy](https://www.khanacademy.org/computing/computer-programming/sql) offers an SQL course that covers SQL basics and more advanced topics with interactive challenges and exercises.

### 4. Mode Analytics SQL Tutorial
[Mode Analytics](https://mode.com/sql-tutorial/) provides a practical SQL tutorial that focuses on real-world data analysis. It's a great resource for those looking to apply SQL skills in data science.

### 5. SQLZoo
[SQLZoo](https://sqlzoo.net/) is an interactive SQL tutorial with a wide range of exercises and quizzes. It covers different SQL databases and provides hands-on practice.

## Practice, practice, and practice

I truly believe that learning any programming language can't be achieved just by reading countless articles, books, or blogs. The real way to learn and remember is to practice, practice, and practice writing the commands. Whenever you encounter an error, take the time to understand where you went wrong. This approach provides countless opportunities for active learning. This is a philosophy I hold dear. Mistakes will teach you more than success ever could.



By following this structured roadmap, you can systematically build and enhance your SQL skills, making you a valuable asset in the field of data science. Happy learning!
