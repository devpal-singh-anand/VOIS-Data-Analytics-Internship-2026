# Getting Started with Sequence Data Types

## Learning Objectives

The learning objective is to gain knowledge on:

* creating sequential data types in Python.
* performing operations on sequential data.
* creating and manipulate lists.
* creating and use tuples.
* creating and manipulate dictionaries.
* creating and use sets.
* performing slicing operations on sequence data.
* modifying and delete elements from lists.
* performing basic dictionary operations.
* performing mathematical set operations such as union, intersection, and difference.

---

## Prerequisites

* Elementary knowledge of Python.

---

# About the Course

This course introduces **sequence data types and other built-in data structures in Python**.

It covers:

* Strings
* Lists
* Tuples
* Dictionaries
* Sets
* Sequence operations
* Slicing
* List modification
* Dictionary operations
* Set operations

---

# What Are Sequence Data Types?

Sequence data types are data types that store elements in an **ordered sequence**.

Elements in sequential data types can generally be accessed using their **indexes**.

The main sequence data types in Python are:

1. **String**
2. **List**
3. **Tuple**

Python also provides other built-in data structures such as:

* Lists
* Dictionaries
* Tuples
* Sets

Python can also be used to implement user-defined data structures such as:

* Stacks
* Queues
* Trees
* Linked lists
* Graphs
* Hash maps

---

# Sequence Data Types as Containers

A sequence can be considered a container that stores data in an organized order.

When data is stored in an ordered structure, it can be analyzed and manipulated in various ways.

For example, because sequence elements have positions, operations such as finding the position of an element become possible.

---

# Operations on Python Sequences

Several common operations can be performed on Python sequences.

These include:

* Concatenation
* Repetition
* Membership testing
* Slicing
* Finding length
* Finding minimum and maximum values
* Finding the index of an element
* Counting occurrences

---

# Concatenation

The `+` operator is used to concatenate two sequences.

### Example

```python
list1 = [1, 3, 4]
list2 = [1, 1, 1]

result = list1 + list2

print(result)
```

Output:

```text
[1, 3, 4, 1, 1, 1]
```

The `+` operator can be used to concatenate compatible sequences such as strings, lists, and tuples.

---

# Repetition

The `*` operator is used to repeat a sequence a specified number of times.

### Example

```python
numbers = [1, 2, 3]

print(numbers * 3)
```

Output:

```text
[1, 2, 3, 1, 2, 3, 1, 2, 3]
```

The repetition operator can also be used with strings and tuples.

---

# Membership Operators

Python provides two membership operators:

* `in`
* `not in`

They are used to determine whether an item exists in a sequence.

The result is a Boolean value:

```text
True
```

or:

```text
False
```

### Example

```python
letters = "Python"

print("P" in letters)
```

Output:

```text
True
```

Another example:

```python
letters = "Python"

print("x" not in letters)
```

Output:

```text
True
```

---

# Slicing Operator

Sequences in Python can be sliced to extract a portion of the sequence.

The slicing syntax is:

```python
sequence[start:end]
```

The `start` index is included, while the `end` index is excluded.

### Example

```python
text = "New York"

print(text[0:3])
```

Output:

```text
New
```

Slicing can be applied to:

* Strings
* Lists
* Tuples

---

# Common Sequence Functions and Methods

Some important functions and methods used with sequences are:

* `len()`
* `min()`
* `max()`
* `index()`
* `count()`

---

# `len()` Function

The `len()` function returns the number of elements in a sequence.

### Example

```python
sentence = "Python is powerful"

print(len(sentence))
```

The function returns the length of the sequence.

For a list:

```python
spam = ["bacon", "eggs", 42]

print(len(spam))
```

Output:

```text
3
```

> **Important:** `len()` returns the number of elements in a list, not the highest index.

For a list containing three elements, the indexes are:

```text
0
1
2
```

Therefore, the last index is:

```python
len(spam) - 1
```

---

# `min()` and `max()` Functions

The `min()` function returns the minimum value in a sequence.

The `max()` function returns the maximum value.

### Example

```python
numbers = [1, 3, 5, 2, 4]

print(min(numbers))
print(max(numbers))
```

Output:

```text
1
5
```

---

# `index()` Method

The `index()` method searches for an element and returns the index of its **first occurrence**.

### Example

```python
words = ["hello", "world", "python"]

print(words.index("world"))
```

Output:

```text
1
```

If the specified value does not exist in the sequence, Python raises a `ValueError`.

---

# `count()` Method

The `count()` method returns the number of times an element occurs in a sequence.

### Example

```python
letters = ["a", "b", "a", "c", "a"]

print(letters.count("a"))
```

