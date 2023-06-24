# Lambda Functions

### [Working with lambda functions](broken-reference) <a href="#working-with-lambda-functions" id="working-with-lambda-functions"></a>

In Python, a lambda function is a small anonymous function. It can take any number of arguments, but can only have one expression. Lambda functions are useful when you need a simple function for a short period of time. They are not meant to be used as standalone functions and are not as flexible as regular functions.

The syntax for a lambda function is:

```
lambda arguments: expression
```

This is an example of a lambda function to multiply two numbers:

```
add = lambda a,b : a * b
print(add(5,5))
```

[**There are several scenarios where lambda functions can be useful in Python:**](broken-reference)

* When you need a small anonymous function for a short period of time.
* When you want to pass a function as an argument to another function (e.g. as a callback).
* When you want to define a function inline (i.e. within another function).
* As a way to avoid creating a function with a def statement when the function is only going to be used once.

