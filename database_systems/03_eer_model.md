# Enhanced Entity-Relationship (EER) Model (增强实体关系模型)

Also known as the Extended Entity-Relationship Model, the EER model extends the traditional ER model by introducing additional concepts to better represent complex data relationships and structures.

**Additional concepts include:**
- Subclasses and Superclasses
- Specialization and Generalization
- Attributes and Relationships
- Constraints
- Object-oriented concepts

---

## Subclasses and Superclasses (子类和超类)

### Subclasses (子类)

A **subclass** is a subset of an entity set, containing entities with specific attributes or relationships that distinguish them from others in the set. The relationship between a subclass and its superclass is represented by the "is-a" relationship.

#### Symbols

- A circle connects the superclass to its subclasses:
    ```
                    --)-- SECRETARY
    EMPLOYEE == (d) --)-- MANAGER
                    --)-- ENGINEER
    ```
    - `d` in the circle: subclasses are **disjoint** (an entity can belong to only one subclass).
    - `o` in the circle: subclasses **overlap** (an entity can belong to more than one subclass).
- Triangles may also represent the "is-a" relationship.

### Inheritance (继承)

**Inheritance** allows a subclass to inherit attributes and relationships from its superclass.

### Superclasses (超类)

A **superclass** is a generalization of one or more subclasses, representing a higher-level entity with shared attributes or relationships.

---

## Specialization and Generalization

### Specialization (特化)

**Specialization** is the process of defining a set of subclasses from a superclass based on distinguishing characteristics.

### Generalization (泛化)

**Generalization** is the process of defining a superclass from a set of subclasses based on common attributes or relationships. Multiple subclasses can be generalized into a single superclass.

---

### Complete and Partial Specialization

- **Complete Specialization**: Every entity in the superclass must belong to at least one subclass (`must`).
- **Partial Specialization**: Some entities in the superclass may not belong to any subclass (`can`).

#### Symbols

- **Complete Specialization**: Double line connects the superclass and its subclasses.
- **Partial Specialization**: Single line connects the superclass and its subclasses.

# Attribute and Relationship

# Constraints

# Object-oriented concepts