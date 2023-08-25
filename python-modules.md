# Python Modules

In Python, a module is a file that contains definitions of functions, classes, and variables, and can be imported into other Python files or programs. Modules are used to organize code and make it more reusable and easier to maintain.

* Using modules is a good way to organize and reuse your code, and it's a common practice in Python programming.

We are going to learn how to import functions from other modules (files) in the following steps:

Create a python file named `circle.py`, then add the following code to the file

```python
# circle module

PI = 3.142

def area_of_a_circle(r):
    """
    Function for computing the area of a circle
    """
    area = PI * r ** 2
    return area

```

Create a python file named `rectangle.py`, then add the following code to the file

```python
# rectangle module

def area_of_a_retangle(l, b):
    """
    Formula for computing the area of a rectangle
    """
    return l * b
```

Now create a new file names `main.py`. This is our main file and our program execution would begin from here.

We will import the circle and rectangle files using the `import` statement

```python
"""
For shorts, a module is simply a python file
The python file can contain classes, functions and even variables

And the classes, functions or variables can be imported to other files
"""


from circle import area_of_a_circle # import area_of_a_circle function
from rectangle import area_of_a_retangle

# called the area of a circle function
print(area_of_a_circle(10))

# called the area of a rectangle function
print(area_of_a_retangle(5, 5))
```

#### Working with module files and subdirectories

When working with multiple directories (folders), accessing your modules would be a quite different approach

* Create a finder directory (folder) within your current directory
* Create a `sayHelloy.py` and `sayHi.py` file.

Within the `sayHi.py`, paste the following code:

```python
def sayHi(name):
    return f'Hi, {name}'
```

Within the `sayHello.py`, paste the following code:

```python
def sayHello(name):
    return f'Hello, {name}'
```

Now, let's access the `sayHello` and `sayHi` functions within those files from our main file using the following block of code:

```python
# import sayHi function
from functions.sayHello import sayHello
from functions.sayHi import sayHi

print(sayHello("Marv"))
print(sayHi("Joy"))
```
