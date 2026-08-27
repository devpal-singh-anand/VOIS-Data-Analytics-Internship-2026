# Getting Started with Linux Administration

## Learning Objectives

The learning objective is to gain knowledge on:

* understanding the basics of Linux.
* understanding the Linux building and booting process.
* understanding the Linux directory structure.
* learning commonly used Linux commands.
* using commands to check processes.
* using commands to monitor Linux system performance.
* understanding basic Linux system administration.
* understanding SSH and remote Linux connections.

---

## Prerequisites

* Basic understanding of Linux.
* Basic understanding of Linux file attributes.
* Basic file and directory management knowledge.
* Basic understanding of Linux system utilities.

---

# About the Course

Linux administration is about managing and maintaining Linux-powered systems.

Linux system administration includes:

* Setting up disaster recovery.
* Managing new system builds.
* Creating backups and restoring data.
* Managing Linux hardware.
* Managing storage.
* Handling file systems.
* Managing Linux security.
* Monitoring system performance.
* Ensuring Linux-powered systems remain stable and secure.

A major part of Linux administration is ensuring that Linux-powered systems are **stable, secure, and available**.

---

# Linux Boot Process

When a Linux computer is turned on, it goes through several phases before finally presenting the login screen.

A normal Linux boot process can be understood through four major steps:

1. BIOS integrity check / POST
2. Loading of the boot loader
3. Kernel initialization
4. Starting `init` / systemd

---

# Step 1 — BIOS

The first process begins once the machine is powered on.

When you press the power button, the **BIOS** looks for instructions that tell the computer how to start.

BIOS determines the available boot devices in the system.

These devices may include:

* Hard disk
* CD/DVD-ROM
* Floppy drive
* USB flash drive
* Other bootable devices

The operating system normally attempts to boot from the hard disk.

The BIOS performs the initial hardware checks before transferring control to the boot loader.

---

# POST — Power-On Self-Test

The BIOS performs a **Power-On Self-Test (POST)**.

POST checks whether the basic hardware required for starting the computer is functioning correctly.

The process occurs immediately after the machine is powered on.

After the BIOS/POST stage, the system looks for a bootable device and loads the boot loader.

---

# Master Boot Record

The **Master Boot Record (MBR)** is located in the first sector of a hard disk.

The traditional MBR has a size of:

```text
512 bytes
```

The traditional layout consists of:

```text
446 bytes  → Primary boot loader
64 bytes   → Partition table
2 bytes    → Boot signature / validation
```

The MBR contains the primary boot loader, which is responsible for beginning the operating-system boot process.

---

# Step 2 — Boot Loader

The boot loader is responsible for loading the Linux kernel.

Linux commonly uses **GRUB**, which stands for:

**GRand Unified Bootloader**

GRUB provides a menu that allows the user to select the Linux kernel version that should be booted.

---

# GRUB

The GRUB menu allows you to:

* Select the Linux kernel version.
* Boot a selected kernel.
* Select different available operating-system entries.
* Boot the default kernel automatically after the timeout period.

For example, a GRUB menu may provide several kernel versions:

```text
Linux Kernel 6.x
Linux Kernel 5.x
Recovery Mode
```

The user can select the required kernel, or the default entry will be selected automatically after the configured timeout.

---

# GRUB Stages

The traditional GRUB boot process is described in multiple stages.

These include:

1. GRUB Stage 1
2. GRUB Stage 1.5
3. GRUB Stage 2

---

## GRUB Stage 1

GRUB Stage 1 is the **primary boot loader**.

It is stored in the MBR and occupies the limited space available there.

Because the MBR has limited space, Stage 1 contains only the instructions necessary to begin loading the more complex parts of GRUB.

Stage 1 then loads the next stage.

---

## GRUB Stage 1.5

Stage 1 can load Stage 2 directly, but it is normally configured to load **Stage 1.5** first.

Stage 1.5 acts as an intermediate stage.

It helps GRUB understand the required file-system structures and locate the files needed for loading Stage 2.

---

## GRUB Stage 2

GRUB Stage 2 is responsible for providing the main boot-loader functionality.

It loads the kernel and other required modules.

Traditional GRUB configuration information may be found under locations such as:

```text
/boot/grub/grub.conf
```

or, depending on the Linux distribution and GRUB version:

```text
/boot/grub/grub.cfg
```

