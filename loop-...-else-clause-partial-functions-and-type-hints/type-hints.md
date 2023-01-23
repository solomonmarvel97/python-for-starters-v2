# Type Hints

Type hints in Python are a way to specify the expected type of function's arguments and return value. They are a form of documentation that can be used to help developers understand and use the code, and they can also be used by static type checkers to detect type errors in the code.

They are completely optional and are not used by the interpreter to enforce any type checking. Instead, they are mainly used as a form of documentation to help other developers understand the code.

* Python’s type hints provide you with optional static typing to leverage the best of both static and dynamic typing.

Here's an example of type annotations in your python code:

```python
"""
The type descriptions are optional but it makes it 
easier for other developers to read your code and 
understand the types that you're working with
"""

name: str = "Marvelous"
number: int = 10

# using types to descript the parameter types and the function return type
def say_hi(name: str) -> str:
    return f'Hi {name}'

greeting = say_hi('Emanuella')
print(greeting)
```

Type annotations can be especially useful when working with large codebases or when collaborating with other developers. They can help to make the code more self-explanatory and easier to understand.

It's worth noting that type annotations are a relatively recent addition to Python (introduced in Python 3.0). Prior to the introduction of type annotations, developers used comments or documentation strings to describe the expected types of variables and expressions.
