# A Comprehensive Guide for Classes in Python

## How to define and interact with a class

[SOURCE](https://towardsdatascience.com/a-comprehensive-guide-for-classes-in-python-e6bb72a25a5e)

- A class represents a type
- Can create many instances of that class
- OOP is built around the idea of having objects that belong to a particular type

### What is a class in python

- Data Attributes: what is needed to create an instance of a class
- Methods (procedural attributes): How we interact with instances of a class

List is an instance

```python
words = ['data', 'science', 'amchine', 'learning']
```

**Abstraction** how to interact with and use lists or other objects

```python
words.remove('data')

print(words)
['science', 'machine', 'learning']
```

---

## Creating a class

```python
class Book():
  def __init__(self, name, writer, word_length):
    self.name = name
    self.writer = writer
    self.word_length = word_length
```

- The `__init__` is a special function that is automatically executed when an instance of class is created. 
  - It is also called class constructor.

***Note**: Self refers to the instance itself. You can use any word instead of “self” but it is a highly common practice to use “self”.*

- Create an instance 

```python
b1 = Book("Pandas", "John Doe", 100000)`


print(type(b1))
<class '__main__.Book'>
```
We can access or modify the attributes of a class using the following way.

```python
print(b1.name)
Pandas

b1.name = 'NumPy' #updates the name attribute

print(b1.name)
NumPy
```

---

## Defining class methods

- The Book class only have data attributes. We should add methods (i.e. procedural attributes) to make it for useful and functional.
- For instance, we can implement a method that returns the number of pages given the fontsize. 
  - We specify the length of the book in number of words. 
  - The method will calculate the number of pages based on the length and fontsize.

```python
def number_of_pages(self, fontsize=12):
  word_length = self.word_length
  if fontsize == 12:
    words_in_page = 300
  else:
    words_in_page = 300 - (fontsize - 12) * 10
  return round(word_length / words_in_page)
```

Can add `number_of_pages` to in the class definition.

If a function declared inside a class definition needs to access the data attributes of an instance, we need to tell the function how to access them - first line of function

```python
b1 = Book('Pandas', 'John Doe, 100_000)

b1.number_of_pages()
333
Book.number_of_pages(b1)
333
```

Default font size of 12, but can specify it.

```python
b1.number_of_pages(14)
357
b1.number_of_pages(fontsize=16)
385
```

There are certain methods that we need to define for our class in order to use some built-in functions of Python. Consider the print function.

```python
print(b1)
<__main__.Book object at 0x7fa4cf9f7588>
```

The print function returns the type and the memory location of the object by default. However, we can customize its behavior by implementing the `__str__` method in our class.

```python
def __str__(self):
  return "<" + self.name + ", by " + self.writer + ">"
  ```

We add the `__str__` method in our class definition as above. Here is how the print function works for our class now:

```python
print(b1)
<Pandas, by John Doe>
```

---

## Class vs. Instance Variables

- Class variables are declared inside a class but outside of any function
  - More general and likely to apply all of the instances of a class
- Instance variables are declared inside the constructor which is the `__init__` method.
  - more specific and defined for each instance separately

Consider the Book class we defined earlier. We run a publishing company and have some standards for the books we publish such as page width and color for the cover. If we define them as class variables, we do not have to explicitly declare for each instance created.

```python
class Book():
  page_width = 14
  cover_color = "blue"
  def __init__(self, name, writer, word_length):
    self.name = name
    self.writer = writer
    self.word_length = word_length
```

We have implemented the `page_width` and `cover_color` as class variables because they are inside the class definition but outside any function definition.

Let’s create an instance of the Book class.

```python
b2 = Book("Machine Learning", "Jane Doe", 120000)
```

We have not specified the class variables while creating this instance. However, the b2 possesses these variables and we can access them.

```python
b2.page_width
14
b2.cover_color
'blue'
```

We have the option to change the class variables for a particular instance.

```python
b2.cover_color = 'red'

b2.cover_color
'red'
```

---

## Creating a Child Class

We can create a class based on a different class. Let’s create a class called “ColorBook” based on the “Book” class.

```python
class ColorBook(Book):
```

- The ColorBook is a child class of the Book class. 
- When we create a class in this way, the child class copies the attributes (both data and procedural) from the parent class. 
- This concept is called **inheritance** which makes the OOP more efficient and powerful

Let’s define the `__init__` function of the ColorBook class. It will have two additional parameters which are “color” indication the color of pages and “has_image” indicating if there are images in the book.

```python
class ColorBook(Book):
  def __init__(self, name, writer, word_length, color, has_image):
    Book.__init__(self, name, writer, word_length
    self.color = color
    self.has_image = has_image
```

Since the name, writer, and word_length have already been defined in the Book class, we can just copy the `__init__` method from it. We just need to define the additional attributes.

*Note*: We are free to define each data attribute manually for the child class. Using the `__init__` of parent is optional.

Let’s create an instance of the ColorBook class.

```python
c1 = ColorBook("Seaborn", "John Doe", 90000, "green", True)
c1.name
"Seaborn"
c1.color
"green"
```

We have the option to override the data and procedural attributes (i.e. methods) inherited from the parent class. This makes the inheritance even more powerful because we are obligated to use everything in the parent class.

For instance, we can modify the `__str__` method for the ColorBook class.

```python
def __str__(self):
  return "<" + self.name + ", in " + self.color + ">"
```

The print function will return the name of the book and its color.

```python
c1 = ColorBook("Seaborn", "John Doe", 90000, "green", True)
print(c1)
<Seaborn, in green>
```