GRUB may also display a graphical splash screen and provide a list of available kernels.

---

# Linux Kernel

The **Linux kernel** is the core of the operating system.

It is responsible for handling important system operations such as:

* Hardware management.
* Memory management.
* Process management.
* Device management.
* File-system interaction.
* Communication between hardware and software.

The kernel is loaded after the boot loader.

---

# Kernel Initialization

As soon as the Linux kernel is loaded, it begins initializing the system.

The kernel:

1. Configures hardware.
2. Allocates memory.
3. Initializes required system components.
4. Loads necessary drivers.
5. Detects storage devices and file systems.
6. Mounts the required file systems.
7. Starts the first user-space process.

---

# Kernel Compression and Extraction

The Linux kernel may be stored in a compressed form.

During the boot process, the kernel extracts itself from its compressed form before performing the remaining initialization tasks.

After extraction, the kernel continues system initialization.

---

# Initial RAM File System — initramfs

During boot, Linux may use an **initial RAM file system**, commonly called:

```text
initramfs
```

It contains temporary files and drivers required during the early stages of booting.

The initramfs can provide the drivers and tools needed to locate and mount the actual root file system.

After the real root file system becomes available, the temporary environment is no longer required.

---

# Root File System

After initializing the required hardware and drivers, the kernel mounts the root file system.

The root file system contains the files and directories required by the operating system.

The root directory is represented by:

```text
/
```

During early boot, the root file system may initially be mounted as **read-only**.

---

# Step 3 — init Process

Once the Linux kernel has been loaded and initialized, it starts the first user-space process.

Traditionally, this process is called:

```text
init
```

The `init` process is assigned:

```text
PID 1
```

This means it is the first process in user space.

The `init` process starts various services and processes required for the system.

---

# Step 4 — systemd

Modern Linux distributions commonly use **systemd** as the replacement for the traditional System V `init` system.

Systemd is responsible for managing many aspects of system startup and operation.

It manages tasks such as:

* Starting services.
* Stopping services.
* Restarting services.
* Mounting file systems.
* Managing system targets.
* Managing system processes.

Systemd can therefore be considered one of the central components responsible for managing the Linux system after the kernel has initialized.

---

# Systemd Targets

Systemd uses **targets** to determine the desired state of the system.

Examples include:

```text
poweroff.target
rescue.target
multi-user.target
graphical.target
reboot.target
```

---

## `poweroff.target`

Used to power off and shut down the system.

---

## `rescue.target`

Provides a rescue environment with a minimal system configuration and rescue shell.

---

## `multi-user.target`

Configures the system for a non-graphical multi-user environment.

This is commonly associated with a server-style environment.

It corresponds approximately to:

```text
Runlevel 3
```

in traditional System V init systems.

---

## `graphical.target`

Configures the system to use a graphical multi-user interface with network services.

It corresponds approximately to:

```text
Runlevel 5
```

in traditional System V init systems.

---

## `reboot.target`

Reboots the system.

---

# Default Systemd Target

The default systemd target depends on the system configuration.

For a desktop system, the default target is commonly:

```text
graphical.target
```

For a server, the default target is commonly:

```text
multi-user.target
```

---

# Checking the Current Target

To check the current target on a Linux system, use:

```bash
systemctl get-default
```

Example:

```bash
$ systemctl get-default
graphical.target
```

This indicates that the system is configured to boot into the graphical target by default.

---

# Switching Between Systemd Targets

Systemd targets can be changed using:

```bash
systemctl isolate <target>
```

For example:

```bash
sudo systemctl isolate multi-user.target
```

This switches the running system to the multi-user target.

---

# Linux Directory Structure

Unlike Windows, where files are commonly organized across drive letters such as:

```text
C:
D:
E:
```

Linux uses a **tree-like directory structure**.

The structure starts from a single root directory:

```text
/
```

All other directories exist under the root directory.

---

# Linux Directory Structure — Common Top-Level Directories

These are common top-level directories associated with the root directory:

```text
/bin
/etc
/home
/opt
/tmp
/usr
/var
```

---

## `/bin`

Contains essential binary or executable programs.

Example:

```text
/bin/ls
/bin/cp
/bin/mv
```

These programs provide commonly used system commands.

---

## `/etc`

Contains system-wide configuration files.

Examples include configuration files for:

