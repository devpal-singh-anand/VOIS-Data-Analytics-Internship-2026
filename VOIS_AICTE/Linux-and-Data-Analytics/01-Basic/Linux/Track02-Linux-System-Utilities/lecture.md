# Linux System Utilities

## Learning Objectives

The learning objective is to gain knowledge on:

* becoming familiar with **Linux system utilities**.
* understanding the purpose of Linux system utilities.
* understanding approximately **ten useful utilities for Linux users**.
* using command-line utilities to monitor system performance.
* viewing disk usage and mounted file systems.
* retrieving system and hardware information.
* monitoring network statistics.
* viewing system activity and logs.

---

## Prerequisites

* A system with **Linux installed**.
* Basic understanding of the Linux environment.
* Basic understanding of the Linux file system.

---

# About the Course

This course introduces **Linux system utilities** and useful utility commands for Linux users.

A **system utility** provides functionality of the operating system to the user and helps users access operating-system features.

Utilities can be used for specialized tasks such as:

* Monitoring system performance.
* Viewing disk usage.
* Finding mounted file systems.
* Retrieving hardware information.
* Monitoring network connections.
* Viewing system statistics.
* Reading and highlighting log files.

---

# Useful Linux Utilities

The course introduces several useful Linux utilities, including:

* `w`
* `nmon`
* `ncdu`
* `Slurm`
* `findmnt`
* `at`
* `saidar`
* `ss`
* `ccze`
* `ran1.be`

---

# `w` Command

The `w` command is used to display information about users currently logged into the Linux system.

It shows:

* Who is logged into the system.
* What the logged-in users are doing.
* Processes being executed by users.

Example:

```bash
w
```

The command displays information about the users currently using the machine and their activities.

---

# `nmon`

**nmon** is a fully interactive performance-monitoring command-line utility for Linux.

It is a monitoring and benchmarking tool that displays performance information about various system resources.

It can monitor:

* CPU
* Memory
* Network
* Disks
* File systems
* Processes
* System resources

---

## Capturing System Data with nmon

One useful capability of `nmon` is its ability to capture system data for a period of time and save the information to a file.

This can be useful when analyzing system performance over time.

Example installation command:

```bash
sudo apt-get install nmon
```

---

# `ncdu`

**ncdu** is a command-line tool used to view and analyze disk-space usage on Linux.

It can drill down into directories and report the amount of space used by individual directories.

It is useful for:

* Finding large directories.
* Analyzing disk usage.
* Identifying files or directories consuming significant storage.

Example:

```bash
ncdu
```

---

# Slurm

**Slurm** is a utility/system used for managing computing resources and jobs.

It helps users:

* Allocate resources.
* Keep track of jobs.
* Monitor job progress.

The course introduces various options and commands associated with Slurm.

---

# `findmnt`

The `findmnt` command is used to find and display mounted file systems.

It can:

* List mounted file systems.
* Search for a particular file system.
* Display mounted file-system information in a list format.

Example:

```bash
findmnt
```

The command can also be used to search for a specific file system.

---

# System Information Utility

The course introduces a utility used to retrieve information and statistics from different components of the system.

It can provide information about components such as:

* Network connections.
* I/O devices.
* CPU.
* Other system components.

This type of information is particularly useful for **system administrators**.

---

# CPU Information

More detailed information about the CPU can be obtained using Linux commands.

CPU information can help administrators understand:

* Processor details.
* CPU resources.
* System hardware characteristics.

---

# `saidar`

**saidar** is a curses-based system-monitoring utility.

---

## Curses-Based Software

Curses-based software is software whose user interface is implemented through the **curses library**.

`saidar` provides a terminal-based interface for viewing system statistics and monitoring Linux systems.

It runs directly in a terminal.

---

## Installing Saidar

The course introduces commands for installing and using `saidar`.

---

## Saidar Arguments

### Display Help

The `-h` argument is used to display help.

```bash
saidar -h
```

### Set Update Interval

The `-c` argument is used to set the update interval.

### Colored Output

The `-v` argument is used to display colored output.

