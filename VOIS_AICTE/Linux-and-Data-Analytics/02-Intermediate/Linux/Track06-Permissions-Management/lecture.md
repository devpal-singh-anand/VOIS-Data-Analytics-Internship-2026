# VOIS FOR TECH — Linux Permissions Management

## Learning Objectives

The learning objective is to gain knowledge on:

* understanding Linux file permissions and ownership.
* understanding different permission modes in Linux.
* understanding how to change file and directory permissions.
* understanding user, group, and other permission categories.
* understanding basic Linux ownership management commands.

---

## Prerequisites

* Basic understanding of Linux.
* Basic understanding of Linux file ownership.
* Basic understanding of Linux file permissions.
* Basic knowledge of changing file and directory permissions.
* Basic knowledge of Linux commands.

---

# About the Course

This course introduces **permission management in Linux**.

Linux uses permissions and ownership to control who can access, modify, execute, or manage files and directories.

The course covers:

* Linux file ownership.
* Linux file permissions.
* User, group, and other permission categories.
* Changing file and directory ownership.
* Changing file and directory permissions.
* Permission modes in Linux.
* Special permissions.

---

# Introduction to Linux Permissions

Linux provides permissions to control who can access and edit files and directories.

Unix-like operating systems such as Linux commonly run in environments where multiple users may access the same system.

Permissions help protect files and directories by controlling access.

Every file and directory has:

* An **owner**.
* A **group**.
* Permissions for the **owner/user**.
* Permissions for the **group**.
* Permissions for **others**.

By default, the user who creates a file generally becomes its owner.

The system administrator or `root` user can change ownership when required.

---

# Linux File Ownership

Every file and directory in Linux is associated with a specific user and group.

For example, a file may have:

```text
Owner: aryan
Group: developers
```

The owner and group determine which permissions apply to users accessing the file.

---

# User, Group, and Other

Linux divides users accessing a file into three major permission categories.

## 1. User / Owner

The **user** is normally the person who created the file.

For example:

```text
-rw-r--r-- 1 aryan developers file.txt
```

Here:

```text
Owner: aryan
```

The owner can have permissions different from the group and other users.

---

## 2. Group

A **group** is a collection of users.

All users belonging to a particular group can receive the permissions assigned to that group.

Example:

```text
Group: developers
```

If the group has read permission on a file, members of the `developers` group can read that file.

---

## 3. Other

**Other** refers to users who are neither:

* The file owner.
* Members of the file's group.

For example:

```text
Owner: aryan
Group: developers
Other: everyone else
```

---

# Linux Permission Types

Linux primarily uses three basic permissions:

| Permission | Symbol | Meaning          |
| ---------- | ------ | ---------------- |
| Read       | `r`    | Allows reading   |
| Write      | `w`    | Allows modifying |
| Execute    | `x`    | Allows executing |

A dash (`-`) means that the corresponding permission is not granted.

For example:

```text
rwx
```

means:

```text
Read + Write + Execute
```

While:

```text
r--
```

means:

```text
Read only
```

---

# Linux Permission Sets

Each file or directory has three permission sets:

1. User/Owner permissions.
2. Group permissions.
3. Other permissions.

For example:

```text
-rwxr-xr--
```

The permissions can be divided as:

```text
- rwx r-x r--
  --- --- ---
   |   |   |
   |   |   └── Other
   |   └────── Group
   └────────── Owner
```

Therefore:

```text
Owner  = rwx
Group  = r-x
Other  = r--
```

---

# Understanding the First Character

The first character displayed by `ls -l` indicates the file type.

Example:

```text
-rw-r--r-- file.txt
```

The first character is:

```text
-
```

A hyphen indicates a regular file.

For a directory, the first character is:

```text
d
```

Example:

```text
drwxr-xr-x Documents
```

The `d` indicates that `Documents` is a directory.

---

# `ls -l` Command

The `ls -l` command displays detailed information about files and directories.

### Command

```bash
ls -l
```

### Example

```text
-rw-r--r-- 1 aryan developers 120 Aug 29 file.txt
```

The output provides information such as:

* File type.
* Permissions.
* Owner.
* Group.
* File size.
* Modification information.
* File name.

---

# Read Permission

The read permission is represented by:

```text
r
```