Output:

```text
3
```

---

# Creating Sequences

Different sequence types use different syntax.

## String

Strings are created using quotes:

```python
text = "Python"
```

## List

Lists are created using square brackets:

```python
numbers = [1, 2, 3]
```

## Tuple

Tuples are generally created using parentheses:

```python
numbers = (1, 2, 3)
```

---

# Lists

A **list** is an ordered collection of values.

Lists are created using square brackets:

```python
spam = []
```

An empty list can be created using:

```python
spam = []
```

A list containing multiple values can be created as:

```python
spam = ["bacon", "eggs", 42]
```

The values are separated by commas.

---

# Lists Can Contain Different Data Types

Python lists can contain objects of different types.

For example:

```python
spam = ["bacon", "eggs", 42]
```

This list contains:

* Strings
* An integer

Lists can also contain other lists.

---

# Accessing List Elements

List elements can be accessed using indexes.

Indexes start at `0`.

### Example

```python
spam = ["bacon", "eggs", 42]

print(spam[0])
```

Output:

```text
bacon
```

The indexes are:

```text
0 → bacon
1 → eggs
2 → 42
```

---

# Negative Indexing in Lists

Lists also support negative indexes.

```python
spam = ["bacon", "eggs", 42]

print(spam[-1])
```

Output:

```text
42
```

Negative indexes count backwards from the end of the list.

---

# Length of a List

The `len()` function can be used to determine the number of items in a list.

```python
spam = ["bacon", "eggs", 42]

print(len(spam))
```

Output:

```text
3
```

The last element can therefore be accessed using:

```python
spam[len(spam) - 1]
```

---

# Modifying Lists

Unlike strings, **lists are mutable**.

This means that list elements can be changed after the list has been created.

### Example

```python
spam = ["bacon", "eggs", 42]

spam[1] = "ham"

print(spam)
```

Output:

```text
['bacon', 'ham', 42]
```

The second element was modified.

---

# Slicing Lists

Lists support slicing just like strings.

### Example

```python
numbers = [1, 2, 3, 4, 5]

print(numbers[1:4])
```

Output:

```text
[2, 3, 4]
```

The slice starts at index `1` and stops before index `4`.

---

# Adding Items to a List

There are several ways to add items to a list.

One of the simplest methods is `append()`.

---

## `append()` Method

The `append()` method adds an item to the end of a list.

### Example

```python
spam = ["bacon", "eggs"]

spam.append(42)

print(spam)
```

Output:

```text
['bacon', 'eggs', 42]
```

> **Important:** You cannot use an index outside the current list range to directly create a new element.

For example:

```python
spam[4] = 10
```

will produce an error if index `4` does not already exist.

---

# Deleting Elements from a List

The `del` statement can be used to delete an element from a list.

### Example

```python
spam = ["bacon", "eggs", 42]

del spam[1]

print(spam)
```

Output:

```text
['bacon', 42]
```

The element at index `1` has been removed.

---

# Extending a List

`append()` adds one object to a list.

What happens if you want to add all elements from another list?

The `extend()` method can be used.

### Example

```python
list1 = [1, 2, 3]
list2 = [4, 5, 6]

list1.extend(list2)

print(list1)
```

Output:

```text
[1, 2, 3, 4, 5, 6]
```

`extend()` adds each element of the iterable to the list.

---

## `append()` vs `extend()`

Consider:

```python
list1 = [1, 2, 3]
list2 = [4, 5, 6]

list1.append(list2)
```

The result is:

```text
[1, 2, 3, [4, 5, 6]]
```

The entire second list is added as one element.

With:

```python
list1.extend(list2)
```

the result is:

```text
[1, 2, 3, 4, 5, 6]
```

Each element is added individually.

---

# `index()` Method with Lists

The `index()` method can be used to find the position of an element in a list.

```python
numbers = [10, 20, 30, 40]

print(numbers.index(30))
```

Output:

```text
2
```

The first matching occurrence is returned.

If the value is not present, a `ValueError` is raised.

---

# Properties of Python Lists

The main properties of Python lists are:

* Lists are **ordered**.
* Lists can contain arbitrary objects.
* List elements can be accessed using indexes.
* Lists can contain different data types.
* Lists can contain other lists.
* Lists can dynamically grow or shrink.
* Lists are **mutable**.
* Elements of a list can be modified after creation.

---

# Tuples

A **tuple** is an ordered collection similar to a list.

The major difference is that tuples are **immutable**.

This means that once a tuple has been created, its elements cannot be changed.

---

# Creating a Tuple

Tuples are generally created using parentheses.

