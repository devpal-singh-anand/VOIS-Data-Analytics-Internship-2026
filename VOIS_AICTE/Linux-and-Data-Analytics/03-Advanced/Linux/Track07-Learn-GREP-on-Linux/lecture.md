# Getting Started with grep on Linux

## Learning Objectives

The learning objective is to gain knowledge on:

* understanding how to **search files for strings**.
* understanding how to **match patterns** and search for them.
* using **grep** to search for strings and patterns.
* understanding the basic use of **regular expressions** with grep.
* understanding different syntax used to search strings in files.

---

## About the Course

This course provides a foundation for searching and matching text in Linux.

The course covers:

* The **grep** command.
* Searching for strings in files.
* Searching for patterns.
* Using grep options.
* **Regular expressions**.
* Special characters used in regular expressions.
* Escaping special characters using the backslash (`\`).
* Character matching using square brackets.
* Extended matching using `-E`.
* Pattern-completion/matching characters.

The course is intended to help learners develop foundational Linux concepts related to text searching and pattern matching.

---

## Who Can Benefit from This Course?

This course is beneficial for students who want to develop **foundation concepts of Linux**.

The course specifically focuses on using Linux commands to search text and files efficiently.

---

## Prerequisites

The course lists the following prerequisites:

* Basics of Linux.
* Linux administration.
* File ownership.
* File permissions.
* Linux administration fundamentals.

---

# grep Command

The **grep** command is a very useful Linux command.

The name **grep** stands for:

```text
Global Regular Expression Print
```

grep is used to select lines from text files that **match specified patterns**.

It is commonly used when searching for particular strings or patterns within text.

---

# grep and find

The course distinguishes between **grep** and **find**.

## grep

`grep` is used to search the **contents of text files** for lines that match a specified pattern.

For example, grep can be used to find lines containing a particular word or string.

---

## find

`find` is used to search the system for:

* Files.
* Directories.

Therefore:

```text
grep → searches inside files for matching text
find → searches the system for files/directories
```

---

# grep Syntax

The basic syntax of grep consists of:

```bash
grep [options] pattern [files]
```

The command contains:

* **Options** — control how grep performs the search.
* **Pattern** — specifies what should be matched.
* **Files** — specifies the files in which the search should be performed.

Conceptually:

```text
grep
 │
 ├── options
 ├── pattern to match
 └── files to search
```

---

## Standard Input

If no file names are given, grep can search from **standard input**.

This means grep can receive text through the standard input stream rather than directly from a specified file.

---

# grep Options

The course introduces several useful options for the grep command.

---

## `-c`

The `-c` option prints only a **count of the lines that match** the specified pattern.

Example:

```bash
grep -c pattern file
```

Instead of displaying every matching line, the command returns the number of matching lines.

---

## `-v`

The `-v` option prints all lines that **do not match** the specified pattern.

Example:

```bash
grep -v pattern file
```

This is useful when the goal is to find lines that exclude a particular pattern.

---

## `-l`

The `-l` option lists the **file names only** for files containing a matching pattern.

Example:

```bash
grep -l pattern file1 file2 file3
```

Instead of printing matching lines, grep prints the names of files in which the pattern was found.

---

# Regular Expressions

A **regular expression** provides an ability to match a string of text in a very flexible and concise manner.

A string of text can be further defined as:

* A single character.
* A word.
* A sentence.
* A particular pattern of characters.

Regular expressions allow searches to be described using patterns rather than requiring an exact literal string.

---

# Special Characters in Regular Expressions

When regular expressions are used, certain characters are processed in a **special way**.

These characters have special meanings within a pattern.

The course presents a table of frequently used special characters.

---

## Escaping Special Characters

If one of the special characters needs to be treated as a **normal/literal character**, it must be preceded by a **backslash (`\`)**.

The backslash tells grep that the following character should be interpreted literally rather than according to its special regular-expression meaning.

---

## Example — Searching for `$`

The dollar sign is a special regular-expression character.

If the goal is to search for an actual dollar character, it should be preceded by a backslash.

Example:

```text
\$
```

Therefore, the backslash is used to escape the special meaning of `$`.

---

# Character Matching Using Square Brackets

Regular expressions also provide useful matching patterns using **square brackets**.

Example structure:

```text
[...]
```

Square brackets can be used to define a set or range of characters that can be matched.

The course provides a table describing useful matching patterns that can be used within square brackets.

These patterns provide additional flexibility when searching for text.

---

# Extended Regular Expressions

The course also introduces **extended matching**.

The `-E` option is used for **extended regular expression matching**.

Example:

```bash
grep -E pattern file
```

Extended regular expressions provide additional pattern-matching capabilities.

---

# Pattern-Completion / Matching Characters

Additional characters can control how matching is performed.

These characters can follow a regular expression and affect the way the pattern is matched or completed.

When these characters have a special meaning, they also need to be preceded by a **backslash** when they are intended to be treated as literal characters.

---

# Backslash and Regular Expressions

The **backslash (`\`)** is important when working with grep and regular expressions.

It is used to:

* Escape special characters.
* Tell grep to treat a special character literally.
* Control the interpretation of certain pattern characters.

For example:

```text
\$
```

means that `$` should be treated as a literal dollar character rather than its regular-expression meaning.

---

# grep Pattern Matching

The main purpose of grep in this course is to search for text that matches a specified pattern.

The matching process can be summarized as:

```text
Pattern
   ↓
grep
   ↓
Search file/text
   ↓
Identify matching lines
   ↓
Display or count results
```

Depending on the options used, grep can:

* Display matching lines.
* Display non-matching lines.
* Count matching lines.
* Display only the names of matching files.

---

# grep vs Regular Expressions

The course combines **grep** with **regular expressions**.

The roles can be understood as:

```text
grep
 ↓
Performs the search

Regular expression
 ↓
Defines the pattern to match
```

Together, they provide a flexible mechanism for searching text in Linux.

---

# Course Completion

After completing the course, the learner should now be able to:

* Understand how to **search files for strings**.
* Understand how to **match a pattern and search for it**.
* Understand the purpose and use of the **grep** command.
* Understand the relationship between grep and **regular expressions**.
* Use grep options to control search output.
* Understand the use of special characters in regular expressions.
* Escape special characters using the backslash.
* Understand character matching using square brackets.
* Understand extended matching using `-E`.

---

# Assessment

The course concludes with an assessment to check the learner's knowledge.

The required passing score is:

```text
80%
```

If the learner is ready, they can proceed to the assessment.

If the learner is not ready, they can select the option to **retake/review the course** before attempting the assessment again.

---

# Course Summary

The key concepts covered in this course are:

* **grep** is a Linux command used to search text for matching patterns.
* grep stands for **Global Regular Expression Print**.
* `find` is used to search the system for files and directories.
* grep can search files for specified patterns.
* If no file name is supplied, grep can use **standard input**.
* The basic grep syntax contains options, a pattern and files to search.
* `-c` prints a count of matching lines.
* `-v` prints lines that do not match the pattern.
* `-l` lists file names containing matches.
* **Regular expressions** provide flexible pattern matching.
* A string can represent a character, word, sentence or pattern of characters.
* Some characters have special meanings in regular expressions.
* A **backslash (`\`)** can be used to escape special characters.
* Square brackets provide useful character-matching patterns.
* `-E` enables extended regular-expression matching.
* Additional matching/completion characters can affect how patterns are matched.
* The course requires **80%** to pass the final assessment.

---

## Course Files

```text
Track07-Learn-GREP-on-Linux/
├── lecture.md
├── assessment.md
└── Certificate.pdf
```
