# Two Must-know OOP Concepts in Python

- Object oriented programming (OOP) built around the idea of having objects that belong to a particular type.
- Everything in Python is an object and every object has a type.
- These types are declared and defined using classes

Creating a class:

```
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
- Definied method called `give_raise`
  - Applies 5% raise 