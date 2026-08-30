# Getting Started with Advanced Shell Scripting

## Learning Objectives

The learning objective is to gain knowledge on:

* becoming familiar with **shell scripting**.
* understanding **basic arithmetic operations**.
* understanding **conditional instructions**.
* understanding **loops** in shell scripting.
* understanding basic shell-scripting constructs used in Linux.

---

## About the Course

This course introduces **Linux shell scripting** and its basic programming constructs.

The course covers:

* Linux shell and shell scripting.
* Shell types.
* Shell scripts.
* Shell variables.
* Comments in shell scripts.
* The shebang.
* Basic mathematical and arithmetic operations.
* Relational operators.
* Conditional statements.
* `if` statements.
* `if-else` statements.
* `elif` statements.
* Nested `if-else` statements.
* `case` statements.
* `for` loops.
* `while` loops.
* `until` loops.
* Differences between `while` and `until` loops.
* Automation using shell scripts.
* Debugging using shell scripts.

---

## Who Can Benefit from This Course?

This course is beneficial for students who want to learn **Linux shell scripting** and develop an understanding of basic programming constructs in the Linux environment.

The course specifically focuses on:

* Basic mathematical operations.
* Conditional instructions.
* Loops.
* Shell scripting fundamentals.

---

## Prerequisites

Before learning shell scripting, you should have:

* Basic knowledge of operating systems.
* Access to the **command line or terminal**.

---

# What Does the Shell Do?

The **shell** is responsible for communicating commands and instructions to the **kernel**.

A shell is a **command language interpreter** that executes commands from:

* Files.
* Standard keyboard input.

The shell is **not part of the system kernel**.

It is required by the user to communicate with the kernel and run programs.

---

# Linux Shell

Linux provides different types of shells.

The course mentions shells such as:

* Bourne shell (`sh`).
* Bash (`bash`).
* C shell (`csh`).
* Korn shell (`ksh`).
* Other shells available on the system.

The shell is a program that:

1. Receives commands and instructions from the user.
2. Interprets those commands.
3. Sends the appropriate instructions to the kernel.
4. Allows programs and commands to be executed.

---

# Shell Scripting

Linux shells such as **Bash** allow script-based programming constructs.

Many Linux commands and scripts can use shell scripting constructs.

Shell scripts are transformed/interpreted into shell commands during execution.

Because scripts are converted/interpreted into shell commands, many Linux commands can themselves be implemented as scripts.

---

# Importance of Shell Scripting for System Administrators

A system administrator should have a **fundamental understanding of scripting**.

This is important for understanding how servers and applications are:

* Started.
* Upgraded.
* Maintained.
* Uninstalled.
* Configured.

Shell scripting also helps administrators understand how the **user environment** is created and configured.

A basic understanding of scripting is therefore important for system administration.

---

# Why Program with Shell?

Shell scripting has several advantages.

The shell:

* Can be programmed rapidly.
* Is easily available on most Linux installations.
* Is always available in a Linux environment.
* Works well for straightforward tasks.
* Provides simplicity.
* Makes configuration and maintenance easier.
* Helps automate daily tasks.

Shell scripting is particularly useful when **portability, simplicity of configuration, and maintenance** are more important than execution efficiency.

---

# Shell Script Execution

Commands in a shell execute in a **preset order**.

Shell scripts are:

* Run by the shell.
* Runtime interpreted.
* Executed according to the instructions contained in the script.

Shell scripting helps automate a number of **daily tasks**.

Debugging can also be made simpler through the use of scripts.

---

# Determining the Shell

The current shell can be determined using an appropriate shell command.

The course demonstrates identifying the shell and shows **Bash** as the shell.

The shell can be identified from the command-line environment.

---

# Dollar Sign in Shell

The **dollar sign (`$`)** is used when referring to shell variables.

For example:

```bash
$var
```

Here, `var` represents the name of a shell variable.

The course also explains that the dollar sign is associated with accessing the value stored in a shell variable.

---

# `echo` Command

The `echo` command returns/displays the text supplied to it.

Example:

```bash
echo "Hello"
```

The text supplied to `echo` is displayed as output.

It can also be used to display the value of a shell variable.

Example:

```bash
echo $var
```

---

# Shebang

The **shebang** is written at the top of a shell script.

