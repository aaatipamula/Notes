# Unpacking

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

> While this may seem somewhat useless it sort of comes in handy for quick conversions using conditions

```python
mycondition = True

# e.g. 
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

```python
x = 10
statement = ""

myFunc(val):
	if val > 5:
		statement = "Hello"
	else:
		statement = "Bye"

myFuncGlobal(val):
	global statement
	if val > 5:
		statement = "Hello"
	else:
		statement = "Bye"

myFunc(x)
print(statement)

myFuncGlobal(x)
print(statement)
```

> Yes you can just return the value of statement and print that, but sometimes you want to make a change to a variable that determines how the ENTIRE program runs.

# Enumerate

```python
mylist = [1, 2, 3, 4, 5, 6, 7, 8]

myfunc(iterable, print_index)
	for index in range(len(iterable)):
		if index == print_index:
			print(f"Reached index {index} with value: {mylist[index]}")

myfunc(iterable, print_index)
	for index, value in enumerate(iterable):
		if index == print_index:
			print(f"Reached index {index} with value: {value}")

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

# Use it in a class!
class myClass:
	def __init__(self):
		self.classlist = [1, 3, 4, 5, 6, 7]

	def generator(self):
		for val in self.classlist:
			yield val

testClass = myClass()
for val in testClass.generator():
	print(val)
```

# Decorators

# Type Annotation

# PDB/VS Code Debugger

# List and Dictionary Comprehensions
