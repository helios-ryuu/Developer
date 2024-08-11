# SQL
**SQL** (Structured Query Language) is a standard language used for managing and manipulating relational databases (cơ sở dữ liệu quan hệ). It is used for querying, updating, and managing data.
## Data Manipulation Language (DML)
**DML** commands are used to interact with and manipulate data in database tables. They allow you to retrieve, insert, update, and delete data.

| Keyword        | Function                                                                           |
| -------------- | ---------------------------------------------------------------------------------- |
| **[[SELECT]]** | Retrieves data from one or more tables or views.                                   |
| **INSERT**     | Adds new rows of data into a table.                                                |
| **UPDATE**     | Modifies existing data within a table.                                             |
| **DELETE**     | Removes rows from a table.                                                         |
| **MERGE**      | Inserts, updates, or deletes data based on conditions; useful for synchronization. |
| **CALL**       | Executes a stored procedure or function.                                           |
| **EXPLAIN**    | Shows the execution plan for a SQL statement.                                      |
| **LOCK TABLE** | Locks a table to prevent other operations from modifying it.                       |
| **UPSERT**     | Inserts or updates rows in a table based on whether they exist.                    |
| **WITH**       | Defines a temporary result set that can be used in a query.                        |
## Data Definition Language (DDL)
**DDL** commands define and manage the structure of database objects like tables, indexes, and schemas.

| Keyword              | Function                                                                            |
| -------------------- | ----------------------------------------------------------------------------------- |
| **[[CREATE]]**       | Creates new tables, databases, indexes, or views.                                   |
| **ALTER**            | Modifies existing database objects (e.g., tables, indexes).                         |
| **DROP**             | Deletes existing database objects.                                                  |
| **TRUNCATE**         | Removes all rows from a table while keeping its structure.                          |
| **RENAME**           | Renames database objects such as tables or columns.                                 |
| **COMMENT**          | Adds or updates comments on database objects.                                       |
| **ADD**              | Adds new columns or objects to existing tables or schemas.                          |
| **MODIFY**           | Changes column data types or attributes.                                            |
| **DROP COLUMN**      | Removes a column from a table.                                                      |
| **CREATE TABLE**     | Defines a new table with specific columns and constraints.                          |
| **CREATE INDEX**     | Creates an index to improve query performance.                                      |
| **CREATE VIEW**      | Defines a view that shows data from one or more tables.                             |
| **CREATE SCHEMA**    | Creates a new schema for organizing database objects.                               |
| **CREATE TRIGGER**   | Defines a trigger that executes SQL statements automatically in response to events. |
| **CREATE SEQUENCE**  | Generates a sequence of unique numbers.                                             |
| **CREATE FUNCTION**  | Defines a user-defined function that can be used in SQL queries.                    |
| **CREATE PROCEDURE** | Defines a stored procedure to perform complex operations.                           |
| **CREATE SYNONYM**   | Creates an alias for another database object.                                       |
| **CREATE DATABASE**  | Creates a new database.                                                             |
## Data Control Language (DCL)
**DCL** commands manage access to data and control permissions within a database.

| Keyword         | Function                                            |
| --------------- | --------------------------------------------------- |
| **[[GRANT]]**   | Gives specific privileges to users or roles.        |
| **REVOKE**      | Removes privileges from users or roles.             |
| **DENY**        | Denies specific privileges to users or roles.       |
| **CONNECT**     | Establishes a new connection to the database.       |
| **DISCONNECT**  | Ends an existing connection to the database.        |
| **EXECUTE**     | Allows execution of a stored procedure or function. |
| **SHOW GRANTS** | Lists the privileges assigned to a user.            |
| **SET ROLE**    | Activates or deactivates roles for a user session.  |
## Transaction Control Language (TCL)
**TCL** commands manage transactions to ensure database consistency and integrity.

