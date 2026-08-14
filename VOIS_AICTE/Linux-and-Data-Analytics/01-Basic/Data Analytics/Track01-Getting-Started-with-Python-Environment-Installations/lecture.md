# Getting Started with Python Environment Installation

## Learning Objectives

The learning objective is to gain knowledge on:

* installing and use data analytics-related applications in **Linux and Windows environments**.
* understanding the purpose and features of the **Anaconda distribution**.
* understanding and use **Conda environments**.
* understanding different attributes of running **Jupyter Notebook**.
* authoring a **Jupyter Notebook**.
* launching and use Jupyter Notebook.
* understanding how Python environments can be isolated.
* deploying and use required **open-source Python libraries**.
* understanding the purpose of commonly used Python libraries such as:
  * Pandas
  * NumPy
  * Requests
  * SciPy
  * SQLite3

---

## Prerequisites

* Elementary knowledge of computers.
* Basic exposure to a **Linux system**.
* Basic familiarity with Python programming concepts.
* Basic understanding of command-line environments.

---

# About the Course

This course introduces the installation and use of tools required for **Python programming and data analytics**.

The course focuses on:

* Installing Anaconda.
* Understanding Anaconda Prompt.
* Understanding Conda.
* Creating and managing isolated environments.
* Using Jupyter Notebook.
* Installing and using Python libraries.
* Performing data analysis and numerical computations using open-source Python libraries.

The course covers both **Linux and Windows environments**.

---

# Anaconda

**Anaconda** is a distribution of the **Python and R programming languages**.

It is commonly used for:

* Scientific computing
* Data science
* Machine learning
* Large-scale data processing
* Predictive analytics

Anaconda aims to simplify:

* Package management
* Environment management
* Software deployment

The Anaconda distribution includes many packages that are useful for data science and scientific computing.

Anaconda is available for:

* Windows
* Linux
* macOS

---

# Features of Anaconda

Anaconda provides an environment for working with Python and R along with many commonly required packages.

It helps users:

* Install Python packages.
* Manage package dependencies.
* Create isolated environments.
* Manage different versions of packages.
* Work with data science tools.
* Run Jupyter Notebook.
* Develop machine learning and scientific computing applications.

---

# Installing Anaconda on Linux

Anaconda can be installed on Linux using the installation file provided by Anaconda.

---

## Step 1: Open the Anaconda Website

Visit:

