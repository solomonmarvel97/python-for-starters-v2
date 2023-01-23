# Python Lists

In Python, a list is an ordered collection of items. Lists can contain items of any data type, including numbers, strings, and even other lists.

### Creating a List

Lists are created using square brackets \[ ] and the items are separated by commas.

```python
fruits = ['apple', 'banana', 'orange', 'mango']
print(fruits)
```

### Accessing List items

You can access the items in a list using their indexes. The indexes start at 0 for the first item, 1 for the second item, and so on.

```python
fruits = ['apple', 'banana', 'orange', 'mango']
first_fruit = fruits[0]
print(first_fruit)
```

You can also use negative indexes to access items from the end of the list

This is an example:

```python
fruits = ['apple', 'banana', 'orange', 'mango']
last_fruit = fruits[-1]
next_to_last_fruit = fruits[-2]
print(last_fruit)
print(next_to_last_fruid)
```

### Append item to a List

We can append items into a list using the following pattern `.append(value)` method adds items to the tail of our list

```python

list = ["John", "Abraham", "Mark", "Trust"]
print(list) # list before append
list.append("Joy")
print(list) # list after append
```

### Insert item in List

We can insert items into a list using the following pattern `.insert(index, value)`. Here, you have to specify the index (i.e. the position) that you intend adding the item to.

```python
list = ["John", "Abraham", "Mark", "Trust"]
list.insert(3, "Marrieth")
print(list)
```

### Removing items from a list

There are variable numbers of ways to remove items from a list, we can remove items from the tail of our list using the `.pop()` command, using the index of the item or even using the value of the item.

#### Removing the last item from the list using `.pop`

```python
list = ["John", "Abraham", "Mark", "Trust"]
print(list) # before .pop() operation
list.pop()
print(list) # after .pop() operation
```

#### Removing items using the item index & the delete keyword `del list[index]`

```python
# removing an item using the index
list = ["John", "Abraham", "Mark", "Trust"]
del list[1]
print(list)
```

#### Removing items using the value of the item `list.remove(value)`

```python
list = ["John", "Abraham", "Mark", "Trust"]
list.remove("John")
print(list)
```

### Finding the index of an element in a list

In Python, a list index refers to the position of an element in a list. A list is an ordered collection of items, and each item has a corresponding index that indicates its position in the list.

```python
names = ["John", "Mark", "Marrieth"]
print(names.index('Mark'))
```

### Sorting a python list

Sorting is the process of rearranging the items in a list in a particular order. In Python, you can use the `sorted()` function to sort a list. By default, the sorted() function sorts the items in ascending order.

We use the `.sort()` and `.sort(reverse=True)` to sort our python list.

Sorting items in ascending order:

```python
list_of_names = ["Emmanuella", "Joy", "John", "Abraham"]

# sorting our list in ascending order

list_of_names.sort()
print(list_of_names)
```

Sorting items in descending order:

```python
list_of_names = ["Emmanuella", "Joy", "John", "Abraham"]

# sorting our list in ascending order

list_of_names.sort(reverse=True)
print(list_of_names)
```

### Slicing a list in python

In Python, you can use slicing to extract a portion of a list (also known as a sublist). Slicing uses a start index, a stop index, and an optional step size to specify the elements that should be included in the slice.

You can use slicing to modify the elements in a list by assigning new values to the slice. For example, you can use slicing to delete elements from a list by assigning an empty list to the slice:

```python
names = ["Emmanuella", "Joy", "Prince", "Melvina", "Mercilia"]

# slicing items from index 1 through 4

print(names[1:4])

# slicing items from index 0 to -2

print(names[:-2])
```

### Unpacking a list in python

In Python, you can use unpacking to assign the elements of a list to separate variables. This can be a convenient way to assign multiple variables at once, rather than assigning them one by one.

Example of list unpacking:

```python
names = ["John", "Mark", "Marrieth"]
john, mark, marrieth = names
print(john, mark, marrieth)

# You can use the (*) to unpack the left overs into another list

john, *others = names
print(others)
```

### Looping through a python list

Looping is a programming construct that allows you to repeat a block of code a certain number of times or until a certain condition is met. In Python, there are two types of loops: `for loops` and `while loops`.

A for loop is used to iterate over a sequence (such as a list, tuple, or string) or an iterable object (such as a dictionary, file, or set). The for loop will execute a block of code for each element in the sequence, and it will automatically iterate through all the elements in the sequence.

You can use loops to perform a wide variety of tasks in Python, such as iterating over a list of items, searching for a particular element in a list, or repeating a set of actions until a certain condition is met. Loops are an essential part of programming and are used extensively in Python and other programming languages.

There are several ways to loop through a list in Python. Here are a few examples:

Using a `for` loop:

```python
names = ["John", "Mark", "Marrieth"]

for i in names:
    print(i)
```

Using a `while` loop:

```python
names = ["John", "Mark", "Marrieth"]
while i < len(names):
    print(numbers[i])
    i += 1
```

Using the `.enumerate()` function:

```python
names = ["John", "Mark", "Marrieth"]
while i, name in enumerate(names):
    print(i, name)
```

Using a list comprehension:

```python
names = ["John", "Mark", "Marrieth"]
[name for name in names]
```

Each of these techniques has its own use cases, and you can choose the one that is most appropriate for your needs. For example, you might use a `for` loop if you want to perform a specific action for each element in the list, or a list comprehension if you want to create a new list based on the elements in the original list.

### Python List Comprehension

List comprehension is a concise way to create a list using a single line of code. It is a powerful tool for creating lists based on existing lists or other iterable objects.

List comprehension has the following syntax: `[expression for item in iterable]`

```python
numbers = [1, 2, 3, 4, 5]

# This is an example iterating through a list and checking for a condition
result = [i for i in numbers if i % 2 == 0]
print(result)
```

List comprehension is a concise and efficient way to create lists in Python, and it is often used to create lists that are based on complex transformations or filters of other lists or iterable objects.