```python
numbers = (1, 2, 3)
```

An empty tuple can be created using:

```python
empty_tuple = ()
```

---

# Accessing Tuple Elements

Tuple indexes work in the same way as list indexes.

```python
numbers = (10, 20, 30)

print(numbers[0])
```

Output:

```text
10
```

Negative indexing is also supported.

```python
print(numbers[-1])
```

Output:

```text
30
```

---

# Tuple Immutability

Once a tuple has been created, its elements cannot be changed.

For example:

```python
numbers = (10, 20, 30)

numbers[0] = 100
```

This raises an error because tuples do not support item assignment.

Similarly, elements cannot be added or removed from an existing tuple.

---

# Advantages of Tuples

Tuples have several advantages:

* They are immutable.
* They can protect data from accidental modification.
* They can be used where an immutable sequence is required.
* Tuples can be used as dictionary keys when their contents are hashable.
* They may be more efficient than lists for certain use cases.

> If data does not need to change, a tuple can be a suitable choice.

---

# Lists vs Tuples

| Feature                 | List | Tuple |
| ----------------------- | ---- | ----- |
| Syntax                  | `[]` | `()`  |
| Ordered                 | Yes  | Yes   |
| Mutable                 | Yes  | No    |
| Elements can be changed | Yes  | No    |
| Elements can be added   | Yes  | No    |
| Elements can be removed | Yes  | No    |
| Supports indexing       | Yes  | Yes   |
| Supports slicing        | Yes  | Yes   |

---

# Dictionaries

A **dictionary** is a collection of **key-value pairs**.

Unlike sequences such as lists and tuples, dictionary values are accessed using their **keys**, rather than numerical positions.

A dictionary can be thought of as a mapping between a key and its associated value.

---

# Creating a Dictionary

Dictionaries are created using curly braces `{}`.

Each entry contains:

```text
key : value
```

### Example

```python
definitions = {
    "guava": "a tropical fruit",
    "python": "a programming language",
    "answer": 42
}
```

Each key is associated with a corresponding value.

---

# Key-Value Pairs

Consider:

```python
student = {
    "name": "Dev",
    "age": 22
}
```

Here:

```text
"name" → "Dev"
"age"  → 22
```

The left side is the **key**.

The right side is the **value**.

---

# Accessing Dictionary Values

A value can be accessed by providing its key inside square brackets.

### Example

```python
definitions = {
    "answer": 42
}

print(definitions["answer"])
```

Output:

```text
42
```

---

# Dictionary Operations

Important dictionary operations include:

* `len()`
* `del`
* `in`
* `not in`
* `keys()`
* `values()`

---

## `len()` with Dictionaries

The `len()` function returns the number of key-value pairs.

```python
student = {
    "name": "Dev",
    "age": 22
}

print(len(student))
```

Output:

```text
2
```

---

# `del` with Dictionaries

The `del` statement can be used to remove a key-value pair.

```python
student = {
    "name": "Dev",
    "age": 22
}

del student["age"]
```

The `"age"` key and its associated value are removed.

---

# `in` with Dictionaries

The `in` operator checks whether a key exists in a dictionary.

```python
student = {
    "name": "Dev",
    "age": 22
}

print("name" in student)
```

Output:

```text
True
```

---

# `not in` with Dictionaries

The `not in` operator checks whether a key does not exist.

```python
print("email" not in student)
```

Output:

```text
True
```

---

# Iterating Through Dictionary Values

The `values()` method provides access to the dictionary's values.

### Example

```python
numbers = {
    "a": 123,
    "b": 304,
    "c": 499
}

for value in numbers.values():
    print(value)
```

The loop processes each value in the dictionary.

---

# Sets

A **set** is an unordered collection of unique elements.

Important properties of sets include:

* Elements are unique.
* Duplicate elements are removed.
* A set itself is mutable.
* Set elements must be hashable, so mutable objects such as lists cannot be elements of a set.
* Sets support mathematical set operations.

Set operations include:

* Union
* Intersection
* Difference
* Symmetric difference

---

# Creating Sets

A set can be created using curly braces.

```python
numbers = {1, 2, 3, 4}
```

A set can contain multiple data types, provided the elements are hashable.

For example:

```python
data = {1, "Python", 3.14}
```

---

# Creating a Set Using `set()`

The built-in `set()` function can be used to create a set from an iterable.

### Example

```python
letters = set("Python")

print(letters)
```

The characters of the string are used as elements of the set.

> **Important:** Sets are unordered, so the displayed order should not be relied upon.

---

# Duplicate Elements in Sets

Sets automatically eliminate duplicate values.

