# SQL
SQL (Structured Query Language - Ngôn ngữ truy vấn có cấu trúc) là một ngôn ngữ tiêu chuẩn dùng để quản lý và thực hiện các thao tác trên các cơ sở dữ liệu quan hệ (Relational database). Nó dùng để truy vấn (Query), cập nhật (Update) và quản lý (Manage) dữ liệu trong cơ sở dữ liệu.
## Truy vấn - Query
Truy vấn (Query) là một yêu cầu lấy dữ liệu hoặc thông tin từ cơ sở dữ liệu. Truy vấn thường được viết bằng SQL và có thể thực hiện các thao tác như:
- Truy xuất dữ liệu cụ thể (sử dụng `SELECT`).
- Lọc dữ liệu dựa trên các điều kiện (Condition).
- Cập nhật hoặc xóa dữ liệu.
- Thực hiện các phép tính và tổng hợp dữ liệu (Aggregation).
## Ngôn ngữ thao tác dữ liệu - DML
Các lệnh DML (Data Manipulation Language) được dùng để tương tác và điều chỉnh dữ liệu trong các bảng (Table) của cơ sở dữ liệu. Chúng cho phép bạn truy xuất (Retrieve), chèn (Insert), cập nhật (Update) và xóa dữ liệu (Delete).

| Keyword        | Function                                                                                                   |
| -------------- | ---------------------------------------------------------------------------------------------------------- |
| **CALL**       | Thực thi một thủ tục lưu trữ (Stored Procedure) hoặc hàm (Function).                                       |
| **DELETE**     | Xóa các hàng khỏi bảng                                                                                     |
| **EXPLAIN**    | Hiển thị kế hoạch thực thi (Execution Plan) cho một câu lệnh SQL.                                          |
| **INSERT**     | Thêm các hàng dữ liệu mới vào bảng.                                                                        |
| **LOCK TABLE** | Khóa một bảng để ngăn các thao tác chỉnh sửa bảng đó.                                                      |
| **MERGE**      | Chèn, cập nhật hoặc xóa dữ liệu dựa trên các điều kiện (Hữu ích cho việc đồng bộ hóa)                      |
| **[[SELECT]]** | Truy xuất dữ liệu từ một hoặc nhiều bảng, view.                                                            |
| **UPDATE**     | Sửa đổi dữ liệu hiện có trong bảng.                                                                        |
| **UPSERT**     | Chèn hoặc cập nhật các hàng trong bảng dựa trên việc liệu chúng có tồn tại hay không.                      |
| **WITH**       | Định nghĩa một tập kết quả tạm thời (Temporary Result Set) có thể được sử dụng trong một truy vấn (Query). |
## Ngôn ngữ định nghĩa dữ liệu - DDL
Các lệnh DDL (Data Definition Language) định nghĩa và quản lý cấu trúc của các đối tượng trong cơ sở dữ liệu như bảng (Table), chỉ mục (Index) và lược đồ (Schema).

| Keyword              | Function                                                                                    |
| -------------------- | ------------------------------------------------------------------------------------------- |
| **ADD**              | Thêm các cột hoặc đối tượng mới vào bảng hoặc lược đồ (Schema) hiện có                      |
| **ALTER**            | Sửa đổi các đối tượng cơ sở dữ liệu hiện có (ví dụ: bảng, chỉ mục).                         |
| **COMMENT**          | Thêm hoặc cập nhật nhận xét của các đối tượng cơ sở dữ liệu.                                |
| **[[CREATE]]**       | Tạo bảng, cơ sở dữ liệu, chỉ mục (Index) hoặc view mới.                                     |
| **CREATE DATABASE**  | Tạo một cơ sở dữ liệu mới.                                                                  |
| **CREATE FUNCTION**  | Định nghĩa một hàm do người dùng tự định nghĩa có thể được sử dụng trong các truy vấn SQL.  |
| **CREATE INDEX**     | Tạo chỉ mục để cải thiện hiệu suất truy vấn.                                                |
| **CREATE PROCEDURE** | Định nghĩa một thủ tục lưu trữ (Stored Procedure) để thực hiện các thao tác phức tạp.       |
| **CREATE SCHEMA**    | Tạo một lược đồ mới để tổ chức các đối tượng cơ sở dữ liệu.                                 |
| **CREATE SEQUENCE**  | Tạo ra một chuỗi các số độc nhất.                                                           |
| **CREATE SYNONYM**   | Tạo một bí danh (Alias) cho một đối tượng cơ sở dữ liệu khác.                               |
| **CREATE TABLE**     | Định nghĩa một bảng mới với các cột và ràng buộc cụ thể.                                    |
| **CREATE TRIGGER**   | Định nghĩa một trigger để thực thi các câu lệnh SQL một cách tự động khi có sự kiện xảy ra. |
| **CREATE VIEW**      | Định nghĩa một view hiển thị dữ liệu từ một hoặc nhiều bảng.                                |
| **DROP**             | Xóa các đối tượng cơ sở dữ liệu hiện có.                                                    |
| **DROP COLUMN**      | Xóa một cột khỏi bảng.                                                                      |
| **MODIFY**           | Thay đổi kiểu dữ liệu hoặc thuộc tính của cột.                                              |
| **RENAME**           | Đổi tên các đối tượng cơ sở dữ liệu như bảng hoặc cột.                                      |
| **TRUNCATE**         | Xóa tất cả các hàng khỏi một bảng nhưng giữ nguyên cấu trúc của nó.                         |
## Ngôn ngữ điều khiển dữ liệu - DCL
Các lệnh DCL (Data Control Language) quản lý quyền truy cập vào dữ liệu và điều khiển các quyền trong cơ sở dữ liệu.

