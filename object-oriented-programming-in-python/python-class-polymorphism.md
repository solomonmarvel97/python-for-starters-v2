# Python Class Polymorphism

Polymorphism is the process of using an operator or function in different ways for different data input. In practical terms, polymorphism means that if `class B` inherits from `class A`, it doesn't have to inherit everything about class A; it can do some of the things that class A does differently.

```python
# basic_polymorphism.py

a = "alfa"
b = (1, 2, 3, 4)
c = ['o', 'm', 'e', 'g', 'a']

print(a[2])
print(b[1])
print(c[3])
```

Python uses polymorphism extensively in built-in types. Here we use the same indexing operator for three different data types.

Polymorphism is mostly used when dealing with inheritance.

```python
# polymorphism.py

class Animal:
   def __init__(self, name=''):
      self.name = name

   def talk(self):
      pass

class Cat(Animal):
   def talk(self):
      print("Meow!")

class Dog(Animal):
   def talk(self):
      print("Woof!")

a = Animal()
a.talk()

c = Cat("Missy")
c.talk()

d = Dog("Rocky")
d.talk()
```

Here we have two species: a _dog_ and a _cat_. Both are _animals_. The `Dog` class and the `Cat` class inherit the `Animal` class. They have a talk method, which gives different output for them.

```bash
$ ./polymorphism.py 

Meow!
Woof!
```
