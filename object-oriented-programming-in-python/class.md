# Class

## Class keyword

In our previous example, we saw the python types were all built-in objects of the Python programming language. The user defined objects are created using the `class keyword`. The class is a blueprint that defines a nature of a future object. From classes, we construct instances. An instance is a specific object created from a particular `class`. For example, `Huck` might be an instance of a `Dog class`.

```python
class First:
    pass

fr = First()

print(type(fr))
print(type(First))
```

This is our first class. The body of the class is left empty for now. It is a convention to give classes a name that starts with a capital letter.

```python
class First:
    pass
```

Here we define the First class. Note that by default, all classes inherit from the base object.

```python
fr = First()
```

Here we see that `fr` is an instance object of the First class.

Inside a `class`, we can define attributes and methods. An attribute is a characteristic of an object. This can be for example a salary of an employee. A method defines operations that we can perform with our objects. A method might define a cancellation of an account.

Technically, attributes are variables and methods are functions defined inside a class.

#### Object initialization

A special method called `__init__` is used to initialize an object.

```python
# object_initialization.py

class Being:
    def __init__(self): # this initialises our object
        print("Being is initialized")

Being()
```

#### Python Object Attributes

Attributes are characteristics of an object. Attributes are set in the `__init__` method.

```python
class Cat:
    def __init__(self, name):
        self.name = name

missy = Cat('Missy')
lucky = Cat('Lucky')

print(missy.name)
print(lucky.name)
```

In this code example, we have a `Cat class`. The special method `__init__` is called automatically right after the object has been created.

```python
def __init__(self, name):
```

Each method in a class definition begins with a reference to the instance object. It is by convention named self. There is nothing special about the self name. We could name it this, for example. The second parameter, name, is the argument. The value is passed during the class initialization.

```python
self.name = name
```

Here we pass an attribute to an instance object.

```python
missy = Cat('Missy')
lucky = Cat('Lucky')
```

Here we create two objects: cats Missy and Lucky. The number of arguments must correspond to the `__init__` method of the class definition. The 'Missy' and 'Lucky' strings become the name parameter of the `__init__` method.

```python
print(missy.name)
print(lucky.name)
```

The attributes can be assigned dynamically, not just during initialization. This is demonstrated by the next example.

```python
class Person:
    pass

p = Person()
p.age = 24
p.name = "Peter"

print("{0} is {1} years old".format(p.name, p.age))
```

#### Python Class Attributes

So far, we have been talking about instance attributes. In Python there are also so-called class object attributes. Class object attributes are same for all instances of a class.

```python
class Cat:
    species = 'mammal' # this is a class attribute
    def __init__(self, name, age):
        self.name = name
        self.age = age

missy = Cat('Missy', 3)
lucky = Cat('Lucky', 5)

print(missy.name, missy.age)
print(lucky.name, lucky.age)

print(Cat.species)
print(missy.__class__.species)
print(lucky.__class__.species)
```

In our example, we have two cats with specific `name` and `age` attributes. Both cats share some characteristics. Missy and Lucky are both mammals. This is reflected in a class level attribute species. The attribute is defined outside any method name in the body of a class.

```python
print(Cat.species)
print(missy.__class__.species)
```

There are two ways how we can access the class object attributes: either via the name of the `Cat class`, or with the help of a special `__class__` attribute.

Executing the code block above gives us this result:

```bash
Missy 3
Lucky 5
mammal
mammal
mammal
```
