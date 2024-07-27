# Keys
- **Definition**: A key is an attribute or a set of attributes that uniquely identifies an entity in an entity set.
-  **Characteristics**:
	- Each entity must have a key value.
	- A key can have 1 or many attributes.
## Primary Keys
A primary key is a unique identifier for a record in a table. It ensures that each record can be uniquely identified and prevents duplicate records.
- **Definition**: A primary key is a column (or a set of columns) whose values uniquely identify every row in a table.
- **Characteristics**:
    - Uniqueness: No two rows can have the same primary key value.
    - Non-null: Primary key columns cannot contain NULL values.
    - A table can have only one primary key.
    - A key can have 1 or many attributes.
	- In an entity which can have many keys, choose 1 key for primary key of entity.
- **Example**:
```sql
CREATE TABLE Employees (     
	EmployeeID INT PRIMARY KEY,     
	FirstName VARCHAR(50),     
	LastName VARCHAR(50) 
);
```
## Candidate Keys
A candidate key is a column, or a set of columns, that can uniquely identify any record in a table. Each table can have multiple candidate keys, but only one of them will be selected as the primary key.
- **Definition**: A candidate key is any column or combination of columns that can qualify as a unique key in a database.
- **Characteristics**:
    - Uniqueness: The values in the candidate key columns must be unique.
    - Non-null: Candidate key columns cannot contain NULL values.
    - Multiple candidate keys can exist in a table.
- **Example**:
```sql
CREATE TABLE Employees (     
	EmployeeID INT,     
	NationalID VARCHAR(20),     
	FirstName VARCHAR(50),     
	LastName VARCHAR(50),     
	PRIMARY KEY (EmployeeID),     
	UNIQUE (NationalID) 
);
```
## Composite Keys
A composite key is a primary key that consists of two or more columns. It is used when a single column is not sufficient to uniquely identify a record.
- **Definition**: A composite key is a primary key composed of multiple columns.
- **Characteristics**:
    - Uniqueness: The combination of the values in the composite key columns must be unique.
    - Non-null: None of the columns in the composite key can contain NULL values.
- **Example**:
```sql
CREATE TABLE OrderDetails (     
	OrderID INT,     
	ProductID INT,     
	Quantity INT,     
	PRIMARY KEY (OrderID, ProductID) 
);
```
## Foreign Keys
A foreign key is a column or a set of columns in one table that refers to the primary key in another table. It establishes a relationship between two tables.
- **Definition**: A foreign key is a column or combination of columns that is used to establish and enforce a link between the data in two tables.
- **Characteristics**:
    - Referential Integrity: The foreign key value must match a primary key value in the referenced table or be NULL.
    - It can be null or duplicate, as long as the relationship integrity is maintained.
- **Example**:
```sql
CREATE TABLE Orders (     
	OrderID INT PRIMARY KEY,     
	CustomerID INT,     
	OrderDate DATE,     
	FOREIGN KEY (CustomerID) REFERENCES Customers(CustomerID)
);
```
# Examples in SQL Server:
Below is an example illustrating all these keys in a database schema:
```sql
-- Create Customers table with CustomerID as the primary key 
CREATE TABLE Customers (     
	CustomerID INT PRIMARY KEY,     
	NationalID VARCHAR(20) UNIQUE, 
	-- Candidate key     
	FirstName VARCHAR(50),     
	LastName VARCHAR(50) 
);  
	-- Create Orders table with OrderID as the primary key and CustomerID as a foreign key 
CREATE TABLE Orders (     
	OrderID INT PRIMARY KEY,     
	CustomerID INT,     
	OrderDate DATE,     
	FOREIGN KEY (CustomerID) REFERENCES Customers(CustomerID)
);  
-- Create OrderDetails table with a composite key (OrderID, ProductID) 
CREATE TABLE OrderDetails (     
	OrderID INT,     
	ProductID INT,     
	Quantity INT,     
	PRIMARY KEY (OrderID, ProductID),     
	FOREIGN KEY (OrderID) REFERENCES Orders(OrderID) 
);
```
In this schema:
- `CustomerID` in the `Customers` table is the primary key.
- `NationalID` in the `Customers` table is a candidate key.
- `OrderID` in the `Orders` table is the primary key.
- `CustomerID` in the `Orders` table is a foreign key that references `CustomerID` in the `Customers` table.
- `OrderID` and `ProductID` in the `OrderDetails` table form a composite primary key.
- `OrderID` in the `OrderDetails` table is a foreign key that references `OrderID` in the `Orders` table.
