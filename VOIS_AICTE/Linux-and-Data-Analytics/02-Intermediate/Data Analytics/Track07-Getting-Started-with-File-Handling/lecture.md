# VOIS FOR TECH — Getting Started with File Handling

## Learning Objectives

The learning objective is to gain knowledge on:

* understanding file handling in Python.
* opening files using Python.
* reading data from files.
* writing data into files.
* appending data to files.
* closing files.
* renaming files.
* deleting files.
* understanding different file handling methods.
* working with text and binary files.

---

# Prerequisites

* Basic knowledge of Python syntax.
* Knowledge of writing and invoking functions.
* Knowledge of creating variables.
* Basic understanding of reading inputs and generating outputs from the Python console.
* Familiarity with using a text editor or IDE.
* Knowledge of how to execute a Python program.
* Basic knowledge of Python keywords.

---

# About the Course

Python provides important features for reading data from files and writing data into files.

In most programming languages, values stored only in variables are **volatile**. They exist during program execution and are lost when the program finishes.

Files provide a way to store data **permanently** so that it can be accessed later.

A typical file-handling process is:

1. Open or create a file.
2. Read from or write to the file.
3. Save the changes.
4. Close the file.

Python provides built-in functions and methods to perform these operations.

---

# File Handling in Python

Python supports working with different types of files.

The two major types covered in this course are:

1. Text files.
2. Binary files.

---

# Text Files

Text files contain data that is stored using a character encoding and can generally be opened and read using a normal text editor.

Examples include:

```text
.txt
.csv
.py
.html
.md
```

Example:

```text
Hello World
Welcome to Python
```

A text editor can display this content directly.

---

# Binary Files

Binary files store data in a binary format that is primarily intended to be interpreted by software rather than directly read as ordinary text.

Examples include:

```text
.jpg
.png
.mp3
.mp4
.pdf
```

Binary files may contain encoded data that cannot be meaningfully interpreted by opening them in a normal text editor.

---

# File Handling Operations

Python supports several important file operations.

The primary operations are:

* Open.
* Read.
* Write.
* Append.
* Close.

Other file-related operations include:

* Create.
* Rename.
* Delete.

A typical workflow looks like:

```text
Open → Read/Write → Save → Close
```

---

# Opening a File

Python provides the built-in:

```python
open()
```

function to open a file.

The `open()` function returns a **file object** that can be used to perform operations such as reading and writing.

### Basic Syntax

```python
file = open("filename.txt", "mode")
```

Example:

```python
my_file = open("test.txt", "r")
```

This opens `test.txt` in read mode.

---

# File Name and Extension

When specifying a file, the file name should include its extension when applicable.

Example:

```python
open("test.txt", "r")
```

Here:

```text
test → file name
.txt → file extension
```

A file can also be specified using its complete path.

Example:

```python
open("/home/aryan/test.txt", "r")
```

---

# File Opening Modes

The mode specified in `open()` tells Python what operation should be performed on the file.

Common modes include:

| Mode | Purpose         |
| ---- | --------------- |
| `r`  | Read            |
| `w`  | Write           |
| `a`  | Append          |
| `r+` | Read and write  |
| `a+` | Append and read |

---

# Read Mode — `r`

The `r` mode is used to read data from a file.

Example:

```python
file = open("test.txt", "r")
```

The file must normally already exist when opened in read mode.

---

# Write Mode — `w`

The `w` mode is used to write data into a file.

Example:

```python
file = open("test.txt", "w")
```

### Important

Write mode can **overwrite existing content**.

For example, if `test.txt` contains:

```text
Hello World
```

and you execute:

```python
file = open("test.txt", "w")
file.write("Hello Python")
file.close()
```

The previous content is replaced with:

```text
Hello Python
```

> **Important:** Be careful when using `w` mode because existing file contents can be overwritten.

---

# Append Mode — `a`

The `a` mode is used to append data to an existing file.

Example:

```python
file = open("test.txt", "a")
file.write("Hello Python")
file.close()
```

The new data is added to the end of the file rather than replacing the existing contents.

For example:

```text
Hello World
```

becomes:

```text
Hello WorldHello Python
```

To place the new content on a separate line:

```python
file.write("\nHello Python")
```

---

# Read and Write Mode — `r+`

The `r+` mode provides both read and write access.

Example:

```python
file = open("test.txt", "r+")
```

This mode allows the program to read from and write to the same file.

---

# Append and Read Mode — `a+`

The `a+` mode provides both append and read access.

Example:

