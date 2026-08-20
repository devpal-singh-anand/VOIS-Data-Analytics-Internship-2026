# Three Building Blocks of Python

## Learning Objectives

The learning objective is to gain knowledge on:

* using Python functionality to interact with users.
* accepting and process user input during program execution.
* displaying output using Python.
* controling the flow of program execution using conditional statements.
* implementing repetition using Python loops.
* using `while` and `for` loops appropriately.
* understanding loop control, nested loops, and infinite loops.
* using the `break` statement to terminate a loop.
* creating and call user-defined Python functions.
* understanding function parameters and arguments.
* using required, keyword, default, and variable-length arguments.
* building more structured and reusable Python programs.

---

## Prerequisites

* Basic knowledge of Python programming.
* Familiarity with Python variables and basic operators.
* Basic understanding of Boolean expressions and conditions.

---

# About the Course

This course introduces the **three major building blocks of Python programming**:

1. User interaction
2. Execution control
3. Repetition

The course also introduces **Python functions**, which allow programs to be organized into reusable blocks of code.

The course is intended to develop the ability to interact with users during program execution and to create fully functional programs using conditional statements, loops, and user-defined functions.

---

# User Interaction

Python provides functionality that allows programs to interact with users during execution.

User interaction mainly involves:

* Receiving input from the user.
* Processing the input.
* Displaying output to the user.

---

# User Interaction Input

The Python `input()` function is used to read input from the user's keyboard.

The `input()` function reads a line of text and returns it as a **string**.

## Basic Syntax

```python
input()
```

A prompt can be provided to the user:

```python
name = input("What's your name? ")
```

If the user enters:

```text
Paris Hilton
```

the value stored in `name` will be:

```text
Paris Hilton
```

---

# Reading Numbers from User Input

The `input()` function returns a string, even when the user enters a number.

Therefore, the input can be converted to another data type when required.

## Reading an Integer

The `int()` function can be used to convert the input to an integer.

```python
age = int(input("How old are you? "))
```

Example:

```text
How old are you? 53
```

The value stored in `age` is:

```text
53
```

---

## Reading a Floating-Point Number

The `float()` function can be used when the user needs to enter a decimal number.

```python
height = float(input("Enter your height: "))
```

For example:

```text
Enter your height: 5.8
```

The value is converted to a floating-point number.

> **Important:** If the user enters something that cannot be converted to the requested numeric type, Python will raise a conversion error.

---

# User Interaction Output

Python uses the `print()` function to display information on the screen.

## Basic Syntax

```python
print(value)
```

Example:

```python
print("Hello Python")
```

Output:

```text
Hello Python
```

---

## Printing Variables

The `print()` function can also display the value stored in a variable.

```python
name = "Python"
print(name)
```

Output:

```text
Python
```

---

## Printing Multiple Values

Multiple values can be passed to `print()`.

```python
name = "Python"
print("Hello", name)
```

Output:

```text
Hello Python
```

By default, multiple arguments passed to `print()` are separated by a space and the output ends with a newline.

---

# User Interaction Example

A simple program can ask the user for their age and calculate the number of years remaining until retirement.

```python
age = int(input("How old are you? "))

print("Your age is", age)
print(65 - age, "years to retirement")
```

Example execution:

```text
How old are you? 53
Your age is 53
12 years to retirement
```

This demonstrates:

* User input using `input()`
* String-to-integer conversion using `int()`
* Variable storage
* Arithmetic operations
* Output using `print()`

---

# Execution Control

Programs designed to solve real-world problems need to control the **flow of execution**.

Different statements may need to be executed depending on conditions during program execution.

Control structures allow programs to determine which statements should be executed and when.

A programming language that supports such control structures is commonly described as supporting **structured programming**.

The main control structures covered in this course include:

* Conditional constructs
* Loops
* Functions

---

# Conditional Constructs

A conditional construct allows a program to execute a selected block of code based on the evaluation of one or more Boolean expressions.

The most common conditional structures in Python are:

* `if`
* `if-else`
* `if-elif-else`

---

# `if` Statement

The `if` statement executes a block of code when a specified condition evaluates to `True`.

## Syntax

```python
if condition:
    statement
```

The condition is a Boolean expression.

Example:

```python
age = 20

if age >= 18:
    print("You are an adult")
```

The statement inside the `if` block is executed only when the condition is true.

---

# `if-else` Statement

The `if-else` statement provides two possible execution paths.

If the condition is true, the first block is executed.

If the condition is false, the `else` block is executed.

## Syntax

```python
if condition:
    statement1
else:
    statement2
```

Example:

```python
age = 16

if age >= 18:
    print("You are an adult")
else:
    print("You are a minor")
```

Output:

```text
You are a minor
```

---

# Multi-Way Decisions

