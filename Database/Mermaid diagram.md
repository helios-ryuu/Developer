1. **Diagram Type Declaration**
    - **Syntax**: `graph <DiagramType>;` or `erDiagram;`
    - **Explanation**: This declares the type of diagram you are creating. For example, `graph TD;` is used for flowcharts, while `erDiagram;` is used for entity-relationship diagrams (ERD).
    
1. **Entities**
    - **Syntax**: `<EntityName> { <Attributes> }`
    - **Explanation**: Entities are represented by their names followed by attributes enclosed in curly braces `{}`. Attributes are typically listed with their data types.
    
3. **Relationships**
    - **Syntax**: `<EntityName> ||--o{ <RelatedEntityName> :<RelationshipDescription>`
    - **Explanation**: Relationships between entities are indicated by connecting lines (`||`, `--`, `-o`, `-|`, `-x`) and arrows (`{`, `}`, `<`, `>`). The type of relationship (one-to-one, one-to-many, many-to-many) can be implied by the arrows and connectors used.
    
4. **Attributes**
    - **Syntax**: `<DataType> <AttributeName>`
    - **Explanation**: Attributes of entities are listed inside the curly braces `{}` following the entity name. Each attribute is described with its data type and name.
    
5. **Example**: 
```markdown
```erDiagram
    CUSTOMER ||--o{ ORDER : places
    ORDER ||--|{ LINE-ITEM : contains
    CUSTOMER {
        string name
        string address
        string phone
    }
    ORDER {
        int orderId
        string orderDate
        int customerId
    }
    LINE-ITEM {
        int lineItemId
        int orderId
        int productId
        int quantity
    }
```

6. **Explanation of the Example**:
- **`erDiagram`**: Declares that this is an entity-relationship diagram.
- **Entities and Relationships**:
    - `CUSTOMER` and `ORDER` are entities.
    - `CUSTOMER ||--o{ ORDER` indicates a relationship where `CUSTOMER` places `ORDER`.
    - `ORDER ||--|{ LINE-ITEM` indicates a relationship where `ORDER` contains `LINE-ITEM`.
- **Attributes**:
    - Inside each entity (`CUSTOMER`, `ORDER`, `LINE-ITEM`), attributes are listed with their data types (`string`, `int`).
    - For example, `CUSTOMER` has attributes `name`, `address`, and `phone`.