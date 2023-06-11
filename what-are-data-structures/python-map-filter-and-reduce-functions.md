# Python Map, Filter & Reduce Functions

### Python Map Function

The `map()` function in Python is a built-in function that applies a function to each element of an iterable (such as a list, tuple, or string) and returns a new iterator with the transformed elements.

The `map()` function has the following syntax:

```python
map(function, iterable)
```

This is an example of a list transformation using the `map()` function:

```python
numbers = [1, 2, 3, 4, 5]
# Map (map(function, list))
# block of code to add 10 to each value in our list

result = map(lambda item: item + 10, numbers)
print(list(result))
```

> The `map()` function is a convenient way to apply a function to many elements in an iterable. It is often used to transform or filter the elements of a list or other iterable object.

#### Python Filter Function

The `filter()` function in Python is a built-in function that takes an iterable and a function as input, and returns an iterator with the elements that return True when passed to the function.

The `filter()` function has the following syntax:

```python
filter(function, iterable)
```

This is an example of a list transformation using the `filter()` function:

```python
numbers = [1, 2, 3, 4, 5]
# Filter (filter(function, list))
# write a python code to filter the items that are divisible by 2

result = filter(lambda item: item % 2 == 0, numbers)
print(list(result))
```

> The filter() function is a convenient way to select specific elements from an iterable based on a certain condition. It is often used to filter lists or other iterable objects to create new lists with only the elements that satisfy a certain criterion.

#### Python Reduce Function

The `reduce()` function in Python is a built-in function that applies a function to an iterable in a cumulative manner to reduce the iterable to a single value. It is a part of the functools module, so you need to import it before you can use it.

The reduce() function has the following syntax:

```python
reduce(function, iterable, initializer=None)
```

The `reduce()` function is a function that takes in two arguments and returns a single value. The `'iterable'` is an `iterable` object, such as a list, tuple, or string. The `initializer` is an optional argument that specifies an initial value to be used in the reduction. If the `initializer` is not provided, the `reduce()` function will use the first element of the `iterable` as the initial value.

This is an example of a list transformation using the `reduce()` function:

```python
numbers = [1, 2, 3, 4, 5]
# Reduce (reduce(function, list))
# we use the reduce function to reduce a list into a single value

from functools import reduce

result = reduce(lambda a, b: a + b , numbers)
print(result)
```

> The `reduce()` function is a useful tool for performing a cumulative operation on an iterable object. It can be used to perform a wide variety of tasks, such as calculating the sum or product of a list of numbers, finding the longest string in a list, or concatenating a list of strings.
