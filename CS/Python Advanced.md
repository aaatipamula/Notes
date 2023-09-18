# Unpacking

Python allows for something called variable unpacking, 

```python
mylist = [11, 45]
mytuple = ("thing1", 2)
mydictionary = {"val1": 20, "val2": 10}

# Keyword arg only function
def divide_vals(*, val1=1, val2=1):
	return val1/val2

# Positional arg only function
def add_args(val1, val2):
	try:
		return str(val1 + val2)
	except Exception:
		return "Something went wrong"

# Unpack list into variables
val1, val2 = mylist
print(val1, val2, sep="\n")

#Unpack list/tuple into function
print(*mylist, sep="\n")
print(*mytuple, sep="\n")

# Unpack dictionary into function
return_val = divide_vals(**mydictionary)
print(return_val)

# Convention
def myfunction(*args, **kwargs):
	print()
	print(*args)
	divide_vals(**kwargs)
	print(**kwargs)

```

# Conditional Variable Assignment

# Generators

# Decorators

# Type Annotation

# List and Dictionary Comprehensions

# PDB/VS Code Debugger

