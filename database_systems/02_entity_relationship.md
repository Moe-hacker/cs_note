# Entity-Relationship Model (实体-关系模型)

The Entity-Relationship (ER) model is a high-level conceptual data model used to represent the structure of a database. It provides a graphical way to visualize the relationships between entities in a system.

## Main Components

- **Entity (实体):** A distinct object or concept in the system, represented as a rectangle in the ER diagram. Entities can be physical objects (e.g., a car) or abstract concepts (e.g., a course).
- **Attribute (属性):** A property or characteristic of an entity, represented as an oval connected to its entity. For example, a "Person" entity may have attributes such as "Name," "Age," and "Address."
- **Relationship (关系):** An association between two or more entities, represented as a diamond in the ER diagram. Relationships can have attributes of their own and can be classified as one-to-one, one-to-many, or many-to-many.
- **Cardinality (基数):** Describes the number of instances of one entity that can be associated with instances of another entity in a relationship. Common cardinalities include:
  - **One-to-One (1:1):** Each instance of Entity A is associated with one instance of Entity B, and vice versa.
  - **One-to-Many (1:N):** Each instance of Entity A can be associated with multiple instances of Entity B, but each instance of Entity B is associated with only one instance of Entity A.
  - **Many-to-Many (M:N):** Instances of Entity A can be associated with multiple instances of Entity B, and vice versa.
- **Primary Key (主键):** A unique identifier for each instance of an entity, represented as an underlined attribute in the ER diagram. The primary key ensures that each entity instance can be uniquely identified.
- **Foreign Key (外键):** An attribute in one entity that refers to the primary key of another entity, establishing a relationship between the two entities.

The ER model is widely used in database design to create a clear and organized representation of the data structure, which can then be translated into a relational database schema.

# Notation (符号)

The ER model uses specific symbols to represent its components in diagrams:

- **Box (矩形):** Represents an entity.
- **Double Box (双矩形):** Represents a weak entity, which cannot be uniquely identified by its own attributes alone and relies on a related strong entity.
- **Oval (椭圆):** Represents an attribute of an entity or relationship.
- **Underlined Oval (下划线椭圆):** Represents a primary key attribute.
- **Double Oval (双椭圆):** Represents a multivalued attribute, which can have multiple values for a single entity instance.
- **Diamond (菱形):** Represents a relationship between entities.
- **Double Diamond (双菱形):** Represents an identifying relationship, which connects a weak entity to its related strong entity.
- **Dotted Oval (虚线椭圆):** Represents a derived attribute, which can be calculated from other attributes.
- **Lines (线):** Connect entities to their attributes and relationships, indicating associations.

# Entity-Relationship Diagram (ER图)

An Entity-Relationship Diagram (ERD) is a visual representation of the ER model, illustrating the entities, attributes, and relationships within a system. ERDs are used in database design to help visualize the structure of the data and how different entities interact with each other.

## Key Components of an ERD

- **Entities:** Represented as rectangles, entities are the main objects or concepts in the system.
- **Attributes:** Represented as ovals, attributes provide additional information about entities and relationships.
- **Relationships:** Represented as diamonds, relationships show how entities are connected and interact with each other.
- **Cardinality:** Indicated by symbols near the relationship lines, cardinality specifies the number of instances of one entity that can be associated with instances of another entity.
- **Primary Keys:** Underlined attributes that uniquely identify each instance of an entity.
- **Foreign Keys:** Attributes that reference the primary key of another entity, establishing relationships between entities.

ERDs can be created using various tools and software, and they serve as a blueprint for designing and implementing a database. They help ensure that the database structure is well-organized, efficient, and meets the requirements of the system being modeled.

# Crow's Foot Notation (乌鸦脚符号)

Crow's Foot Notation is a popular way to represent the cardinality of relationships in ER diagrams. It uses specific symbols at the ends of relationship lines to indicate the nature of the relationship:

- A single line (`—`) indicates "one."
- A crow's foot (three prongs, `<`) indicates "many."
- A circle (`O`) indicates "zero" (optional).
- A vertical line (`|`) indicates "one" (mandatory).