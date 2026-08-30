# Getting Started with Process Management

## Learning Objectives

The learning objective is to gain knowledge on:

* understanding **Linux processes**.
* understanding **process structure**.
* understanding how to **create a process**.
* understanding **foreground and background processes**.
* understanding **process management**.
* understanding process-management commands.

---

## About the Course

This course provides a foundation for understanding **Linux process management**.

The course covers:

* Linux processes.
* Process structure.
* Creating child processes.
* `fork()` and `exec()` functions.
* Linux threads.
* Thread creation.
* Thread termination.
* Foreground and background processes.
* Managing background jobs.
* Process management commands.
* `ps`.
* `kill`.
* `jobs`.
* `fg`.
* `bg`.
* `disown`.
* `nohup`.
* `screen`.

The course is intended to help learners understand the working of processes, their creation and termination, and process management in Linux.

---

## Who Can Benefit from This Course?

This course is beneficial for students who want to understand the **working of processes**, their creation and termination.

The course specifically focuses on process management commands and foreground and background processes.

---

## Prerequisites

The course lists the following prerequisites:

* Basics of Linux.
* Linux administration.
* File ownership.
* File permissions.
* Privileged access to a Linux system as `root` or through the `sudo` command.

---

# Linux Processes

A Linux process is a **kernel abstraction to which system resources are allocated to execute a program**.

A process consists of:

* User-space memory containing a program's code and variables.
* Kernel data structures containing information about the process.

The kernel maintains information associated with the process.

This includes:

* Virtual memory.
* Process tables.
* Open file descriptors.
* Signal-handling information.
* Process resource state.
* Resource limits.
* Parent process information.
* Working directory.
* Other information associated with the process.

---

# Process Structure

A Linux process contains different memory areas and structures used during program execution.

The process structure discussed in the course includes:

* Fixed segment.
* Read-only/shareable segment.
* Initialized data segment.
* Uninitialized data segment.
* Stack.
* Swap.
* Heap.

---

## Fixed Segment

The fixed segment contains the **machine-language program instructions**.

These instructions represent the executable code of the program.

---

## Read-Only / Shareable Segment

The read-only/shareable portion contains machine-language program instructions.

This information can be shared where appropriate because it does not need to be modified during normal execution.

---

## Initialized Data Segment

The initialized data segment contains:

* Global data that has been initialized.
* Local static data that has been initialized.

This data is read when the program is loaded.

---

## Uninitialized Data Segment

The uninitialized data segment contains:

* Uninitialized global data.
* Uninitialized static data.

When the program is loaded, this area is filled with **zeroes**.

---

## Stack

The stack contains **stack frames** associated with program execution.

Stack frames are created dynamically as functions are called.

---

## Heap

The heap provides an area for **dynamic memory allocation**.

It is the area used for dynamic memory allocation made by the program.

---

# Creating a Child Process

A child process can be created in two ways discussed in the course:

* `fork()`
* `exec` functions

---

## `fork()`

The `fork()` function creates a **clone of the parent process**.

After a `fork()` operation, there is normally distinct code execution for:

* The parent process.
* The child process.

The child process is created from the parent process.

---

## `exec` Functions

The `exec` functions replace the existing process program.

They purge/replace the process's existing **code and data** and load another program for execution.

The basic distinction is:

```text
fork()
    ↓
Creates a clone/child process

exec()
    ↓
Replaces the process program
and loads another program
```

---

# Linux Threads

A **thread of execution** is often regarded as the smallest unit of processing that a scheduler works on.

A Linux thread has:

* A process-unique thread ID.
* A set of register values.
* A stack.
* Scheduling priority.
* Scheduling policy.
* A signal mask.
* Thread-specific data.

---

## Thread Execution

A thread starts running the function pointed to by the thread's **run function**.

The run function receives a single argument.

The thread ID points to the thread ID supplied during thread creation.

The thread attributes pointer points to the **thread attributes structure**.

---

# Thread Creation

Linux creates a thread by **cloning the parent thread's execution context**.

The cloned execution context can include resources such as:

* Memory.
* File descriptors.

Each thread has its **own stack**.

Two threads can share:

* Global data.
* Data passed to both threads.
* Appropriate shared structures.

The course emphasizes that although threads can share process resources, each thread has its own execution-related state, including its stack.

---

# Thread Termination

The course describes three ways in which a thread can terminate.

---

## 1. Return from the Run Function

A thread can terminate by returning from its run function.

The return value becomes the thread's exit code.

Conceptually:

```text
return value
      ↓
Thread exit code
```

---

