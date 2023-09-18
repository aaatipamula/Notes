# Unpacking

Python allows for something called variable unpacking, 

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

```python
mycondition = True

myvar = 
```
# Generators

# Decorators

# Type Annotation

# List and Dictionary Comprehensions

# PDB/VS Code Debugger