| Keyword         | Function                                                                      |
| --------------- | ----------------------------------------------------------------------------- |
| **CONNECT**     | Thiết lập một kết nối mới tới cơ sở dữ liệu.                                  |
| **DENY**        | Từ chối quyền cụ thể cho người dùng hoặc vai trò.                             |
| **DISCONNECT**  | Kết thúc một kết nối hiện có tới cơ sở dữ liệu.                               |
| **EXECUTE**     | Cho phép thực thi một Thủ tục lưu trữ (Stored Procedure hoặc Hàm (Function).  |
| **[[GRANT]]**   | Cấp quyền (Privilege) cụ thể cho người dùng hoặc vai trò.                     |
| **REVOKE**      | Thu hồi quyền từ người dùng hoặc vai trò.                                     |
| **SET ROLE**    | Kích hoạt hoặc hủy kích hoạt vai trò cho một phiên người dùng (User Session). |
| **SHOW GRANTS** | Liệt kê các quyền đã được cấp cho một người dùng.                             |
## Ngôn ngữ điều khiển giao dịch - TCL
Các lệnh TCL (Transaction Control Language) quản lý các giao dịch (Transaction) để đảm bảo tính nhất quán (Consistency) và toàn vẹn (Integrity) của cơ sở dữ liệu.

| Keyword               | Function                                                                            |
| --------------------- | ----------------------------------------------------------------------------------- |
| **BEGIN TRANSACTION** | Bắt đầu một giao dịch mới.                                                          |
| **[[COMMIT]]**        | Lưu tất cả các thay đổi được thực hiện trong giao dịch hiện tại.                    |
| **LOCK**              | Kiểm soát quyền truy cập vào tài nguyên để tránh xung đột (khác nhau tùy vào DBMS). |
| **ROLLBACK**          | Hoàn tác tất cả các thay đổi được thực hiện trong giao dịch hiện tại.               |
| **SAVEPOINT**         | Đặt một điểm trong giao dịch mà sau này có thể quay lại điểm đó.                    |
| **SET TRANSACTION**   | Cấu hình các thuộc tính của giao dịch như mức độ cô lập (Isolation Level).          |
| **START TRANSACTION** | Khởi tạo một giao dịch mới, đánh dấu sự bắt đầu của một chuỗi các thao tác.         |
# SQL Server
SQL Server là một hệ quản trị cơ sở dữ liệu quan hệ (Relational Database Management System - RDBMS) của Microsoft. Nó hỗ trợ SQL cho các thao tác cơ sở dữ liệu và cung cấp nhiều dịch vụ khác nhau.
### Dịch vụ - Services
- **Database Engine**: Dịch vụ cốt lõi cho lưu trữ, xử lý và bảo mật dữ liệu.
- **SQL Server Agent**: Quản lý và lên lịch các công việc.
- **Dịch vụ báo cáo của SQL Server (SQL Server Reporting Services - SSRS)**: Tạo và quản lý báo cáo.
- **Dịch vụ tích hợp của SQL Server (SQL Server Integration Services - SSIS)**: Xử lý tích hợp dữ liệu (Data Integration) và luồng công việc (Workflow).
- **Dịch vụ phân tích của SQL Server (SQL Server Analysis Services - SSAS)**: Cung cấp khả năng OLAP (Online Analytical Processing) và khai phá dữ liệu.
# NoSQL
**NoSQL** là các cơ sở dữ liệu phi quan hệ (Non-relational Database), được thiết kế để xử lý các mô hình dữ liệu khác nhau với cấu trúc linh hoạt. Chúng phù hợp cho việc xử lý khối lượng lớn dữ liệu không cấu trúc hoặc bán cấu trúc.
### Các loại cơ sở dữ liệu NoSQL
- **Document Stores**: Lưu trữ dữ liệu dưới dạng tài liệu (ví dụ: JSON) (ví dụ: MongoDB, CouchDB).
- **Key-Value Stores**: Lưu trữ dữ liệu dưới dạng cặp khóa-giá trị (ví dụ: Redis, DynamoDB).
- **Wide-Column Stores**: Tổ chức dữ liệu trong các bảng với hàng và cột động (ví dụ: Cassandra, HBase).
- **Graph Databases**: Biểu diễn dữ liệu dưới dạng cấu trúc đồ thị với các nút và cạnh (ví dụ: Neo4j, OrientDB).
# Entity-Relationship Model
Mô hình quan hệ thực thể (ER Model) được sử dụng để biểu diễn trực quan các thực thể và mối quan hệ giữa chúng trong thiết kế cơ sở dữ liệu. Thành phần chính gồm: Thực thể (Entities), Khóa (Keys), và Quan hệ (Relationships).
## Mô hình ER mở rộng - Extended ER Model
### Chuyên biệt hóa và tổng quát hóa - Specialization and Generalization
Chuyên biệt hóa (Specialization) và tổng quát hóa (Generalization) quản lý các mối quan hệ phân cấp (Hierarchical Relationship) và thừa kế (Inheritance).
- **Chuyên biệt hóa (Specialization)**: là quá trình định nghĩa các thực thể con từ một thực thể cấp cao dựa trên các đặc điểm phân biệt.
- **Ví dụ**:
    - **Thực thể (Entity)**: Nhân viên - Employee
    - **Thực thể con**: Kỹ sư - Engineer, Quản lý - Manager, Kỹ thuật viên - Technician
    - **Thuộc tính**:
        - Kỹ sư: Ngôn ngữ lập trình - Programming Language
        - Quản lý: Phòng ban - Department
        - Kỹ thuật viên: Trình độ kỹ năng - Skill Level
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