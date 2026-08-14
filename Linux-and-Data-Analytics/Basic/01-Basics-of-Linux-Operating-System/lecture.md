# Basics of Linux Operating System

## Course Instructions

* The course resumes from where you left off when relaunched.
* Complete and pass the final assessment before exiting.
* The assessment can be retaken as many times as needed.
* Some slides require you to complete/read the slide before **Next** becomes active.
* Some slides have on-screen buttons that must all be clicked before **Next** becomes active.

---

## Learning Objectives

After completing this course, you should be able to:

* Become familiar with the **Linux operating system**.
* Understand the **components of Linux**.
* Understand the **Linux installation steps**.

## Prerequisite

A system with **Linux installed**.

---

# Introduction to Linux

## What is Linux?

Linux is an operating system or kernel made available under an **open-source license**.

Its feature set is very similar to **UNIX**.

The Linux kernel is a piece of software that handles basic tasks, including enabling communication between hardware and software.

---

# Components of Linux Operating System

The Linux operating system consists of several important components that work together.

## Hardware Layer

The hardware layer consists of physical components and peripherals such as:

* RAM
* Hard Disk Drives (HDDs)
* CPUs
* Other peripherals

## Kernel

The **kernel** is the core component of the Linux operating system.

It is responsible for various operations and interacts directly with the hardware.

The kernel provides low-level services, including giving the system access to hardware resources and data.

## Types of Kernels

The two types of kernels mentioned in the course are:

* **Monolithic Kernel**
* **Microkernel**

## Shell

The **shell** acts as an interface between the user and the kernel.

It hides the complexity of the kernel's functions from the user.

The shell:

* Accepts human commands.
* Interprets the commands.
* Carries out the requested tasks.

## Utilities

Utilities provide access to operating-system features.

**System utilities** are used for specialized tasks.

---

# Characteristics of Linux

Linux can be utilized using **commands**.

## Linux Commands

Linux commands are used to perform one or multiple tasks.

Examples include:

* Copy
* Paste
* Find

Commands allow tasks to be carried out efficiently and effectively, including executing programs and performing system operations.

---

# Linux File System

The Linux kernel maintains a **single hierarchical directory structure** to organize all files in the system.

## `/bin`

Contains common programs shared by:

* The system
* System administrators
* Users

## `/boot`

Contains the startup files and the Linux kernel, such as `vmlinuz`.

In some recent distributions, it also contains **GRUB data**.

### GRUB

**GRUB** stands for **GRand Unified Bootloader**.

It is an attempt to provide a common bootloader instead of the many different bootloaders used historically.

## `/dev`

Contains references to CPU peripheral hardware.

Hardware devices are represented as files with **special properties**.

## `/etc`

Contains the most important **system configuration files**.

The directory contains data similar to the **Control Panel in Windows**.

The `/etc` directory does not contain binary files.

## `/home`

Contains the **home directories of common users**.

## `/initrd`

On some distributions, this directory contains information required for **booting**.

> **Important:** Do not remove this directory.

## `/lib`

Contains **library files** required by various programs used by the system and users.

## `/lost+found`

Every partition has a `lost+found` directory in its upper directory.

Files that were saved during system failures are stored here.

## `/misc`

Used for **miscellaneous purposes**.

## `/mnt`

A standard mount point for external file systems.

Examples include:

* CD-ROM
* Digital camera

## `/net`

A standard mount point for **entire remote file systems**.

## `/opt`

Typically contains **extra and third-party software**.

## `/proc`

A **virtual file system** containing information about system resources.

More information about the meaning of the files in `/proc` can be obtained by entering:

```bash
man proc
```

The `proc.txt` file discusses the virtual file system in detail.

## `/root`

The **administrative user's home directory**.

### `/` vs `/root`

It is important to distinguish between:

* `/` — The root directory
* `/root` — The home directory of the root user

## `/sbin`

Contains programs used by:

* The system
* System administrators

## `/tmp`

Provides temporary space for system use.

The contents are cleaned upon reboot.

> **Important:** Do not use `/tmp` for saving important work.

## `/usr`

Contains:

* Programs
* Libraries
* Documentation
* Other resources for user-related programs