## 2. Thread Cancellation

A thread can be cancelled by another thread within the **same process**.

This provides a mechanism for one thread to request the termination of another thread.

---

## 3. Waiting for a Thread to Complete

One thread, usually the parent, can wait for another thread to terminate.

The course refers to a function used to wait for the thread to complete.

The return value is:

```text
0 → success
Non-zero → error code
```

---

# Foreground and Background Processes

Linux systems allow **simultaneous process execution**.

Linux also allows programs to run in:

* Foreground.
* Background.

Running commands in the background is a common task when:

* The terminal needs to remain available.
* A command runs for a long time.
* A process needs to continue while other commands are executed.
* Working through an SSH session requires a process to continue independently.

Long-running commands may either listen for events or perform lengthy tasks.

---

# Stopping a Foreground Process

If a command is running and needs to be placed into the background, the course demonstrates using:

```text
Ctrl + Z
```

This stops/suspends the process.

The suspended job can then be managed using the job-control commands.

---

# `jobs` Command

The `jobs` command displays a list of jobs running or stopped in the background.

Example:

```bash
jobs
```

It can be used to check the status of jobs associated with the current shell.

A job can have a job ID that can be referenced using the `%` sign.

---

# `fg` Command

The `fg` command brings a background job back to the **foreground**.

Example:

```bash
fg
```

If multiple stopped jobs exist, the appropriate job ID can be specified using the `%` sign.

Conceptually:

```bash
fg %job_id
```

This allows the required job to be brought back to the foreground.

---

# `bg` Command

The `bg` command resumes a stopped job and allows it to continue running in the **background**.

Example:

```bash
bg
```

When a stopped job is resumed with `bg`, its status changes from:

```text
Stopped
```

to:

```text
Running
```

The job continues executing in the background.

---

# `disown` Command

If the terminal needs to be closed while a background job should continue running, the job can be removed from the shell's job table using the `disown` command.

Example:

```bash
disown
```

If multiple jobs exist, the appropriate job can be specified using its job ID after the `%` sign.

Conceptually:

```bash
disown %job_id
```

After a job is disowned:

* It is no longer shown in the shell's job table.
* Closing the terminal does not cause the shell to manage it as one of its jobs.
* The command can continue running.

This is useful when working with long-running commands.

---

# Starting a Command Directly in the Background

A command can be started directly in the background by placing an **ampersand (`&`)** at the end of the command.

Example:

```bash
command &
```

The command starts running in the background immediately.

The job can then be viewed using:

```bash
jobs
```

Unlike using `Ctrl + Z`, the command does not first need to be manually stopped and resumed.

---

# Closing the Terminal While Keeping a Background Job Running

The course discusses multiple ways to allow background commands to continue after the terminal is closed.

These include:

* `disown`
* `nohup`
* `screen`

---

# `nohup` Command

The `nohup` command tells a process to **ignore SIGHUP (hangup) signals** that it receives.

A **SIGHUP** signal can be sent to a background job when the current terminal is closed.

Using `nohup` allows a command to continue running after the terminal is closed.

Conceptually:

```text
Terminal
    ↓
Closed
    ↓
SIGHUP
    ↓
Normally affects background job

nohup
    ↓
Process ignores SIGHUP
    ↓
Process continues running
```

---

## Using `nohup`

A command can be started with:

```bash
nohup command
```

The command can then continue running after the terminal is closed.

When the terminal is opened again, the process can still be found running.

---

# `screen` Command

The course also introduces the **screen** command.

`screen` can be used to start a persistent terminal session.

It allows a command or script to continue running even after the terminal session is disconnected.

---

## Starting a Screen Session

A new screen session can be started using:

```bash
screen
```

The course also mentions that the `-S` option can optionally be used to provide a name for the screen session.

Conceptually:

```bash
screen -S name
```

---

## Running a Command in Screen

After starting a screen session:

1. Start a new screen session.
2. Execute the command or script that should continue running.
3. Detach from the screen session.
4. Close the terminal or log out of the SSH session.

The screen session persists after the terminal is closed.

---

## Detaching from Screen

To detach from a screen session, use:

```text
Ctrl + A
```

followed by:

```text
D
```

This detaches the current screen session.

The command running inside the screen continues running.

---

## Closing the Terminal

After detaching from screen:

* The terminal can be closed.
* The user can log out of SSH.
* The screen session persists.
* Commands running inside the screen session continue executing.

---

# Listing Screen Sessions

The course demonstrates a command for viewing existing screen sessions.

The command is:

```bash
screen -ls
```

This displays a list of available screen sessions.

---

