> **Data Manipulation Language (DML)** is a subset of SQL (Structured Query Language) used to manage and manipulate data within existing database objects. DML commands are utilized to retrieve, insert, update, and delete data in database tables. These commands are crucial for interacting with the database and performing everyday tasks related to data handling.
## **[[SELECT]]**
- **Purpose**: To retrieve data from one or more tables.
- **Syntax**:
```sql
SELECT column1, column2, ...
FROM table_name
WHERE condition;
```
---
```sql
SELECT first_name, last_name, salary
FROM employees
WHERE department_id = 10;
```
## **[[INSERT]]**
- **Purpose**: To add new rows of data into a table.
- **Syntax**:
```sql
INSERT INTO table_name (column1, column2, ...)
VALUES (value1, value2, ...);
```
---
```sql
INSERT INTO employees (first_name, last_name, hire_date, salary, department_id)
VALUES ('John', 'Doe', '2024-07-14', 50000, 10);
```
## **[[UPDATE]]**
- **Purpose**: To modify existing data in a table.
- **Syntax**:
```sql
UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;
```
---
```sql
UPDATE employees
SET salary = 55000
WHERE employee_id = 123;
```
## **[[DELETE]]**
- **Purpose**: To remove rows of data from a table.
- **Syntax**:
```sql
DELETE FROM table_name
WHERE condition;
```
---
```sql
DELETE FROM employees
WHERE employee_id = 123;
```