# Data Hierarchy (数据层次)

Data hierarchy describes how data is organized in a database, typically in a tree-like structure with multiple abstraction levels:

- **Bit (比特)**: The smallest unit of data, representing a binary value (0 or 1).
- **Byte (字节)**: Consists of 8 bits, representing a character or small integer.
- **Field (字段)**: A single piece of data within a record, representing an attribute.
- **Record (记录)**: A collection of related fields, representing an entity.
- **File (文件)**: A collection of related records, forming a dataset.
- **Database (数据库)**: A collection of related files, representing a complete information system.

Understanding the data hierarchy is fundamental for designing efficient databases and maintaining data integrity.

# Data Entities, Attributes, and Relationships (数据实体、属性和关系)

- **Entity (实体)**: A real-world object or concept that can be uniquely identified, such as a person, place, event, or object. In databases, entities are usually represented as tables.
- **Attribute (属性)**: A property or characteristic of an entity, represented as columns in a table. For example, a "Person" entity may have attributes like "Name," "Age," and "Address."
- **Relationship (关系)**: An association between two or more entities, defining how they interact. Relationships are often implemented using foreign keys or junction tables.

# Data Models (数据模型)

A data model is a conceptual framework that defines how data is structured, stored, and manipulated in a database. Common data models include:

- **Hierarchical Model (层次模型)**: Organizes data in a tree structure with parent-child relationships. Each parent can have multiple children, but each child has only one parent.
- **Network Model (网状模型)**: Similar to the hierarchical model but allows more complex relationships, where a child can have multiple parents.
- **Relational Model (关系模型)**: Structures data into tables (relations) with rows (tuples) and columns (attributes). Relationships are established using primary and foreign keys.
- **Object-Oriented Model (面向对象模型)**: Represents data as objects that encapsulate both data and behavior, supporting inheritance and complex data structures.