It begins with:

```text
#!
```

The shebang specifies which interpreter should be used to execute the script.

For example:

```bash
#!/bin/sh
```

This tells the system to use `/bin/sh` to run the script.

The shell specified by the shebang should be supported by the system.

---

# Shell Scripting Comments

Comments can be added to shell scripts.

A line beginning with a **hash (`#`)** is treated as a comment, except for the special `#!` shebang at the beginning of a script.

Comments:

* Explain code.
* Are not used during script execution.
* Do not appear as normal script output.

Example:

```bash
# This is a comment
```

The line beginning with `#` is not executed as a command.

---

# Shell Scripting Variables

Variables can be contained inside shell scripts.

Variables are used to store values that can be accessed during script execution.

For example:

```bash
var1=value1
var2=value2
```

The values can then be accessed using:

```bash
echo $var1
echo $var2
```

The course demonstrates variables such as:

```text
$var1
$var2
```

---

## Variable Lifetime

Shell variables created inside a script do not survive the conclusion of that script in the same way as persistent external environment settings.

This is because shell scripts execute in their own shell/environment.

Therefore, variables created within the script are generally available during the script's execution.

---

# Basic Math Operations

Mathematical and arithmetic operations are essential in **Bash scripting**.

Shell scripting supports basic arithmetic operations that can be used when processing numeric values.

The course provides a table showing various mathematical operations and their usage.

These arithmetic operations allow calculations to be performed within shell scripts.

---

# Relational Operators

Operators that specify the relationship between two operands are known as **relational operators**.

Relational operators are used to compare values.

The course provides a table containing relational operators and their functions.

---

## Less Than Operator

The **less-than (`<`)** operator returns true if the first operand is less than the second operand.

If the first operand is not less than the second operand, the result is false.

Conceptually:

```text
first operand < second operand
```

The result is:

```text
True  → first operand is less than second operand
False → otherwise
```

---

# Conditional Statements

The course introduces conditional statements used in Bash programming.

The main conditional constructs covered include:

* `if`
* `if-else`
* `elif`
* Nested `if-else`
* `case`

These constructs allow a shell script to make decisions based on conditions.

---

# `if` Statement

An `if` statement executes a block of code when a specified condition is **true**.

Conceptually:

```text
if condition is true
        ↓
execute statements
```

If the specified condition is not true, the statements inside the `if` block are not executed.

---

# `if-else` Statement

An `if-else` statement provides two possible execution paths.

If the specified condition is **true**, the `if` part is executed.

If the condition is **false**, the `else` part is executed.

Conceptually:

```text
Condition
   │
   ├── True  → if block
   │
   └── False → else block
```

---

# `elif` Statement

The `elif` keyword is used when **multiple conditions** need to be evaluated in one conditional structure.

If expression 1 is true, its corresponding statements are executed.

If it is false, the next condition is checked.

This process continues until:

* A true condition is found.
* None of the conditions are true.

If none of the conditions is true, the `else` part is processed.

Conceptually:

```text
if expression 1
    statement 1
elif expression 2
    statement 2
elif expression 3
    statement 3
else
    statement
```

---

# Nested `if-else` Block

A **nested `if-else` block** is used when one condition needs to be checked and, after satisfying that condition, another condition needs to be checked.

For example:

```text
Condition 1
   ↓
Condition satisfied
   ↓
Check Condition 2
```

If expression 1 is false, the `else` portion is processed.

Another expression can then be checked within the appropriate conditional block.

Nested conditional structures allow more detailed decision-making.

---

# `case` Statement

The **case statement** works similarly to a switch statement.

It compares a specified value with available patterns.

If the specified value matches a pattern, the associated block of statements is executed.

Conceptually:

```text
Value
  ↓
Compare with patterns
  ↓
Matching pattern
  ↓
Execute associated statements
```

---

## Pattern Matching in `case`

When a match is found, the statements associated with that pattern are executed.

Execution continues until the terminating:

```text
;;
```

is encountered.

The case branch is terminated when the last command associated with the matching pattern is executed.

If there is **no match**, the case statement completes without executing a matching branch.

The exit status of the case statement reflects the result of the operation.

---

# Shell Scripting `for` Loop

The `for` loop is used to repeatedly execute a block of commands.