* System services.
* Networking.
* Users.
* Other system components.

---

## `/home`

Contains users' home directories.

For example:

```text
/home/alice
/home/bob
```

A user's home directory is generally the default working directory after logging in.

---

## `/opt`

Contains optional or third-party software packages.

For example:

```text
/opt/application
```

may contain software installed separately from the main system packages.

---

## `/tmp`

Contains temporary files.

The `/tmp` directory is generally used for temporary data and is commonly cleared during reboot or according to system policies.

---

## `/usr`

Contains user-related programs, libraries, documentation, and other resources.

Examples include:

```text
/usr/bin
/usr/lib
/usr/share
```

---

## `/var`

Contains variable data that changes during system operation.

A common example is:

```text
/var/log
```

which contains system and application log files.

---

# Linux Daily-Use Commands

Linux provides many commands for managing files, directories, and the system.

Some commonly used commands are:

* `cd`
* `ls`
* `man`
* `cat`
* `mkdir`
* `chmod`
* `rmdir`
* `rm`
* `mv`
* `echo`
* `free`

---

# `cd` Command

The `cd` command is used to **change the current directory**.

Example:

```bash
cd /home
```

To move into a directory named `Documents`:

```bash
cd Documents
```

To move to the parent directory:

```bash
cd ..
```

---

# `ls` Command

The `ls` command means **list**.

It displays files and directories contained in a particular location.

Example:

```bash
ls
```

To display detailed information:

```bash
ls -l
```

To display hidden files as well:

```bash
ls -a
```

A commonly used combination is:

```bash
ls -la
```

---

# `man` Command

The `man` command stands for **manual**.

It provides reference documentation for Linux commands and utilities.

Example:

```bash
man ls
```

This displays the manual page for the `ls` command.

Another example:

```bash
man chmod
```

---

# `cat` Command

The `cat` command is short for **concatenate**.

It is commonly used to display the contents of a file on standard output.

Example:

```bash
cat file.txt
```

It can also be used to concatenate files.

Example:

```bash
cat file1.txt file2.txt
```

---

# `mkdir` Command

The `mkdir` command is used to **make a directory**.

Example:

```bash
mkdir project
```

This creates a directory named:

```text
project
```

---

# `chmod` Command

The `chmod` command is used to change the permissions of files and directories.

Linux permissions determine who can:

* Read a file.
* Write to a file.
* Execute a file.

Example:

```bash
chmod +x script.sh
```

This adds execute permission to the file.

---

# `rmdir` Command

The `rmdir` command is used to remove an empty directory.

Example:

```bash
rmdir old_directory
```

The directory must generally be empty for `rmdir` to remove it.

---

# `rm` Command

The `rm` command is used to remove files.

Example:

```bash
rm file.txt
```

It can also be used to remove directories with appropriate options.

For example:

```bash
rm -r directory
```

---

# `mv` Command

The `mv` command is used to move or rename files and directories.

Example:

```bash
mv file.txt /home/user/Documents/
```

This moves the file to another directory.

It can also rename a file:

```bash
mv old.txt new.txt
```

---

# `echo` Command

The `echo` command is used to print specified text to the terminal.

Example:

```bash
echo "Hello Linux"
```

Output:

```text
Hello Linux
```

It can also be used with shell variables and file redirection.

Example:

```bash
echo "Hello" > file.txt
```

---

# `free` Command

The `free` command provides information about memory usage.

It displays information about:

* RAM.
* Swap memory.
* Used memory.
* Free memory.
* Available memory.

Example:

```bash
free
```

A more readable form is:

```bash
free -h
```

---

# Linux Process Monitoring

Linux provides several commands for monitoring processes and system performance.

Important commands include:

* `top`
* `vmstat`
* `lsof`
* `iostat`
* `htop`
* `iotop`

---

# `top` Command

The `top` command is a performance-monitoring program commonly used by system administrators.

It displays running processes in real time.

The display is regularly updated.

It can show information such as:

* Process ID (PID).
* User.
* CPU usage.
* Memory usage.
* Swap usage.
* Process state.
* Command.
* System load.

Example:

```bash
top
```

The command provides a continuously updating view of active processes.

---

# `vmstat` Command

The `vmstat` command displays statistics about system performance.

It can provide information about:

