> **Data Definition Language (DDL)** is a subset of SQL (Structured Query Language) used to define and manage the structure of a database and its objects. DDL statements are used to create, modify, and delete database objects such as tables, indexes, and schemas. These operations are essential for setting up and maintaining the database structure.
## **[[CREATE]]**
- **Purpose**: To create a new database object.
- **Syntax**: 
```sql
CREATE TABLE table_name (
	column1 datatype constraints, 
	column2 datatype constraints,
	...
);
```
---
```sql
CREATE TABLE employees (
	employee_id INT PRIMARY KEY,
	first_name VARCHAR(50),
	last_name VARCHAR(50),
	hire_date DATE,
	salary DECIMAL(10, 2)
);
```
## **[[ALTER]]**
- **Purpose**: To modify an existing database object.
- **Syntax**:
```sql
ALTER TABLE table_name 
ADD column_name datatype;
    
ALTER TABLE table_name 
MODIFY column_name new_datatype;
    
ALTER TABLE table_name 
DROP COLUMN column_name;
```
---
```sql
-- Add a new column 
ALTER TABLE employees ADD department_id INT;
    
-- Modify an existing column 
ALTER TABLE employees MODIFY salary DECIMAL(12, 2);
    
-- Drop a column 
ALTER TABLE employees DROP COLUMN hire_date;
```
## **[[DROP]]**
- **Purpose**: To delete an existing database object.
- **Syntax**:
```sql
DROP TABLE table_name; DROP INDEX index_name;
```
---
```sql
-- Drop a table 
DROP TABLE employees;  
    
-- Drop an index 
DROP INDEX employee_index;
```
## **[[TRUNCATE]]**
- **Purpose**: To remove all records from a table, but keep the structure intact.
- **Syntax**:
```sql
TRUNCATE TABLE table_name;
```
---
```sql
TRUNCATE TABLE employees;
```
## **[[RENAME]]**
- **Purpose**: To rename an existing database object.
- **Syntax**:
```sql
ALTER TABLE old_table_name
RENAME TO new_table_name;
```
---
```sql
ALTER TABLE employees 
RENAME TO staff;
```
## **[[COMMENT]]**
- **Purpose**: To add comments to database objects, providing descriptions.
- **Syntax**:
```sql
COMMENT ON TABLE table_name 
IS 'comment';  
    
COMMENT ON COLUMN table_name.column_name 
IS 'comment';
```
---
```sql
COMMENT ON TABLE employees 
IS 'Table containing employee information';

COMMENT ON COLUMN employees.salary 
IS 'Salary of the employee';
```