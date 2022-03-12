# Learning Object-Orient Programming with Python

[Source](https://python.plainenglish.io/learning-object-orient-programming-and-if-name-main-in-python-in-10-minutes-9b43504a739b)

## Class

- Like a multi-functional Cookie Cutter
- Can create objects of many variations with similar properties

```python
class cookie():
    def __init__(self, r,flavor):
        self.radius = r
        self.theFlavor = flavor

    def area(self):
        return 3.1416 * self.radius * self.radius
    
    def perimeter(self):
        return 2 * 3.1416 * self.r

smallCookie = cookie(3,'rasin')
largeCookie = cookie(10,'chocolate')
```

- The basic structure of a class could be daunting because it has `__init__` and `self`.
- The `__init__` is a reserved word and is called a **constructor**


When you see `def __init__(self, r, flavor)`, just remember it is where the class is making a new object with the attributes “r” and “flavor”. Notice that code puts the attributes “r” or “flavor” within the `__init__` step, not in the () in the first line of the code “class cookie()”.

### Self

- The word “self” is used to represent the instance of a class.
- Think of “self” as the original prototype that other copies copied from.
- The word “self” is not a reserved word and can be called any names you like.

### Make it a Python module to be imported by another code

- A Python module is a file that has a `.py` extension.
- A Python file can include functions, classes, or variables.
- If you make a Python file with `.py`, you have already made a new module.


```python
import NotCoolYet

greatCookie = NotCoolYet.cookie(20,'Frosting')
```

### “if __name__ == “__main__”

- Python has a reserved variable “__name__” for every python file. 
- The value for the variable “__name__” is the file name, i.e., the value for __name__ of the file VeryCool.py is “VeryCool”.