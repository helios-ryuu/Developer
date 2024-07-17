> The Entity-Relationship (ER) model is a high-level conceptual data model<sup>mô hình dữ liệu khái niệm cấp cao</sup> that is widely used in database design to visually represent data entities and their relationships. Here's an in-depth look at the ER model, including its components, types of relationships, constraints, and practical applications.
## Components of the ER Model
1. **[[Entities]]**
    - **Definition**: An entity is an object or concept about which data is stored. Entities represent real-world objects or concepts.
    - **Entity Set**: A collection of similar types of entities. For example, all students in a university form the "Student" entity set.
    - **Representation**: Entities are represented by rectangles in ER diagrams.
    - **Examples**: Student, Course, Instructor, Department.
2. **[[Attributes]]**
    - **Definition**: Attributes are the properties or characteristics of an entity. Each attribute has a specific value.
    - **Types of Attributes**:
        - **Simple<sup>đơn trị</sup> (Atomic)**: Cannot be divided further (e.g., StudentID, Name).
        - **Composite**<sup>đa hợp</sup>: Can be divided into smaller sub-parts (e.g., Address can be divided into Street, City, Zip Code - Address(Street, City, Zip Code)).
        - **Derived**: Can be derived from other attributes (e.g., Age can be derived from DateOfBirth).
        - **Multivalued**<sup>đa trị</sup>: Can have multiple values (e.g., PhoneNumbers - {PhoneNumbers}).
    - **Representation**: Attributes are represented by ovals connected to their respective entities.
    - **Examples**: Name, DateOfBirth, Gender, GPA for a Student entity.
3. **[[Relationships]]**
    - **Definition**: Relationships represent the associations between entities. Between the two entity sets there may exist more than one type of relationship.
    - **Relationship Set**: A collection of similar types of relationships.
    - **Representation**: Relationships are represented by diamonds in ER diagrams, connected to the entities involved.
    - **Examples**: "Enrolls In" between Student and Course, "Teaches" between Instructor and Course.
4. **[[Keys]]**
	- **Definition**: A key is an attribute or a set of attributes that uniquely identifies an entity in an entity set.
	-  **Characteristics**:
		- Each entity must have a key value.
		- A key can have 1 or many attributes.
		- In an entity which can have many keys, choose 1 key for primary key of entity.
#### Keys
1. **Primary Key**
    - An attribute or set of attributes that uniquely identifies each instance of an entity.
    - Example: StudentID in the Student entity.
2. **Foreign Key**
    - An attribute or set of attributes in one entity that references the primary key of another entity.
    - Example: CourseID in the Enrollment entity that references CourseID in the Course entity.
## ER Diagram Notations
1. **Entities**: Represented by rectangles.
2. **Attributes**: Represented by ovals.
3. **Relationships**: Represented by diamonds.
4. **Primary Key**: Underlined attribute.
5. **Multivalued Attribute**: Represented by a double oval.
6. **Composite Attribute**: Represented by an oval connected to sub-ovals.
## Practical Applications
1. **Database Design**: ER models are used to create a clear and structured design of a database, ensuring data integrity and efficient organization.
2. **Communication**: Provides a visual representation that helps stakeholders understand the data requirements and relationships, facilitating communication between database designers, developers, and end-users.
3. **Documentation**: Serves as documentation for the database structure, which is useful for future maintenance and updates.
## Example ER Diagram
Here is an example of an ER diagram for a university database:
- **Entities**:
    - Student (StudentID, Name, DateOfBirth, Address)
    - Course (CourseID, CourseName, Credits)
    - Instructor (InstructorID, Name, Office)
    - Department (DeptID, DeptName)
- **Relationships**:
    - Enrolls (Student, Course, EnrollmentDate)
    - Teaches (Instructor, Course, Semester)
    - BelongsTo (Instructor, Department)
    - Offers (Department, Course)

> **In this ER diagram**:
> - Students can enroll in multiple courses (Many-to-Many relationship between Student and Course).
> - Instructors can teach multiple courses (One-to-Many relationship between Instructor and Course).
> - Instructors belong to a department (Many-to-One relationship between Instructor and Department).
> - Departments offer courses (One-to-Many relationship between Department and Course).