```text
anaconda.com
````

Navigate to the **Download** section.

---

## Step 2: Download the Latest Version

Download the latest version of Anaconda compatible with your Linux system.

For Linux, the installation package is provided as an:

```text
.sh
```

installation file.

---

## Step 3: General Installation Process

The general process for installing an SH file includes:

1. Find a version compatible with your Linux distribution.
2. Download the software.
3. Unzip or extract the software if required.
4. Run the installation software.
5. Follow the instructions provided by the installer.
6. Restart the computer if required.

---

# Running the Anaconda Installation File

After downloading the Anaconda SH file, open the Linux terminal.

The installation file can be executed from the command line using the appropriate shell command.

**Bash** is a command-line interpreter and Unix shell commonly used in GNU/Linux operating systems.

During the installation, Bash executes the commands contained in the installation script.

---

# Completing the Linux Installation

During the installation:

* Read the license agreement.
* Accept the terms and conditions.
* Follow the installation instructions.
* Select the appropriate installation location if prompted.
* Allow the installation to complete.

After installation, Anaconda and its associated tools can be used from the Linux environment.

---

# Installing Anaconda on Windows

Anaconda can also be installed on a Windows computer using its graphical installer.

---

## Step 1: Open the Anaconda Website

Visit:

```text
anaconda.com
```

Navigate to the **Download** section.

---

## Step 2: Download the Latest Version

Download the latest Windows-compatible version of Anaconda.

---

## Step 3: Locate the Downloaded File

After downloading the installer:

* Open the folder containing the downloaded file.
* Locate the Anaconda installation executable.

---

## Step 4: Run the Setup

Double-click the installation file to start the Anaconda setup process.

---

## Step 5: Continue the Installation

Click:

```text
Next
```

to continue with the installation.

---

## Step 6: Accept the Terms and Conditions

Read the license agreement.

Accept the terms and conditions to continue.

---

## Step 7: Select the Installation Type

The installer provides installation options.

For individual users and beginners, select:

```text
Just Me
```

---

## Step 8: Select the Installation Location

Choose the location where Anaconda should be installed.

The course recommends keeping the:

```text
Default location
```

Click:

```text
Next
```

---

## Step 9: Configure the PATH Environment Variable

The installer provides an option to add Anaconda to the:

```text
PATH
```

environment variable.

Adding Anaconda to PATH allows Anaconda-related commands to be accessed from the Windows Command Prompt.

Click:

```text
Install
```

to begin installation.

---

## Step 10: Confirm the Installation Location

Confirm the location where Anaconda will be installed.

Keep the default location if appropriate.

Click:

```text
Next
```

---

## Step 11: Installation Process

The installation process may take several minutes.

Wait until the installation is completed.

---

## Step 12: Complete the Installation

Once the installation finishes, click:

```text
Next
```

to continue.

---

## Step 13: Finish Setup

Click:

```text
Finish
```

to complete the Anaconda installation.

Anaconda is now installed on the Windows system.

---

# Anaconda Prompt

## What is Anaconda Prompt?

**Anaconda Prompt** is a command-line interface similar to the Windows Command Prompt.

It is configured so that:

* Anaconda commands can be executed.
* Conda commands can be executed.
* Python environments can be managed.
* Packages can be installed and updated.

Users do not need to manually navigate to Anaconda's installation directory before using Anaconda-related commands.

---

# Uses of Anaconda Prompt

Anaconda Prompt can be used to:

* Create Python environments.
* Activate environments.
* Deactivate environments.
* Maintain Python environments.
* Update Python environments.
* Install additional libraries.
* Manage package dependencies.
* Switch between different environments.

---

# Environment Isolation

Anaconda allows users to create separate environments for different projects.

This provides **dependency isolation**.

For example, two projects may require different versions of the same library.

One project may require:

```text
NumPy 1.18
```

while another may require:

```text
NumPy 1.12
```

Separate environments allow both projects to operate without interfering with each other.

---

# Package Installation

Additional Python libraries can be installed using package management tools such as:

* **Conda**
* **PIP**

Conda is commonly used for managing packages and environments within the Anaconda ecosystem.

PIP is the standard Python package installer.

---

# Conda

## What is Conda?

**Conda** is an open-source:

* Package management system
* Environment management system

Conda is used to manage software packages and isolated environments.

It is available on:

* Windows
* macOS
* Linux
* z/OS

---

# Features of Conda

Conda can be used to:

* Install packages.
* Run packages.
* Update packages.
* Update package dependencies.
* Create environments.
* Save environments.
* Load environments.
* Activate environments.
* Deactivate environments.
* Switch between environments.

---

# Conda Environments

A **Conda environment** is a directory containing a specific collection of Conda packages installed for that environment.

Each environment can contain its own:

* Python version.
* Package versions.
* Dependencies.
* Configuration.

This allows different projects to maintain separate software requirements.

---

# Why Use Conda Environments?

Suppose two projects require different versions of NumPy.

Project A requires:

```text
NumPy 1.18
```

Project B requires:

```text
NumPy 1.12
```

Installing both versions globally could create dependency conflicts.

Instead, separate environments can be created:

```text
Environment A
└── NumPy 1.18

