# Python Libraries & Packages

### Working with Python Libraries

A Python library is a collection of modules that contain functions and classes that you can use in your code. You can import a library into your code using the `import` statement, and then use the functions and classes defined in the library by calling them using dot notation. For example, you might import the math library and use the `sqrt` function like this:

```python
import math

x = math.sqrt(25)
print(x)
```

Here, the `sqrt` function returns the square root of its argument. There are many standard libraries included with Python, and you can also install third-party libraries using the `pip` package manager.

Python has a large standard library that you can use right away.

If you require a package that is not included in the standard library, you can look it up on the Python Package Index.

The largest Python repository is the `Python Package Index (PyPI)`. It includes many Python packages created and maintained by the Python community.

You can use the search box to find a package. For example, you can use the `requests` keyword to find packages that deal with HTTP requests.

Many relevant packages will be displayed in the search results. You can get more information about each package by clicking the corresponding link.

You can install the python _request_ library using the command globally or in a virtual environment using the command bellow:

```bash
pip install requests
```

This library would be downloaded from the https://pypi.org repository.

Then try it out by creating a new python file called main.py and entering the code block bellow:

```python
import requests

response = requests.get('https://pypi.org/')

# This would return the status code of the website request
print(response.status_code)
```

#### More on python libraries

Libraries are useful because they provide a way for you to reuse code that has already been written and tested, saving you the time and effort of writing that code yourself.

There are many Python libraries available, covering a wide range of functionality. Some common libraries include:

* `numpy`: a library for working with large, multidimensional arrays and matrices of numerical data
* `pandas`: a library for working with data in a tabular form, such as data frames
* `matplotlib`: a library for creating static, animated, and interactive visualizations
* `scikit-learn`: a library for machine learning tasks, including classification, regression, and clustering
* `requests`: a library for making HTTP requests to web servers

Then, you can import the library into your program using the import statement. For example, to use the NumPy library, you would include the following line at the top of your Python script:

```python
import numpy as np # as alias np
```

This imports the NumPy library and gives it the alias `np`, so that you can refer to it as `np` in your code. You can then use functions and other resources from the library by calling them using the `np.function_name()` syntax.
