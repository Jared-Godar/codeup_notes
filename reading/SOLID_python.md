# [The S.O.L.I.D Principles in Python](https://medium.com/geekculture/the-s-o-l-i-d-principles-in-python-a041c5aa9969)

## S — Single responsibility principle

***A class should have only one reason to change***

- Each class or module should have one responsibility, thus one reason to change the code.
- If you find that you need to change a class or module for multiple reasons, it could likely be a violation of this principle.

```python
class Car:
    def __init__(self, car_name):
        self.car_name = car_name
    def get_car_name(self):
        pass
    
    def add_car_to_garage(self, garage):
        pass
```
The above code is a violation. Aside from the main get_car_name method, if you change how the garage store the car (eg: changing data structure from list to tuples/dictionary), you need to update this Car class as well. The Car class is having additional responsibilities that should be handled by the Garage.

```python
class Car:
    def __init__(self, car_name):
        self.car_name = car_name
    def get_car_name(self):
        pass

class Garage:
    def __init__(self):
        # garage has a list of cars
        self.cars = []
    def add_car(self, car):
        pass
    def remove_car(self, car):
        pass
```

By creating another class Garage, all the responsibility of adding and removing cars is moved to the new class, and the Car class contains only the single responsibility of dealing with the car properties.

---

## Open-Closed principle

***Software entities (classes, modules, functions, etc.) should be open for extension, but closed for modification***

- We shouldn’t need to change existing codes to add new functionalities.
- One easy way to spot a violation is you have a lot of similar if-else statements in a class.

```python
class Car:
    def __init__(self, brand):
        self.brand = brand
    def print_engine_type(self):
        if self.brand == 'Tesla Model 3':
            print('Electric')
        elif self.brand == 'Audi A3':
            print('Gasoline')
        elif self.brand == 'Myvi':
            print('Gasoline')
tesla_car = Car('Tesla Model 3')
audi_car = Car('Audi A3')
myvi_car = Car('Myvi')
for car in [tesla_car, audi_car, myvi_car]:
    car.print_engine_type()  # print Electric, Gasoline, Gasoline
```

Now, if you need to add a new engine type (hybrid), you need to update the print_engine_type method in the Car class to add another if-statement.

```python
if self.brand == 'Tesla Model 3':
    print('Electric')
elif self.brand == 'Audi A3':
    print('Gasoline')
elif self.brand == 'Myvi':
    print('Gasoline')
elif self.brand == 'Some hybrid brand':
    # NEED TO ADD THIS EVERYTIME A NEW BRAND SURFACED
    print('Hybrid')
```

To fix the violation, we can create a base class Car, and extend the class for each of the different car types we have.

```python
from abc import ABC, abstractmethod
class Car(ABC):
    def __init__(self, brand):
        self.brand = brand
    @abstractmethod
    def print_engine_type(self):
        pass
class ElectricCar(Car):
    def print_engine_type(self):
        print('Electric')
class GasolineCar(Car):
    def print_engine_type(self):
        print('Gasoline')
class HybridCar(Car):
    def print_engine_type(self):
        print('Hybrid')
tesla_car = ElectricCar('Tesla Model 3')
audi_car = GasolineCar('Audi A3')
myvi_car = GasolineCar('Myvi')
jazz_car = HybridCar('Honda Jazz Hybrid')

for car in [tesla_car, audi_car, myvi_car, jazz_car]:
    car.print_engine_type()  # print Electric, Gasoline, Gasoline, Hybrid
```

As you can see, the base class Car is now closed for modification but opened for extension for any new car engine type to be created.

---

## L — Liskov substitution principle

***if S is a subtype of T, then objects of type T may be replaced with objects of type S (i.e., an object of type T may be substituted with any object of a subtype S) without altering any of the desirable properties of the program (correctness, task performed, etc.)***

- When you have a parent class (say Car) and a subclass (Tesla), any where you are using the parent class in code, you should be able to substitute it with the subclass without causing any issue.

---

## I - Interface segregation principle

***No client should be forced to depend on methods it does not use***

- If the function is not needed by the subclass, we probably shouldn’t define that interface to be inherited in the parent class.

---

## D — Dependency inversion principle

***High-level modules should not import anything from low-level modules. Both should depend on abstractions (e.g., interfaces).***

***Abstractions should not depend on details. Details (concrete implementations) should depend on abstractions.***

- A class shouldn’t need to understand the inner workings of another class for it to function properly.