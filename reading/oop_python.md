# Two Must-know OOP Concepts in Python

[SOURCE](https://towardsdatascience.com/2-must-know-oop-concepts-in-python-48d643a7385)

- Object oriented programming (OOP) built around the idea of having objects that belong to a particular type.
- Everything in Python is an object and every object has a type.
- These types are declared and defined using classes

Creating a class:

```python
class Employee():

    def __init__(self, emp_id, salary):
        self.emp_id = emp_id
        self.salary = salary
    
    def give_raise(self):
        self.salary = self.salary * 1.05
```

- Created a class called Employee
  - Two attributes
    - Employee id (`emp_id`)
    - `salary`
- Defined method called `give_raise`
  - Applies 5% raise

- Can create an instance of the Employee class (i.e, an object of `Employee` type)

```python
emp1 = Employee(1001, 5600)

print(emp1.salary)
5600

emp1.give_raise()

print(emp1.salary)
5880.0
```

Create a class based on another class

```python
class Manager(Employee):
    pass
```

- Manager a child class of Emplopyee class
- Copies attributes (both data and proceduaral) from parent class
- Concept is called **inheritance**
  - Not just a copy
  - Can add new attributes or modify existing ones
  
```python
mgr1 = Manager(101, 75000)
print(mgr1.salary)
```

Update give raise method so it gives 10% raise to managers

```python
class Manager(Employee):

   def give_raise(self):
      self.salary = self.salary * 1.10

mgr1 = Manager(101, 75000)
print(mgr1.salary)
75000

mgr1.give_raise()
print(mgr1.salary)
82500
```

Create new Director class

```python
class Director(Employee):

   def give_raise(self):
     self.salary = self.salary * 1.20
```

- Three different classes
- All have `give_raise` method
- Although the name of the method is the same, it behaves differently for different types of objects
- Example of **Polymorphism**


```python
def bulk_raise(list_of_emps):
   for emp in list_of_emps:
      emp.give_raise()
```

The bulk_raise function takes a list of employees and apply the give_raise function to each object in the list. The next step is to create a list of employees of different types.

```python
emp1 = Employee(101, 45000)
emp2 = Manager(103, 60000)
emp3 = Director(105, 70000)
list_of_emps = [emp1, emp2, emp3]
```

Our list contains one employee, one manager, and one director objects. We can now call the bulk_raise function.

```python
bulk_raise(list_of_emps)

print(emp1.salary)
47250.0

print(emp2.salary)
66000.0

print(emp3.salary)
84000.0
```

Although each object in the list has a different type, we do not have to explicitly state it in our function. Python knows which `give_raise` method to apply.

## Conclusion

- Both **inheritance** and **polymorphism** are fundamental concepts of object oriented programming.
- Inheritance is a great way to eliminate unnecessary repetitive code.
  - A child class can inherit from the parent class partially or entirely.
- Polymorphism contributes to Python’s flexibility as well. An object with a particular type can be used as if it belonged to a different type.