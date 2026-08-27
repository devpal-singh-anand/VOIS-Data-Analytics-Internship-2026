# Getting Started with Linux VI Text Editors

## Learning Objectives

The learning objective is to gain knowledge on:

* understanding the **Linux VI editor**.
* understanding the different **modes of operation** in VI.
* creating and edit files using VI.
* saving and exit files using VI.
* navigating through file contents.
* deleting, copy, and paste text within files.

---

## Prerequisites

* Basic understanding of Linux.
* Basic knowledge of Linux system utilities.
* Basic understanding of Linux commands.

---

# About the Course

This course introduces the **VI text editor** and its operations on Unix/Linux systems.

VI is a screen-oriented text editor that allows users to:

* Create files.
* Edit existing files.
* Read text files.
* Navigate through file contents.
* Insert and delete text.
* Copy and paste text.
* Save changes.
* Exit the editor.

---

# Introduction to VI Editor

The default editor traditionally associated with Unix operating systems is called **VI**, which stands for **Visual Editor**.

Using the VI editor, you can:

* Make changes to an existing file.
* Create a new file from scratch.
* Read the contents of a text file.
* Modify individual lines.
* Navigate through the file.

### Starting VI

The basic command to open a file using VI is:

```bash
vi filename
````

Example:

```bash
vi notes.txt
```

If `notes.txt` does not exist, VI can create the file when it is saved.

---

# Modes of Operation in VI

The VI editor has **three main modes of operation**:

1. Command Mode
2. Insert Mode
3. Last Line Mode

Understanding these modes is essential when working with VI.

---

# Command Mode

When VI starts, it opens in **Command Mode**.

In Command Mode, characters entered from the keyboard are interpreted as commands rather than being inserted into the file.

Command Mode can be used to:

* Navigate through the file.
* Delete text.
* Copy text.
* Paste text.
* Move the cursor.
* Execute commands.

### Returning to Command Mode

Press:

```text
Esc
```

The **Esc** key is used to return to Command Mode from another mode.

### Example

If you are typing text in Insert Mode and want to execute a command:

```text
Esc
```

This returns you to Command Mode.

---

# Insert Mode

**Insert Mode** is used to add text to a file.

When VI is in Insert Mode, characters entered from the keyboard are treated as text and inserted into the file.

### Enter Insert Mode

The `i` command is commonly used:

```text
i
```

After pressing `i`, you can start typing.

### Example

Open a file:

```bash
vi notes.txt
```

Press:

```text
i
```

Then type:

```text
Hello Linux
This is my first VI file.
```

To stop inserting text and return to Command Mode:

```text
Esc
```

---

# Last Line Mode

Last Line Mode is used to execute commands related to the file and editor.

From Command Mode, pressing:

```text
:
```

moves the cursor to the last line of the screen.

VI then waits for a command.

Last Line Mode can be used for operations such as:

* Saving files.
* Exiting VI.
* Saving and exiting.
* Executing editor commands.

---

# Important VI Mode Flow

A basic VI workflow looks like:

```text
Start VI
   ↓
Command Mode
   ↓
Press i
   ↓
Insert Mode
   ↓
Enter text
   ↓
Press Esc
   ↓
Command Mode
   ↓
Press :
   ↓
Last Line Mode
   ↓
