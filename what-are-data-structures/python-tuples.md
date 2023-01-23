# Python Tuples

In Python, a tuple is an immutable sequence type. This means that once you create a tuple, you can not change the values it contains: you can not add, remove, or modify the values of the elements in the tuple.

You can also use the `len()` function to get the length of a tuple, and the in operator to check if an element is in a tuple.

#### Creating a tuple

Tuples are defined using parentheses, with the elements separated by commas.

This is an example of a tuple:

```python
names = ("john", "mark", "marrieth")
print(names)
```

#### Accessing Values in tuples

We can access the values of a tuple by using the square bracket and the index as found in the example below:

```python
names = ("john", "mark", "marrieth")
print(names[0])
```

#### Iterating through a tuple

A tuple is an iterable, this means that we can iterate through the values of a tuple using same pattern as we have seen in lists.

This is an example of how to iterate within a tuple

```python
names = ("john", "mark", "marrieth")
for name in names:
    if name == "Abraham":
        print('Abraham was found')
    print("{} is a name".format(name))
```

#### Returning tuples from function

Tuples are often used to return multiple values from a function, since they allow you to return multiple values in a single return statement.

```python
def get_user():
  name = 'John'
  age = 40
  return name, age

person = get_user()
print(person)  # Output: ('John', 40)

# You can also unpack the tuple into separate variables
name, age = get_user()
print(name)  # Output: 'John'
print(age)   # Output: 40
```
