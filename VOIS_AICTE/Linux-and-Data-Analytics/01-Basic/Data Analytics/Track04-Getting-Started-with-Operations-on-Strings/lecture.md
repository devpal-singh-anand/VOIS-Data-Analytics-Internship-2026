# Getting Started with Operations on String

## Learning Objectives

The learning objective is to gain knowledge on:

* creating and use Python strings.
* understanding how strings are represented in Python.
* performing basic string operations.
* handling single-line and multi-line strings.
* accessing individual characters using indexing.
* extracting portions of strings using slicing.
* understanding string immutability.
* concatenating strings.
* repeating strings using the repetition operator.
* formating strings using different techniques.
* using Python string methods to perform common string operations.

---

## Prerequisites

* Elementary knowledge of Python.
* Basic understanding of Python variables and operators.

---

# About the Course

This course introduces **Python strings** and the various operations that can be performed on them.

The course focuses on:

* Creating strings.
* Multi-line strings.
* Indexing.
* Slicing.
* String immutability.
* Concatenation.
* Repetition.
* String formatting.
* String methods.

---

# Strings

A **string** is a sequence of characters.

In Python, strings can be represented using either:

* Single quotes `' '`
* Double quotes `" "`
* Triple single quotes `''' '''`
* Triple double quotes `""" """`

### Example

```python
name = "Python"
```

or:

```python
name = 'Python'
```

Strings can contain letters, numbers, symbols, spaces, and other characters.

---

# String Immutability

Python strings are **immutable**.

This means that once a string has been created, its individual characters cannot be changed.

For example:

```python
text = "Hello"
```

The following is not allowed:

```python
text[0] = "J"
```

This produces an error because individual characters of a string cannot be modified.

Instead, a new string must be created:

```python
text = "Jello"
```

The variable `text` now refers to a new string.

> **Important:** String operations generally create new strings rather than modifying the original string.

---

# Creating a String

Creating a string is as simple as assigning a string value to a variable.

```python
message = "Hello Python"
```

Another example:

```python
name = "Developer"
```

The variable stores a reference to the string.

---

# Multi-Line Strings

Sometimes a string is very long and placing it on a single line can make code difficult to read.

Python provides several ways to create multi-line strings.

Common approaches include:

1. Triple quotes
2. Parentheses
3. Backslash line continuation
4. Joining strings

---

## Multi-Line String Using Triple Quotes

Triple quotes can be used to create strings spanning multiple lines.

```python
message = """This is a
multi-line
string."""
```

Triple single quotes can also be used:

```python
message = '''This is a
multi-line
string.'''
```

---

# Multi-Line String Using Parentheses

Adjacent string literals can be placed inside parentheses.

```python
message = (
    "This is a "
    "multi-line "
    "string."
)
```

Python automatically combines the adjacent string literals.

---

# Multi-Line String Using Backslash

A backslash can be used as a line-continuation character.

```python
message = "This is a \
multi-line string."
```

The backslash tells Python that the statement continues on the next line.

---

# Indexing Strings

A Python string is a sequence of characters.

Python does not have a separate character data type. A single character is simply a string whose length is `1`.

Square brackets `[]` are used to access characters by their position.

### Example

```python
text = "Python"
```

The indexes are:

```text
 P  y  t  h  o  n
 0  1  2  3  4  5
```

Therefore:

```python
print(text[0])
```

Output:

```text
P
```

---

# String Indexing

The first character of a Python string always has index:

```text
0
```

For example:

```python
text = "Hello"

print(text[0])
print(text[1])
print(text[2])
```

Output:

```text
H
e
l
```

---

# Negative Indexing

Python also supports **negative indexing**.

Negative indexes start from the end of the string.

For example:

```text
 H  e  l  l  o
 0  1  2  3  4
-5 -4 -3 -2 -1
```

Therefore:

```python
text = "Hello"

print(text[-1])
```

Output:

```text
o
```

And:

```python
print(text[-2])
```

Output:

```text
l
```

---

# Slicing a String

**String slicing** is used to access a range of characters from a string.

The slicing operator uses a colon `:`.

### Syntax

```python
string[start:stop]
```

The `start` index is included, while the `stop` index is excluded.

---

## Slicing Example

```python
text = "Python"

print(text[0:3])
```

Output:

```text
Pyt
```

Indexes `0`, `1`, and `2` are included, while index `3` is excluded.

---

# String Slicing with a Step

A third value can be provided to specify the step.

### Syntax