Environment B
└── NumPy 1.12
```

Changes made inside one environment do not normally affect the other environment.

---

# Activating a Conda Environment

A Conda environment can be activated so that its packages and configuration become available to the current terminal session.

The general command is:

```bash
conda activate environment_name
```

Example:

```bash
conda activate data-analysis
```

---

# Deactivating a Conda Environment

An active Conda environment can be deactivated using:

```bash
conda deactivate
```

This returns the terminal to the previous environment level.

---

# Switching Between Environments

Users can deactivate the current environment and activate another environment.

Example:

```bash
conda deactivate
conda activate machine-learning
```

This makes it possible to work with different project configurations.

---

# Updating Conda

Conda can be updated through **Anaconda Prompt**.

## Step 1: Open Anaconda Prompt

Open:

```text
Anaconda Prompt
```

from the Windows Start Menu.

## Step 2: Update Conda

Use the appropriate Conda update command from the Anaconda Prompt.

The update process downloads and installs the required updates.

---

# Jupyter Notebook

## What is Jupyter Notebook?

**Jupyter Notebook** is a **client-server application**.

When Jupyter Notebook is launched:

1. A local server is started.
2. The Jupyter Notebook interface becomes available.
3. The interface opens in a web browser.
4. Users can create, edit, and execute notebook code.

Jupyter Notebook is widely used for:

* Python programming.
* Data analysis.
* Data visualization.
* Scientific computing.
* Machine learning.
* Interactive experimentation.

---

# Jupyter Notebook File Format

Jupyter Notebook files use the:

```text
.ipynb
```

extension.

Example:

```text
data_analysis.ipynb
```

The notebook can contain:

* Python code.
* Code output.
* Markdown text.
* Explanations.
* Visualizations.
* Mathematical content.

---

# Advantages of Jupyter Notebook

Jupyter Notebook allows users to:

* Write code interactively.
* Execute individual code cells.
* Immediately view output.
* Combine code and documentation.
* Perform exploratory data analysis.
* Display charts and visualizations.
* Save the complete notebook for later use.

---

# Exporting Jupyter Notebooks

Jupyter Notebooks can be exported into several formats.

Common formats include:

* HTML
* PDF
* LaTeX

This allows notebooks to be shared and presented in different formats.

---

# Launching Jupyter Notebook

## Step 1: Open Anaconda Prompt

Start:

```text
Anaconda Prompt
```

---

## Step 2: Run Jupyter Notebook

Enter:

```bash
jupyter notebook
```

Press:

```text
Enter
```

---

## Step 3: Launch Jupyter Notebook

The Jupyter Notebook server starts on the local machine.

The Notebook interface generally opens automatically in a web browser.

---

## Step 4: Select an Environment

Click:

```text
New
```

and select the required Python environment.

---

## Step 5: Launch a New Notebook

Select the appropriate environment to create a new Jupyter Notebook.

---

## Step 6: Write Python Code

Python code can now be written and executed inside the notebook.

Example:

```python
print("Hello Python")
```

Output:

```text
Hello Python
```

---

# Jupyter Notebook Cells

A Jupyter Notebook is divided into **cells**.

Cells can contain different types of content.

Common cell types include:

* Code
* Markdown

A code cell is used to write and execute Python code.

A Markdown cell can be used to add:

* Headings
* Explanations
* Notes
* Documentation

---

# Python Libraries

Python provides a large ecosystem of **open-source libraries**.

These libraries provide functionality for:

* Data science
* Data analysis
* Machine learning
* Mathematical computation
* Scientific computing
* HTTP requests
* Database operations

The course introduces several commonly used libraries.

---

# Pandas

**Pandas** is an open-source Python library primarily used for:

* Data science
* Data analysis
* Data manipulation
* Machine learning workflows

Pandas provides powerful data structures and tools for working with data.

---

## Uses of Pandas

Pandas can be used for:

* Manipulating numerical tables.
* Reading datasets.
* Cleaning data.
* Analyzing data.
* Working with time-series data.
* Filtering data.
* Grouping data.
* Transforming data.

---

## Example

```python
import pandas as pd
```

A common Pandas data structure is the:

```text
DataFrame
```

A DataFrame represents tabular data organized into rows and columns.

---

# NumPy

**NumPy** is a Python library used primarily for **numerical and mathematical operations**.

NumPy is particularly useful for:

* Array processing.
* Matrix processing.
* Mathematical functions.
* Numerical computations.
* Scientific computing.

NumPy is widely used in:

* Data science.
* Machine learning.
* Scientific computing.

---

## Example

```python
import numpy as np
```

NumPy provides an efficient multidimensional array structure called:

```text
ndarray
```

---

# Requests

**Requests** is a Python library used for sending **HTTP requests**.

It allows Python applications to communicate with web servers and APIs.

Requests supports functionality such as:

* Sending HTTP requests.
* Adding HTTP headers.
* Forming request data.
* Accessing response objects.
* Accessing response content.
* Accessing response encoding.
* Accessing HTTP status information.

---

## Example

```python
import requests
```

A simple HTTP request can be made using:

```python
response = requests.get("https://example.com")
```

The response object can then be used to inspect information returned by the server.

---

# SciPy

**SciPy** is an open-source Python library used primarily for:

* Mathematical computations.
* Scientific computations.
* Technical computations.
* Engineering computations.

SciPy provides functionality for various scientific and mathematical tasks.

SciPy is primarily built on top of **NumPy**.

---

## Relationship Between NumPy and SciPy

NumPy provides fundamental numerical structures and operations.

SciPy builds on these capabilities to provide additional scientific and technical functionality.

Conceptually:

```text
NumPy
  ↓
