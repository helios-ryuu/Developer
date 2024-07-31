# Normalization
Normalization is a process in database design that organizes columns and tables to minimize data redundancy and improve data integrity. It involves decomposing tables into smaller, related tables and defining relationships between them. The main goal is to ensure that data dependencies are logical and that the database structure facilitates efficient querying and updates.
# Why Normalize?
1. **Eliminate Redundancy**: Redundant data wastes storage and can lead to anomalies during data manipulation.
2. **Ensure Data Integrity**: Consistent data across the database ensures accuracy and reliability.
3. **Simplify Database Maintenance**: A well-structured database is easier to maintain and update.
# Normalization Process and Normal Forms
Normalization is achieved through a series of stages called **normal forms**. Each normal form has specific requirements. The most commonly used normal forms are:
## First Normal Form (1NF)
- **Requirements**:
  - Each column contains atomic (indivisible) values.
  - Each column contains values of a single type.
  - Each column must contain unique values, and there should be no repeating groups or arrays.
- **Example**: Consider a table with customer orders:

| OrderID | CustomerName | Items               |
|---------|--------------|---------------------|
| 1       | John         | Bread, Milk         |
| 2       | Alice        | Butter, Cheese      |

  In 1NF, we would split the "Items" column into separate rows:

| OrderID | CustomerName | Item   |
|---------|--------------|--------|
| 1       | John         | Bread  |
| 1       | John         | Milk   |
| 2       | Alice        | Butter |
| 2       | Alice        | Cheese |

## Second Normal Form (2NF)
- **Requirements**:
  - Meet all the requirements of 1NF.
  - All non-key attributes must be fully functionally dependent on the primary key. This means no partial dependency of any column on the primary key.
- **Example**: In the 1NF example, if the table also includes the customer's address, and the primary key is `OrderID`, the address would depend on the customer, not on the specific order. To meet 2NF, we would separate the customer details:
  **Customers Table**:
  
| CustomerID | CustomerName | Address       |
|------------|--------------|---------------|
| 1          | John         | 123 Elm St    |
| 2          | Alice        | 456 Maple St  |

  **Orders Table**:

| OrderID | CustomerID | Item   |
|---------|------------|--------|
| 1       | 1          | Bread  |
| 1       | 1          | Milk   |
| 2       | 2          | Butter |
| 2       | 2          | Cheese |

## Third Normal Form (3NF)
- **Requirements**:
  - Meet all the requirements of 2NF.
  - All the attributes in a table must depend on the primary key and nothing but the primary key (i.e., no transitive dependencies).
- **Example**: If the `Customers` table includes a column like `City` and `PostalCode`, and `City` can determine `PostalCode`, we should separate them:
  **Customers Table**:

| CustomerID | CustomerName | City     |
|------------|--------------|----------|
| 1          | John         | Springfield |
| 2          | Alice        | Metropolis  |

  **CityPostalCodes Table**:

| City        | PostalCode |
|-------------|------------|
| Springfield | 12345      |
| Metropolis  | 54321      |

## Boyce-Codd Normal Form (BCNF)
- **Requirements**:
  - Meet all the requirements of 3NF.
  - Every determinant must be a candidate key. A determinant is an attribute or a set of attributes on which some other attribute is fully functionally dependent.
- **Example**: Consider a table with `CourseID`, `Instructor`, and `RoomNumber` where a room can have only one course at a time but a course can have multiple instructors. We split into:
**Courses Table**:

| CourseID | Instructor |
|----------|------------|
| 1        | Smith      |
| 1        | Doe        |
| 2        | Jane       |

**RoomAssignments Table**:

| RoomNumber | CourseID |
|------------|----------|
| 101        | 1        |
| 102        | 2        |

## Fourth Normal Form (4NF)
- **Requirements**:
  - Meet all the requirements of BCNF.
  - There should be no multi-valued dependencies.
- **Example**: If a person can have multiple skills and speak multiple languages, and these are independent of each other, separate them:
**Persons Table**:

| PersonID | Name  |
|----------|-------|
| 1        | John  |
| 2        | Alice |

**Skills Table**:

| PersonID | Skill       |
|----------|-------------|
| 1        | Programming |
| 1        | Writing     |
| 2        | Design      |

**Languages Table**:

| PersonID | Language |
|----------|----------|
| 1        | English  |
| 1        | French   |
| 2        | Spanish  |
Normalization continues to higher forms (5NF, 6NF), but these are less commonly applied.
# Benefits of Normalization
1. **Data Integrity**: Reduces anomalies such as insert, update, and delete anomalies.
2. **Efficient Data Access**: Reduces the need for large amounts of duplicate data.
3. **Flexibility**: Makes it easier to modify the database structure without affecting existing data.
4. **Consistency**: Ensures that changes in one place are reflected consistently throughout the database.
# When Not to Normalize
In some cases, denormalization may be beneficial, particularly in scenarios requiring fast read operations, such as in data warehousing and OLAP systems, where query performance can be improved by storing data in a less normalized form. However, this comes at the cost of potential data anomalies and increased storage requirements.
