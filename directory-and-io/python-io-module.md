# Python IO Module

In Python, the `io` module provides a uniform interface for reading and writing streams of data. It is part of the Python Standard Library, which means it is available to use in any Python program without the need to install additional packages.

The `io` module defines several classes that can be used to read and write data in various formats, including text, binary, and raw data. These classes include `TextIOWrapper`, `BufferedReader`, and `BufferedWriter`, among others.

One common use of the `io` module is to read and write files. For example, you can use the open() function from the `io` module to open a file, and then use methods like `read()` and `write()` to read from and write to the file. Here is an example of reading from a file and printing its contents to the console:

The `mode` is an optional parameter. It’s a string that specifies the mode in which you want to open the file. Below, we will show available modes for opening a text file:

* `'r'` Open for text file for reading text
* `'w'` Open a text file for writing. If the file exists, the function will truncate all the contents as soon as you open it. If the file doesn’t exist, the function creates a new file.
* `'a'` Open a text file for appending text. If the file exists, the function append contents at the end of the file.
* `'+'` Open a text file for updating (both reading & writing).
* `'x'` Create a file and write to the file

You can also use the `io` module to read and write data from other sources, such as network sockets or in-memory buffers. The `io` module provides a consistent interface for working with these different types of data streams, making it easier to write code that is portable across different platforms and environments.

In this example `io` operations we are using a context manager to manage the context of the read operation:

```python
import io

# Open the file in read mode

with io.open('filename.txt', 'r', encoding='utf-8') as f:
  # Read the contents of the file
  contents = f.read()
  
  # Print the contents
  print(contents)
```

### What is a context manager?

The `with` keyword is used when creating a context manager i.e. managing the context of the ongoing operation (in this case a file open operation).

A context manager is an object that defines the methods `__enter__` and `__exit__`, which allow you to execute code before and after a block of code, respectively. Context managers are used in the with statement, which ensures that the code in the block is executed within the context of the manager.

Context managers are very useful because they allow you to manage resources, such as files or database connections, in a structured way. They ensure that resources are properly cleaned up when they are no longer needed, which can help prevent errors and improve the performance of your code.

#### Reading from file

In this example, we are reading from a file:

First create a file `read.txt` in the location/directory, then add the following lines of text:

```
Hello
World!
```

The following code block will read the `read.text` file and print the result to your terminal console.

```python
# reading from a file
with open('read.txt', 'r') as f:
    lines = f.readlines() # read the lines in the file
    for i in lines:
        print(i)
    f.close() # close the file
```

#### Writing to a file

In this example, we are writing to a file:

* First create a file `write.txt` in the location/directory:

The following code block will write the items in the list to the file we have just created.

```python
# writing to a file
lines = ['My name is Trust', 'I am a software engineer', 'Learning to become a data scientist']
with open('write.txt', 'w') as f:
    for line in lines:
        # write the line to the file
        f.write(line)
        f.write('\n')
        # You can check the write.md to see the result
```

#### Creating and writing to a file using the `'x'` mode

In this example, we are creating a file if the file does not exist, and we are writing to the file at the same time:

```python
with open('ellajoyifeoma.txt', 'x') as f:
    f.write('Ella, Joy and Ifeoma attended class today')
```

#### Checking if a file exist using `os.path.exists(filename)`

We can check if a file exist before proceeding to make any computational operation with the file using the `os.path.exists(filename)` command.

Here is an example to do that:

```python
import os.path

# check if the file exist
file_exists = os.path.exists('readme.txt')

if(file_exists):
    print("File exists")
else:
    print("File does not exist")
```

#### Python CSV Module

The `csv` module in Python provides functions for reading and writing CSV (comma-separated value) files.

**Reading from a CSV file**

Here's an example of how to use `csv.reader` to read a CSV file and print each row:

```python
import csv

with open('data.csv', 'r') as f:
    reader = csv.reader(f)
    for row in reader:
        print(row)
```

This code will open the file `data.csv` in read mode, create a `csv.reader` object, and iterate over the rows in the file. Each row is returned as a list of values, with the values in each column separated by commas.

NB: Add a sample csv file called `data.csv` to the directory.

You can also use the `csv.DictReader` class to read the CSV file into a list of dictionaries, with the keys of the dictionary being the column names and the values being the cell values.

```python
import csv

with open('data.csv', 'r') as f:
    reader = csv.DictReader(f)
    for row in reader:
        print(row)
```

This code will print each row as a dictionary, with the keys being the column names and the values being the cell values.

**Writing to a CSV file**

Here's an example of how to write to a csv file using python:

```python
import csv  

header = ['country', 'area code', 'city', 'state']
data = ['Nigeria', 200211, 'AGB', 'OG']

with open('data.csv', 'w', encoding='UTF8') as f:
    writer = csv.writer(f)
    
    # write the header
    writer.writerow(header)
    
    # write the data
    writer.writerow(data)
```

#### Renaming files using `os.rename(filename, new_name)` command

To rename a python file using the `os` module, we have to use the `os.rename(filename, new_name)` where the filename describes the current name of the file including the file extension e.g. `data.csv` and the `new_name` describes the name you want to change the `filename` to.

Here is a simple python code to achieve this operation with ease:

```python
import os

try:
    os.rename('data.csv', 'file.csv')
except FileNotFoundError as e:
    print(e)
```

This will successfully rename the `data.csv` file to `file.csv`.

#### Deleting files using the `os.remove(filename)` command

To delete a file using the `os` module, we can simply use the `os.remove(filename)`.

Here is a python snippet to achieve the `os.remove` operation:

```python
import os

try:
    os.remove('data.csv')
except FileNotFoundError as e:
    print(e)
```

This will successfully delete the `data.csv` file from the directory.
