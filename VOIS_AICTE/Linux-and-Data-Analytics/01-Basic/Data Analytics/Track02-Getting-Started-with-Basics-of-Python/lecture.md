# Getting Started with Basics of Python

## Learning Objectives

The learning objective is to gain knowledge on:

* understanding the basics of **Python programming**.
* using variables to store, retrieve, and calculate information.
* reading and comprehend basic Python code.
* writing Python scripts for general productivity tasks.
* applying basic operators in Python.
* understanding Python literals, identifiers, keywords, and variables.
* understanding the fundamentals required to progress toward **Object-Oriented Programming**.
* working with basic Python programs using a **Jupyter Notebook**.

---

## Prerequisites

* Basic understanding of programming concepts.
* Basic familiarity with computers and programming environments.
* Access to Python or a **Jupyter Notebook** environment.

---

# About the Course

This course introduces the fundamental concepts of **Python programming**.

The course is intended to develop the ability to:

* Create and use Python variables.
* Apply basic operators in Python.
* Read and understand Python code.
* Write simple Python scripts.
* Build a foundation for advanced Python programming and Object-Oriented Programming.

Python was invented in the Netherlands in the early 1990s by **Guido van Rossum**.

The language was named after the comedy group **Monty Python**.

Python was open-source from the beginning and is commonly used as a general-purpose programming and scripting language.

Python supports multiple programming paradigms, including:

* Object-oriented programming
* Functional programming
* General-purpose scripting

Python has become increasingly popular and is widely used in areas such as automation, data analysis, web development, and artificial intelligence.

---

# Compiler and Interpreter

Programming languages need to be translated into a form that a computer can execute.

---

## Compiler

A **compiler** is a program that translates a complete program into machine code before the program is executed.

A compiler generally:

* Processes the entire program.
* Checks various errors and constraints.
* Translates the program into machine code.
* May require more memory during compilation.
* Can provide faster execution after compilation because the program has already been translated.

The compiler goes through the entire program before producing the translated output.

---

## Interpreter

An **interpreter** is a program that translates and executes programming instructions progressively.

Unlike the traditional compiler model, an interpreter does not translate the entire program into machine code before execution.

Interpreters are generally smaller than compilers.

Python is commonly described as an **interpreted programming language**.

> **Note:** Modern Python internally compiles source code into bytecode before execution, but Python is traditionally introduced as an interpreted language.

---

# Literals and Identifiers

In programming, literals represent fixed values, while identifiers are names used to identify program elements.

Consider the following statement:

```python
x = 123
````

Here:

* `x` is an **identifier**.
* `123` is a **literal**.
* `=` is the **assignment operator**.

---

# Python Literals

A **literal** is a fixed value written directly in a Python program.

Python supports several types of literals.

---

## Integer Literals

Integer literals represent whole numbers.

They can be:

* Positive
* Negative
* Zero

Integer literals do not contain fractional parts.

Examples:

```python
10
25
0
-15
1000
```

---

## Floating-Point Literals

Floating-point literals represent numbers containing an integer and fractional component.

Examples:

```python
3.14
10.5
-2.75
0.5
```

---

## Binary Literals

Binary literals represent numbers using the binary number system.

They are written using the prefix:

```text
0b
```

or:

```text
0B
```

Examples:

```python
0b1010
0b1111
```

---

## Octal Literals

Octal literals represent numbers using the octal number system.

They use the prefix:

```text
0o
```

or:

```text
0O
```

Examples:

```python
0o12
0o17
```

---

## Hexadecimal Literals

Hexadecimal literals represent numbers using the hexadecimal number system.

They use the prefix:

```text
0x
```

or:

```text
0X
```

Examples:

```python
0x10
0xFF
```

---

# Boolean Literals

Python has two Boolean literals:

```python
True
False
```

They represent logical truth values.

Example:

```python
is_logged_in = True
```

Boolean values are commonly used in conditions and logical expressions.

---

# String Literals

A **string literal** is a sequence of characters enclosed within quotation marks.

Python supports single quotes, double quotes, and triple quotes.

## Single Quotes

```python
'Hello Python'
```

## Double Quotes

```python
"Hello Python"
```

## Triple Quotes

Triple quotes can be used for multi-line strings.

```python
"""Hello
Python
World"""
```

---

# Special Literal

Python has one special literal:

```python
None
```

`None` represents the absence of a value.

Example:

```python
result = None
```

---

# Identifiers

An **identifier** is a name used to identify a:

* Variable
* Function
* Class
* Module
* Object
* Other programming element

Example:

```python
student_name = "Dev"
```

Here:

```text
student_name
```

is an identifier.

---

# Python Identifier Naming Rules

Python identifiers follow specific naming rules.

An identifier:

* Can start with a letter.
* Can start with an underscore `_`.
* Can contain letters.
* Can contain digits from `0` to `9`.
* Can contain underscores.
* Cannot start with a digit.
* Cannot contain punctuation characters.
* Is case-sensitive.

---

## Valid Identifiers

Examples of valid identifiers:

```python
name
student_name
age2
total_marks
_private
```

---

## Invalid Identifiers

Examples of invalid identifiers:

```python
2name
student-name
student@name
student name
```

---

# Case Sensitivity

Python is a **case-sensitive programming language**.

This means that uppercase and lowercase letters are treated differently.

For example:

```python
name = "Python"
Name = "Java"
```

`name` and `Name` are two different identifiers.

Similarly:

```python
variable
Variable
VARIABLE
```

are different identifiers.

---

# Underscores in Identifiers

Python uses underscores as part of identifier naming conventions.

## Single Leading Underscore

An identifier beginning with a single underscore conventionally indicates an internal or non-public name.

Example:

```python
_private_variable
```

---

## Double Leading Underscore

An identifier beginning with two underscores has special behavior in classes and is associated with name mangling.

Example:

```python
__private_variable
```

---

## Leading and Trailing Double Underscores

Identifiers that begin and end with two underscores are commonly used for Python-defined special names.

Examples:

```python
__init__
__name__
__str__
```

These are commonly called **dunder names**.

---

# Keywords / Reserved Words

**Keywords**, also called **reserved words**, have special meanings in the Python language.

They are defined by the Python interpreter and generally cannot be used as ordinary identifiers.

Examples include:

```python
if
else
for
while
def
class
return
import
True
False
None
and
or
not
```

Keywords are an important part of Python syntax.

---

# Variables

Variables are used for **storing information** that a program needs to use or process.

A variable can be thought of as a name associated with a value.

---

## Creating a Variable

Example:

```python
some_variable = 10
```

Here:

* `some_variable` is the variable.
* `10` is the value.
* `=` is the assignment operator.

A variable can later be assigned another value.

```python
some_variable = 20
```

The variable now contains the new value.

---

# Assignment Operator

The equals sign:

```python
=
```

is called the **assignment operator**.

It assigns the result of the expression on the right-hand side to the variable on the left-hand side.

Example:

```python
x = 10
```

The right-hand side can contain a mathematical expression.

```python
x = 5 + 9
```

Multiple variables can also be used.

```python
a = 10
b = 5
c = a + b
```

When a variable appears on the right-hand side of an expression, Python uses the value currently associated with that variable.

---

# Python Variable Types

Variables can refer to values of different types.

Basic types introduced in this course include:

* Integer
* Floating-point number
* Boolean
* String

Examples:

```python
age = 20
price = 99.50
is_active = True
name = "Python"
```

---

# Operators

Operators are constructs used to manipulate and evaluate data.

Python provides several categories of operators:

1. Arithmetic operators
2. Assignment operators
3. Comparison operators
4. Logical operators
5. Membership operators
6. Bitwise operators
7. Identity operators

---

# Arithmetic Operators

Arithmetic operators are used to perform mathematical calculations.

| Operator | Operation      |
| -------- | -------------- |
| `+`      | Addition       |
| `-`      | Subtraction    |
| `*`      | Multiplication |
| `/`      | Division       |
| `//`     | Floor division |
| `%`      | Modulo         |
| `**`     | Exponentiation |

---

# Addition and Subtraction

The `+` operator performs addition.

Example:

```python
10 + 5
```

Output:

```text
15
```

The `-` operator performs subtraction.

Example:

```python
10 - 5
```

Output:

```text
5
```

Addition and subtraction have lower precedence than multiplication and division.

---

# Multiplication and Division

The `*` operator performs multiplication.

Example:

```python
10 * 5
```

Output:

```text
50
```

The `/` operator performs division.

Example:

```python
10 / 5
```

Output:

```text
2.0
```

Multiplication and division have higher precedence than addition and subtraction.

---

# Floor Division

The `//` operator performs **floor division**.

It divides two numbers and returns the floor of the result.

Example:

```python
10 // 3
```

Output:

```text
3
```

Floor division removes the fractional part for positive operands by taking the floor of the mathematical result.

---

# Modulo Operator

The `%` operator is called the **modulo operator**.

It returns the remainder after division.

Example:

```python
10 % 3
```

Output:

```text
1
```

Because:

```text
10 = 3 × 3 + 1
```

---

# Exponentiation Operator

The `**` operator is used for **exponentiation**.

It raises one number to the power of another number.

Example:

```python
2 ** 3
```

Output:

```text
8
```

Because:

```text
2 × 2 × 2 = 8
```

---

# Arithmetic Expression Evaluation

Python evaluates arithmetic expressions according to operator precedence.

For example:

```python
2 + 3 * 4
```

Multiplication is performed first.

Therefore:

```text
2 + 12 = 14
```

Parentheses can change the order of evaluation.

```python
(2 + 3) * 4
```

Output:

```text
20
```

---

# Assignment Operators

Assignment operators are used to assign values to variables.

The basic assignment operator is:

```python
=
```

Python also provides combined assignment operators.

| Operator | Example   | Equivalent   |
| -------- | --------- | ------------ |
| `=`      | `x = 5`   | `x = 5`      |
| `+=`     | `x += 5`  | `x = x + 5`  |
| `-=`     | `x -= 5`  | `x = x - 5`  |
| `*=`     | `x *= 5`  | `x = x * 5`  |
| `/=`     | `x /= 5`  | `x = x / 5`  |
| `//=`    | `x //= 5` | `x = x // 5` |
| `%=`     | `x %= 5`  | `x = x % 5`  |
| `**=`    | `x **= 5` | `x = x ** 5` |

---

## Example of Combined Assignment

Instead of writing:

```python
x = x + 5
```

you can write:

```python
x += 5
```

These combined assignment operators provide a shorter way to perform an operation and assign the result back to the same variable.

---

# Comparison Operators

Comparison operators compare two values.

They always return a Boolean result:

```text
True
```

or:

```text
False
```

| Operator | Meaning                  |
| -------- | ------------------------ |
| `<`      | Less than                |
| `<=`     | Less than or equal to    |
| `>`      | Greater than             |
| `>=`     | Greater than or equal to |
| `==`     | Equal to                 |
| `!=`     | Not equal to             |

---

# Comparison Examples

Consider:

```python
a = 10
b = 20
```

### Less Than

```python
a < b
```

Output:

```text
True
```

### Less Than or Equal To

```python
a <= b
```

Output:

```text
True
```

### Greater Than

```python
a > b
```

Output:

```text
False
```

### Greater Than or Equal To

```python
a >= b
```

Output:

```text
False
```

### Equal To

```python
a == b
```

Output:

```text
False
```

### Not Equal To

```python
a != b
```

Output:

```text
True
```

> **Important:** `=` is used for assignment, while `==` is used for comparison.

---

# Logical Operators

Logical operators are sometimes called **Boolean operators**.

Python provides three main logical operators:

* `and`
* `or`
* `not`

They allow simple Boolean expressions to be combined into more complex expressions.

---

# `and` Operator

The `and` operator produces `True` when **both conditions are true**.

Example:

```python
a = 10
b = 20

a < b and b > 15
```

Both conditions are true, so the result is:

```text
True
```

### Truth Table

| A     | B     | `A and B` |
| ----- | ----- | --------- |
| False | False | False     |
| False | True  | False     |
| True  | False | False     |
| True  | True  | True      |

---

# `or` Operator

The `or` operator produces `True` when **at least one condition is true**.

Example:

```python
a = 10
b = 20

a > b or a < b
```