Enter command
```

---

# Creating a New File Using VI

A new file can be created using the `vi` command.

### Step 1: Open VI

```bash
vi example.txt
```

### Step 2: Enter Insert Mode

Press:

```text
i
```

### Step 3: Enter Content

For example:

```text
Welcome to Linux.
This file was created using VI.
```

### Step 4: Return to Command Mode

Press:

```text
Esc
```

### Step 5: Save and Exit

Enter:

```text
:wq
```

Then press:

```text
Enter
```

The file is saved and VI exits.

---

# Starting the VI Editor

The basic syntax for opening a file is:

```bash
vi filename
```

### Example

```bash
vi test.txt
```

If the file already exists, VI opens it for editing.

If the file does not exist, VI can create it when the file is saved.

---

# Saving and Exiting VI

When you finish editing a file, you can save the changes and exit VI.

You must first be in **Command Mode**.

Press:

```text
Esc
```

Then enter:

```text
:wq
```

Press **Enter**.

### Meaning

```text
:w   → Write/save the file
:q   → Quit VI
```

Therefore:

```text
:wq
```

means **save the file and quit VI**.

---

# Exiting VI Without Saving

To exit VI without saving changes:

```text
:q!
```

Press **Enter**.

### Meaning

```text
:q   → Quit
!    → Force the operation
```

Therefore:

```text
:q!
```

means **quit without saving changes**.

---

# Saving a File Without Exiting

To save the current file without leaving VI:

```text
:w
```

Press **Enter**.

This writes the current changes to the file while keeping VI open.

---

# Common VI Save and Exit Commands

| Command | Purpose             |
| ------- | ------------------- |
| `:w`    | Save/write the file |
| `:q`    | Quit VI             |
| `:wq`   | Save and quit       |
| `:q!`   | Quit without saving |
| `ZZ`    | Save and exit       |

> **Important:** Save and exit commands are executed from Command Mode.

---

# Insert Mode Commands

There are several ways to enter Insert Mode.

## `i` — Insert Before Cursor

```text
i
```

Allows text to be inserted before the current cursor position.

---

## `a` — Append After Cursor

```text
a
```

Allows text to be inserted after the current cursor position.

---

## `o` — Open a New Line

```text
o
```

Creates a new line below the current line and enters Insert Mode.

### Example

If the file contains:

```text
Hello Linux
```

Using:

```text
o
```

allows you to enter a new line below it:

```text
Hello Linux
Welcome to VI
```

---

# Navigating Within a File

Navigation is performed primarily from **Command Mode**.

The keyboard arrow keys can also be used in many VI implementations.

Common navigation keys include:

| Key | Purpose    |
| --- | ---------- |
| `h` | Move left  |
| `j` | Move down  |
| `k` | Move up    |
| `l` | Move right |

### Example

```text
        k
        ↑
    h ←   → l
        ↓
        j
