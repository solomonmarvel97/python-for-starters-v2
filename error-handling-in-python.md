# Error handling in Python

Error handling is an important part of writing Python programs. It allows you to catch and handle errors and exceptions that may occur in your program, so that it can continue to run smoothly.

There are several ways to handle errors in Python. One of the most common is to use the `try` and `except` statements. Here's an example of how you might use these statements:

```python
try:
    # some code here
except SomeException:
    # code to handle the exception
```

The `try` block contains the code that might throw an exception. If an exception is raised while this code is being executed, the program will jump to the `except` block and execute the code there. If no exception is raised, the `except` block is skipped.

You can also specify multiple exceptions to catch by separating them with a comma, like this:

```python
try:
    # some code here
except SomeException, AnotherException:
    # code to handle the exception
```

You can also use the `finally` block to specify code that should be executed whether an exception is raised or not. This is often used to clean up resources that were being used, such as closing a file or database connection.

```python
try:
    # some code here
except SomeException:
    # code to handle the exception
finally:
    # clean up code
```

You can also raise your own exceptions using the `raise` statement. This is useful when you want to signal that something has gone wrong in your program, and you want to stop execution.

```python
if some_condition:
    raise SomeException("An error occurred")
```

#### Try ... Catch Example

Here's a typical example of how try and except can be used in Python:

```python
number = 10
name = "John"

print(name)

try:
    print(str(number) + name)
    print(name/number)
except Exception as e:
    print(e)

age = 40
print(age + number)
```

#### Try ... Catch ... Finally Example

```python
joy = "Joy"
ella = "Emmanuella"

try:
    value = len(joy)/ella # this will throw an error
    print(value)
except Exception as e:
    print("Error: ", e)
    value = len(joy)/len(ella)
    print("Error resolution" + " " + str(value))
finally:
    print("Finally, We implemented error handling here")
```

#### Try ... Catch ... else Example

In Python, the `try` and `except` statements are used to handle exceptions, which are runtime errors that can occur when executing a program. The `try` block contains code that may throw an exception, and the `except` block contains code that will be executed if an exception is thrown.

The `else` clause is optional and is used to specify a block of code that should be executed only if the `try` block **does not throw an exception**

```python
try:
    value = len(joy)/ella # this will throw an error
    print(value)
except Exception as e:
    print("Error: ", e)
    value = len(joy)/len(ella)
    print("Error resolution" + " " + str(value))
else:
    print("This would print if there's no error")
```