### Display Version

The `-d` argument is used to display the version of `saidar`.

---

# `ss` — Socket Statistics

The **`ss` command** is a command-line utility used to display network statistics.

`ss` stands for **socket statistics**.

It can be used to gather network information and troubleshoot network issues.

---

## Advantages of `ss`

The `ss` command is:

* Simple.
* Fast.
* Useful for network troubleshooting.

It is commonly considered a faster and simpler replacement for the now-obsolete `netstat` command.

The `ss` command is commonly used together with the `ip` command when gathering network information.

Example:

```bash
ss
```

---

# `ss` Features

The course mentions that `ss` can provide information related to:

* Network sockets.
* Network connections.
* Socket statistics.

This information is useful for:

* Network monitoring.
* Troubleshooting.
* Understanding active connections.

---

# `ccze`

**ccze** is a tool that **color-highlights log files**, making them easier to read.

It can be useful when working with system logs and other log files.

Color highlighting makes important information easier to identify visually.

---

# `ran1.be`

The course introduces a Python-based terminal utility referred to as **ran1.be**.

It can be used to display system activities graphically.

It runs in a terminal and presents system information in an easily understandable format.

---

## Installing and Using the Utility

The course provides commands for:

* Installing the utility.
* Installing Python on a Linux system.
* Updating the system.

The utility is implemented as a Python script.

---

# System Activity Visualization

The Python-based utility displays detailed information about the user's computer or system while maintaining an easily understandable presentation.

It can display information such as:

* Total system running time.
* Daily average.
* System activity.

It presents activity information using a **histogram**.

The result provides a visual representation of system activity directly in the terminal.

---

# Linux System Utilities — Quick Reference

| Utility                       | Main Purpose                               |
| ----------------------------- | ------------------------------------------ |
| `w`                           | Shows logged-in users and their activities |
| `nmon`                        | Monitors system performance                |
| `ncdu`                        | Analyzes disk-space usage                  |
| `Slurm`                       | Allocates resources and monitors jobs      |
| `findmnt`                     | Displays mounted file systems              |
| System information utilities  | Retrieve hardware/system statistics        |
| `saidar`                      | Displays system statistics in a terminal   |
| `ss`                          | Displays network/socket statistics         |
| `ccze`                        | Color-highlights log files                 |
| Python-based activity utility | Displays system activity graphically       |

---

# Important Commands

## Install nmon

```bash
sudo apt-get install nmon
```

---

## Find Mounted File Systems

```bash
findmnt
```

---

## Display Logged-In Users

```bash
w
```

---

## Display Saidar Help

```bash
saidar -h
```

---

## Display Network Statistics

```bash
ss
```

---

## Analyze Disk Usage

```bash
ncdu
```

---

# Utility Categories

Linux utilities covered in this course can be grouped according to their purpose.

### User and Process Information

```text
w
```

Used to see logged-in users and their activities.

### Performance Monitoring

```text
nmon
saidar
```

Used to monitor system performance and statistics.

### Disk Management

```text
ncdu
findmnt
```

Used to analyze disk usage and mounted file systems.

### Job and Resource Management

```text
Slurm
```

Used for resource allocation and job monitoring.

### Network Monitoring

```text
ss
```

Used to display socket and network statistics.

### Log Management

```text
ccze
```

Used to color-highlight log files.

### System Activity Visualization

```text
ran1.be
```

Used to display system activity graphically in the terminal.

---

# Course Summary

After completing this course, you should now be familiar with:

* Linux system utilities.
* The purpose of system utilities.
* The `w` command.
* `nmon` system monitoring.
* `ncdu` disk-space analysis.
* Slurm resource and job management.
* `findmnt` for mounted file systems.
* System information utilities.
* `saidar` system monitoring.
* `ss` socket and network statistics.
* `ccze` log-file highlighting.
* Python-based system activity visualization.
* Useful Linux commands for system administration and troubleshooting.

---

## Course Files

```text
02-Linux-System-Utilities/
├── lecture.md
├── assessment.md
└── certificate.pdf
```