* Virtual memory.
* Processes.
* CPU activity.
* Memory.
* Paging.
* I/O blocks.
* Interrupts.
* Disks.

Example:

```bash
vmstat
```

To update the information periodically:

```bash
vmstat 2
```

This requests an update every two seconds.

On some Linux systems, `vmstat` is provided by the `sysstat` package or related system utilities.

---

# `lsof` Command

The `lsof` command stands for:

**List Open Files**

It displays information about files that are currently opened by processes.

Open files can include:

* Disk files.
* Network sockets.
* Pipes.
* Devices.
* Other file descriptors.

Example:

```bash
lsof
```

One important use of `lsof` is troubleshooting situations where a file system or disk cannot be unmounted because some process is still using a file.

For example:

```bash
lsof /mount/point
```

can help identify processes using the mount point.

---

# `iostat` Command

The `iostat` command is used to monitor:

* CPU statistics.
* Input/output statistics.
* Device statistics.
* Disk I/O activity.

Example:

```bash
iostat
```

It is particularly useful for monitoring disk I/O performance.

On systems where it is not installed by default, it is commonly provided by the `sysstat` package.

---

# `htop` Command

`htop` is an interactive process-monitoring tool similar to `top`.

It provides a more user-friendly interface for viewing and managing processes.

Features include:

* Interactive process management.
* Process selection.
* Shortcut keys.
* Vertical and horizontal views.
* CPU and memory monitoring.

Example:

```bash
htop
```

---

# `iotop` Command

`iotop` is used to monitor disk input/output activity of processes.

It is particularly useful for identifying which processes are performing heavy disk reads or writes.

Example:

```bash
sudo iotop
```

It can help identify processes responsible for high disk I/O usage.

---

# SSH

**SSH** stands for:

**Secure Shell**

SSH is a protocol used to securely connect to a remote Linux server or system.

It provides encrypted communication between the client and the remote host.

SSH can transfer:

* User input.
* Commands.
* Command output.
* Other data.

SSH commonly operates over:

```text
TCP port 22
```

---

# SSH Client and Server

SSH communication generally involves two sides:

```text
SSH Client  →  SSH Server
```

The client is the machine from which the connection is made.

The server is the remote Linux system accepting SSH connections.

For example:

```text
Local Computer
      |
      | SSH
      ↓
Remote Linux Server
```

---

# Installing and Configuring SSH on Ubuntu

The following steps describe a basic SSH server setup on Ubuntu.

---

## Step 1 — Open the Terminal

Open a terminal on the Ubuntu system.

---

## Step 2 — Update the System

Before installing new software or packages, update the package information.

Use:

```bash
sudo apt update
```

This updates the local package lists.

---

## Step 3 — Install OpenSSH Server

Install the OpenSSH server package:

```bash
sudo apt install openssh-server
```

OpenSSH provides the software required for the machine to accept SSH connections.

---

# Step 4 — Verify the SSH Service

After installation, verify that the SSH service is running.

Use:

```bash
sudo systemctl status ssh
```

A running service should show an active status such as:

```text
active (running)
```

---

# Step 5 — Enable and Start SSH

If SSH is not running, it can be enabled and started using:

```bash
sudo systemctl enable --now ssh
```

The `enable` portion configures the service to start automatically during boot, while `--now` starts it immediately.

---

# Step 6 — Allow SSH Through the Firewall

Ubuntu commonly uses **UFW**, which stands for:

**Uncomplicated Firewall**

If UFW is active, it may block incoming SSH connections unless SSH is allowed.

Use:

```bash
sudo ufw allow ssh
```

or:

```bash
sudo ufw allow 22/tcp
```

This allows TCP connections to SSH's standard port.

---

# Step 7 — Check SSH Configuration

The SSH server configuration is commonly stored in:

```text
/etc/ssh/sshd_config
```

The SSH service can be inspected using:

```bash
sudo systemctl status ssh
```

---

# Testing SSH

Once the SSH server is running, a client can connect to it using:

```bash
ssh username@ip_address
```

Example:

```bash
ssh alice@192.168.1.100
```

Here:

```text
alice       → username on the remote system
192.168.1.100 → IP address of the remote system
```

The client will normally prompt for authentication credentials unless another authentication method, such as SSH keys, is configured.

---

# Setting Up an SSH Client on Linux

A Linux machine can act as an SSH client and connect to another remote system.

