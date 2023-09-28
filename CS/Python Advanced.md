# Unpacking

Unpacking is a feature that exists in multiple high-level languages but is particularly useful in python when dealing with function parameters.

**e.g.**

```python
mylist = [11, 45]
mytuple = ("thing1", 2, 3)
mydictionary = {"val1": 20, "val2": 10}
wrongdictionary = {"val1": 40, "val2": 10, "val3": 3}

# Keyword arg only function
def divide_vals(*, val1=1, val2=1):
        return val1/val2

# Positional arg only function
def add_vals(val1, val2, /):
        try:
                return str(val1 + val2)
        except Exception:
                return "Something went wrong"

# Unpack list into variables
val1, val2 = mylist
print(f"val1 = {val1}")
print(f"val2 = {val2}")

#Unpack list/tuple into function
print("\nUnpacked List: ")
print(*mylist, sep="\n")

print("\nUnpacked Tuple: ")
print(*mytuple, sep="\n")

# Unpack dictionary into function
print("\nUnpacked Dictionary: ")
return_val = divide_vals(**mydictionary)
print(return_val)

# Unpack incorrect dictionary into function
print("\nIncorrect Unpacked Dictionary: ")
# return_val = divide_vals(**wrongdictionary)
print(return_val)

# Unpack incorrect list into function
print("\nIncorrect Unpacked Tuple: ")
# return_val = add_vals(*mytuple)
print(return_val)

# Unpacking in function arguments
def myfunction(*args, **kwargs):
    print("\nMy Function Got args: ")
    print(*args, sep="\n")
    print("\nMy Function Got kwargs: ")
    for key, value in kwargs.items():
        print(f"{key} = {value}")

myfunction(1, 2, 4, 10, val1="thing1", val2="thing2", val3="thing3")
```

# Conditional Variable Assignment

While this may seem somewhat useless it sort of comes in handy for easy one liners It may also come in handy when dealing with [[#Type Annotation]].

**e.g.**

```python
mycondition = True

myvar = None
if mycondition: 
	myvar = "yes"
else:
	myvar = "no"
print(myvar)

# becomes
myvar = "yes" if mycondition else "no"
print(myvar)
```

# Global Variable Scope

This allows for a function to modify the state of a global variable, or just create a global scope variable.

> Yes you can just return the value of statement and print that, but you may occasionally want to modify or instantiate a variable that determines how an entire program runs.

```python
# global variable
statement = "empty"

# creates a local variable "statement"
myFunc(val):
	if val > 5:
		statement = "Hello"
	else:
		statement = "Bye"

# modifies the global variable "statement"
myFuncGlobal(val):
	global statement
	if val > 5:
		statement = "Hello"
	else:
		statement = "Bye"

myFunc(10)
print(statement)

myFuncGlobal(10)
print(statement)
```

# Enumerate

Enumerate is a builtin function that takes any iterable and returns another iterable of tuples. Each tuple contains an index and 

```python
mylist = [1, 2, 3, 4, 5, 6, 7, 8]

# Print a value in an iterable with indexing starting at 1
# A classic implementation
myFuncIterate(iterable, print_index)
	count = 1
	for index in range(len(iterable)):
		if index + 1 == print_index:
			print(f"Reached index {count} with value: {mylist[index]}")
		count += 1

# Print a value in an iterable with indexing starting at 1
# A ca
myFuncEnumerate(iterable, print_index)
	for index, value in enumerate(iterable, 1):
		if index == print_index:
			print(f"Reached index {index} with value: {value}")

myfunc(mylist, 3)
```

# Generators

```python
# Useful when dealing with large sets, lists, tuples that can't be stored in memory.
def mygenerator(n):
	num = 0
	while num < n:
		yield num * 10
		num += 1

for val in mygenerator():
	print(val)

import base64

# Use it in a class!
class myClass:
	def __init__(self):
		self.class_list = ["Dave", "Maria", "Arjun", "Minjoon", "Sunday", "Naatya"]

	# Return a base64 encoded string version of each name
	def class_list_b64(self):
		for name in self.class_list:
			nameb = name.encode("ascii")
			nameb_b64 = base64.b64encode(nameb)
			name_b64 = nameb_b64.decode("ascii")
			yield name_b64

testClass = myClass()
for val in testClass.class_list_b64():
	print(val)
```

# Decorators
```python

def mywrapper(other_function, *args, **kwargs):
	def inner_function()
		print("Run before function")
		other_function(*args, **kwargs)
		print("Run after functionn")
	return inner_function

@mywrapper
def printer(value):
	print(value)

printer("Run  within the function")
```

# Type Annotation

# Asyncio

# PDB/VS Code Debugger

# List and Dictionary Comprehensions
