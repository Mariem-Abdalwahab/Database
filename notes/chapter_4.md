## Enhanced Entity-relationship (EER) Modeling

- Enhanced ⇒ more advanced
- Extended == Enhanced
- Some entity have subgrouping of its
    - Employee ⇒ engineers, secretary….
- **Subclass** ⇒ subgroupings of the entity
- **Superclass** ⇒ the entity it self
- **Local Attribute** ⇒ attribute for one of subclasses
- **Defining (type) Attribute** ⇒ the subclasses created based on it
- Entity of superclass can be in more then subclass
- not every member in superclass be one of subclass

### Specialization

- **Specialization** ⇒ the defining the subclasses of superclass
- Why we do Specialization?
    1. some attributes may not allow to all superclass
    2. some relationship may allow to some of subclass

## Generalization

- **Generalization X Specialization**
- Generalization is the process of extracting common properties from a set of entities and creating a generalized entity from it. It is a bottom-up approach
- collect attributes which common in subclasses to superclass

## Constraints on specialization and generalization

1. Disjointness Constraint 
- Subclasses must be disjoint (or)
- entity member at one subclass only
    - d character
    1. Overlapping Constraint
        - entity member at more than one subclass (and)
        - o character
    
    ![img](/img/4.1.gif)
    


2- **Completeness Constraint X partial Completeness** 

- the superclass must be on of the subclass
- show as double line

### Hierarchy ⇒ subclass has one superclass (single inheritance)

### Lattice ⇒ subclass has more than one superclass (Shared subclass)

![img](/img/4.2.jpg)

---

## Categories (Union of super-classes)

- It is a method to collect super-classes in entity to connect it with other relationship and entities

![img](/img/4.3.png)

- **Shared class** ⇒ share its attributes from all the superclass (intersection between then)