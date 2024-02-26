## Mapping ER Model to relational model

## Steps from EER ⇒ schema

- Option of mapping specialization or generalization
    - Multiple relations for super-classes and subclasses
        
        Subclass attributes → local attribute and PK superclass only
        🎯 all constrain is ok
        
        ![img](/img/7.1.png)
        
        ![img](/img/7.2.png)
        
    - Multiple relations for subclasses
        
        Subclass attributes → local attribute and all superclass attributes
        🎯 Disjoint and total
        
        ![img](/img/7.3.png)
        
        ![img](/img/7.4.png)
        
    - Single relation (to sub and super) with one type attribute
        
        🎯Disjoint
        
        ![img](/img/7.5.png)
        
        ![img](/img/7.6.png)
        
        ![img](/img/7.7.png)
        
    - Single relation with multiple type attributes
        PK + all attribute from sub and type attribute
         type attribute it is a boolean value
        🎯 overlapping  

        ![img](/img/7.8.png)

        ![img](/img/7.9.png)
