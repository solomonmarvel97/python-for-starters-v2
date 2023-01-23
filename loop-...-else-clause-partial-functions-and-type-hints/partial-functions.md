# Partial Functions

In Python, a partial is a function that allows you to fix some arguments of another function. This is useful when you need to use a function with a fixed set of arguments in multiple places, but the arguments that you want to fix are not always the same.

For example, suppose you have a function that takes three arguments:

* A partial function returns a new partial object that is callable by another function

Here's an example of how to work with Partial Functions

```python
def multiply(a, b):
    return a*b

def double(a):
    return multiply(a, 2)

result = double(10)
print(result) 
```

#### Using partials from the python in-built functools library

```python
# import partials

# example 1
from functools import partial

def multiply(a, b):
    return a * b

number = 2
partial_function = partial(multiply, number) # creates a partial

result = partial_function(10)
print(result)

# example 2

from functools import partial

def foo(x, y, z):
    return x + y + z
    
foo_with_y_fixed = partial(foo, 5)

print(foo_with_y_fixed(1, 2))  # prints 8
print(foo_with_y_fixed(3, 4))  # prints 12
```

NB: Note that when you create a partial, you need to specify the arguments in the order in which they appear in the original function. If you want to specify arguments by name, you need to use the functools partial method function.