For example:

```python
numbers = {1, 2, 2, 3, 3, 3}

print(numbers)
```

The resulting set contains only unique elements:

```text
{1, 2, 3}
```

---

# Immutable Elements in Sets

Set elements must be **hashable**.

Therefore, mutable objects such as lists cannot normally be used as set elements.

For example:

```python
my_set = {[1, 2, 3]}
```

is invalid.

Immutable objects such as numbers, strings, and suitable tuples can be elements of a set.

---

# Union of Sets

The **union** of two sets contains all elements that occur in either set.

The `union()` method can be used to perform this operation.

### Example

```python
set1 = {1, 2, 3}
set2 = {3, 4, 5}

result = set1.union(set2)

print(result)
```

Output:

```text
{1, 2, 3, 4, 5}
```

The `|` operator can also be used:

```python
result = set1 | set2
```

---

# Intersection of Sets

The **intersection** of two sets contains elements that occur in **both** sets.

### Example

```python
set1 = {1, 2, 3}
set2 = {2, 3, 4}

result = set1.intersection(set2)

print(result)
```

Output:

```text
{2, 3}
```

The `&` operator can also be used:

```python
result = set1 & set2
```

---

# Difference of Sets

The **difference** of two sets contains elements that are present in the first set but not in the second.

### Example

```python
set1 = {1, 2, 3}
set2 = {2, 3, 4}

result = set1.difference(set2)

print(result)
```

Output:

```text
{1}
```

The `-` operator can also be used:

```python
result = set1 - set2
```

The original sets remain unchanged when using these methods.

---

# Symmetric Difference

The **symmetric difference** contains elements that belong to either set, but not to both.

### Example

```python
set1 = {1, 2, 3}
set2 = {3, 4, 5}

result = set1.symmetric_difference(set2)

print(result)
```

Output:

```text
{1, 2, 4, 5}
```

---

# Comparison of Python Data Structures

| Data Structure | Ordered             | Mutable | Access Method | Allows Duplicates   |
| -------------- | ------------------- | ------- | ------------- | ------------------- |
| String         | Yes                 | No      | Index         | Yes                 |
| List           | Yes                 | Yes     | Index         | Yes                 |
| Tuple          | Yes                 | No      | Index         | Yes                 |
| Dictionary     | Key-based           | Yes     | Key           | Keys: No duplicates |
| Set            | No guaranteed order | Yes     | Membership    | No                  |

---

# Common Operations Summary

| Operation                | Purpose                       |
| ------------------------ | ----------------------------- |
| `+`                      | Concatenates sequences        |
| `*`                      | Repeats sequences             |
| `in`                     | Checks membership             |
| `not in`                 | Checks absence                |
| `[]`                     | Accesses an element           |
| `[:]`                    | Performs slicing              |
| `len()`                  | Returns number of elements    |
| `min()`                  | Returns minimum value         |
| `max()`                  | Returns maximum value         |
| `index()`                | Finds first index of a value  |
| `count()`                | Counts occurrences            |
| `append()`               | Adds one item to a list       |
| `extend()`               | Adds multiple items to a list |
| `del`                    | Deletes an element            |
| `union()`                | Performs set union            |
| `intersection()`         | Performs set intersection     |
| `difference()`           | Performs set difference       |
| `symmetric_difference()` | Performs symmetric difference |

---

# Course Summary

After completing this course, you should understand:

* What sequence data types are.
* Strings, lists, and tuples as sequence types.
* Basic operations on Python sequences.
* Concatenation.
* Repetition.
* Membership operators.
* Sequence slicing.
* `len()`, `min()`, and `max()`.
* `index()` and `count()`.
* Creating and accessing lists.
* Modifying and deleting list elements.
* `append()` and `extend()`.
* Properties of lists.
* Creating and using tuples.
* Tuple immutability.
* Creating and accessing dictionaries.
* Dictionary key-value pairs.
* Basic dictionary operations.
* Creating and using sets.
* Set uniqueness and immutability requirements.
* Union of sets.
* Intersection of sets.
* Difference of sets.
* Symmetric difference of sets.

---

# Knowledge Assessment

The course concludes with a knowledge assessment covering:

* Sequence data types.
* Sequence operations.
* Lists.
* Tuples.
* Dictionaries.
* Sets.
* Slicing.
* List modification.
* List deletion.
* Dictionary operations.
* Set union.
* Set intersection.
* Set difference.

A score of **80% or higher** is required to pass the assessment.

## Course Files

```text
08-Getting-Started-with-Sequenced-Data-Types/
├── lecture.md
├── assessment.md
└── certificate.pdf
```