```

These keys allow you to move the cursor through the file.

---

# Moving to the Beginning and End of a Line

Common VI navigation commands include:

```text
0
```

Moves to the beginning of the current line.

```text
$
```

Moves to the end of the current line.

### Example

For:

```text
Hello Linux World
```

Using:

```text
0
```

moves the cursor to:

```text
H
```

Using:

```text
$
```

moves the cursor to:

```text
d
```

---

# Moving Through the File

Some useful navigation commands are:

```text
gg
```

Moves to the beginning of the file.

```text
G
```

Moves to the end of the file.

### Example

If a file contains 100 lines:

```text
gg
```

moves to line 1.

```text
G
```

moves to the last line.

---

# Deleting Text

Text can be deleted from a file while in **Command Mode**.

### Delete a Character

```text
x
```

Deletes the character under the cursor.

### Delete a Line

```text
dd
```

Deletes the current line.

### Example

Suppose the file contains:

```text
Hello Linux
Welcome to VI
Learning Linux commands
```

Place the cursor on:

```text
Welcome to VI
```

Then press:

```text
dd
```

The line is deleted.

---

# Copying and Pasting Text

VI provides commands for copying and pasting text.

## Copy a Line

```text
yy
```

Copies the current line.

## Paste

```text
p
```

Pastes the copied text after the current position.

### Example

If the file contains:

```text
Hello Linux
Welcome to VI
```

Place the cursor on:

```text
Hello Linux
```

Press:

```text
yy
```

Then:

```text
p
```

The result becomes:

```text
Hello Linux
Hello Linux
Welcome to VI
```

---

# Cutting and Pasting Text

The delete command can also be used to cut text.

For example:

```text
dd
```

deletes the current line and places it in the buffer.

It can then be pasted using:

```text
p
```

This can be used to move lines within a file.

---

# Undoing Changes

The `u` command can be used to undo the most recent change.

```text
u
```

### Example

If you accidentally delete a line using:

```text
dd
```

you can use:

```text
u
```

to undo the deletion.

---

# Redoing Changes

In many VI/Vim implementations, redo can be performed using:

```text
Ctrl + r
```

This re-applies an undone change.

---

# Searching Within a File

VI allows you to search for text.

Use:

```text
/search_term
```

### Example

To search for the word `Linux`:

```text
/Linux
```

Press **Enter**.

VI searches for the specified text.

---

# Case Sensitivity

VI commands are generally **case sensitive**.

For example:

```text
:wq
```

is different from:

```text
:WQ
```

Therefore, commands must be entered using the correct letter case.

> **Important:** Using the wrong command or incorrect case can result in an unexpected operation.

---

# Reading a Text File Using VI

VI can also be used simply to read a text file.

### Example

```bash
vi notes.txt
```

Once the file is open, you can navigate through its contents without making changes.

To exit:

```text
:q
```

---

# Complete Practical Example

The following demonstrates a basic VI workflow.

## Step 1: Create/Open a File

```bash
vi linux.txt
```

## Step 2: Enter Insert Mode

```text
i
```

## Step 3: Enter Text

```text
Linux is an open-source operating system.
VI is a command-line text editor.
Linux provides many useful commands.
```

## Step 4: Return to Command Mode

```text
Esc
```

## Step 5: Save the File

```text
:w
```

Press **Enter**.

## Step 6: Exit VI

```text
:q
```

Press **Enter**.

---

# Practical Example: Save and Quit in One Command

Instead of:

```text
:w
:q
```

you can use:

```text
:wq
```

This saves the file and exits VI.

---

# Practical Example: Exit Without Saving

Open a file:

```bash
vi example.txt
```

Make some changes.

Press:

```text
Esc
```

Then:

```text
:q!
```

Press **Enter**.

The editor exits without saving the changes.

---

# VI Editor Command Summary

| Command       | Purpose                         |
| ------------- | ------------------------------- |
| `vi filename` | Open or create a file           |
| `i`           | Enter Insert Mode before cursor |
| `a`           | Enter Insert Mode after cursor  |
| `o`           | Open a new line below           |
| `Esc`         | Return to Command Mode          |
| `:`           | Enter Last Line Mode            |
| `h`           | Move left                       |
| `j`           | Move down                       |
| `k`           | Move up                         |
| `l`           | Move right                      |
| `0`           | Beginning of line               |
| `$`           | End of line                     |
| `gg`          | Beginning of file               |
| `G`           | End of file                     |
| `x`           | Delete character                |
| `dd`          | Delete line                     |
| `yy`          | Copy line                       |
| `p`           | Paste                           |
| `u`           | Undo                            |
| `Ctrl + r`    | Redo                            |
| `:w`          | Save                            |
| `:q`          | Quit                            |
| `:wq`         | Save and quit                   |
| `:q!`         | Quit without saving             |

---

# Key Concepts to Remember

## Command Mode

Used for:

* Navigation.
* Deleting text.
* Copying text.
* Pasting text.
* Executing commands.

---

## Insert Mode

Used for:

* Adding text.
* Editing file contents.

Common commands to enter Insert Mode:

```text
i
a
o
```

---

## Last Line Mode

Used for:

* Saving files.
* Exiting VI.
* Executing editor commands.

It is entered using:

```text
:
```

---

# Important VI Workflow

Remember the basic sequence:

```text
vi filename
      ↓
Command Mode
      ↓
i
      ↓
Insert Mode
      ↓
Type text
      ↓
Esc
      ↓
Command Mode
      ↓
:wq
      ↓
Save and Exit
```

---

# Course Completion

After completing this course, you should now be able to:

* Understand the **Linux VI editor**.
* Understand the three modes of VI.
* Create and edit files using VI.
* Enter and exit Insert Mode.
* Navigate through file contents.
* Delete text.
* Copy and paste text.
* Save files.
* Exit VI with or without saving.
* Use common VI commands.

---

# Knowledge Assessment

The course concludes with a knowledge assessment covering:

* Introduction to the Linux VI editor.
* VI modes of operation.
* Creating and editing files.
* Saving and exiting files.
* Navigating file contents.
* Deleting content.
* Copying and pasting text.
* Common VI commands.

---

## Course Files

```text
Track05-Linux-VI-Text-Editors/
├── lecture.md
├── assessment.md
└── certificate.pdf
```
