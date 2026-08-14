# Getting Started with Linux File System

## Learning Objectives

The learning objective is to gain knowledge on:

* becoming familiar with the **Linux operating system**.
* understanding the major **components of Linux**.
* understanding the different methods used to install Linux.
* understanding the **Linux startup and boot process**.
* understanding Linux user environments.
* understanding the basic structure of the **Linux file system**.

---

## Prerequisites

* Interest in learning the Linux operating system.
* Basic familiarity with computers and operating systems.
* Basic understanding of system hardware and software.

---

# About the Course

This course introduces the fundamentals of the **Linux operating system**.

The course covers:

* Linux operating system fundamentals.
* Components of Linux.
* Characteristics of Linux.
* Advantages and disadvantages of Linux.
* Installing Linux using a USB stick.
* Installing Linux using CD-ROM.
* Installing Linux using a virtual machine.
* Linux startup and boot process.
* Linux user environments.
* Linux file system.

---

# Linux Operating System

Linux is an operating system/kernel that is made available under an **open-source license**.

Its feature set is very similar to **Unix**.

The Linux operating system uses a **kernel** as its core component. The kernel is a piece of software responsible for handling basic tasks, including communication between hardware and software.

---

# Components of Linux

The Linux operating system consists of several major components.

---

## Hardware Layer

The hardware layer consists of peripherals and hardware components such as:

* RAM
* Hard disk drives
* CPUs
* Other hardware devices

---

## Kernel

The **kernel** is the core component of the Linux operating system.

It is responsible for a number of operations and directly interacts with the hardware.

The kernel provides low-level services such as:

* Access to hardware.
* Communication between hardware and software.
* Management of system resources.
* Access to hardware data.

Two types of kernels mentioned in the course are:

* **Monolithic kernel**
* **Microkernel**

---

## Shell

The **shell** serves as an interface between the user and the kernel.

It hides the complex nature of the kernel's functions from the user.

The shell:

* Accepts human-readable commands.
* Translates commands.
* Executes requested tasks.
* Provides access to operating-system features.

---

## System Utilities

System utilities are programs that can be used for **specialized tasks**.

They provide additional functionality for managing and working with the Linux operating system.

---

# Characteristics of Linux

Linux can be utilized using **commands**.

Linux commands can perform one or multiple tasks.

Examples include:

* Copying files.
* Pasting files.
* Finding files.
* Managing system resources.

Using commands allows tasks to be performed efficiently and effectively.

---

# Advantages of Linux

## Free

Linux is free and can be downloaded from the internet.

There are no hidden costs for:

* Registration.
* Updates.
* Basic usage.

---

## Flexible

Linux is flexible and can be installed on different types of hardware.

Users who are unsure about which operating system to install can consider Linux as an option.

---

# Disadvantages of Linux

Linux is licensed under the **GNU General Public License (GPL)**.

The GPL allows users to:

* Modify Linux.
* Distribute modified versions.

Because many versions and distributions can exist, it can sometimes be confusing to determine which version is best suited to a particular need.

Linux can also be less user-friendly for beginners and may initially be confusing for new users.

---

# Installing Linux Using a USB Stick

Installing Ubuntu or another Linux distribution using a USB stick is one of the easiest installation methods.

---

## Step 1 — Download Required Files

Download the required **ISO file** onto the computer.

---

## Step 2 — Download Universal USB Installer

Download free software such as **Universal USB Installer** to create a bootable USB stick.

---

## Step 3 — Select the Distribution

In Universal USB Installer:

1. Select the Ubuntu distribution from the dropdown.
2. Select the Ubuntu ISO file downloaded in Step 1.
3. Select the drive letter of the USB.
4. Press the **Create** button.

---

## Step 4 — Install Ubuntu

Use the created USB stick to install Ubuntu.

---

## Step 5 — Check the Installation

After everything has been installed and configured, a confirmation window appears indicating that Ubuntu is ready on the USB stick.

---

# Installing Linux Using CD-ROM

Users can also install Linux using a CD-ROM.

---

## Steps

### Step 1

Download the required ISO file onto the computer.

### Step 2

Burn the ISO file to a CD.

### Step 3

Boot the computer from the optical drive.

### Step 4

Follow the installation instructions.

---

# Installing Linux Using a Virtual Machine

Installing Linux using a **virtual machine** is a popular method.

A virtual installation allows Linux to run on an existing operating system already installed on the computer.

The course uses **VirtualBox** as the example.

---

# Installing VirtualBox

## Step 1

Download VirtualBox.

## Step 2

Open the setup file after downloading it.

## Step 3

Select the directory where VirtualBox should be installed and click **Next**.

## Step 4

Select the desktop icon option and click **Next**.

## Step 5

Click **Install** to install VirtualBox.

## Step 6

Once installation is complete, click **Finish** to start VirtualBox.

The VirtualBox dashboard will then appear.

---

# Downloading Ubuntu

Download the Ubuntu ISO file that will be used to install Ubuntu inside VirtualBox.

---

# Creating an Ubuntu Virtual Machine

## Step 1 — Create a New Machine

Click the **New** button in VirtualBox.

---

## Step 2 — Select Operating System

Enter the name of the operating system being installed.

