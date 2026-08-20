# Getting Started with Class and Objects

## Learning Objectives

The learning objective is to gain knowledge on:

* understanding the basic concepts of **Object-Oriented Programming (OOP)**.
* modeling problems using **classes and objects**.
* creating classes and objects in Python.
* adding member functions to classes.
* creating constructors in Python.
* understanding and implement **inheritance** in Python.

---

## Prerequisites

* Basic knowledge of Python syntax.
* Knowledge of writing and invoking functions.
* Understanding of creating variables.
* Familiarity with reading inputs and generating outputs from the Python console.
* Familiarity with using a text editor.
* Knowledge of how to execute a Python program.
* Basic knowledge of Python keywords.

---

# About the Course

This course introduces the concepts of **classes and objects** in Python and provides an introduction to **Object-Oriented Programming (OOP)**.

---

# What is Object-Oriented Programming?

**Object-Oriented Programming (OOP)** is a programming paradigm based on the idea of grouping related **data and functions** into units called **objects**.

These objects represent entities that contain:

* Data
* Attributes
* Functions or behaviors

Regardless of the programming paradigm being used, programs generally follow a series of steps to solve problems.

### Data Input

Data is read from a source such as:

* A file system
* A database
* User input
* Other data sources

### Data Processing

The data is interpreted and possibly altered or processed before being displayed.

### Data Output

The processed data is presented so that it can be read or interacted with by:

* A user
* Another system
* A device

---

# Modeling Problems

During the modeling phase, a description of a particular domain or problem is analyzed to identify the important concepts and actions.

## Identifying Actors

The first step is to identify **actors**.

Actors are entities that perform actions.

### Example

A printer can be considered an actor.

Its action may be:

```text
Print
```

After identifying the actors, examine:

1. What they do.
2. Their behavior.
3. The data they need to perform their actions.

In Object-Oriented Programming:

* Actors become **objects**.
* Their traits or properties become **data/attributes**.
* Their behaviors become **functions/methods**.

Therefore, modeling in OOP combines:

* Data
* Algorithms
* Output/behavior

---

# Classes and Objects

A **class** is a description or template for something.

It is not a concrete object itself. Instead, it provides a blueprint that defines what an object should contain and what it can do.

A class generally consists of:

* Attributes
* Methods
* Constructor
* Operations

---

# What is an Object?

An **object** is an instance of a class that represents something within a system.

An object can:

* Have properties.
* Perform actions.
* Change its state.
* Interact with other objects.

---

# Real-World Example of Objects

Imagine you are in a car park.

You may see many cars with different:

* Makes
* Models
* Colors
* Types

For example:

```text
Make: Ferrari
Model: 488
Color: Red
Type: Sports Car
```

Another object might be:

```text
Make: Ford
Model: Mustang
Color: Yellow
Type: Sports Car
```

The properties help identify and describe individual objects.

---

# What is a Class?

A **class** is a data type that acts as a template or blueprint for a particular kind of object.

A useful way to remember the relationship is:

> **Class = Blueprint**
> **Object = Actual instance created from the blueprint**

### Example

A car blueprint represents the **class**.

An actual Honda Accord or Jeep Wrangler represents an **object** created from that class.

---

# Examples of Classes and Objects

| Class / Blueprint | Objects                        |
| ----------------- | ------------------------------ |
| Car               | Honda Accord, Jeep Wrangler    |
| Cat               | Garfield                       |
| Ice Cream         | Strawberry, Chocolate, Vanilla |

The class describes what an object should look like, while the object is the actual instance.

---

# Creating a Class in Python

A class in Python is created using the `class` keyword.

### Syntax

```python
class ClassName:
    pass
```

### Example

```python
class Car:
    pass
```

This creates a class named `Car`.

---

# Creating an Object from a Class

Creating an object from a class is called **instantiation**.

To instantiate a class, use parentheses after the class name.

### Example

```python
class Car:
    pass

car1 = Car()
```

Here:

* `Car` is the class.
* `car1` is the variable holding the object.
* `Car()` creates/instantiates the object.

Therefore:

```python
car1 = Car()
```

means that an object of the `Car` class has been created.

---

# Constructor

Many programming languages provide a special function called a **constructor**.

A constructor is invoked when an object is first created.

In Python, the constructor is commonly written as:

```python
def __init__(self):
```

The constructor is used to initialize the attributes of an object.

---

# The `self` Parameter

The `self` parameter refers to the **current object instance**.

It allows attributes and methods to be associated with the specific object.

### Example

```python
class Car:

    def __init__(self):
        self.color = "Red"
```

Here:

```python
self.color
```

is an attribute belonging to the particular object instance.

---

# Initializing Attributes in a Class

Attributes can be initialized inside the constructor.

### Example

