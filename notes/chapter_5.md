## The Relational Data Model and
Relational Database Constraints

- Relation data model ⇒ representation data model
    - has some details user can understand it
    - based in Relation (it mean table of values)
    - Relation based on mathematical concepts and set of rows
    - row include information about entity
    - Row called Tuples in the formal model (DR Codd)
    - Row == Tuple == Record
    - Each column has a column header
    - in the formal model it column == Attribute == Field
    
    ![img](/img/5.1.png)
    

### Key of Relation

- Each row has a unique attribute it called key (SSN)
- In case no unique attribute I will create it and it called **Artificial Key or Surrogate Key**

### Formal Definition

- **Schema**
    - Denoted by R(A1, A2,….. An)
    - R ⇒ relation name
    - A ⇒ attributes of relation
    - Each attribute has a **domain** (set of valid values)
        - the domain of ID is digit numbers

- **Tuple**
    - <…..>
    - <132, “ Mariem ”, “12c street”> ⇒ 3-tuples

- **Domain**
    - domain has a logical definition ⇒ EX: each phone number is a set of 10 digit
    - domain has a data type or a format defined ⇒ (ddd)ddd-dddd each d is a decimal, Date ⇒ yyyy-mm-dd
- **State**
    - r(R) ⇒ dom(A1) X dom (A2)
    - X ⇒ cartesian product
    
    ![img](/img/5.2.png)

    
    - **Relation State**
    
    A Relation state ‘r’ of a relation schema R(A1, A2, A3, …., An), also denoted by **r( R ), is the set of n tuples**.
    
    The relation state represents a relation with all the tuples at any particular point in time.
    
    The relation state of the employee relation at that particular point in time, as shown below.
    

![img](/img/5.3.png)

### **Definition Summary**

![img](/img/5.4.png)

---

## **Characteristics of Relation**

- You don’t have to order tuples in relation
- You don’t have to order attributes in relation
- ti = <v1, v2,….>, r(R) = {t1, t2, t3}
- value in tuples considered to be atomic (indivisible)
- t[Ai] == t.Ai  ⇒ component values of a tuple

## Relation Integrity Constrain

1. **Key** constrain
2. **Entity integrity** constrain
3. **Referential integrity** constrain
4. Domain constrain ⇒ (implicit constrain) NULL or valid
    - **Key constrain**
        1. Super Key (SK) or R ⇒a set of attributes, no two tuples have the same key
        2. **Key**
            1. Key ⇒ it is a minimal SK can’t delete attributes from it
            2. Any key is a super key but not vice versa
            3. Attributes + Key == super key
            - In case have many key you can choose one key to be the primary key ≠ null, primary key smallest size and number
            
            ### Relational Database Schema
            
            It is a set of relation schemas that belong to the same database
            
            S ⇒ the whole database Schema
            
            S = { R1, R2, R3} R ⇒ the individual relation in the schema
            
    - **Entity integrity**
        - Primary key (PK) in R in S can’t have null values in tuple
        - t[PK] ≠ null
        - if PK have several attributes null can’t be one of them
    - **Referential integrity**
        - A constrain involving two relation
        - used to specify a relationship between two tuples
            - referencing relation (employee) and referenced relation (department)
        - t1[FK] == t2[PK]
        - FK can be value of PK in relation two or be Null
        - if it be null the FK can’t be PK in one

## Displaying a relational database schema and its constrains

![img](/img/5.5.png)

### Other constrains can’t be appear in the diagram

- Semantic Integrity constrain
    - hour per employee is 56hr it is expressed by programming language
    - Triggers and Assertion it is a code run when a specific thing happen

Relation state + Relation states + …. == relation database state

# Operation for changing database

- Insert
- Delete
- Modify

![img](/img/5.6.png)

![img](/img/5.7.png)

## Possible violations for each operation

- Insert
    - Domain constrains
    - Key constrains ⇒ exist before
    - Referential integrity
    - Entity integrity ⇒ PK == null
- Delete
    - Referential integrity ⇒ PK deleted when a FK is connected
    - we can handle it RESTRICT, CASCADE, SET NULL
        - RESTRICT: reject deletion
        - CASCADE: delete referenced and referencing relation
        - SET NULL: set FK to NULL
- Modification
    - Domain constrain
    - update PK
    - update FK
    - update an ordinary attribute (not PK, FK)