Sometimes a program needs to make a decision between more than two possibilities.

Python provides the `elif` statement for this purpose.

`elif` is short for **else if**.

## Syntax

```python
if condition1:
    body1
elif condition2:
    body2
elif condition3:
    body3
else:
    body4
```

Each condition is evaluated in order.

If the first condition is true, its corresponding block is executed and the remaining conditions are skipped.

If the first condition is false, Python evaluates the next condition.

This continues until a true condition is found.

If none of the conditions is true, the optional `else` block is executed.

---

## Multi-Way Decision Example

```python
marks = 75

if marks >= 90:
    print("Grade A")
elif marks >= 75:
    print("Grade B")
elif marks >= 60:
    print("Grade C")
else:
    print("Grade D")
```

Output:

```text
Grade B
```

---

# Characteristics of Conditional Constructs

Each condition is a Boolean expression.

Each conditional body contains one or more statements that are executed when its condition is satisfied.

For example:

```python
if condition1:
    body1
elif condition2:
    body2
else:
    body3
```

The conditions are evaluated from top to bottom.

Only the block associated with the first true condition is executed.

The final `else` clause is optional.

There can be any number of `elif` clauses.

---

# Repetition

Repetition means executing a section of a program multiple times.

Loops are used when a task needs to be performed repeatedly.

A loop generally continues executing while a particular condition is satisfied or while elements remain in a sequence.

Examples of situations where loops can be used include:

* Repeating a process while a condition is true.
* Processing multiple values.
* Repeating an operation a specific number of times.
* Processing items in a sequence.

---

# Basic Structure of Loops

A typical loop contains the following components:

1. Initialize the loop control.
2. Test the loop control against a stopping condition.
3. Execute the body of the loop.
4. Update the loop control.
5. Return to the condition check.

The loop control determines whether the repetition should continue.

---

# Types of Loops

Loops can be classified based on when the stopping condition is checked.

The two general types are:

1. **Pre-test loops**
2. **Post-test loops**

---

# Pre-Test Loops

A pre-test loop checks the stopping condition **before** executing the body of the loop.

Therefore, a pre-test loop may execute:

* Zero times
* One time
* Multiple times

If the condition is false when the loop is first reached, the loop body is not executed.

Python's `while` loop is a pre-test loop.

---

# Post-Test Loops

A post-test loop checks the stopping condition **after** executing the loop body.

Therefore, a post-test loop executes its body at least once.

A traditional post-test loop is not directly implemented as a separate loop construct in Python.

The behavior can instead be simulated using a `while` loop and appropriate logic.

---

# `while` Loop

The `while` loop is a pre-test loop.

It is useful when the number of repetitions is not known in advance and the loop should continue while a condition remains true.

## Syntax

```python
while boolean_expression:
    body
```

The Boolean expression is evaluated before every iteration.

---

## Simple `while` Loop

```python
i = 1

while i <= 5:
    print(i)
    i += 1
```

Output:

```text
1
2
3
4
5
```

The loop:

1. Initializes `i` to `1`.
2. Checks whether `i <= 5`.
3. Executes the loop body.
4. Increments `i`.
5. Checks the condition again.

---

# Compound Conditions in a `while` Loop

A `while` loop can use compound Boolean expressions.

Example:

```python
while age >= 18 and age <= 60:
    print("Eligible age")
```

Multiple Boolean conditions can be combined using operators such as:

* `and`
* `or`
* `not`

---

# `for` Loop

The `for` loop is commonly used to iterate through a sequence or a range of values.

The `range()` function is frequently used with `for`.

## Basic Syntax

```python
for variable in range(start, stop, step):
    body
```

The `stop` value is **excluded** from the generated range.

---

# `range()` Function

The `range()` function can be used to generate a sequence of numbers.

Its common form is:

```python
range(start, stop, step)
```

Where:

* `start` specifies the starting value.
* `stop` specifies the ending boundary and is excluded.
* `step` specifies the increment.

---

## Example Using `range()`

```python
for i in range(1, 6, 1):
    print(i)
```

Output:

```text
1
2
3
4
5
```

The value `6` is not included.

---

# Understanding `range(1, 6, 1)`

The range:

```python
range(1, 6, 1)
```

produces:

```text
1
2
3
4
5
```

The loop control takes each of these values in sequence.

After the loop completes, the loop variable retains the last assigned value in normal Python execution.

For example:

```python
for i in range(1, 6):
    print(i)

print(i)
```

The final `print(i)` displays:

```text
5
```

---

# `for` Loop with a Step Value

The increment does not have to be `1`.

For example:

```python
for i in range(0, 101, 5):
    print(i)
```

Output begins:

```text
0
5
10
15
20
...
95
100
```

This is useful when processing values using a fixed increment.

---

