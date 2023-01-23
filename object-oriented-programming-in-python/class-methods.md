# Class Methods

Methods are functions defined inside the body of a class. They are performed operations with the attributes of our objects.

Methods are essential in the encapsulation concept of the OOP paradigm. For example, we might have a connect method in our `ConnectDatabase` class. We need not be informed how exactly the method connects to the database. We only know that it is used to connect to a database. This is essential in dividing responsibilities in programming, especially in large applications.

```python
# methods.py

class Circle:
    pi = 3.141592
    def __init__(self, radius=1):
        self.radius = radius

    def area(self):
        return self.radius * self.radius * Circle.pi

    def setRadius(self, radius):
        self.radius = radius

    def getRadius(self):
        return self.radius

c = Circle()

c.setRadius(5)
print(c.getRadius())
print(c.area())
```

In the code example, we have a `Circle class`. We define three new methods.

```python
def area(self):
    return self.radius * self.radius * Circle.pi
```

The area method returns the area of a circle.

```python
def setRadius(self, radius):
    self.radius = radius
```

The `setRadius` method sets a new value for the radius attribute.

```python
def getRadius(self):
    return self.radius
```

The `getRadius` method returns the current radius.

```python
c.setRadius(5)
```

The method is called on an instance object. The `c` object is paired with the self parameter of the class definition. The number `5` is paired with the radius parameter.

```bash
$ ./methods.py 

5
78.5398
```

In Python, we can call methods in two ways. There are bounded and unbounded method calls.

```python
# bound_unbound_methods.py

class Methods:
    def __init__(self):
        self.name = 'Methods'

    def getName(self):
        return self.name

m = Methods()

print(m.getName())
print(Methods.getName(m))
```

In this example, we demonstrate both method calls.

```python
print(m.getName())
```

This is the bounded method call. The Python interpreter automatically pairs the `m` instance with the self parameter.

```python
print(Methods.getName(m))
```

And this is the unbounded method call. The instance object is explicitly given to the `getName` method.

```bash
$ ./bound_unbound_methods.py 
Methods
Methods
```
