# [9 Rules To Consider for Defining Your First Python Class](https://betterprogramming.pub/9-rules-to-consider-for-defining-your-first-python-class-5109e02771b4)

## Leverage the power of Python as an OOP

### Override Initialization Method

- In most cases, you need to override the initialization method (`__init__`).
- This method accepts parameters you want to set to each instance object of the class.

Suppose that we are creating an application that manages products for a company and we want to define a class as a data model for products. Per business needs, the most important information for products is the name and the SKU (stock-keeping unit) number. Thus, we can have the following code for the initialization method:

```python
class Product:
    def __init__(self, name, sku):
        self.name = name
        self.sku = sku
```
In some cases, products have additional pieces of information that are not ready to be set when the instance is created. For example, let’s say the available number of units for a product will be determined later on. Instead of doing `product.unit_count = xxx` later on, it’s a good practice to set this attribute in the `__init__` method, as shown below:

```python
class Product:
    def __init__(self, name, sku):
        self.name = name
        self.sku = sku
        self.unit_count = None
```

The largest advantage of this approach is being explicit. Readers of your code will find all instance attributes in a single place (i.e. the initialization method), so they will know exactly what attributes an instance has.

---

### Define Class Attributes

Besides instance attributes, we can also define class attributes (those that are shared by all the instances of the class). For example, because all the products are made by the same company, all instances share the same maker and brand. In this case, we can define class attributes:

```python
class Product:
    maker = "ABC Company"
    brand = "abc"
```

As a best practice, you want to define these class attributes at the top of the class’s body so that they’re clear to the readers.

It should also be noted that when you access class attributes, you can either use the class or an instance object. Normally, they should give you the same result. However, when you access it with an instance object, you want to make sure the instance object hasn’t been accidentally set a different value with the same attribute name. When that happens, the instance’s attribute will be used directly and the class attribute is only used as a fallback. This may sound confusing, but you can observe this effect below:

```python
product = Product("Vacuum", 1001)
# the instance has the class attribute as the class
product.brand == Product.brand == "abc"
True
product.brand = "Dx"
# the instance now has the attribute different from the class
product.brand
'Dx'
```

---

### Define Instance Methods

We often need to apply specific operations to instance objects. Usually, these operations are defined using functions. When functions are defined within a class and these functions are to be called by instance objects, we refer to them as instance methods. The following code snippet shows you a trivial example:

```python
class Product:
    # the same initialization method as before
    def update_stock(self, warehouse):
        # get the stock info for the warehouse
        self.unit_count = get_stock_from(warehouse)
```

`update_stock` is an example of an instance method that takes the `warehouse` parameter and gets the stock information accordingly. One thing to note is that the first parameter is conventionally named `self`, which refers to the instance object that calls the method. Although this parameter can be named differently, it’s a best practice to name it `self`.

---

### Define Static and Class Methods

As discussed, instance methods are intended to manipulate instance objects. However, there are cases where we need functions that are independent of instances. In these cases, we may need to define static and class methods. Static methods are usually utility functions that are often not dependent on the class or any instance. Thus, you can think of them as functions that can theoretically be placed outside a class.

The following shows a possible example. Suppose that a product has an attribute of its weight as a unit of pounds. Some other parts of the application have other weight-related information. Chances are that we want to show weights as a unit of kilograms. In this case, we can have this function as a static method. The syntax is that you place a decorator called `staticmethod`, which signifies that we’re defining a static method.

```python
class Product:
    # the same initialization method as before
    @staticmethod
    def to_kg(weight_pound):
        return weight_pound * 0.453592
```

Class methods are often used less frequently. Sometimes, we may use them as a convenient way for instantiation. Let’s say that our application may receive a dict object that has product information from an external API call. Here’s how we can use a class method to address this need:

```python
class Product:
    @classmethod
    def from_dict(cls, dict_obj):
        name = dict_obj["name"]
        sku = dict_obj["sku"]
        return cls(name, sku)
```

