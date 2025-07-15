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


When you need to dynamically access some attributes starting from a string input, the built-in getattr() function is what you need. 
It takes an object as its first argument, and a string containing the attribute name as its second attribute.


the __repr__ method is supposed to return the string needed to instantiate the object


You can access the name of a class with __class__.__name__


The __repr__ method is called under the hood by the repr function.


The __getattribute__ method is called under the hood any time you try to access an instance attribute. 
If the attribute is not found at the instance level, the method will search for it at the class level, and eventually in parent classes.


The default implementation of __getattribute__ is to raise an AttributeError when the requested attribute is not an instance attribute or it is not present in the class tree.

__getattr__ is called if defined by the class. You can consider it as a sort of fallback when the usual attribute accessing procedure fails.


The special method __add__ can be implemented to override what happens by default when two objects are added together using the + operator.

The other parameter of your __add__ method represents the operand placed at the right side of the + operator in an addition operation.
Example Code:
```
    def __add__(self, other):
        pass
```     


In Python, NotImplemented is a special value used to indicate that an operation is not implemented for a specific case.

NotImplemented does not raise an exception immediately. Instead, it signals to ask to the other operand how to perform the operation. 
If the request cannot be satisfied, a TypeError is returned by default.


You can unpack a dictionary into keyword arguments by using the ** operator:
Example Code:
```
    def spam(a, b):
        return a + b

    my_dict = {a: 11, b: 4}

    spam(**my_dict) # 15
```


In the same way __add__ is called under the hood when two objects are added together, 
the __sub__ method is called implicitly in case of subtraction.


The special method __mul__ can be implemented to specify what should happen when the current instance is multiplied by another object.


The __eq__ method can be implemented to specify what should happen in case the comparison operator (==) is used to compare an object with something else.


he __ne__ method is called under the hood when the != operator is used. 


The __lt__ method is called under the hood when the < operator is used to compare an object with something else.


The __gt__ method is called under the hood when the > operator is used to compare an object with something else.


The __le__ method is called when the <= operator is used to compare two objects.


The __ge__ method is called when the >= is used to compare two objects.


