# Advanced Python

**Python tips and tricks so you don't look like a noob at your next internship.**

- - - 

# Lambda Functions

Also known as *anonymous* functions. They are similar, in essence, to regularly defined functions. The only real difference being they are slightly more lightweight and intended to be used for simple operations.

- - -
# Lambda Examples

Simple uses
```python
addOne = lambda x: x + 1
print(addOne(3))

class Person:
    def __init__(self, name):
        self.name = name
        self.id = hash(name)

myList = [Person("JJ"), Person("Purdy"), Person("Kelce"), Person("Achane")]

myList.sort(key=lambda person: person.id)

print(myList)
```