# Loop Control and Increment

For a loop to terminate correctly, its control condition must eventually become false.

For example:

```python
i = 1

while i <= 5:
    print(i)
    i += 1
```

The value of `i` is updated after every iteration.

If the loop control is never updated appropriately, the loop may never terminate.

---

# Infinite Loops

An **infinite loop** is a loop that never ends because its stopping condition is never reached.

Example:

```python
i = 1

while i <= 5:
    print(i)
```

The value of `i` never changes.

Therefore, the condition:

```python
i <= 5
```

always remains true.

This creates an infinite loop.

Infinite loops can be caused by:

* Logic errors.
* Failing to update the loop control.
* Updating the loop control incorrectly.
* Never moving the loop control toward the stopping condition.

---

# `break` Statement

The `break` statement is used to terminate a loop immediately.

It provides a way to stop repetition independently of the loop's normal stopping condition.

## Example

```python
i = 1

while i <= 10:
    if i == 5:
        break
    print(i)
    i += 1
```

Output:

```text
1
2
3
4
```

When `i` becomes `5`, the `break` statement terminates the loop.

---

# Nested Loops

A **nested loop** is a loop placed inside another loop.

Example:

```python
for i in range(1, 4):
    for j in range(1, 4):
        print(i, j)
```

The inner loop executes for each iteration of the outer loop.

Nested loops are useful when working with:

* Tables
* Grids
* Multi-dimensional data
* Repeated combinations of values

Nested loops can be more challenging for beginners because multiple loop controls must be tracked simultaneously.

---

# Python Functions

A **function** is a block of organized and reusable code designed to perform a specific related action.

Functions provide:

* Better modularity.
* Code reuse.
* Better program organization.
* Easier maintenance.

Python provides many built-in functions, such as:

```python
print()
input()
```

Python also allows programmers to create their own functions.

These are called **user-defined functions**.

---

# Defining a Function

A function is defined using the keyword:

```python
def
```

## General Syntax

```python
def function_name(parameters):
    statements
```

The function definition consists of:

* The `def` keyword.
* The function name.
* Parentheses containing optional parameters.
* A colon `:`.
* An indented function body.

---

## Function Example

```python
def greet():
    print("Hello Python")
```

The function can then be called:

```python
greet()
```

Output:

```text
Hello Python
```

---

# Calling a Function

Defining a function does not automatically execute it.

The function must be called.

Example:

```python
def greet():
    print("Hello Python")

greet()
```

The statement:

```python
greet()
```

calls the function.

A function can be called multiple times.

```python
def greet():
    print("Hello Python")

greet()
greet()
```

Output:

```text
Hello Python
Hello Python
```

---

# Function Parameters

Parameters allow information to be passed into a function.

Example:

```python
def greet(name):
    print("Hello", name)
```

The function can be called with an argument:

```python
greet("Python")
```

Output:

```text
Hello Python
```

Here:

* `name` is a parameter.
* `"Python"` is an argument.

---

# Positional Arguments

Function parameters can receive values based on their position.

Example:

```python
def add(a, b):
    print(a + b)
```

Calling:

```python
add(10, 20)
```

assigns:

```text
a = 10
b = 20
```

The order of the arguments matters when using positional arguments.

---

# Return Statement

The `return` statement is used to return a value from a function to its caller.

Example:

```python
def add(a, b):
    return a + b
```

The function can be called as:

```python
result = add(10, 20)
print(result)
```

Output:

```text
30
```

A `return` statement without an expression returns `None`.

Example:

```python
def test():
    return
```

This is equivalent to returning `None`.

---

# Function Arguments

Python functions can use different types of arguments.

The course introduces:

1. Required arguments
2. Keyword arguments
3. Default arguments
4. Variable-length arguments

---

# Required Arguments

Required arguments must be supplied when calling the function.

Example:

```python
def greet(name):
    print("Hello", name)
```

Correct call:

```python
greet("Python")
```

If the required argument is not supplied, Python raises an error.

---

# Keyword Arguments

Keyword arguments are supplied using the parameter name.

Example:

```python
def student(name, age):
    print(name, age)
```

The function can be called using:

```python
student(name="Dev", age=23)
```

Keyword arguments make the relationship between values and parameters explicit.

---

# Default Arguments

A default argument has a predefined value that is used when the caller does not provide a value.

Example:

```python
def greet(name="Python"):
    print("Hello", name)
```

Calling:

```python
greet()
```

produces:

```text
Hello Python
```

A different value can also be provided:

```python
greet("Developer")
```

Output:

```text
Hello Developer
```

---

# Variable-Length Arguments

Variable-length arguments allow a function to accept more arguments than the number explicitly specified in the function definition.

Python provides syntax for collecting additional positional arguments using `*args`.

Example:

