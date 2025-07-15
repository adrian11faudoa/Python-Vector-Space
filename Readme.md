Subject:

A vector is an object that has a length (or magnitude) and a direction and it cannot be expressed by a single number. 
In physics, vectors are commonly used to represent forces, velocities, accelerations, and other quantities.


A vector can be defined by two coordinates, x and y, in the Euclidean plane. 
The distance between the origin of the axes and the point (x, y) will be its length, or norm. 
And the vector direction will point towards (x, y).


Python offers various methods that include both a leading and trailing double underscore in their names. 
You may already be familiar with some, such as __init__ and __str__. 
These methods, which follow the __<name>__ naming pattern, are referred to as special methods, magic methods, or dunder (which stands for double underscore) methods.


Defining special methods in a class affects the behavior of that class. 
They are called under the hood in specific situations 
(e.g. __init__ during instantiation, __str__ when the object is printed or passed to str()).


Inheritance enables you to define a class from an existing one. 
The new class, called child, inherits all the methods and properties of the existing class, called parent.
Example Code:
```
    class Tree:
        def sprout(self):
            print('Making new leaves!')

    class Oak(Tree):
        pass

    Oak().sprout() # Output: Making new leaves!
```
In the example above, the child class Oak inherits from Tree and inherits the sprout method from the parent class Tree.


using the super() function. super() enables you to refer implicitly to the parent class: super().__init__(x, y) calls the __init__ method of the parent class


In Python, you can enforce the use of keyword-only arguments by adding a * as an additional argument to the function or method signature. 
Modify both __init__ methods by adding a * as the second parameter (after self). 
Every parameter placed after that will require the use of a keyword argument in the function/method call.


Every object in Python has a special attribute named __dict__, which is a dictionary that stores the object attributes.


The vars() built-in function takes an object as its argument and returns the __dict__ attribute of that object.


Step 23


