For a regular file, read permission allows a user to view its contents.

Example:

```text
-r--r--r--
```

This gives read permission to:

* Owner.
* Group.
* Others.

The contents of a file can be viewed using commands such as:

```bash
cat file.txt
```

---

# Write Permission

The write permission is represented by:

```text
w
```

For a file, write permission allows its contents to be modified.

Example:

```text
-rw-------
```

The owner has:

```text
Read + Write
```

while the group and others have no permissions.

For directories, write permission allows changes to the directory's contents, such as creating or removing files, subject to the applicable permissions.

---

# Execute Permission

The execute permission is represented by:

```text
x
```

For a regular executable file, execute permission allows the file to be run.

For a directory, execute permission allows a user to access/traverse the directory.

Example:

```text
drwx------
```

The owner has full permissions on the directory.

---

# Directory Permissions

Permissions behave somewhat differently for directories.

For a directory:

* `r` allows listing its contents.
* `w` allows modifying its contents, such as creating or removing entries, when combined with appropriate permissions.
* `x` allows entering/traversing the directory.

For example:

```bash
cd Documents
```

requires execute/traverse permission on the directory.

The contents can be listed with:

```bash
ls Documents
```

when the user has the required read permission.

---

# File Ownership Commands

Linux provides commands for changing ownership.

The main command is:

```bash
chown
```

`chown` stands for **change owner**.

---

# `chown` Command

The `chown` command changes the owner and/or group of a file or directory.

### General Syntax

```bash
chown user:group filename
```

### Example

```bash
chown aryan:developers test.txt
```

This changes:

```text
Owner → aryan
Group → developers
```

---

# Changing Only the Owner

To change only the owner:

```bash
chown aryan test.txt
```

The group remains unchanged.

---

# Changing Only the Group

A group can be changed using:

```bash
chown :developers test.txt
```

This changes the group ownership to:

```text
developers
```

The owner remains unchanged.

---

# `chgrp` Command

The `chgrp` command is used to change the group ownership of a file or directory.

### Syntax

```bash
chgrp group filename
```

### Example

```bash
chgrp developers test.txt
```

This changes the group ownership of `test.txt` to:

```text
developers
```

Normal users frequently use `chgrp` when they need to change the group ownership of files they are permitted to manage.

---

# Linux Groups

A Linux user can belong to multiple groups.

Group information can be found in:

```text
/etc/group
```

A user normally has one **primary group**.

The primary group information is associated with the user's account information in:

```text
/etc/passwd
```

When a user creates a file, the file normally inherits the user's primary group as its group ownership.

---

# Changing File Permissions

Linux provides the:

```bash
chmod
```

command to change file and directory permissions.

`chmod` stands for **change mode**.

### General Syntax

```bash
chmod permissions filename
```

Example:

```bash
chmod +x script.sh
```

This adds execute permission to the file.

---

# Symbolic Permission Mode

Permissions can be modified symbolically using:

* `u` — User/Owner
* `g` — Group
* `o` — Other
* `a` — All

Permission operators include:

* `+` — Add permission.
* `-` — Remove permission.
* `=` — Set permission.

---

# Examples of `chmod`

## Add Execute Permission to Owner

```bash
chmod u+x script.sh
```

This gives the owner execute permission.

---

## Add Read and Write Permission to Group

```bash
chmod g+rw file.txt
```

This adds:

```text
Read + Write
```

permissions for the group.

---

## Remove Write Permission from Others

```bash
chmod o-w file.txt
```

This removes write permission from other users.

---

## Set Permissions for Everyone

```bash
chmod a+r file.txt
```

This gives read permission to:

* Owner.
* Group.
* Others.

---

# Numeric Permission Mode

Linux permissions can also be represented using numeric values.

The common values are:

| Permission    | Value |
| ------------- | ----: |
| Read (`r`)    |     4 |
| Write (`w`)   |     2 |
| Execute (`x`) |     1 |

The values are added together to represent a permission set.

### Examples

```text
r-- = 4
-w- = 2
--x = 1
```

Therefore:

```text
rw- = 4 + 2 = 6
r-x = 4 + 1 = 5
rwx = 4 + 2 + 1 = 7
```

---

# Example of Numeric `chmod`

Consider:

```bash
chmod 755 script.sh
```

