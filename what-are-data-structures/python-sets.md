# Python Sets

In Python, a set is an unordered collection of unique elements. Sets are used to store multiple items in a single variable. Sets are useful when you need to keep track of a collection of elements, but don't care about the order, or when you want to eliminate duplicates.

* Elements in a set are unordered.
* Elements in a set are unique. A set doesn’t allow duplicate elements.
* Elements in a set cannot be changed. For example, they can be numbers, strings, and tuples, but cannot be lists or dictionaries.

#### Creating a set in python

In Python, you can create a set using the `set()` function or using curly braces `{}`. Note that using curly braces `{}` to create a set will only work if you have a list of elements. If you try to create a set from a list using curly braces, you will actually create a dictionary.

```python
unique_user = {"john", "emmanuella", "faith", "linux"}
print(unique_user)
```

To create a set from a list of elements, you should use the set() function or curly braces {}.

#### Creating an empty set

To create an empty set, you should use the set() function.

```python
unique_user = set()
print(unique_user)
```

#### Clear a set

To remove all the items in a set, we can use the `.clear()` method to achieve this.

```python
unique_user = {"john", "emmanuella", "faith", "linux"}
unique_user.clear() # cleared the set
print(unique_user)
```

#### Remove items from a set

When removing items from a set, there are different ways to achieve this.

**Removing items using `.remove(key)`**

The `.remvoe()` method removes an item from the set. This operation would throw an error if the item is not found in the set

This is an example:

```python
unique_user = {"john", "emmanuella", "faith", "linux"}
unique_user.remove("john")
print(unique_user)
```

**Removing items using `.discard(key)`**

When using discard, it checks if the item exists in the set before removing the item

This is an example:

```python
unique_user = {"john", "emmanuella", "faith", "linux"}
unique_user.discard("john")
print(unique_user)
```

**Removing items using `.pop()`**

In Python, the `set.pop()` method removes and returns an arbitrary element from the set. If the set is empty, it raises a `KeyError`.

This is an example:

```python
person = {"john", "emmanuella", "andrew", "zack", "melvina", "mercilia"}
person.pop()
print(person)
```

#### Add items to a set

We can add items to a set using the `.add(value)` method

This is an example:

```python
unique_users = set() # initialised an empty set
unique_users.add("mark") # add item "mark" to the set
unique_users.add("john") # add item "john" to the set
print(unique_users)
```

#### Set Comprehension

A set comprehension is a concise way to create a new set from an iterable. It is similar to list comprehensions and dictionary comprehensions, but it creates a set instead of a list or dictionary.

Here is the syntax for a set comprehension:

```python
{expression for item in iterable}
```

Here is an example of a set comprehension:

```python
unique_user = {"john", "emmanuella", "faith", "linux"}
uppercase = {user.upper() for user in unique_user}
print(uppercase)
```

Set comprehensions are a concise and efficient way to create sets in Python. They are also a good way to learn about the syntax and usage of comprehensions in Python.

#### Set Union

In Python, you can use the union() method to find the union of two sets. The union of two sets is a new set that contains all the elements from both sets, without any duplicates.

```python
users1 = {'John', 'Melvina'}
users2 = {'Amaka', 'Emmanuella', "John"}
union = users1.union(users2)
print(union)
```

We can also use the `|` operator to find the union of two sets. This is known as the pipe operator.

```python
users1 = {'John', 'Melvina'}
users2 = {'Amaka', 'Emmanuella', "John"}
union = users1 | users2
print(union)
```

Both of these methods will return a new set that contains all the elements from both sets, without any duplicates.

#### Set Intersection

In Python, you can use the intersection() method to find the intersection of two sets. The intersection of two sets is a new set that contains only the elements that are common to both sets.

Here is an example of set intersection in python:

```python
users1 = {'John', 'Melvina'}
users2 = {'Amaka', 'Emmanuella', "John"}
intersection = users1.intersection(users2)
print(intersection)
```

We can also use the `&` operator to find the intersection of two sets. This is known as the ampersand operator.