```python
class Elevator:

    def __init__(self, make, floor):
        self.make = make
        self.floor = floor
```

When creating an object, values must be supplied for the required parameters.

```python
elevator1 = Elevator("OTIS", 5)
```

The object now has attributes such as:

```text
make = OTIS
floor = 5
```

---

# Simple Class Example

```python
class MyClass:
    pass

object_a = MyClass()
```

Here:

* `MyClass` is the class.
* `object_a` is an instance of `MyClass`.

---

# Class Attributes and Instance Attributes

Python classes can contain both **class attributes** and **instance attributes**.

### Example

```python
class Dog:

    species = "Canis familiaris"

    def __init__(self, name, age):
        self.name = name
        self.age = age
```

Here:

```python
species
```

is a **class attribute**.

While:

```python
name
age
```

are **instance attributes**.

---

# Creating Dog Objects

To create objects from the `Dog` class, values must be provided for `name` and `age`.

```python
buddy = Dog("Buddy", 9)
miles = Dog("Miles", 4)
```

This creates two separate Dog objects:

```text
Buddy → 9 years old
Miles → 4 years old
```

If required arguments are not provided, Python raises an error.

---

# Instance Methods

**Instance methods** are functions defined inside a class.

They can be called from an instance of that class.

The first parameter of an instance method is conventionally:

```python
self
```

### Example

```python
class Dog:

    def __init__(self, name, age):
        self.name = name
        self.age = age

    def description(self):
        return f"{self.name} is {self.age} years old"
```

Now:

```python
miles = Dog("Miles", 4)

print(miles.description())
```

Output:

```text
Miles is 4 years old
```

The `description()` method accesses the attributes belonging to the particular object.

---

# Rectangle Class Example

A class can contain multiple methods.

For example, a `Rectangle` class can contain methods for calculating:

* Area
* Perimeter

### Example

```python
class Rectangle:

    def __init__(self, length, width):
        self.length = length
        self.width = width

    def get_area(self):
        return self.length * self.width

    def get_perimeter(self):
        return 2 * (self.length + self.width)
```

The methods operate on the attributes of the object.

---

# Inheritance

**Inheritance** is the process by which one class takes on the attributes and methods of another class.

The newly created class is called the:

**Child class / Derived class**

The class from which it inherits is called the:

**Parent class / Base class**

Inheritance allows code to be reused and extended.

---

# Types of Inheritance

Python supports several forms of inheritance.

## 1. Single Inheritance

A derived class inherits characteristics from a **single parent class**.

```text
Parent
  ↓
Child
```

---

## 2. Multilevel Inheritance

A derived class inherits from a parent class that itself inherits from another parent.

```text
Grandparent
     ↓
   Parent
     ↓
   Child
```

---

## 3. Hierarchical Inheritance

More than one derived class inherits from the same parent class.

```text
       Parent
       /    \
      ↓      ↓
   Child1  Child2
```

---

## 4. Multiple Inheritance

A single derived class inherits properties from **more than one base class**.

```text
Parent 1 ──┐
           ↓
         Child
           ↑
Parent 2 ──┘
```

---

# Overriding and Extending Parent Classes

A child class can:

* Inherit attributes from a parent.
* Inherit methods from a parent.
* Add its own attributes.
* Add its own methods.
* Override inherited methods.

Therefore, a child class can extend the functionality provided by its parent class.

---

# Example of Inheritance in Python

Consider a base class called `Animal`.

```python
class Animal:

    def eat(self):
        print("Animal is eating")

    def sleep(self):
        print("Animal is sleeping")
```

A `Dog` class can inherit from `Animal`:

```python
class Dog(Animal):

    def bark(self):
        print("Dog is barking")
```

Now a `Dog` object can use both its inherited methods and its own method:

```python
dog = Dog()

dog.eat()
dog.sleep()
dog.bark()
```

The `Dog` class inherits:

```text
eat()
sleep()
```

from `Animal`, while defining its own:

```text
bark()
```

---

# Key Concepts to Remember

| Concept                 | Meaning                                           |
| ----------------------- | ------------------------------------------------- |
| **Class**               | Blueprint/template for creating objects           |
| **Object**              | Instance of a class                               |
| **Instantiation**       | Creating an object from a class                   |
| **Constructor**         | Special method used when an object is created     |
| `__init__()`            | Python constructor method                         |
| `self`                  | Refers to the current object instance             |
| **Attribute**           | Data/property belonging to a class or object      |
| **Method**              | Function defined inside a class                   |
| **Inheritance**         | Mechanism for deriving a class from another class |
| **Parent/Base Class**   | Class being inherited from                        |
| **Child/Derived Class** | Class that inherits from another class            |

---

## Course Files

```text
09-Getting-Started-with-Class-and-Objects/
├── lecture.md
├── assessment.md
└── certificate.pdf
```
