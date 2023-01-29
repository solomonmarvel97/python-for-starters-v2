# Python Dictionaries

A dictionary is a built-in data type in Python that stores data in key-value pair format. It is similar to a list or an array in that it stores a key-value pair at each index rather than a single value. A dictionary's keys must be unique, and they are used to access the corresponding values.

#### Create a new dictionary

We can create a python dictionary using the open and close curly brackets, with a `key value` combination representing each item in the dictionary. Here's an example of how you can create and use a dictionary in Python:

```python
dict = {
    "name" : "John",
    "age" : 40,
    "department": "Software Engineering"
}
print(dict)
```

#### Adding a new key value pair

We can add items to an existing dictionary by wrapping the new item key in a square bracket along with the items value. `dict[key] = value`

This is an example:

```python
dict = {
    "name" : "John",
    "age" : 40
}
dict["job title"] = "Lead Engineer"
print(dict)
```

You can access the values in a dictionary using the keys, which are unique within a dictionary. You can also use the len() function to get the number of key-value pairs in a dictionary, and the in operator to check if a key is in a dictionary.

Furthermore, you can also use the items(), keys(), and values() methods to get a view of the key-value pairs, keys, or values in a dictionary, respectively

#### Fetch items using key

To fetch specific items from a python dictionary, we use the following pattern `dict[key]`

```python
# fetch item using key
name = dict["name"]
age = dict["age"]
department = dict["department"]
job_title = dict["job title"]
```

#### fetch item using the .get()

To fetch specific items from a python dictionary, we use the following pattern `dict[key]`

```python
dict = {
    "name" : "John",
    "age" : 40
}
name = dict.get("name")
age = dict.get("age")
print(name)
print(age)
```

#### Deleting items from a dictionary using the `del` keyword

We can delete items from a dictionary using the `del` keyword following the key enclosed in a square bracket. This is an example of how to delete items in a dictionary.

```python
dict = {
    "name" : "John",
    "age" : 40,
    "department": "Engineering"
}
del dict["name"]
print(dict)
```

#### Iterating through a dictionary

Giving the fact that a dictionary is a `iter` (an iterable type), we can iterate over the items `.items()` while accessing the key and value following the pattern `for key, value in dictionary.items()`.

In this example, we are iterating over a list of dictionaries:

```python
array_of_dict = [
    {
        "id" : '09812hAA',
        "name" : "John",
        "age" : 40,
        "department": "Software Engineering"
    },
    {
        "id" : '09812hAB',
        "name" : "Emmanuella",
        "age" : 16,
        "department": "Software Engineering"
    },
]

# getting the key and the value using .items
for dictionary in array_of_dict: # iterating over the array
    for key, value in dictionary.items(): # iterating over the dictionary items
        print(f'{key} -> {value}')
```

#### Dictionary comprehension

A dictionary comprehension is a concise way to create a dictionary. It is similar to a list comprehension, but it returns a dictionary instead of a list.

```python
stocks = {
    'AAPL': 121,
    'AMZN': 3380,
    'MSFT': 219,
    'BIIB': 280,
    'QDEL': 266,
    'LVGO': 144
}

new_stocks = {name: value * 1.2 for (name, value) in stocks.items()}

print(new_stocks)
```

Dictionaries are useful for storing data that needs to be quickly retrieved using a unique key. They are also used to implement many other data structures in Python, such as sets and graphs.
