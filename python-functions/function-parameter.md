# Function Parameter

### Python For Starters

### [Function with parameter](broken-reference) <a href="#function-with-parameter" id="function-with-parameter"></a>

In Python, a function parameter is a variable that is used to pass information into a function when it is called. When you define a function, you can specify the parameters that the function should accept as input. These parameters become variables that you can use within the function to perform your desired task.

```
# This function should return the area of a circle when given the appropriate 

# parameter Pi * r ** r

PI = 3.142 # a constant, meaning that you should not change it [but of course can be changed eventually]

def area_of_a_circle(radius):
    result = PI * radius ** radius
    return result

area = area_of_a_circle(3)

print(area)
```

### [Working with default parameters](broken-reference) <a href="#working-with-default-parameters" id="working-with-default-parameters"></a>

In Python, you can specify default values for function parameters, which will be used if the caller does not provide a value for that parameter. This can be useful if there is a common value that you want to use for a parameter in most cases, but you still want to allow the caller to override it if needed.

To specify a default value for a function parameter, you can include an assignment expression in the parameter list when defining the function

* If a value is passed to the function when called, the value passed will override the default vale

```
PI = 3.142
def area_of_a_circle(radius=2):
    result = PI * radius ** radius
    return result

area = area_of_a_circle()
print(area)
```

### [Working with arguments (\*args)](broken-reference) <a href="#working-with-arguments-args" id="working-with-arguments-args"></a>

In Python, the \*args syntax is used to pass a variable number of arguments to a function. It allows you to pass a variable number of arguments to a function as a tuple.

Here is an example of how to use \*args in a function definition:

```
# Collecting Arguments using

def args_get_bio(*args):    
    
    print(args[0])

    print(args[1])
    
    print(args[2])

get_bio = args_get_bio(2022, "john", "solomon", 45, "Nexford")

print(get_bio)
```

### [Working with keyword arguments (\*\*kwargs)](broken-reference) <a href="#working-with-keyword-arguments-kwargs" id="working-with-keyword-arguments-kwargs"></a>

In Python, the \*\*kwargs syntax is used to pass a variable-length argument dictionary to a function. It allows you to pass a variable number of keyword arguments to a function as a dictionary.

Here is an example of how to use \*\*kwargs in a function definition:

```

# Collecting Arguments using **kwargs

def kwargs_get_bio(**kwargs):    
    year = kwargs['year']
    first_name = kwargs['first_name']
    print(first_name, year)
    
get_user_bio = kwargs_get_bio(first_name="John", year=2022)
```

