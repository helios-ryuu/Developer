# Entities
**Entities** are objects or concepts about which data is stored. They represent real-world objects or concepts in a database.
## Entity Set
An **Entity Set** is a collection of similar types of entities. For example, all students in a university form the "Student" entity set.
## Representation
In ER diagrams, entities are represented by rectangles.
## Examples
- **Student**
- **Course**
- **Instructor**
- **Department**
## Entity Attributes
Attributes are properties or characteristics of an entity. They can be categorized as follows:
- **Simple (Atomic)**: Cannot be divided into smaller parts. Example: `StudentID`, `Name`.
- **Composite**: Can be divided into smaller sub-parts. Example: `Address` can be divided into `Street`, `City`, `Zip Code` (e.g., `Address(Street, City, Zip Code)`).
- **Derived**: Attributes that can be derived from other attributes. Example: `Age` can be derived from `DateOfBirth`.
- **Multivalued**: Attributes that can have multiple values. Example: `PhoneNumbers` (e.g., `{PhoneNumbers}`).