```python
def add_numbers(*numbers):
    total = 0

    for number in numbers:
        total += number

    return total
```

The function can accept different numbers of arguments:

```python
print(add_numbers(10, 20))
print(add_numbers(10, 20, 30))
```

Output:

```text
30
60
```

Variable-length arguments are useful when the number of arguments is not known in advance.

---

# Function Reusability

One of the major advantages of functions is **code reuse**.

Instead of repeatedly writing the same code:

```python
print("Hello Python")
print("Hello Python")
print("Hello Python")
```

a function can be created:

```python
def greet():
    print("Hello Python")
```

and called multiple times:

```python
greet()
greet()
greet()
```

This makes programs easier to organize and maintain.

---

# Three Building Blocks of Python

The major concepts covered in this course can be summarized as:

## 1. User Interaction

Programs can communicate with users using:

```python
input()
print()
```

---

## 2. Execution Control

Programs can make decisions using:

```python
if
elif
else
```

---

## 3. Repetition

Programs can repeat operations using:

```python
while
for
```

Loop control can also be performed using:

```python
break
```

---

## Functions

Functions provide a way to organize and reuse code:

```python
def function_name():
    statements
```

These concepts provide a foundation for creating structured and functional Python programs.

---

# Control Structures Quick Reference

| Construct   | Purpose                                |
| ----------- | -------------------------------------- |
| `if`        | Executes code when a condition is true |
| `if-else`   | Selects between two execution paths    |
| `elif`      | Tests additional conditions            |
| `while`     | Repeats while a condition is true      |
| `for`       | Iterates through a sequence or range   |
| `range()`   | Generates a sequence of numbers        |
| `break`     | Terminates a loop immediately          |
| Nested loop | Places one loop inside another         |

---

# User Interaction Quick Reference

| Function  | Purpose                                     |
| --------- | ------------------------------------------- |
| `input()` | Reads user input as a string                |
| `int()`   | Converts a value to an integer              |
| `float()` | Converts a value to a floating-point number |
| `print()` | Displays output                             |

---

# Function Quick Reference

| Concept                  | Description                                      |
| ------------------------ | ------------------------------------------------ |
| `def`                    | Defines a function                               |
| Function                 | Reusable block of code                           |
| Parameter                | Variable defined in a function                   |
| Argument                 | Value passed to a function                       |
| `return`                 | Returns a value from a function                  |
| Required argument        | Argument that must be supplied                   |
| Keyword argument         | Argument supplied using its parameter name       |
| Default argument         | Parameter with a predefined value                |
| Variable-length argument | Allows a function to accept additional arguments |

---

# Basic Python Program Example

The following example combines user interaction, conditional execution, repetition, and a function.

```python
def greet(name):
    print("Hello", name)


name = input("What is your name? ")

greet(name)

age = int(input("How old are you? "))

if age >= 18:
    print("You are an adult.")
else:
    print("You are a minor.")

for i in range(1, 4):
    print("Iteration:", i)
```

This example demonstrates:

* User input.
* Variables.
* A user-defined function.
* Function parameters.
* Function calls.
* Conditional statements.
* A `for` loop.
* The `range()` function.
* Output using `print()`.

---

# Important Concepts to Remember

## `input()` Returns a String

Even if the user enters a number:

```python
age = input("Enter your age: ")
```

`age` is initially a string.

For numeric calculations, convert it:

```python
age = int(input("Enter your age: "))
```

---

## `if` Conditions Must Be Boolean Expressions

Example:

```python
if age >= 18:
    print("Adult")
```

The condition:

```python
age >= 18
```

is evaluated as either `True` or `False`.

---

## `range()` Excludes the Stop Value

For:

```python
range(1, 6)
```

the values are:

```text
1
2
3
4
5
```

`6` is not included.

---

## Loop Control Must Progress

A loop should eventually reach its stopping condition.

For example:

```python
i = 1

while i <= 5:
    print(i)
    i += 1
```

The increment:

```python
i += 1
```

moves the loop toward termination.

---

## Functions Must Be Called

Defining:

```python
def greet():
    print("Hello")
```

does not execute the function.

It must be called:

```python
greet()
```

---

# Course Summary

The course concludes with a knowledge assessment covering:

* User interaction input
* User interaction output
* Conditional constructs
* `if-else` statements
* Multi-way decisions
* Repetition
* Types of loops
* `while` loops
* `for` loops
* `range()`
* Loop control
* `break`
* Nested loops
* Infinite loops
* Python functions
* Function parameters and arguments
* Required arguments
* Keyword arguments
* Default arguments
* Variable-length arguments
* `return` statements

---

## Course Files

```text
05-Three-Building-Blocks-of-Python/
├── lectures.md
├── assessment.md
└── certificate.pdf
```