```python
string[start:stop:step]
```

Example:

```python
text = "Python"

print(text[0:6:2])
```

Output:

```text
Pto
```

The step value determines how many positions are skipped between selected characters.

---

# Updating a String

Because strings are immutable, individual characters cannot be updated.

This is invalid:

```python
text = "Python"
text[0] = "J"
```

Python will raise an error because item assignment is not supported for strings.

Instead, create a new string:

```python
text = "Jython"
```

---

# Deleting Characters from a String

Individual characters cannot be deleted from a string.

For example:

```python
text = "Python"
del text[0]
```

is not supported.

However, the **entire string variable** can be deleted using `del`.

```python
text = "Python"

del text
```

After this statement, the variable `text` no longer exists.

> This is another consequence of string immutability.

---

# String Concatenation

**Concatenation** means joining two or more strings together.

The `+` operator can be used to concatenate strings.

### Example

```python
first = "Hello"
second = "Python"

result = first + " " + second

print(result)
```

Output:

```text
Hello Python
```

The `+` operator joins the strings together.

---

# String Repetition

Sometimes a string needs to be repeated multiple times.

Python provides the `*` repetition operator for this purpose.

### Example

```python
text = "Hello "

print(text * 3)
```

Output:

```text
Hello Hello Hello
```

The repetition operator repeats the string the specified number of times.

---

# Repeating a Part of a String

A sliced portion of a string can also be repeated.

Example:

```python
text = "Python"

print(text[0:2] * 3)
```

Output:

```text
PyPyPy
```

Here:

```python
text[0:2]
```

produces:

```text
Py
```

which is then repeated three times.

---

# String Formatting

Python provides several ways to format strings.

String formatting is useful when a program needs to combine text with variable values.

For example, directly combining a string and a number using `+` is not allowed without converting the number:

```python
age = 20

# This is invalid:
# print("Age: " + age)
```

The value must first be converted to a string, or a string-formatting technique can be used.

Python provides several formatting approaches, including:

* `format()`
* `%` formatting
* f-strings

---

# `format()` Method

The `format()` method allows selected parts of a string to be replaced with values.

Placeholders are represented using curly brackets:

```text
{}
```

### Example

```python
name = "Python"

message = "Hello, {}".format(name)

print(message)
```

Output:

```text
Hello, Python
```

---

# Multiple Placeholders

The `format()` method can accept multiple arguments.

```python
name = "Python"
version = 3

message = "{} version {}".format(name, version)

print(message)
```

Output:

```text
Python version 3
```

The arguments are inserted into the corresponding placeholders.

---

# Positional Formatting

Index numbers can be used inside placeholders to control which argument is inserted.

```python
message = "{0} is learning {1}".format("Dev", "Python")

print(message)
```

Output:

```text
Dev is learning Python
```

Here:

* `{0}` refers to the first argument.
* `{1}` refers to the second argument.

---

# String Formatting Operator `%`

Python also supports the `%` operator for string formatting.

Example:

```python
name = "Python"

message = "Hello %s" % name

print(message)
```

Output:

```text
Hello Python
```

The `%` formatting style is an older string-formatting technique that is still supported by Python.

---

# F-Strings

**F-strings** provide a convenient way to insert variables and expressions directly into strings.

An f-string is created by placing `f` before the opening quotation mark.

### Example

```python
name = "Python"

message = f"Hello {name}"

print(message)
```

Output:

```text
Hello Python
```

---

## F-String with Expressions

Expressions can also be placed inside the curly braces.

```python
age = 20

print(f"Next year you will be {age + 1}")
```

Output:

```text
Next year you will be 21
```

F-strings are one of the most convenient modern approaches to string formatting in Python.

---

# Python String Methods

Python provides many built-in methods for performing operations on strings.

The course introduces several important methods, including:

* `capitalize()`
* `upper()`
* `lower()`
* `partition()`
* `strip()`
* `split()`

---

# `capitalize()` Method

The `capitalize()` method returns a new string with:

* The first character converted to uppercase.
* The remaining characters converted to lowercase.

### Example

```python
text = "python programming"

print(text.capitalize())
```

Output:

```text
Python programming
```

The original string is not modified because strings are immutable.

---

# `upper()` Method

The `upper()` method returns a new string with all alphabetic characters converted to uppercase.

### Example

```python
text = "python"

print(text.upper())
```

Output:

```text
PYTHON
```

---

# `lower()` Method

The `lower()` method returns a new string with all alphabetic characters converted to lowercase.