The three digits represent:

```text
Owner  = 7
Group  = 5
Other  = 5
```

Where:

```text
7 = rwx
5 = r-x
5 = r-x
```

Therefore:

```text
Owner  → Read + Write + Execute
Group  → Read + Execute
Other  → Read + Execute
```

Another common example is:

```bash
chmod 644 file.txt
```

This means:

```text
Owner  → rw-
Group  → r--
Other  → r--
```

---

# Special Permissions

In addition to standard read, write, and execute permissions, Linux supports special permissions.

The course introduces:

1. **Setuid**
2. **Setgid**
3. **Sticky Bit**

These special permissions provide additional behavior for files and directories.

---

# Setuid

The **Setuid** permission is a special permission associated primarily with executable files.

When applied to an executable, it can cause the program to run with the privileges of the file's owner.

It is represented by:

```text
s
```

in the owner's execute position.

---

# Setgid

The **Setgid** permission is represented by:

```text
s
```

in the group's execute position.

For executable files, it can cause the program to run with the privileges of the file's group.

For directories, Setgid can cause newly created files and directories to inherit the directory's group ownership.

---

# Sticky Bit

The **sticky bit** is commonly used on shared directories.

It is represented by:

```text
t
```

in the others' execute position.

A common example is:

```text
/tmp
```

The sticky bit helps prevent users from deleting or renaming files belonging to other users in a shared directory, subject to the relevant ownership and privilege rules.

---

# Permission Management Example

Consider a file:

```text
-rw-r--r-- 1 aryan developers file.txt
```

The permissions are:

```text
Owner  → rw-
Group  → r--
Other  → r--
```

To give the owner execute permission:

```bash
chmod u+x file.txt
```

To give the group write permission:

```bash
chmod g+w file.txt
```

To remove read permission from others:

```bash
chmod o-r file.txt
```

To view the updated permissions:

```bash
ls -l file.txt
```

---

# Common Permission Management Commands

| Command | Purpose                                                 |
| ------- | ------------------------------------------------------- |
| `ls -l` | Displays file permissions, ownership, and other details |
| `chmod` | Changes file or directory permissions                   |
| `chown` | Changes file owner and/or group                         |
| `chgrp` | Changes group ownership                                 |
| `cat`   | Displays file contents                                  |
| `cd`    | Changes directory                                       |
| `ls`    | Lists directory contents                                |

---

# Permission Management Workflow

A basic permission-management workflow can be:

## 1. Check File Permissions

```bash
ls -l file.txt
```

## 2. Change the Owner

```bash
sudo chown aryan file.txt
```

## 3. Change the Group

```bash
sudo chgrp developers file.txt
```

## 4. Add Execute Permission

```bash
chmod u+x file.txt
```

## 5. Verify the Permissions

```bash
ls -l file.txt
```

---

# Important Concepts to Remember

### Permission Groups

```text
u → User/Owner
g → Group
o → Other
a → All
```

### Basic Permissions

```text
r → Read
w → Write
x → Execute
```

### Permission Operators

```text
+ → Add
- → Remove
= → Set
```

### Numeric Values

```text
r = 4
w = 2
x = 1
```

### Ownership Commands

```text
chown  → Change owner/group
chgrp  → Change group
```

### Permission Command

```text
chmod → Change permissions
```

---

# Course Completion

After completing this course, you should now be able to:

* Understand Linux file permissions.
* Understand Linux file ownership.
* Understand the user, group, and other permission categories.
* Understand read, write, and execute permissions.
* Identify file and directory types using `ls -l`.
* Change ownership using `chown`.
* Change group ownership using `chgrp`.
* Change permissions using `chmod`.
* Understand symbolic and numeric permission modes.
* Understand Setuid, Setgid, and Sticky Bit.

---

# Knowledge Assessment

The course concludes with a knowledge assessment to check your understanding of:

* Linux file permissions.
* Linux file ownership.
* Permission groups.
* `chmod`.
* `chown`.
* `chgrp`.
* Special permissions.

You must achieve **80%** to pass the assessment.

If you are not ready for the assessment, you can review the course material before attempting it again.

---

## Course Files

```text
Track06-Linux-Permissions-Management/
├── lecture.md
├── assessment.md
└── certificate.pdf
