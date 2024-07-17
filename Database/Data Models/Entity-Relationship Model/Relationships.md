## [[Types of Relationships]]
1. **One-to-One (1:1)**
    - **Definition**: A single entity in one entity set is associated with a single entity in another entity set.
    - **Example**: Each student has one unique student ID card, and each card is assigned to one student.
    - **Representation**: A line connecting two entities with "1" on both ends.
2. **One-to-Many (1)**
    - **Definition**: A single entity in one entity set is associated with multiple entities in another entity set.
    - **Example**: One instructor teaches many courses, but each course is taught by one instructor.
    - **Representation**: A line connecting two entities with "1" on one end and "N" on the other end.
3. **Many-to-One (N:1)**
    - **Definition**: Multiple entities in one entity set are associated with a single entity in another entity set.
    - **Example**: Many students are advised by one advisor, but each student has only one advisor.
    - **Representation**: A line connecting two entities with "N" on one end and "1" on the other end.
4. **Many-to-Many (M)**
    - **Definition**: Multiple entities in one entity set are associated with multiple entities in another entity set.
    - **Example**: Students enroll in many courses, and each course has many students.
    - **Representation**: A line connecting two entities with "M" on one end and "N" on the other end.
## [[Relationship Constraints]]
1. **Cardinality Constraints**
    - Specifies the number of instances of one entity that can or must be associated with each instance of another entity.
    - Types: One-to-One, One-to-Many, Many-to-One, Many-to-Many.
2. **Participation Constraints**
    - Specifies whether all or only some entity instances participate in a relationship.
    - **Total Participation**: Every instance of the entity must participate in the relationship (e.g., every student must enroll in at least one course).
    - **Partial Participation**: Some instances of the entity may not participate in the relationship (e.g., some instructors may not be teaching any courses).