The second condition is true, so the overall result is:

```text
True
```

### Truth Table

| A     | B     | `A or B` |
| ----- | ----- | -------- |
| False | False | False    |
| False | True  | True     |
| True  | False | True     |
| True  | True  | True     |

---

# `not` Operator

The `not` operator reverses a Boolean value.

Example:

```python
not True
```

Output:

```text
False
```

Similarly:

```python
not False
```

Output:

```text
True
```

### Truth Table

| A     | `not A` |
| ----- | ------- |
| True  | False   |
| False | True    |

---

# Complex Expressions

Multiple operators can be combined in a single expression.

Example:

```python
a and (b or c)
```

Parentheses can be used to control the order of evaluation.

Python follows operator precedence when evaluating complex expressions.

For logical operators, the general order of precedence is:

1. `not`
2. `and`
3. `or`

For example:

```python
True or False and False
```

The `and` operation is evaluated before the `or` operation.

---

# Operator Categories Summary

| Category   | Examples                            |                         |
| ---------- | ----------------------------------- | ----------------------- |
| Arithmetic | `+`, `-`, `*`, `/`, `//`, `%`, `**` |                         |
| Assignment | `=`, `+=`, `-=`, `*=`, `/=`         |                         |
| Comparison | `<`, `<=`, `>`, `>=`, `==`, `!=`    |                         |
| Logical    | `and`, `or`, `not`                  |                         |
| Membership | `in`, `not in`                      |                         |
| Bitwise    | `&`, `                              | `, `^`, `~`, `<<`, `>>` |
| Identity   | `is`, `is not`                      |                         |

---

# Basic Python Examples

## Variables

```python
name = "Python"
age = 30
```

---

## Arithmetic Operations

```python
a = 10
b = 3

print(a + b)
print(a - b)
print(a * b)
print(a / b)
print(a // b)
print(a % b)
print(a ** b)
```

---

## Comparison Operations

```python
a = 10
b = 20

print(a < b)
print(a <= b)
print(a > b)
print(a >= b)
print(a == b)
print(a != b)
```

---

## Logical Operations

```python
age = 25

print(age >= 18 and age <= 60)
print(age < 18 or age > 60)
print(not False)
```

---

# Python Basics Quick Reference

| Concept          | Description                              |
| ---------------- | ---------------------------------------- |
| Python           | General-purpose programming language     |
| Guido van Rossum | Creator of Python                        |
| Literal          | Fixed value written directly in code     |
| Identifier       | Name used to identify a program element  |
| Keyword          | Reserved word with special meaning       |
| Variable         | Name used to refer to stored information |
| `=`              | Assignment operator                      |
| `==`             | Equality comparison                      |
| `//`             | Floor division                           |
| `%`              | Modulo/remainder                         |
| `**`             | Exponentiation                           |
| `and`            | True when both conditions are true       |
| `or`             | True when at least one condition is true |
| `not`            | Reverses a Boolean value                 |
| `True`           | Boolean true value                       |
| `False`          | Boolean false value                      |
| `None`           | Represents absence of a value            |

---

# Important Concepts to Remember

## Literal vs Identifier

```python
x = 123
```

* `x` → Identifier
* `123` → Literal

---

## Assignment vs Comparison

```python
x = 10
```

`=` assigns a value.

```python
x == 10
```

`==` compares a value.

---

## Floor Division vs Modulo

```python
10 // 3
```

Returns the floor-division result:

```text
3
```

While:

```python
10 % 3
```

returns the remainder:

```text
1
```

---

## `and` vs `or`

`and` requires both conditions to be true.

```python
condition1 and condition2
```

`or` requires at least one condition to be true.

```python
condition1 or condition2
```

---

# Course Summary

The course concludes with a knowledge assessment to check your understanding of:

* Python fundamentals
* Compiler and interpreter concepts
* Literals
* Identifiers
* Keywords and reserved words
* Variables
* Basic data types
* Arithmetic operators
* Assignment operators
* Comparison operators
* Logical operators
* Operator precedence

---

## Course Files

```text
04-Getting-Started-with-Python-Basics/
├── lectures.md
├── assessment.md
└── certificate.pdf
```