Like with static methods, we use the decorator `classmethod` above the function to signal that we’re creating a class method. The convention for a class method is to have the first parameter named `cls`, which refers to the class (`Product` in this case).

---

### Use the property Decorator for Read-Only Attributes

If you have any other OOP experience, you may know that there are read-only attributes. This feature can be implemented in Python with the use of the `property` decorator. The following code snippet shows you an example.

```python
class Product:
    # the same initialization method as before
    @property
    def formatted_sku(self):
        return f"SKU: {self.sku}"
```

Just as with the `staticmethod` and `classmethod` decorators, we place the `property` decorator above the method. Typically, we decorate an instance method such that we can use this function as if we’re accessing a normal attribute, which makes your code a little bit cleaner.

Certainly, the full feature of the property decorator also includes creating setters and deleters
for the same property. You can find related information [in my previous article](https://betterprogramming.pub/why-bother-using-property-decorators-in-python-935c425f86ed).

---

### Use Finer Access Control

Another OOP feature is concerned with encapsulation, with which you’ll consider what methods and attributes you want to expose to external users of your class. You may have heard of various terms related to encapsulation, such as private vs. public. W

hen we say *public*, we mean those that can be accessed by entities outside of the class, while *private* attributes refer to those that are available for access inside the class.

By default, everything inside a class is public. When you want to define private attributes, the convention is to change how you name attributes. Instead of starting with a letter, we start the naming with an underscore. It should be noted that there is a nuance between those with one underscore (e.g. `_var_name`) and those with two underscores (e.g. `__var_name`).

Although both are intended to be used non-publicly, you’ll see that we mostly need to use the names with one underscore (aka protected attributes). In contrast, those with two underscores are termed private attributes. Accessing them involves name mangling. The following code snippet shows you relevant examples:

```python
class Product:
    def __init__(self, name, sku):
        self.name = name
        self.sku = sku
        self._short_name = name[:3]
        self.__wacky_name = name[::-1]
```

In the example, `_short_name` is a protected attribute, while `__wacky_name` is a private attribute. 

In the body of the class, you use these two attributes as you normally would. However, they’ll act differently when you access them outside of the class. For example, the autocompletion hints in PyCharm don’t even include them, which is the desired behavior because they’re intended to be accessed non-publicly.

It should be noted that Python doesn’t restrict your access to these non-public attributes if you choose to do so. Note how we access the private attribute that begins with double underscores. It’s what mangling means: `__var_name` becomes `_ClassName__var_name`. Applying this conversion rule, `__wacky_name` becomes `_Product__wacky_name`.

```python
product = Product("Vacuum", 1001)
product._short_name
'Vac'

product._Product__wacky_name
'muucaV'
```

---

### Integrate Type Hints

Since Python 3.5, type hints have become available. This feature adds clarity to the code, and common IDEs can take advantage of the provided hints about the types to make more meaningful auto-completion suggestions. You can find many online tutorials on using type hints in Python. This article isn’t intended to provide a thorough review of the topic. Instead, I’ll just show you some common ways to use type hints in a class definition.

In the initialization or other methods, you can provide type hints to the parameters and return data types. Another common case is for class attributes. To specify the types, you use colons followed by the types. Some examples are shown below:

```python
class Product:
    maker: str
    upc_shared: int

    def __init__(self, name: str, sku: int):
        self.name = name
        self.sku = sku

    def get_annual_sales(self, year: int) -> float:
        return 2000

    @staticmethod
    def evaluate_sales(sales: list[float]) -> tuple[float, float]:
        sales_mean = 100.0
        sales_std = 17.7
        return sales_mean, sales_std
```
Regarding a method’s return value, you provide the hint by using `->` to specify the returned data type.

---

### Write Docstrings

It should first be noted that writing clear docstrings isn’t a permit to write unclear code. You always need to make sure that your code is readable by itself without any docstrings. 

Docstrings are just to add additional clarity for those who are not familiar with the code so they can quickly figure out how to use the class, its attributes, and its methods. 

For a class — particularly a public one — you’ll have to provide two pieces of docstrings.

First, you’ll write docstrings for the class.

Typically, it has the following components:
- A one-sentence summary of the class’s intended purpose.
- The list of the public attributes.
- The list of the public methods.

Second, you’ll write separate docstrings for each of the public methods. For these functions, you follow the docstring convention for a function, which includes the function’s purpose, input parameters, and return data. Where applicable, you may also need to specify possible exceptions that it can raise. The following code shows you the docstrings for a class:



```python
class Product:
    """
    A class to manage product-related data for the application.
    Attributes:
        name: str, the name of the product
        sku: int, the Stock-Keeping Unit number for the product
    Methods:
        get_annual_sales: get the annual sales data for a product
    """

    def __init__(self, name: str, sku: int):
        """
        Initialize a Product instance
        :param name: str, the product's name
        :param sku: int, the product's sku (stock-keeping unit) number
        :return None
        """
        pass

    def get_annual_sales(self, year: int) -> float:
        """
        Get the product's annual sales amount for the specified year
        :param year: int, the year for which you want to get the annual sales
        :return: float, the annual sales in dollars
        """
        pass
```

The code snippet above just gives you a general idea about writing docstrings for a class. Whenever applicable, you can also add comments to your code. But remember that you should find a balance between too few and too many comments. When you feel that your code may be confusing, think about re-writing your code to make it clear so that you don’t need to write any comments. If you feel that your code can’t tell what it does itself, you may want to add some comments. Please note that your comments should always be kept concise because comments can be distracting noise for those who read your code.

---

### String Representations

When you define a class, it’s a best practice to override the `__str__` and `__repr__` methods such that the instances can have proper string representations. These two methods have different purposes.

- The `__str__` method is the one that is used when you print an instance object. Usually, it provides descriptive information about the instance. It’s intended for users who are less concerned about how your class should be instantiated, which is the job that `__repr__` should do.
- The `__repr__` method is the string that you’ll see when a Python variable is entered in an interactive console. In most cases, it should be unambiguously showing how you create an instance that has the same values for the attributes. This is important because you want to show the instantiation method for the users who care more about the underlying implementations of the class, such as other developers.

The following code snippet shows you how we can override these two methods:

```python
class Product:
    def __init__(self, name: str, sku: int):
        self.name = name
        self.sku = sku

    def __str__(self):
        return f"{self.name} (SKU: {self.sku})"

    def __repr__(self):
        # or return f"{self.__class__.__name__}({self.name!r}, {self.sku})"
        return f"Product({self.name!r}, {self.sku})"
```

With the current implementation of the Product class, this is how they’re used by the `print` function and the console for inspection:

```python
>>> product = Product("Vacuum", 1001)
>>> print(product)
Vacuum (SKU: 1001)
>>> product
Product('Vacuum', 1001)
```

---

### Conclusion

In this article, we reviewed nine elements that you should consider for your Python classes. Applying these elements will make your classes readable and consistent so that they’ll be easier to maintain in the long term.

Here’s a quick recap:

1. In the initialization method, specify all instance attributes — even for those that don’t have a good initial value.
2. Class attributes are those that are to be shared by all instances or something related to the class itself.
3. The functionalities of the class mainly come from a variety of instance methods. So be sure to define good ones.
4. Static methods are usually utility functions related to the class. In these methods, you’re expected to access no attributes of the class or any instance. By contrast, class methods need to access the class-related attributes or methods.
5. Read-only attributes can be implemented by the property decorator that converts a function call to a dot notation access, which acts like accessing an attribute.
6. It’s a convention to use underscores as a prefix to make non-public attributes/methods not readily accessible to external users.
7. Use type hints to provide clarity to the code and make your IDEs offer useful auto-completion suggestions.
8. Docstrings are a must if your class is intended to be used publicly. Even if a class is used privately, it’s a good practice to have meaningful docstrings.
9. String representations are useful for inspection purposes to help users better understand your class.