---

# Advantages of Linux

## Free to Use

Linux is free and can be downloaded from the internet.

There are no hidden costs for:

* Registration
* Updates
* Basic usage

## Flexible

Linux is flexible and can be installed on different types of hardware.

If a user is unsure which operating system can be installed on their machine, Linux can be a suitable option.

---

# Disadvantages of Linux

## Multiple Distributions

Linux is licensed under the **GNU General Public License (GPL)**, which allows anyone to modify and distribute a changed version.

Because of this, there are many different Linux distributions, which can make it confusing to find a version suitable for a particular need.

## Not Very User-Friendly for Beginners

Linux can be somewhat confusing for beginners and is not always considered very user-friendly.

---

# Installing Linux Using a USB Stick

Installing Linux using a USB stick is one of the easiest methods of installing **Ubuntu or another Linux distribution** on a computer.

## Step 1: Download Required Files

Download the required **ISO or operating system files** onto the computer.

## Step 2: Download Universal USB Installer

Download free software such as **Universal USB Installer** to create a bootable USB stick.

## Step 3: Select Distribution

* Select an Ubuntu distribution from the drop-down list.
* Select the Ubuntu ISO file downloaded in Step 1.
* Select the USB drive letter.
* Click **Create**.

## Step 4: Install Ubuntu

Click **Yes** to install Ubuntu onto the USB.

After everything has been installed and configured, a confirmation window appears.

Ubuntu is then available on the USB stick and is **bootable and ready to use**.

---

# Installing Linux Using CD-ROM

Another method of installing Linux is using a **CD-ROM**.

## Steps

### Step 1: Download the ISO

Download the Linux ISO or operating system files onto the computer.

### Step 2: Burn the Files to a CD

Burn the downloaded files to a CD.

### Step 3: Boot From the Optical Drive

Boot the computer from the optical drive and follow the installation instructions.

---

# Installing Linux Using a Virtual Machine

Installing Linux using a **virtual machine** is a popular method.

Virtual installation allows Linux to run on an existing operating system already installed on the computer.

---

# Installing VirtualBox

## Step 1: Download VirtualBox

Download VirtualBox using the provided link.

Once the download is complete, open the setup file.

## Step 2: Select Installation Directory

Select the directory where VirtualBox should be installed.

Click **Next**.

## Step 3: Select Desktop Icon

Select the desktop icon option.

Click **Next**.

Click **Yes** when prompted.

## Step 4: Install VirtualBox

Click **Install** to install VirtualBox on Windows.

## Step 5: Complete Installation

The VirtualBox installation starts.

Once installation is complete, click **Finish** to start VirtualBox.

The VirtualBox dashboard will appear.

---

# Download Ubuntu

Download the Ubuntu ISO file using the provided link.

---

# Creating a Virtual Machine in VirtualBox

## Step 1: Create a New Machine

Open VirtualBox and click the **New** button.

## Step 2: Configure the Operating System

In the next window:

* Enter the name of the operating system.
* Select **Linux** as the operating system type.
* Select **Ubuntu 32-bit** as the version.
* Click **Next**.

## Step 3: Allocate RAM

Allocate RAM to the virtual operating system.

The course recommends **1024 MB RAM** to run Ubuntu better.

Click **Next**.

## Step 4: Create a Virtual Hard Disk

Select:

**Create a Virtual Hard Disk Now**

Then click **Create**.

The virtual hard disk stores:

* OS installation files
* Data
* Applications installed in the Ubuntu virtual machine

## Step 5: Select VHD

Select the **VHD** option.

Click **Next**.

## Step 6: Select Dynamic Allocation

Select **Dynamically Allocated**.

Click **Next**.

This means that the size of the disk will increase dynamically according to requirements.

## Step 7: Allocate Virtual Hard Disk Space

Allocate **8 GB** to the virtual hard drive as recommended.

Click **Create**.

## Step 8: Verify the Machine

The newly created virtual machine appears in the **left panel** of VirtualBox.

---

# Installing Ubuntu in VirtualBox

## Step 1: Start the Machine

Select the virtual machine and click **Start**.

Select the folder option and choose the Ubuntu ISO file.

