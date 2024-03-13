[[Inheritance Summary]]
Terminology
- Parent class
- Super class
- Base class
- Child class
- Subclass
- Derived class
**Inheritance** 
- inheritance is how you can relate two classes together
- two similar classes that differ in their degree of specialization
- attributes aren't copied down into the subclasses, but the interest is 
```python
class Parent:
    def __init__(self, param):
        self.v1 = param
    
class Child(Parent):
    def __init__(self, param):
        self.v2 = param
obj = Child(11)
print(obj.v1 + " " + obj.v2)
# Error
```
```python
class Fruit:
    pass
class Orange(Fruit):
    has_pulp = True
    def squeeze(self):
        return has_pulp
print(Orange().squeeze())
```
This would return Error because you have to do self.has_pulp
**Composition** is when one object has another object as an attribute
Inheritance is best for representing is-a relationship 
CheckingAccount is a specific type of Account
CheckingAccount would inherit from Account
Composition is for representing has-a relationships
Bank has a collection of bank accounts that it manages
So a bank has a list of accounts as an attributes
![[Screenshot 2024-03-04 at 4.21.53 PM.png]]
