# Control flow in python

#### [Control Flow in Python](broken-reference) <a href="#control-flow-in-python" id="control-flow-in-python"></a>

A program's control flow is the order in which the program's code executes. The control flow of a Python program is regulated by conditional statements, loops, and function calls.



[**If statement in python**](broken-reference)

In a Python program, the if statement is how you perform this sort of decision-making. It allows for conditional execution of a statement or group of statements based on the value of an expression.

```
# example 1: Make a guess game
guess = 5
if(int(guess) == 7):
    print('You won')
    

# example 2: if statement example 2
if 2>5 and 2>1:
    print("One of this condition is correct")


# examle 3: if elif else conditionals
name = "John"

if name == "John":
    print(name)
elif name == "Andrew":
    print('name is not marv')
else:
    print('The name is neither John nor Andrew')

# if statement short hand (tenary operator)    
condition = True if 5 > 5 else False
```

[**For Loop**](broken-reference)

A for loop is used for iterating over a sequence (that is either a list, a tuple, a dictionary, a set, or a string). This is less like the for keyword in other programming languages, and works more like an iterator method as found in other object-orientated programming languages.

```
# for loop control flow - example 1
for i in range(2):
    if i == 0:
        continue
    elif i%2 == 0:
        print (f'{i} is an even number')
    else:
        print(f'{i} is an odd number')

name = "Joy"
result = "Name is Joy" if name == "Joy" else "Name is not Joy"
print(result)
```

[**For loop break keyword**](broken-reference)

'break' in Python is a loop control statement. It is used to control the sequence of the loop. Suppose you want to terminate a loop and skip to the next code after the loop; break will help you do that. A typical scenario of using the Break in Python is when an external condition triggers the loop's termination.

```
# Using the continue keyword in a loop
for i in range(50):
    if(i == 25):
        break
    print(i)
```

[**For loop continue keyword**](broken-reference)

'continue' in Python is a loop control statement. It is used to control the sequence of the loop. Suppose you want to skip a certain item and move to the next in a loop, 'continue' will help you achieve that.

```
# Using the continue keyword in a loop
for i in range(50):
    if(i == 25):
        continue
    print(i)
```

[**While loop in python**](broken-reference)

A while loop will run a piece of code while a condition is True. It will keep executing the desired set of code statements until that condition is no longer True. A while loop will always first check the condition before running. If the condition evaluates to True then the loop will run the code within the loop's body.

```
# While loop

max = 5
count = 1
while count < max:
    print("We are live")
    count += 1
```