```python
file = open("test.txt", "a+")
```

This allows data to be appended while also providing read access.

---

# Reading from a File

To read data from a file:

1. Open the file in read mode.
2. Use an appropriate read method.
3. Process the data.
4. Close the file.

Python provides three commonly used methods:

```text
read()
readline()
readlines()
```

---

# `read()` Method

The `read()` method reads data from a file.

### Read the Entire File

```python
file = open("test.txt", "r")

content = file.read()

print(content)

file.close()
```

This reads all available content from the file.

---

# Reading a Specific Number of Characters

An argument can be passed to `read()` to specify how many characters to read.

Example:

```python
file = open("test.txt", "r")

content = file.read(5)

print(content)

file.close()
```

This reads the first **5 characters**.

---

# `readline()` Method

The `readline()` method reads one line from a file.

Example:

```python
file = open("test.txt", "r")

line = file.readline()

print(line)

file.close()
```

If the file contains:

```text
Hello World
Hello Python
Welcome to Linux
```

the first call to `readline()` reads:

```text
Hello World
```

A subsequent call reads the next line.

---

# `readlines()` Method

The `readlines()` method reads all lines from a file and returns them as a list.

Example:

```python
file = open("test.txt", "r")

lines = file.readlines()

print(lines)

file.close()
```

For a file containing:

```text
Hello World
Hello Python
Welcome to Linux
```

the result is similar to:

```python
[
    "Hello World\n",
    "Hello Python\n",
    "Welcome to Linux"
]
```

The newline characters are included where present.

---

# Reading an Entire File

An entire file can be read using:

```python
file = open("test.txt", "r")

data = file.read()

print(data)

file.close()
```

This is useful when the complete file content needs to be loaded at once.

---

# Writing to a File

To write data into a file:

1. Open the file in write mode.
2. Use the `write()` method.
3. Close the file.

Example:

```python
file = open("test.txt", "w")

file.write("Hello World")

file.close()
```

The file will contain:

```text
Hello World
```

---

# `write()` Method

The `write()` method writes a string to a file.

Example:

```python
file.write("Hello World")
```

To write multiple lines:

```python
file.write("Hello World\n")
file.write("Hello Python\n")
```

The `\n` character moves the content to the next line.

The resulting file will contain:

```text
Hello World
Hello Python
```

---

# Writing Without a Newline

If `\n` is not included, the text is written continuously.

Example:

```python
file.write("Hello World")
file.write("Hello Python")
```

The file may contain:

```text
Hello WorldHello Python
```

---

# `writelines()` Method

The `writelines()` method can write a sequence of strings to a file.

Example:

```python
lines = [
    "Hello World\n",
    "Hello Python\n",
    "Welcome to Linux\n"
]

file = open("test.txt", "w")

file.writelines(lines)

file.close()
```

The resulting file contains:

```text
Hello World
Hello Python
Welcome to Linux
```

> **Note:** `writelines()` does not automatically add newline characters. If separate lines are required, `\n` must be included in the strings.

---

# Appending Data to a File

To append data, open the file using `a` mode.

Example:

```python
file = open("test.txt", "a")

file.write("\nWelcome to Python")

file.close()
```

If the original file contains:

```text
Hello World
```

the resulting file becomes:

```text
Hello World
Welcome to Python
```

---

# Closing a File

Python provides the:

```python
close()
```

method to close an opened file.

Example:

```python
file = open("test.txt", "r")

data = file.read()

file.close()
```

Closing a file is important because it releases the resources associated with the file.

It is especially important after writing because the written data needs to be properly flushed and the file should no longer remain open unnecessarily.

---

# Why Close a File?

After completing file operations, the file should be closed.

Benefits include:

* Releases system resources.
* Ensures file operations are completed properly.
* Prevents unnecessary open file handles.
* Helps avoid problems caused by leaving files open.

Basic pattern:

```python
file = open("test.txt", "r")

# Perform file operation

file.close()
```

---

# Renaming a File

Python provides the `os` module for file-system operations such as renaming files.

First import the module:

```python
import os
```

Use:

```python
os.rename()
```

### Example

```python
import os

os.rename("test.txt", "newtest.txt")
```

This changes:

```text
test.txt
```

to:

```text
newtest.txt
```

---

# Deleting a File

The `os` module can also be used to delete files.

Example:

```python
import os

os.remove("test.txt")
```

This deletes:

```text
test.txt
```

> **Important:** Make sure the file name and path are correct before using `os.remove()`.

---

# Working with Binary Files

Binary files should be opened using binary modes.