Select:

* **Type:** Linux
* **Version:** Ubuntu 32-bit

Click **Next**.

---

## Step 3 — Allocate RAM

Allocate memory to the virtual machine.

The course recommends:

```text
1024 MB (1 GB)
```

of RAM to run Ubuntu better.

Click **Next**.

---

## Step 4 — Create Virtual Hard Disk

A virtual hard disk is required to run the operating system.

Click:

```text
Create a virtual hard disk now
```

The virtual hard disk stores:

* Operating system files.
* Installation files.
* Applications.
* User-created data.

---

## Step 5 — Select Hard Disk Type

Select the **Hard Disk** option and click **Next**.

---

## Step 6 — Select Allocation Type

Select:

```text
Dynamically allocated
```

and click **Next**.

A dynamically allocated disk increases its size as required.

---

## Step 7 — Allocate Disk Space

Allocate storage to the virtual hard drive.

The course recommends:

```text
8 GB
```

Click **Create**.

---

## Step 8 — View the Virtual Machine

The newly created machine will appear in the left panel of VirtualBox.

---

# Installing Ubuntu in VirtualBox

## Step 1 — Start the Machine

Select the virtual machine and click **Start**.

---

## Step 2 — Select Ubuntu ISO

Select the folder option and choose the Ubuntu ISO file.

---

## Step 3 — Start Installation

Ubuntu provides an option to run without installing.

For this tutorial, select the option to install Ubuntu.

---

## Step 4 — Select Disk Installation

Select the option to erase the virtual disk and install Ubuntu.

This installs Ubuntu into the **virtual hard disk created earlier**.

It does not affect the existing Windows installation when the virtual machine is configured correctly.

---

## Step 5 — Select Location

Select the location for configuring the time zone.

Click **Continue**.

---

## Step 6 — Select Keyboard Layout

The default keyboard layout is:

```text
English (US)
```

Select another layout if required and click **Continue**.

---

## Step 7 — Create User Account

Enter the required information for the Ubuntu administrator account:

* Username.
* Password.
* Other requested account details.

This information is required for:

* Logging into Ubuntu.
* Installing software packages.

An automatic-login option may also be selected.

---

## Step 8 — Complete Installation

The installation process begins.

The process may take approximately **30 minutes**.

After installation is completed, the **Ubuntu desktop** appears.

---

# Managing the Linux Startup Process

When the power button is pressed, the firmware stored on a chip on the motherboard initializes the system.

---

## POST

The firmware performs **POST (Power-On Self-Test)**.

POST checks the state of the system's hardware resources.

After POST is completed, the firmware searches for and loads the **first-stage boot loader** from the first available disk.

---

# Master Boot Record (MBR)

The MBR contains important information related to the boot process.

---

## First 446 Bytes

The first 446 bytes contain:

* Executable boot-loader code.
* Error-message text.

---

## Next 64 Bytes

The next 64 bytes contain the **partition table**.

The partition table contains records for partitions such as:

* Primary partitions.
* Extended partitions.

Each record contains information such as:

* Active/inactive status.
* Size.
* Starting sectors.

---

## Last 2 Bytes

The last 2 bytes contain the **magic number**.

The magic number serves as a validation check of the MBR.

---

# GRUB Boot Loader

**GRUB** is the Linux boot loader.

The course mentions the GRUB legacy configuration and the GRUB 2 configuration.

GRUB loads:

* The default kernel.
* The `initrd`.

---

# initrd

The **initrd (initial RAM disk)** helps perform the hardware and device operations required to start the Linux system.

It assists with:

* Hardware detection.
* Kernel module loading.
* Device discovery.
* Mounting the real root file system.

---

# Managing Linux Environments

Linux user environments help users find and execute commands without needing to know every detail about how the system is configured.

A user environment allows users to:

* Run commands without knowing their exact locations.
* Reuse previously executed commands.
* Manage environment settings.

---

# Viewing Environment Settings

The `env` command can be used to view environment settings.

Example:

```bash
env
```

---

# Changing Environment Settings

Environment settings can be changed using commands such as:

```bash
export HISIZE=1234
```

To retain a setting, it can be added to the:

```text
~/.bashrc
```

file.

---

# Linux File System

The Linux kernel maintains a **single hierarchical directory structure** for organizing files throughout the system.

This differs from Microsoft Windows.

In Windows, each disk device generally has its own directory hierarchy.

Linux uses a unified hierarchical file-system structure.

---

# Course Summary

After completing this course, you should now be familiar with:

* The Linux operating system.
* Linux components.
* Hardware and the kernel.
* The shell.
* System utilities.
* Characteristics of Linux.
* Advantages and disadvantages of Linux.
* Installing Linux using a USB stick.
* Installing Linux using CD-ROM.
* Installing Linux using a virtual machine.
* Installing Ubuntu using VirtualBox.
* Linux startup and boot process.
* POST.
* MBR.
* GRUB.
* `initrd`.
* Linux user environments.
* Environment variables.
* `.bashrc`.
* Linux file-system hierarchy.

---

## Course Files

```text
01-Basics-of-Linux-Operating-System/
├── lecture.md
├── assessment.md
└── certificate.pdf
```
