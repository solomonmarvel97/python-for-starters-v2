# Object Oriented Programming in Python

Object-oriented programming (OOP) is a programming paradigm that is based on the concept of "objects", which can contain data and code that manipulates that data. In Python, everything is an object and each object has a type, called a class.

In object-oriented programming, you define classes to represent the types of objects you want to manipulate, and you create objects that are instances of those classes. Each object has its own set of attributes (data) and behaviors (methods). For example, you might define a Dog class with attributes like name, breed, and age, and behaviors like bark() and fetch(). You could then create individual dog objects that represent specific dogs, like a dog1 object with a name attribute of "Fido" and a breed attribute of "Labrador".

In Python, you define a class using the class keyword, followed by the name of the class and a colon. The body of the class is indented and typically contains a series of methods (functions that are defined within the class). Here's an example of a simple Dog class:

```python
class Dog:
    def __init__(self, name, breed, age):
        self.name = name
        self.breed = breed
        self.age = age

    def bark(self):
        print("Woof!")

dog1 = Dog("Fido", "Labrador", 3)
print(dog1.name)  # Output: "Fido"
dog1.bark()  # Output: "Woof!"
```

In this example, the `__init__` method is a special method in Python that is called when an object is created. It initializes the attributes of the object. The `self` parameter is a reference to the current object, and is used to access the attributes and methods of the object.

The `bark()` method is a simple method that prints the string "Woof!". To call a method on an object, you use the dot notation, like object.method().

I hope this helps to give you a basic understanding of object-oriented programming in Python! Let me know if you have any questions.

#### There are some basic programming concepts in OOP:

* `Abstraction` is simplifying complex reality by modeling classes appropriate to the problem.
* `Polymorphism` is the process of using an operator or function in different ways for different data input.
* `Encapsulation` hides the implementation details of a class from other objects.
* `Inheritance` is a way to form new classes using classes that have already been defined.

At the basic level, everything in Python is an object. Objects are basic building blocks of a Python OOP (Object-oriented Programming) program.

```python
import sys

print(type(1))
print(type(""))
print(type([]))
print(type({}))
print(type(()))
print(type(object))
print(type(function))
print(type(sys))
```

In this example we show that all these entities are in fact objects. The type function returns the type of the object specified when we run the code block.

```bash
<class 'int'>
<class 'str'>
<class 'list'>
<class 'dict'>
<class 'tuple'>
<class 'type'>
<class 'function'>
<class 'module'>
```

_Integers, strings, lists, dictionaries, tuples, functions, and modules are Python objects._
