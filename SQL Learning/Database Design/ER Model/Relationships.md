# Relationships
Relationships represent the associations between entities. There may be more than one type of relationship between two entity sets.
**Relationship Set**: A collection of similar types of relationships.
**Representation**: Relationships are represented by diamonds in ER diagrams, connected to the entities involved.
**Examples**:
- "Enrolls In" between Student and Course
- "Teaches" between Instructor and Course
# Relationship Constraints
## Cardinality Constraints
Cardinality constraints specify the number of instances of one entity that can or must be associated with each instance of another entity. There are several types:
- **One-to-One (1:1)**: A single entity in one entity set is associated with a single entity in another entity set.
- **One-to-Many (1:N)**: A single entity in one entity set is associated with multiple entities in another entity set.
- **Many-to-One (N:1)**: Multiple entities in one entity set are associated with a single entity in another entity set.
- **Many-to-Many (M:N)**: Multiple entities in one entity set are associated with multiple entities in another entity set.
## Participation Constraints
Participation constraints specify whether all or only some entity instances participate in a relationship.
- **Total Participation**: Every instance of the entity must participate in the relationship. For example, every student must enroll in at least one course.
- **Partial Participation**: Some instances of the entity may not participate in the relationship. For example, some instructors may not be teaching any courses.
# Relationship Degree
The term "relationship degree" refers to the number of entities involved in a relationship. Relationships can be classified based on the number of participating entities.
- **Unary Relationship (Degree 1)**: Involves a single entity set. For example, an employee supervises other employees.
- **Binary Relationship (Degree 2)**: Involves two entity sets. For example, a student enrolls in a course.
- **Ternary Relationship (Degree 3)**: Involves three entity sets. For example, a supplier supplies a product to a customer through a contract.
- **N-ary Relationship (Degree N)**: Involves more than three entity sets. For example, a project involves multiple employees, managers, and resources.
# Relationship Attributes
**Definition**: Relationship attributes are characteristics or properties that describe a relationship. They are typically associated with the relationship itself rather than with the entities.
**Examples**:
- In a "Enrollment" relationship between Student and Course, attributes might include "EnrollmentDate" and "Grade".
- In a "Contract" relationship between Supplier, Product, and Customer, attributes might include "ContractDate" and "ContractAmount".
# Relationship Cardinality
## One-to-One (1:1)
**Definition**: A single entity in one entity set is associated with a single entity in another entity set.
**Example**: Each student has one unique student ID card, and each card is assigned to one student.
**Representation**: A line connecting two entities with "1" on both ends.
## One-to-Many (1:N)
**Definition**: A single entity in one entity set is associated with multiple entities in another entity set.
**Example**: One instructor teaches many courses, but each course is taught by one instructor.
**Representation**: A line connecting two entities with "1" on one end and "N" on the other end.
## Many-to-One (N:1)
**Definition**: Multiple entities in one entity set are associated with a single entity in another entity set.
**Example**: Many students are advised by one advisor, but each student has only one advisor.
**Representation**: A line connecting two entities with "N" on one end and "1" on the other end.
## Many-to-Many (M:N)
**Definition**: Multiple entities in one entity set are associated with multiple entities in another entity set.
**Example**: Students enroll in many courses, and each course has many students.
**Representation**: A line connecting two entities with "M" on one end and "N" on the other end.