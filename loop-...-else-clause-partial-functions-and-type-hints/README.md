# Loop ... Else Clause, Partial Functions & Type Hints

## Loop ... Else Clause

In Python, the `else` clause in a loop is executed when the loop terminates normally (when a break statement is not executed). This is in contrast to the `try` and `except` statements, where the `else` block is executed when no exception is raised.

#### For... else

In Python, the for statement is used to iterate over a sequence (such as a list, tuple, or string) or other iterable object. The `else` clause in a for loop is optional and is executed only if the loop completed normally (that is, if the loop was not interrupted by a break statement).

* The `else` clause would execute if our iteration or loop executes normally without breaking
* The `else` clause will also execute if the loop is empty

```python
items = [1 , 2]

for i in items:
    print("number", i)
    
    # if we break the loop at some point the else would not work
    if(i == 2):
        break
else:
    print("The loop is either empty or did not run normally")
```

#### While... else

In Python, the while loop executes a block of code repeatedly as long as a certain condition is true. The `else` clause in a while loop in Python is optional and is executed only when the condition in the while loop becomes False. It is not executed if the loop is terminated by a break statement.

```python
items = [1, 2, 3, 4, 5]
count = 0

while count < len(items):
    count = count + 1
    if(count == 4):
        break
    print(count)
else:
    print("The loop is either empty or did not run normally")
```

The `else` clause in a loop can be a useful way to add some additional logic that should be executed only if the loop completes normally. However, it's important to note that the `else` clause is not the same as the `else` clause in a `try` and `except` block. The `else` clause in a `try` and `except` block is executed when no exception is raised, whereas the `else` clause in a loop is executed when the loop terminates normally.
