# Using Global Variables in Functions

### Python For Starters

### [Python working with global variables](broken-reference) <a href="#python-working-with-global-variables" id="python-working-with-global-variables"></a>

In Python, a global variable is a variable that is defined outside any function or class, and can be accessed from anywhere in the program. Global variables can be useful for storing values that need to be shared across different parts of your program.

Here is an example of how to define and access a global variable in Python:

```
# Referencing a global variable inside a function
count = 1
def func():
    """
    This function would increament the value of count by 1
    Basically we just added 1 to the count variable
    """

    # specifies that we might change the value of count

    global count 
    count += 1
    return count

print(func.__doc__)
```

* When working with a global variable inside a function, we have to use the `global` keyword to reference the global variable to specify that we want to modify the global variable

