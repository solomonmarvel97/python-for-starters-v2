# Type Conversion

### Python For Starters

#### [Type Conversion](broken-reference) <a href="#type-conversion" id="type-conversion"></a>

Type conversion is the process of converting a data type into another data type. Implicit type conversion is performed by a Python interpreter only. Explicit type conversion is performed by the user by explicitly using type conversion functions in the program code. Explicit type conversion is also known as typecasting

```
# file name type_conversion1.py

x: int = 20
y: str = str(x)
```

Run Code:

```
python type_conversion1.py
```

The code returns a `string` type showing that the variable `x` was converted to a `string` type.

Let's try another example:

```
# file_name - type_conversion2.py

name = "John Doe"
conv_name = int(name)

print(type(name))
```

Run Code:

```
python type_conversion2.py
```

The code returns an error `ValueError: invalid literal for int() with base 10: 'John Doe'`.

We got the `ValueError` because the value `John Doe` is not a valid number therefore converting a `string` type to a `number` type is only possible if the `string` can become a valid `number`.

