# Enhanced Entity-Relationship (EER) Model(增强实体关系模型)
Also named Extended Entity-Relationship Model.
The EER model is an extension of the traditional ER model that includes additional concepts to better represent complex data relationships and structures.
Additional concepts include:
- Subclasses and Superclasses
- Specialization and Generalization
- Attribute and Relationship
- Constraints
- Object-oriented concepts
# Subclasses and Superclasses(子类和超类)
## Subclasses(子类)
A subclass is a subset of an entity set. It contains entities that have some specific attributes or relationships that distinguish them from other entities in the entity set.
We use the "is-a" relationship to represent the relationship between a subclass and its superclass.
## Symbols
We use a circle to connect the superclass and its subclasses.
```
EMPLOYEE == (d) --)-- MANAGER
                --)-- ENGINEER
```
- The `d` in the circle indicates that the subclasses are disjoint, meaning an entity can belong to only one subclass.
- If the subclasses are not disjoint, we use `o` in the circle to indicate that an entity can belong to more than one subclass.
## Inheritance(继承)
Inheritance is a mechanism that allows a subclass to inherit attributes and relationships from its superclass.
## Superclasses(超类)
A superclass is a generalization of one or more subclasses. It represents a higher-level entity that shares common attributes or relationships with its subclasses.

# Specialization and Generalization
## Specialization(特化)
Specialization is the process of defining a set of subclasses from a superclass based on some distinguishing characteristics.
## Generalization(泛化)
Generalization is the process of defining a superclass from a set of subclasses based on common attributes or relationships.
Several subclasses can be generalized into a single superclass.
# Attribute and Relationship

# Constraints

# Object-oriented concepts