## **[[Internal Level (Physical Level)]]**
This is the lowest level of abstraction<sup>trừu tượng</sup> and deals with how the data is physically stored in the database. It focuses on the technical details of data storage, indexing, and access methods. It involves:
- **Storage Management**: Determining how data will be stored on the physical medium (e.g., hard drives, SSDs).
- **Data Structures**: Choosing the right data structures (e.g., B-trees, hash tables) for efficient storage and retrieval.
- **Indexing**: Deciding on the types of indexes needed to speed up data retrieval.
- **Access Methods**: Choosing between sequential access or random access based on how the data will be used.
- **File Organization**: Organizing data into files and determining the placement of these files.
- **DBMS Administration**: This level is primarily the concern of database administrators (DBAs) who manage the technical aspects of storage.
## **[[Conceptual Level (Logical Level)]]**
This level describes what data is stored in the database and the relationships among those data. It focuses on the logical structure and relationships of the data without concern for how it is physically stored. It involves:
- **Data Types**: Defining the various types of data that need to be stored (e.g., integers, strings, dates).
- **Relationships**: Establishing the relationships between different data entities (e.g., customers and orders).
- **Schema Design**: Creating a logical schema that represents the entire database structure without considering how data will be stored physically.
- **Data Integrity**: Ensuring that data relationships and constraints (e.g., primary keys, foreign keys) are maintained.
- **DBMS Independence**: This level abstracts the physical details from the users and application programmers.
## **[[External Level (User View)]]**
This is the highest level of abstraction and is concerned with how the data is viewed by individual users or specific application programs. It focuses on how users and applications interact with the database, providing customized views and access controls. It involves:
- **User Interfaces**: Providing different views of the database for different users or user groups.
- **Customized Views**: Allowing users to see only the data they are interested in and hide the rest.
- **Application Programs**: Supporting the specific requirements of various applications by providing appropriate views.
- **Access Control**: Implementing security measures to ensure that users can only access the data they are authorized to see.