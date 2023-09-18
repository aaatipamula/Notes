# Unpacking

```python
mylist = [11, 45]
mytuple = ("thing1", 2)
mydictionary = {"val1": 20, "val2": 10}

def divide_vals(*, val1=1, val2=1):
	return val1/val2

# Unpack list into variables
val1, val2 = mylist
print(val1, val2, sep="\n")

#Unpack list into function
print(*myoptions, sep="\n")

# Unpack dictionary into function
return_val = divide_vals(**mydictionary)
print(return_val)

# Convention
def myfunction(*args, **kwargs):
	print(*args)
	print(**kwargs)
```

# Conditional Variable Assignment

# Generators

# Decorators

# Type Annotation

# List and Dictionary Comprehensions

# PDB/VS Code Debugger

