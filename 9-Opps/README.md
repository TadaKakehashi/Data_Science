# Object Oriented Programming (OOP) in Python

Object-Oriented Programming (OOP) is a programming paradigm that organizes code using **objects and classes**.  
It helps make programs **modular, reusable, and easier to maintain**.

In Python, OOP is built around **four main pillars**:

- Encapsulation
- Abstraction
- Inheritance
- Polymorphism

---

# The Four Pillars of OOP

## 1. Encapsulation

Encapsulation means **bundling data (variables) and methods (functions) together inside a class** and restricting direct access to some components.

This helps protect data from unintended modification.

### Example

```python
class BankAccount:

    def __init__(self, balance):
        self.__balance = balance   # private variable

    def deposit(self, amount):
        self.__balance += amount

    def get_balance(self):
        return self.__balance


acc = BankAccount(1000)
acc.deposit(500)
print(acc.get_balance())
```

## 2. Abstraction

Abstraction means hiding internal implementation details and showing only the necessary functionality.

Python implements abstraction using abstract classes from the abc module.

```python
from abc import ABC, abstractmethod

class Shape(ABC):

    @abstractmethod
    def area(self):
        pass


class Circle(Shape):

    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.14 * self.radius * self.radius


c = Circle(5)
print(c.area())
```

## 3. Inheritance

Inheritance allows a child class to inherit properties and methods from a parent class.
