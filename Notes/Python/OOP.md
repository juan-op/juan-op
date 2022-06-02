# OOP

## Definition
Object-oriented programming (OOP) is a method of structuring a program by bundling related properties and behaviors into individual objects.
# Class
A class is a *blueprint*. When you write a class, you define the general behavior that a whole category of objects can have.

Creating a new class creates a new type of *object*, allowing new *instances* of that type to be made. 

Each class instance can have *attributes* attached to it for maintaining its state. 

Class instances can also have *methods* for modifying its state. 

```python
class ClassName:
    
    # class attribute
    alias = ''
    
    # initializer method
    def __init__(self, a, b, ...):
        # instance attributtes
        self.a = a
        self.b = b
        ...
        
    # method (function inside a class)
    def function(self, ...):
        action
        return
    
    # dunder methods
    def __str__(self): #executed when the object is converted to a string
        action
        return
    
    def __eq__(self, other): #compares two objects
        return self.a = other.a ...
    
# instance
x = ClassName(1, 'Name', 55, ...)
```
# Principles
### Inheritance
One class (*child class*) inherits all of the methods and attributes of another class (*parent class*).

```python
class ParentClass:
    def __init__(self, a, b, ...):
        self.a = a
        self.b = b
        ...

class ChildClass(ParentClass):
    def __init__(self, a, b, c, d, ...):
        super().__innit__(a, b): # we can use the parameters from the parent class.
        self.c = c
        self.d = d
        ...
```

### Polymorphism
Allows us to use a *child class* exactly like his *parent class* but the *child class* mantains its methods as they are.

### Encapsulation
Hiding data of implementation. It prevents outside effects impact the inside code, it restricts the access to elements of the class from outside.

### Abstraction 
An extension of encapsulation. Hiding theinternal implementation details (attributes, functions).

```python
class ClassName:
    
    def __init__(self, a, b):
        self.a = a
        self.b = b
        self._c = c # This keeps the value of c 'protected'
        ///
        self.__c = c # This keeps the value of c 'private'    
```