The keywords associated with the basic structure include:

```text
for
in
do
done
```

Conceptually:

```bash
for variable in list
do
    statements
done
```

---

## List in a `for` Loop

A **list** is a collection of variables or values separated by spaces.

The loop processes the values in the list.

If a list is not mentioned in the `for` statement, the **positional parameter values supplied to the shell** are used.

The variable name in the loop can be selected by the user.

---

# Shell Scripting `while` Loop

The `while` loop in Linux shell scripts is comparable to the `while` loop in the C programming language.

The `while` loop executes its code block while the specified condition remains true.

Conceptually:

```text
Condition true
     ↓
Execute loop body
     ↓
Check condition again
     ↓
Continue while condition is true
```

When the condition is no longer true, the loop stops.

---

# Shell Scripting `until` Loop

The `until` loop is similar to the `while` loop but works with the opposite condition.

The fundamental difference is:

* The **while** loop executes its code block while the conditional expression is **true**.
* The **until** loop executes its code block while the conditional expression is **false**.

---

# Difference Between `while` and `until`

The distinction between the two loops can be summarized as:

| Loop    | Condition for continuing               |
| ------- | -------------------------------------- |
| `while` | Continues while the condition is true  |
| `until` | Continues while the condition is false |

In terms of shell status:

* A `while` loop continues while the condition returns a **zero** status.
* An `until` loop continues until a value other than **zero** is returned.

---

# Shell Scripting and Automation

Shell scripting assists in **automating daily tasks**.

Instead of manually executing a sequence of commands, commands can be placed into a script and executed as a group.

This can improve:

* Automation.
* Repeatability.
* Maintenance.
* Administration efficiency.

---

# Course Completion

After completing the course, the learner should now be able to:

* Become familiar with **shell scripting**.
* Understand basic **arithmetic operations**.
* Understand **relational operators**.
* Understand conditional instructions.
* Use `if` statements.
* Use `if-else` statements.
* Use `elif` for multiple conditions.
* Understand nested `if-else` blocks.
* Understand the `case` statement.
* Understand `for` loops.
* Understand `while` loops.
* Understand `until` loops.
* Understand the difference between `while` and `until`.
* Understand shell variables.
* Understand comments.
* Understand the shebang.
* Understand how shell scripts help automate tasks.

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

* A **shell** communicates commands and instructions between the user and the kernel.
* The shell is a **command language interpreter**.
* The shell is not part of the system kernel.
* Linux provides different shells, including **Bash**, `sh`, `csh`, and `ksh`.
* Shell scripting allows programming constructs to be used in Linux.
* Shell scripts are interpreted by the shell at runtime.
* Shell scripting can automate daily tasks.
* Shell scripting is useful for straightforward jobs where portability, simplicity, configuration, and maintenance are important.
* The **dollar sign (`$`)** is used when accessing shell variable values.
* `echo` displays supplied text or variable values.
* The **shebang (`#!`)** specifies the interpreter used to execute a script.
* Lines beginning with `#` are comments and are not executed.
* Shell scripts can contain variables.
* Variables created within a script generally exist within that script's shell/environment.
* Bash supports basic mathematical and arithmetic operations.
* **Relational operators** specify relationships between operands.
* The `<` operator returns true when the first operand is less than the second operand.
* Conditional statements allow scripts to make decisions.
* `if` executes statements when a condition is true.
* `if-else` provides separate paths for true and false conditions.
* `elif` allows multiple conditions to be checked.
* Nested `if-else` blocks allow additional conditions to be checked within another condition.
* The `case` statement works similarly to a switch statement and matches values against patterns.
* The `for` loop uses keywords such as `for`, `in`, `do`, and `done`.
* A list in a `for` loop is a collection of values separated by spaces.
* If a list is not specified, positional parameters supplied to the shell can be used.
* The `while` loop continues while its condition is true.
* The `until` loop continues while its condition is false.
* A `while` loop continues while a zero status is returned.
* An `until` loop continues until a non-zero status is returned.
* Shell scripting is useful for automation, configuration, maintenance, and administration tasks.
* The course requires **80%** to pass the final assessment.

---

## Course Files

```text
Track09-Advanced-Shell-Scripting/
├── lecture.md
├── assessment.md
└── Certificate.pdf
```