Click **Start**.

## Step 2: Select Ubuntu Installation

Ubuntu provides an option to run Ubuntu without installing it.

For this tutorial, select the option to **install Ubuntu**.

Click **Continue**.

## Step 3: Select Installation Option

Select:

**Erase the disk and install Ubuntu**

Click **Install Now**.

This option installs Ubuntu into the virtual hard drive created earlier.

The course notes that this will not harm the physical PC or Windows installation because Ubuntu is being installed inside the virtual machine.

## Step 4: Select Location

Select your location to configure the time zone.

Click **Continue**.

## Step 5: Select Keyboard Layout

Select the required keyboard layout.

English is selected by default, but another layout can be selected from the list if required.

Click **Continue**.

## Step 6: Create Ubuntu User Account

Enter:

* Username
* Password
* Required account details

This information is needed for:

* Logging into Ubuntu
* Installing software packages

Select **Log in automatically** if you want to skip the login prompt.

Click **Continue**.

## Step 7: Installation Process

The installation process starts.

The course states that installation may take **up to 30 minutes**.

Wait until the installation process is complete.

## Step 8: Ubuntu Desktop

After the installation finishes, the **Ubuntu Desktop** appears.

---

# Managing the Linux Startup Process

When the power button is pressed on a machine, the firmware stored in an **EEPROM chip** on the motherboard initializes the **POST** to check the state of the system's hardware resources.

## Firmware and POST

**POST** stands for **Power-On Self-Test**.

The firmware initializes POST to check the state of the system's hardware resources.

## Bootloader

After POST finishes, the firmware:

1. Searches for the first-stage bootloader.
2. Loads the bootloader.
3. Gives control to the bootloader.

---

# MBR Method

The **Master Boot Record (MBR)** contains three main sections.

## First 446 Bytes — Bootloader

The first **446 bytes** contain the bootloader.

The bootloader contains:

* Executable code
* Error message text

## Next 64 Bytes — Partition Table

The next **64 bytes** contain the partition table.

It contains a record for each of up to four partitions, which can be primary or extended.

Each record indicates information such as:

* Status — active or not active
* Size
* Starting sector
* Ending sector

## Last 2 Bytes — Magic Number

The last **2 bytes** contain the magic number.

It serves as a **validation check of the MBR**.

---

# GRUB Configuration

The course mentions:

* **GRUB Legacy configuration file**
* **GRUB2 configuration file**

Although the objectives of the **LFCS exam** do not explicitly require knowledge about GRUB internals, experimentation with GRUB should preferably be done on a **virtual machine** to avoid damaging the main system.

## Updating GRUB

The course mentions the `update-grub` command.

Basically, **GRUB loads the default kernel and the init/initramfs image**.

## Init and Initramfs

`init` or `initramfs` helps perform the tasks necessary to get the real root file system mounted.

These tasks include:

* Hardware detection
* Kernel module loading
* Device discovery

---

# Managing Linux Environments

Linux user environments help users find commands and accomplish tasks without needing detailed knowledge of how the system is configured.

## User Environment Configuration

The configuration of a Linux user account simplifies system usage in many ways.

For example:

* Commands can be run without knowing where they are located.
* Previously run commands can be reused without worrying about how the system keeps track of them.

## Viewing Environment Settings

The `env` command can be used to view environment settings.

```bash
env
```

## Changing Environment Settings

Environment settings can be modified using configuration files.

For example, a setting such as:

```bash
HISTSIZE=1234
```

can be added to:

```text
~/.bashrc
```

if the setting needs to be retained.

---

# Linux File System vs Microsoft Windows

## Linux

The Linux kernel maintains a **single hierarchical directory structure** to organize all files in the system.

## Microsoft Windows

Each disk device has its **own directory hierarchy**.

---

# Course Completion

After completing the course, you should be able to:

* Become familiar with the **Linux operating system**.
* Understand the **components of Linux**.
* Understand the **Linux installation steps**.

---

## Course Files

```text
01-Basics-of-Linux-Operating-System/
├── lectures.md
├── assessment.md
└── certificate.pdf
```

The `certificate.pdf` should be added after the course certificate has been obtained.