| Keyword               | Function                                                                    |
| --------------------- | --------------------------------------------------------------------------- |
| **[[COMMIT]]**        | Saves all changes made during the current transaction.                      |
| **ROLLBACK**          | Reverts all changes made during the current transaction.                    |
| **SAVEPOINT**         | Sets a point within a transaction to which you can later roll back.         |
| **SET TRANSACTION**   | Configures transaction properties like isolation levels.                    |
| **LOCK**              | Controls access to resources to prevent conflicts (varies by DBMS).         |
| **BEGIN TRANSACTION** | Starts a new transaction.                                                   |
| **START TRANSACTION** | Initiates a new transaction, marking the start of a sequence of operations. |
# SQL Server
**SQL Server** is a relational database management system (RDBMS) by Microsoft. It supports SQL for database operations and offers various services.
### Services
- **Database Engine**: Core service for data storage, processing, and security.
- **SQL Server Agent**: Manages and schedules jobs.
- **SQL Server Reporting Services (SSRS)**: Creates and manages reports.
- **SQL Server Integration Services (SSIS)**: Handles data integration and workflow.
- **SQL Server Analysis Services (SSAS)**: Provides OLAP and data mining capabilities.
# Query
A **query** is a request for data or information from a database. Queries are typically written in SQL and can perform operations such as:
- Retrieving specific data (using `SELECT`).
- Filtering data based on conditions.
- Updating or deleting data.
- Performing calculations and aggregations.
# NoSQL
**NoSQL** databases are non-relational and designed for handling various data models with flexible schemas. They are suitable for large volumes of unstructured or semi-structured data.
### Types of NoSQL Databases
- **Document Stores**: Store data as documents (e.g., JSON) (e.g., MongoDB, CouchDB).
- **Key-Value Stores**: Store data as key-value pairs (e.g., Redis, DynamoDB).
- **Wide-Column Stores**: Organize data in tables with rows and dynamic columns (e.g., Cassandra, HBase).
- **Graph Databases**: Represent data in graph structures with nodes and edges (e.g., Neo4j, OrientDB).
# Entity-Relationship Model
The **Entity-Relationship (ER) Model** is used to visually represent data entities and their relationships in database design. Its components are [[Entities]], [[Keys]], [[Relationships]].
## Extended ER Model
### Specialization and Generalization
**Specialization** and **Generalization** manage hierarchical relationships and inheritance.
#### Specialization
**Specialization** is the process of defining sub-entities from a higher-level entity based on distinguishing characteristics.
- **Example**:
    - **Entity**: Employee
    - **Sub-entities**: Engineer, Manager, Technician
    - **Attributes**:
        - Engineer: Programming Language
        - Manager: Department
        - Technician: Skill Level
#### Generalization
**Generalization** combines multiple entities into a single higher-level entity based on common attributes.
- **Example**:
    - **Entities**: Car, Truck, Motorcycle
    - **Generalized Entity**: Vehicle
    - **Common Attributes**: Make, Model, Year
#### Diagram Representation
**In ER diagrams**:
- **Specialization** is represented with a triangle pointing towards the specialized entities from the generalized entity.
- **Generalization** is represented with a triangle pointing towards the generalized entity from the specialized entities.

**Example Scenario**:
1. **Generalization**:
    - Entities: Undergraduate Student, Graduate Student
    - Generalized Entity: Student
    - Common Attributes: Student_ID, Name, Date_of_Birth
2. **Specialization**:
    - Entity: Student
    - Sub-entities: Undergraduate Student, Graduate Student
    - Specific Attributes:
        - Undergraduate Student: Major, Year
        - Graduate Student: Thesis_Title, Advisor
### Recursive Relationship
**Recursive relationships** occur when an entity has a relationship with itself. Example: An employee managing other employees.
### Weak Entity
A **weak entity** depends on another entity (known as the owner entity) for its existence and identification. It cannot be uniquely identified by its own attributes alone.
### Extended Relationships
**Extended relationships** capture more complex interactions between entities, often involving more advanced modeling concepts.