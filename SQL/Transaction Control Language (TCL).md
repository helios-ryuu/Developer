> **Transaction Control Language (TCL)** is a subset of SQL (Structured Query Language) used to manage transactions within a database. TCL commands ensure that the database remains consistent and reliable by grouping a series of operations into a single transaction, which is either fully completed or fully rolled back. This ensures data integrity, particularly in environments where multiple operations are executed simultaneously.
## **[[COMMIT]]**
- **Purpose**: To save all changes made during the current transaction.
- **Syntax**: 
```sql
COMMIT;
```
---
```sql
BEGIN TRANSACTION;
UPDATE employees SET salary = 55000 WHERE employee_id = 123;
INSERT INTO audit_log (log_message) VALUES ('Updated salary for employee 123');
COMMIT;
```
> This command commits all changes, ensuring they are permanently saved to the database.
## **[[ROLLBACK]]**
- **Purpose**: To undo all changes made during the current transaction.
- **Syntax**: 
```sql
ROLLBACK;
```
---
```sql
BEGIN TRANSACTION;
UPDATE employees SET salary = 55000 WHERE employee_id = 123;

-- Something goes wrong here
ROLLBACK;
```
> This command rolls back all changes, reverting the database to its previous state before the transaction began.
## **[[SAVEPOINT]]**
- **Purpose**: To set a point within a transaction to which you can later roll back.
- **Syntax**: 
```sql
SAVEPOINT savepoint_name;
```
---
```sql
BEGIN TRANSACTION;
UPDATE employees SET salary = 55000 WHERE employee_id = 123;
SAVEPOINT before_bonus;
UPDATE employees SET bonus = 5000 WHERE employee_id = 123;

-- If something goes wrong with the bonus update, rollback to savepoint
ROLLBACK TO before_bonus;
COMMIT;
```
> This command allows partial rollback within a transaction, useful for complex operations.
## **[[RELEASE SAVEPOINT]]**
- **Purpose**: To remove a savepoint, making it no longer available for rollback.
- **Syntax**: 
```sql
RELEASE SAVEPOINT savepoint_name;
```
---
```sql
SAVEPOINT before_bonus;

-- Some operations
RELEASE SAVEPOINT before_bonus;
```
> This command allows partial rollback within a transaction, useful for complex operations.
## **[[SET TRANSACTION]]**
- **Purpose**: To specify characteristics for the transaction, such as isolation level.
- **Syntax**: 
```sql
SET TRANSACTION {READ WRITE | READ ONLY};
```
---
```sql
SET TRANSACTION READ ONLY;
```