# Reattaching to a Screen Session

A detached screen session can be reattached.

The appropriate screen/session ID is supplied when reattaching.

Conceptually:

```bash
screen -r <process_id>
```

The course explains that the number shown for the screen session can be substituted when reconnecting to it.

---

# Process Management Commands

Linux provides commands that allow users to monitor and manage running processes.

The course specifically discusses:

* `ps`
* `kill`
* `jobs`
* `fg`
* `bg`
* `disown`
* `nohup`
* `screen`

---

# `ps` Command

The `ps` command can be used to keep an eye on **running commands/processes**.

Example:

```bash
ps
```

It provides information about processes running on the system/session.

---

# `kill` Command

The `kill` command can be used to stop a running process.

The process ID (**PID**) is specified with the command.

Conceptually:

```bash
kill <process_id>
```

The command sends a signal to the specified process.

---

# Process ID

Processes are identified using a **process ID (PID)**.

The PID can be used with process-management commands such as:

```bash
kill <PID>
```

The PID allows the appropriate process to be identified and managed.

---

# Foreground and Background Workflow

The course demonstrates the following workflow for managing a process:

```text
Run command
      ↓
Foreground process
      ↓
Ctrl + Z
      ↓
Stopped job
      ↓
bg
      ↓
Background running job
      ↓
jobs
      ↓
View job
```

A background job can later be returned to the foreground:

```text
Background job
      ↓
fg
      ↓
Foreground process
```

---

# Background Process Workflow

A command can also be started directly in the background:

```text
command &
      ↓
Running background job
      ↓
jobs
      ↓
View job
```

If the terminal needs to be closed, additional methods include:

```text
disown
```

or:

```text
nohup
```

or:

```text
screen
```

---

# Comparing Background Job Methods

| Method     | Purpose                                              |
| ---------- | ---------------------------------------------------- |
| `Ctrl + Z` | Suspend a foreground process                         |
| `jobs`     | Display shell jobs                                   |
| `fg`       | Bring a job to the foreground                        |
| `bg`       | Resume a stopped job in the background               |
| `&`        | Start a command directly in the background           |
| `disown`   | Remove a job from the shell's job table              |
| `nohup`    | Allow a process to ignore SIGHUP                     |
| `screen`   | Maintain a persistent terminal session               |
| `ps`       | View running processes                               |
| `kill`     | Send a signal to a process, commonly to terminate it |

---

# Course Completion

After completing the course, the learner should now be able to:

* Understand **Linux processes**.
* Understand **process structure**.
* Understand how to **create a process**.
* Understand the use of `fork()`.
* Understand the use of `exec` functions.
* Understand **Linux threads**.
* Understand thread creation.
* Understand thread termination.
* Understand **foreground and background processes**.
* Use `jobs` to view jobs.
* Use `fg` to bring jobs to the foreground.
* Use `bg` to resume jobs in the background.
* Use `disown` to detach jobs from the shell's job table.
* Use `nohup` to allow processes to ignore SIGHUP.
* Use `screen` for persistent terminal sessions.
* Use `ps` to monitor processes.
* Use `kill` to manage running processes.

---

# Course Summary

The key concepts covered in this course are:

* A Linux process is a **kernel abstraction to which system resources are allocated to execute a program**.
* A process contains user-space memory and kernel data structures.
* Process information includes virtual memory, process tables, open file descriptors, signal information, resource state and limits, parent information and working directory.
* Process memory contains areas such as code, initialized data, uninitialized data, stack and heap.
* `fork()` creates a clone of the parent process.
* `exec` functions replace the existing process program with another program.
* A thread is a unit of execution that a scheduler works on.
* Threads have their own stack and execution-related information.
* Threads can share resources such as global data.
* A thread can terminate by returning from its run function.
* A thread can be cancelled by another thread in the same process.
* A thread can be waited on until it completes.
* Linux supports foreground and background processes.
* `Ctrl + Z` stops/suspends a foreground process.
* `jobs` lists background/stopped jobs.
* `fg` brings a job to the foreground.
* `bg` resumes a stopped job in the background.
* `&` starts a command directly in the background.
* `disown` removes a job from the shell's job table.
* `nohup` allows a process to ignore SIGHUP.
* `screen` provides a persistent terminal session.
* `screen -ls` lists screen sessions.
* `screen -r` can be used to reattach to a screen session.
* `ps` is used to view running processes.
* `kill` can be used to send a signal to a process using its PID.

---

## Course Files

```text
Track08-Process-Management/
├── lecture.md
├── assessment.md
└── Certificate.pdf
```