The `b` character can be combined with modes such as:

```text
rb
wb
ab
```

Examples:

```python
open("image.jpg", "rb")
```

and:

```python
open("image.jpg", "wb")
```

---

# Reading a Binary File

Example:

```python
file = open("image.jpg", "rb")

data = file.read()

file.close()
```

The data is returned in binary form rather than ordinary text.

---

# Writing to a Binary File

Binary data must be supplied in an appropriate bytes format.

Example:

```python
file = open("data.bin", "wb")

file.write(b"Hello")

file.close()
```

The `b` prefix creates a bytes literal.

---

# File Methods

The following are important file-related methods:

| Method         | Purpose                              |
| -------------- | ------------------------------------ |
| `open()`       | Opens a file                         |
| `close()`      | Closes an open file                  |
| `read()`       | Reads characters/data from the file  |
| `readline()`   | Reads one line from the file         |
| `readlines()`  | Reads all lines from the file        |
| `write()`      | Writes a string/data to the file     |
| `writelines()` | Writes a list/sequence of strings    |
| `readable()`   | Returns whether the file is readable |
| `writable()`   | Returns whether the file is writable |

---

# `readable()` Method

The `readable()` method checks whether a file is open for reading.

Example:

```python
file = open("test.txt", "r")

print(file.readable())

file.close()
```

The output will generally be:

```text
True
```

when the file is readable.

---

# `writable()` Method

The `writable()` method checks whether a file is open for writing.

Example:

```python
file = open("test.txt", "w")

print(file.writable())

file.close()
```

The output will generally be:

```text
True
```

---

# Complete File Handling Example

The following example demonstrates a basic file-handling workflow:

```python
# Open file in write mode
file = open("student.txt", "w")

# Write data
file.write("Name: Aryan\n")
file.write("Course: Python\n")

# Close file
file.close()

# Open file in read mode
file = open("student.txt", "r")

# Read data
data = file.read()

print(data)

# Close file
file.close()
```

Output:

```text
Name: Aryan
Course: Python
```

---

# File Handling Workflow

A basic Python file-handling workflow is:

```text
Create/Open
     ↓
Read / Write / Append
     ↓
Process Data
     ↓
Close
```

For example:

```python
file = open("data.txt", "r")

data = file.read()

print(data)

file.close()
```

---

# Common File Handling Examples

## Open a File

```python
file = open("test.txt", "r")
```

## Read a File

```python
data = file.read()
```

## Read One Line

```python
line = file.readline()
```

## Read All Lines

```python
lines = file.readlines()
```

## Write to a File

```python
file = open("test.txt", "w")
file.write("Hello Python")
```

## Append to a File

```python
file = open("test.txt", "a")
file.write("\nWelcome")
```

## Close a File

```python
file.close()
```

## Rename a File

```python
import os
os.rename("old.txt", "new.txt")
```

## Delete a File

```python
import os
os.remove("old.txt")
```

---

# Important Differences

## `w` vs `a`

### Write Mode

```python
open("test.txt", "w")
```

* Writes data.
* Can overwrite existing content.

### Append Mode

```python
open("test.txt", "a")
```

* Adds data to the end.
* Does not overwrite existing content in normal append usage.

---

## `read()` vs `readline()` vs `readlines()`

| Method        | Function                  |
| ------------- | ------------------------- |
| `read()`      | Reads file content        |
| `readline()`  | Reads one line            |
| `readlines()` | Reads all lines as a list |

---

# Course Completion

After completing this course, you should now be able to:

* Understand file handling in Python.
* Understand text and binary files.
* Open files using `open()`.
* Read data using `read()`.
* Read individual lines using `readline()`.
* Read all lines using `readlines()`.
* Write data using `write()`.
* Write multiple strings using `writelines()`.
* Append data using append mode.
* Close files using `close()`.
* Check whether a file is readable using `readable()`.
* Check whether a file is writable using `writable()`.
* Rename files using `os.rename()`.
* Delete files using `os.remove()`.
* Understand common file opening modes.

---

# Knowledge Assessment

The course concludes with a knowledge assessment to check your understanding of Python file handling.

The assessment covers:

* Text and binary files.
* File opening modes.
* Reading files.
* Writing files.
* Appending files.
* Closing files.
* Renaming files.
* Deleting files.
* File methods.

You must achieve **80%** to pass the assessment.

---

## Course Files

```text
Track07-Getting-Started-with-File-Handling/
├── lecture.md
├── assessment.md
└── certificate.pdf
```
