# Recursive Functions

### [Recursive Functions in python](broken-reference) <a href="#recursive-functions-in-python" id="recursive-functions-in-python"></a>

In Python, a recursive function is a function that calls itself. Recursive functions can be used to solve problems that can be broken down into smaller problems of the same type.

Here is an example of a simple recursive function in Python that calculates the factorial of a number:

```
def factorial_example(n):
    if n == 1:
        return 1
    else:
        return (n * factorial_example(n-1))
factorial_example(5)
```