Numerical foundation
  ↓
SciPy
  ↓
Scientific and technical computing
```

---

# SQLite3

**SQLite3** is used for performing **database operations** using SQL queries.

Python provides the `sqlite3` module for working with SQLite databases.

SQLite is a lightweight database system that stores data in a database file.

---

## Uses of SQLite3

SQLite3 can be used to:

* Create databases.
* Create tables.
* Insert records.
* Retrieve records.
* Update records.
* Delete records.
* Execute SQL queries.

---

## Example

```python
import sqlite3
```

A connection to a SQLite database can be established using Python.

```python
connection = sqlite3.connect("example.db")
```

---

# Common Python Libraries Summary

| Library      | Primary Purpose                       |
| ------------ | ------------------------------------- |
| **Pandas**   | Data analysis and data manipulation   |
| **NumPy**    | Mathematical and numerical operations |
| **Requests** | Sending HTTP requests                 |
| **SciPy**    | Scientific and technical computing    |
| **SQLite3**  | Database operations using SQL         |

---

# Conda vs Anaconda

Although **Anaconda** and **Conda** are related, they are not the same thing.

## Anaconda

Anaconda is a **Python and R distribution** that includes many packages and tools for data science.

## Conda

Conda is a **package and environment management system**.

In simple terms:

```text
Anaconda
    ↓
Distribution containing tools and packages

Conda
    ↓
Package and environment manager
```

---

# Anaconda Prompt vs Command Prompt

## Command Prompt

Windows Command Prompt is the standard Windows command-line interface.

## Anaconda Prompt

Anaconda Prompt is configured specifically for working with:

* Anaconda.
* Conda.
* Python environments.
* Python packages.

Therefore, Anaconda Prompt provides a convenient environment for managing Anaconda installations.

---

# Linux and Windows Environment Comparison

Anaconda can be installed and used on different operating systems.

| Feature             | Linux        | Windows                          |
| ------------------- | ------------ | -------------------------------- |
| Anaconda available  | Yes          | Yes                              |
| Installation method | SH installer | Graphical installer              |
| Terminal            | Linux shell  | Anaconda Prompt / Command Prompt |
| Conda support       | Yes          | Yes                              |
| Jupyter Notebook    | Yes          | Yes                              |
| Python libraries    | Yes          | Yes                              |

---

# Basic Environment Workflow

A typical Python data analytics workflow can involve:

```text
Install Anaconda
       ↓
Open Anaconda Prompt
       ↓
Create/activate Conda environment
       ↓
Install required packages
       ↓
Launch Jupyter Notebook
       ↓
Create .ipynb notebook
       ↓
Write Python code
       ↓
Perform analysis
       ↓