### Example

```python
text = "PYTHON"

print(text.lower())
```

Output:

```text
python
```

---

# `partition()` Method

The `partition()` method splits a string at the **first occurrence** of a specified separator.

It returns a tuple containing three elements:

1. The part before the separator.
2. The separator itself.
3. The part after the separator.

### Syntax

```python
string.partition(separator)
```

### Example

```python
text = "Python is powerful"

result = text.partition("is")

print(result)
```

Output:

```text
('Python ', 'is', ' powerful')
```

The separator is included in the returned tuple.

---

# `strip()` Method

The `strip()` method removes leading and trailing whitespace from a string.

### Example

```python
text = "   Hello Python   "

print(text.strip())
```

Output:

```text
Hello Python
```

By default, `strip()` removes whitespace from both ends of the string.

---

## Removing Specific Characters with `strip()`

Characters can also be specified.

```python
text = "xxxPythonxxx"

print(text.strip("x"))
```

Output:

```text
Python
```

The specified characters are removed from the beginning and end of the string.

> `strip()` does not remove characters from the middle of a string.

---

# `split()` Method

The `split()` method divides a string into a list of substrings.

### Example

```python
text = "Python is easy"

words = text.split()

print(words)
```

Output:

```text
['Python', 'is', 'easy']
```

By default, whitespace is used as the separator.

---

## `split()` with a Separator

A specific separator can be provided.

```python
text = "apple,banana,orange"

fruits = text.split(",")

print(fruits)
```

Output:

```text
['apple', 'banana', 'orange']
```

---

# Important String Operations

| Operation         | Purpose                            | Example                   |
| ----------------- | ---------------------------------- | ------------------------- |
| Indexing          | Access one character               | `text[0]`                 |
| Negative indexing | Access from the end                | `text[-1]`                |
| Slicing           | Access a range                     | `text[1:4]`               |
| Concatenation     | Join strings                       | `"Hello" + " Python"`     |
| Repetition        | Repeat strings                     | `"Hi " * 3`               |
| `format()`        | Format strings                     | `"Hello {}".format(name)` |
| `%`               | Old-style formatting               | `"Hello %s" % name`       |
| f-string          | Modern formatting                  | `f"Hello {name}"`         |
| `capitalize()`    | Capitalize first character         | `text.capitalize()`       |
| `upper()`         | Convert to uppercase               | `text.upper()`            |
| `lower()`         | Convert to lowercase               | `text.lower()`            |
| `partition()`     | Split at first separator           | `text.partition(":")`     |
| `strip()`         | Remove leading/trailing characters | `text.strip()`            |
| `split()`         | Split into a list                  | `text.split()`            |

---

# String Immutability and Methods

String methods do not modify the original string.

For example:

```python
text = "python"

text.upper()

print(text)
```

Output:

```text
python
```

The result of `upper()` must be stored if you want to use the changed version:

```python
text = "python"

text = text.upper()

print(text)
```

Output:

```text
PYTHON
```

---

# Basic String Operations Example

```python
text = "Python Programming"

print(text[0])
print(text[-1])
print(text[0:6])
print(text.upper())
print(text.lower())
print(text.capitalize())
```

These operations demonstrate:

* Indexing.
* Negative indexing.
* Slicing.
* Uppercase conversion.
* Lowercase conversion.
* Capitalization.

---

# Course Summary

After completing this course, you should understand:

* Creating strings.
* Multi-line strings in Python.
* String indexing.
* Negative indexing.
* String slicing.
* String immutability.
* Deleting an entire string.
* String concatenation.
* String repetition.
* String formatting.
* The `format()` method.
* `%` string formatting.
* F-strings.
* `capitalize()`.
* `upper()`.
* `lower()`.
* `partition()`.
* `strip()`.
* `split()`.

---

# Knowledge Assessment

The course concludes with a knowledge assessment covering:

* Creating strings.
* Multi-line strings.
* String indexing.
* Negative indexing.
* String slicing.
* Updating and deleting strings.
* String immutability.
* String concatenation.
* String repetition.
* String formatting.
* `format()`.
* `%` formatting.
* F-strings.
* `capitalize()`.
* `upper()`.
* `lower()`.
* `partition()`.
* `strip()`.
* `split()`.

A score of **80% or higher** is required to pass the assessment.

---

## Course Files

```text
07-Getting-Started-with-Operations-on-String/
├── lecture.md
├── assessment.md
└── certificate.pdf
```
