# Directory & IO

## Working with Directories

In Python, you can use the `os` module to work with directories (also called "folders"). The `os` module provides functions to perform various operations on directories.

Here are a few examples of common tasks you might perform with the `os` module:

**Creating a Directory**

To create a new directory, you can use the `os.mkdir()` function. This function takes a single argument, which is the name of the directory you want to create.

```python
import os

# Create a new directory called "newdir"
os.mkdir("emmanuella")
```

**Changing the Current Working Directory**

To change the current working directory, you can use the `os.chdir()` function. This function takes a single argument, which is the path of the directory you want to change to.

```python
import os

# Change the current working directory to "newdir"
os.chdir("emmanuella")
```

**Listing the Contents of a Directory**

To list the contents of a directory, you can use the `os.listdir()` function. This function takes a single argument, which is the path of the directory you want to list the contents of. It returns a list of the names of the files and directories in that directory.

```python
import os

# List the contents of the current working directory
contents = os.listdir()
print(contents)
```

**Checking if a Path is a Directory**

To check if a given path is a directory, you can use the `os.path.isdir()` function. This function takes a single argument, which is the path you want to check. It returns `True` if the path is a directory, and `False` if it is not.

```python
import os

# Check if the current working directory is a directory
is_dir = os.path.isdir(".")
print(is_dir)
```
