> **Data Control Language (DCL)** is a subset of SQL (Structured Query Language) used to control access to data in a database. DCL commands are primarily concerned<sup>được quan tâm chủ yếu</sup> with the permissions and security of the database objects. The two main DCL commands are `GRANT` and `REVOKE`.
## **[[GRANT]]**
- **Purpose**: To give a user permission to perform specific actions on the database.
- **Syntax**: 
```sql
GRANT privilege_name ON object_name TO user_name;
```
---
```sql
GRANT INSERT ON employees TO user_name;
```
## **[[REVOKE]]**
- **Purpose**: To remove a user's permission to perform specific actions on the database.
- **Syntax**: 
```sql
REVOKE privilege_name ON object_name FROM user_name;
```
---
```sql
REVOKE INSERT ON employees FROM user_name;
```
## **[[ROLE]]**
- **Purpose**: These are named groups of related privileges that can be granted to users. Using roles can simplify the management of user permissions..
- **Example**: 
```sql
CREATE ROLE manager;
GRANT SELECT, INSERT, UPDATE ON employees TO manager;
GRANT manager TO user_name;
```
