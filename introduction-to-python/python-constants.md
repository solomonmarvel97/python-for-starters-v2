# Python constants

### Python For Starters

#### [Constants](broken-reference) <a href="#constants" id="constants"></a>

In Python, a constant is a variable whose value remains unchanged throughout the program. Constants are usually defined in all capital letters so that they can be easily identified.

In Python, there is no built-in support for constants. However, you can define constants in your program by assigning a value to a variable and then not changing the value of the variable.

Here is an example of how to define and use constants in Python:

```
"""
Constants -> Python doesn't support constants, 
but we use the uppercase letters to show 
that it is a constant
"""

WEBSITE_HOST = 'https://solomonmarvel.com'

print(WEBSITE_HOST)


# code example

PI = 3.14159265

def calculate_area(radius):
  return PI * radius * radius

radius = 10
area = calculate_area(radius)
print(f"The area of a circle with radius {radius} is {area}")
```