Export notebook
```

---

# Example Python Environment Workflow

## Step 1: Open Anaconda Prompt

Launch:

```text
Anaconda Prompt
```

---

## Step 2: Activate an Environment

```bash
conda activate data-analysis
```

---

## Step 3: Launch Jupyter Notebook

```bash
jupyter notebook
```

---

## Step 4: Create a Notebook

Create a new Python notebook using the required environment.

---

## Step 5: Import Libraries

Example:

```python
import pandas as pd
import numpy as np
import requests
```

---

## Step 6: Perform Analysis

Python libraries can now be used to:

* Load data.
* Manipulate data.
* Perform calculations.
* Access web resources.
* Analyze results.

---

# Important Commands

| Command                           | Purpose                                                        |
| --------------------------------- | -------------------------------------------------------------- |
| `jupyter notebook`                | Launches Jupyter Notebook                                      |
| `conda activate environment_name` | Activates a Conda environment                                  |
| `conda deactivate`                | Deactivates the current Conda environment                      |
| `conda`                           | Command-line tool for Conda package and environment management |

---

# Important Concepts to Remember

## Anaconda

Anaconda is a distribution for:

* Python
* R
* Data science
* Machine learning
* Scientific computing

---

## Conda

Conda is used for:

* Package management.
* Environment management.
* Dependency management.

---

## Conda Environment

A Conda environment provides an isolated collection of packages and dependencies for a project.

---

## Jupyter Notebook

Jupyter Notebook is a client-server application that provides an interactive browser-based environment for writing and executing code.

Notebook files use:

```text
.ipynb
```

---

## Pandas

Pandas is mainly used for:

```text
Data analysis
Data manipulation
```

---

## NumPy

NumPy is mainly used for:

```text
Mathematical and numerical operations
```

---

## Requests

Requests is mainly used for:

```text
HTTP requests
```

---

## SciPy

SciPy is mainly used for:

```text
Scientific and technical computing
```

---

## SQLite3

SQLite3 is mainly used for:

```text
Database operations
```

---

# Quick Reference

| Concept           | Description                                                          |
| ----------------- | -------------------------------------------------------------------- |
| Anaconda          | Python and R distribution for data science and scientific computing  |
| Conda             | Package and environment management system                            |
| Anaconda Prompt   | Command-line environment configured for Anaconda and Conda           |
| Conda Environment | Isolated environment containing specific packages and dependencies   |
| Jupyter Notebook  | Interactive client-server application for writing and executing code |
| `.ipynb`          | Jupyter Notebook file extension                                      |
| Pandas            | Data analysis and manipulation library                               |
| NumPy             | Numerical and mathematical computing library                         |
| Requests          | HTTP request library                                                 |
| SciPy             | Scientific and technical computing library                           |
| SQLite3           | Database library/module for SQLite operations                        |

---

### Common Knowledge Check Points

Remember:

```text
Distribution for Python and R → Anaconda

Package/environment manager → Conda

Command-line tool provided with Anaconda → Anaconda Prompt

Interactive Python notebook → Jupyter Notebook

Jupyter Notebook file extension → .ipynb

Mathematical/numerical functions → NumPy

HTTP requests → Requests

Data analysis/manipulation → Pandas

Scientific/technical computing → SciPy

Database operations → SQLite3
```

---

# Course Summary

This course introduced the tools and environments required for **Python programming and data analytics**.

The major topics covered were:

* **Anaconda** as a Python and R distribution for data science and scientific computing.
* Installation of Anaconda on **Linux**.
* Installation of Anaconda on **Windows**.
* **Anaconda Prompt** for managing Anaconda and Conda commands.
* **Conda** as a package and environment management system.
* **Conda environments** for isolating project dependencies.
* **Jupyter Notebook** as an interactive client-server application.
* The `.ipynb` notebook file format.
* Launching and using Jupyter Notebook.
* Exporting Jupyter Notebooks to formats such as HTML, PDF, and LaTeX.
* Python libraries used for different tasks.
* **Pandas** for data analysis and manipulation.
* **NumPy** for mathematical and numerical operations.
* **Requests** for sending HTTP requests.
* **SciPy** for scientific and technical computations.
* **SQLite3** for database operations.

The overall workflow can be summarized as:

```text
Anaconda
   ↓
Conda
   ↓
Environment Management
   ↓
Python Libraries
   ↓
Jupyter Notebook
   ↓
Data Analysis / Scientific Computing
```

After completing the course, you should be familiar with setting up a Python environment, managing packages and isolated environments, launching Jupyter Notebook, and using common open-source Python libraries.

---

# Course Files

```text
Track01-Getting-Started-with-Python-Environment-Installation/
├── lectures.md
├── assessment.md
└── certificate.pdf
```