---

## Step 1 — Install the SSH Client

On Ubuntu, the SSH client can be installed using:

```bash
sudo apt update
sudo apt install openssh-client
```

Many Linux distributions already include an SSH client by default.

---

# Step 2 — Connect to a Remote System

Use:

```bash
ssh username@remote_ip_address
```

Example:

```bash
ssh user@192.168.1.100
```

The connection is established from the local computer to the remote system.

---

# Linux Administration — Important Commands

A basic command reference from this course includes:

| Command  | Purpose                             |
| -------- | ----------------------------------- |
| `cd`     | Change directory                    |
| `ls`     | List files/directories              |
| `man`    | Display command manual              |
| `cat`    | Display/concatenate file contents   |
| `mkdir`  | Create directory                    |
| `chmod`  | Change file permissions             |
| `rmdir`  | Remove empty directory              |
| `rm`     | Remove files/directories            |
| `mv`     | Move or rename files/directories    |
| `echo`   | Print text                          |
| `free`   | Display memory usage                |
| `top`    | Monitor running processes           |
| `vmstat` | Display system statistics           |
| `lsof`   | List open files                     |
| `iostat` | Monitor I/O statistics              |
| `htop`   | Interactive process monitor         |
| `iotop`  | Monitor disk I/O by processes       |
| `ssh`    | Securely connect to a remote system |

---

# Linux Boot Process — Summary

The basic Linux boot sequence can be represented as:

```text
Power On
   ↓
BIOS / POST
   ↓
Boot Device
   ↓
MBR / Boot Loader
   ↓
GRUB
   ↓
Linux Kernel
   ↓
init / systemd
   ↓
System Targets
   ↓
Login Screen / System Ready
```

---

# Key Concepts to Remember

| Concept     | Meaning                                                                   |
| ----------- | ------------------------------------------------------------------------- |
| **BIOS**    | Firmware that initializes hardware and begins the boot process            |
| **POST**    | Power-On Self-Test performed during startup                               |
| **MBR**     | Traditional first sector containing boot-loader and partition information |
| **GRUB**    | Linux boot loader                                                         |
| **Kernel**  | Core of the Linux operating system                                        |
| **init**    | Traditional first user-space process, PID 1                               |
| **systemd** | Modern system and service manager commonly used as PID 1                  |
| **Target**  | Systemd-defined desired system state                                      |
| `/`         | Root directory                                                            |
| `/bin`      | Essential executable programs                                             |
| `/etc`      | System configuration files                                                |
| `/home`     | Users' home directories                                                   |
| `/opt`      | Optional/third-party software                                             |
| `/tmp`      | Temporary files                                                           |
| `/usr`      | User-related programs and resources                                       |
| `/var`      | Variable data such as logs                                                |
| `top`       | Real-time process monitoring                                              |
| `vmstat`    | Virtual memory and system statistics                                      |
| `lsof`      | List open files                                                           |
| `iostat`    | CPU and I/O statistics                                                    |
| `htop`      | Interactive process monitoring                                            |
| `iotop`     | Disk I/O monitoring                                                       |
| **SSH**     | Secure Shell remote-access protocol                                       |
| **UFW**     | Uncomplicated Firewall                                                    |

---

# Course Summary

After completing this course, you should understand:

* Basic Linux system administration.
* The Linux boot process.
* BIOS and POST.
* The Master Boot Record.
* GRUB and its stages.
* Linux kernel initialization.
* The role of `init`.
* The role of systemd.
* Systemd targets.
* How to check the default system target.
* How to switch between system targets.
* Linux's tree-like directory structure.
* Common Linux directories.
* Common daily-use Linux commands.
* Linux process monitoring.
* Memory and system monitoring.
* Disk I/O monitoring.
* Open-file monitoring.
* SSH and secure remote connections.
* Installing and configuring an SSH server on Ubuntu.
* Installing and using an SSH client.

---

## Course Completion

Well done! You have completed the course.

You should now be able to:

* Understand the Linux booting process.
* Understand the Linux directory structure.
* Use daily Linux commands.
* Check and monitor running processes.
* Monitor system and disk performance.
* Understand basic Linux administration.
* Connect securely to remote systems using SSH.

---

## Course Files

```text
Track04-Linux-Administration/
├── lecture.md
├── assessment.md
└── certificate.pdf
```