```python
users1 = {'John', 'Melvina'}
users2 = {'Amaka', 'Emmanuella', "John"}
intersection = users1 & users2
print(intersection)
```

#### Set Difference

In Python, you can use the difference() method to find the difference of two sets. The difference of two sets is a new set that contains the elements that are in the first set, but not in the second set.

Here is an example showing a set difference:

```python
users1 = {'John', 'Melvina', "Emmanuella", "Joy"}
users2 = {'Melvina', 'Emmanuella', "John"}
difference = users1.difference(users2)
print(difference)
```

You can also use the `-` operator to find the difference of two sets. This is known as the subtraction operator.

```python
users1 = {'John', 'Melvina', "Emmanuella", "Joy"}
users2 = {'Melvina', 'Emmanuella', "John"}
difference = users1 - users2
print(difference)
```

#### Set Symmetric\_difference

In Python, you can use the symmetric\_difference() method to find the symmetric difference of two sets. The symmetric difference of two sets is a new set that contains the elements that are in one set or the other, but not both.

Here is an example showing a set symmetric\_difference:

```python
users1 = {'John', 'Melvina', "Emmanuella", "Joy"}
users2 = {'Melvina', 'Emmanuella', "John", "Konan"}
symmetric_difference = users1.symmetric_difference(users2)
print(symmetric_difference)
```

You can also use the `^` operator to find the symmetric difference of two sets. This is known as the caret operator.

```python
users1 = {'John', 'Melvina', "Emmanuella", "Joy"}
users2 = {'Melvina', 'Emmanuella', "John", "Konan"}
symmetric_difference = users1 ^ users2
print(symmetric_difference)
```

#### Set subset

In Python, you can use the `issubset()` method to check if a set is a subset of another set. A set is a subset of another set if all the elements in the first set are also in the second set.

Here is an example showing a set subset:

```python
users1 = {'John', 'Melvina', "Emmanuella", "Joy"}
users2 = {'Melvina', 'Emmanuella'}
is_subset = users2.issubset(users1)
print(is_subset)
```

You can also use the `<=` operator to check if a set is a subset of another set. This is known as the less than or equal to operator.

```python
users1 = {'John', 'Melvina', "Emmanuella", "Joy"}
users2 = {'Melvina', 'Emmanuella'}
is_subset = users2 <= users1
print(is_subset)
```

#### Set superset

In Python, you can use the `issuperset()` method to check if a set is a superset of another set. A set is a superset of another set if it contains all the elements in the other set.

Here is an example showing a set superset:

```python
users1 = {'John', 'Melvina', "Emmanuella", "Joy"}
users2 = {'Melvina', 'Emmanuella'}
is_superset = users1.issuperset(users2)
print(is_superset)
```

You can also use the >= operator to check if a set is a superset of another set. This is known as the greater than or equal to operator.

```python
users1 = {'John', 'Melvina', "Emmanuella", "Joy"}
users2 = {'Melvina', 'Emmanuella'}
is_superset = users1 >= users2
print(is_superset)
```

#### Set disjoint

In Python, you can use the `isdisjoint()` method to check if two sets are disjoint. Two sets are disjoint if they have no elements in common.

Here is an example showing a set disjoint:

```python
users1 = {'John', "Joy"}
users2 = {'Melvina', 'Emmanuella'}
is_disjoint = users1.isdisjoint(users2)
print(is_disjoint)
```

The isdisjoint() method returns True if the two sets are disjoint, and False otherwise.

Note that the empty set is considered to be disjoint with all other sets.

#### Frozen set

A frozen set is an immutable version of a Python set object. It is a set that cannot be modified after it is created. You can create a frozen set by using the frozenset() function

Frozen sets are useful when you need to use a set as a key in a dictionary or as an element in another set, because immutable objects can be used as keys or elements.

```python
unique_user_set = {"john", "emmanuella", "faith", "linux"} # our set is mutable
frozen_unique_users = frozenset(unique_user_set) # our set becomes immutable
print(frozen_unique_users)
```

Frozen sets also support all the methods and operations that regular sets do, such as union, intersection, and difference.
