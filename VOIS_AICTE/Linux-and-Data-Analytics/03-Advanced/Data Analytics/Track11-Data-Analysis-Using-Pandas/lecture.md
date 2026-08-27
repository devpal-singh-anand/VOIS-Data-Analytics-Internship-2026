# Getting Started with Data Analysis Using Pandas

## Learning Objectives

The learning objective is to gain knowledge on:

* performing a multitude of data operations using Python's popular **Pandas** library.
* understanding commonly used Pandas methods and attributes.
* working with Pandas objects such as **Series** and **DataFrames**.
* understanding and manipulate one-dimensional, two-dimensional, and three-dimensional datasets.
* creating Series objects using different types of data.
* creating DataFrame objects using lists, dictionaries, Series, and other data structures.
* importing data from external files such as:

  * TXT files
  * CSV files
* Export Pandas DataFrames to CSV files.
* Access data using indexing and slicing.
* Retrieve data using labels.
* Use `loc`, `iloc`, and `ix` for data selection.
* Add, delete, and rename columns.
* Add and delete rows.
* Iterate over DataFrame rows.
* Perform arithmetic operations on DataFrames.
* Merge or join DataFrames.
* Handle common issues in broken or incomplete datasets.
* Create visualizations using Pandas and Matplotlib.

---

## Prerequisites

Before learning Pandas, you should have:

* Elementary knowledge of Python.
* Basic knowledge of Python data types and objects.
* Basic familiarity with Python libraries.
* Basic understanding of Jupyter Notebook.
* Basic knowledge of data analysis concepts.

---

# About the Course

This course introduces the basics of **Pandas**, a popular Python library for data analysis and manipulation.

Pandas provides powerful and flexible data structures that make it easier to work with raw data and obtain meaningful information from it.

Pandas is built on top of technologies such as:

* **NumPy**
* **Matplotlib**

It is commonly used for:

* Data analysis.
* Data manipulation.
* Data cleaning.
* Data transformation.
* Data importing and exporting.
* Data visualization.

Pandas can work with:

* One-dimensional data.
* Two-dimensional data.
* Three-dimensional data.

---

# Pandas

**Pandas** is one of the major Python tools used for data analysis.

It provides powerful data structures and functions for working with structured data.

Pandas makes it possible to:

* Import data.
* Organize data.
* Analyze data.
* Manipulate data.
* Clean data.
* Handle missing data.
* Reshape datasets.
* Index datasets.
* Export processed data.

Pandas is widely used by:

* Data analysts.
* Data scientists.
* Python developers.
* Machine learning practitioners.

---

# Basic Features of Pandas

Pandas provides significant features for data analysis.

## DataFrame Object

The **DataFrame** object helps keep track of data.

A DataFrame can contain different data types in different columns, such as:

* Integer.
* Float.
* String.
* Date/time.

Therefore, heterogeneous data can be stored and analyzed in a single DataFrame.

---

## Data Manipulation and Cleaning

Pandas provides built-in functionality for:

* Data manipulation.
* Data cleaning.
* Data transformation.
* Missing-data handling.

---

## Input and Output Capabilities

Pandas provides input/output functionality.

Data can be imported from and exported to useful formats such as:

* CSV.
* Excel.
* Text files.

---

## Alignment and Missing Data

Pandas provides support for:

* Data alignment.
* Missing-data handling.

This makes it easier to work with incomplete datasets.

---

## Reshaping and Pivoting

Pandas allows datasets to be:

* Reshaped.
* Pivoted.
* Reorganized.

---

## Label-Based Indexing

Pandas provides support for:

* Label-based slicing.
* Indexing.
* Subsetting.

This is particularly useful when working with large datasets.

---

# Installation and Environment Setup

To use Pandas on a local machine, the course recommends installing **Anaconda**.

Anaconda provides Python along with many commonly used data-analysis libraries.

Anaconda can be downloaded from:

```text
www.anaconda.com
```

After installing Anaconda:

1. Start **Jupyter Notebook**.
2. Create a new notebook cell.
3. Import Pandas using:

```python
import pandas as pd
```

4. Run the cell.

If the command executes without an error, Pandas is available in the installed Anaconda environment.

---

# Pandas Data Structures

Pandas primarily provides two important data structures:

1. **Series**
2. **DataFrame**

---

# Series

A **Series** is a one-dimensional array-like data structure.

A Series can hold a collection of values.

For example, a Series can represent the runs scored by a cricket player:

```text
100
75
45
120
60
```

Each value can be associated with an index.

---

## Characteristics of Series

A Series has the following characteristics:

* It is one-dimensional.
* Data is generally homogeneous.
* The size of a Series is immutable after creation.
* Values can be changed or mutated.
* Each value can be associated with an index.

Conceptually:

```text
Index     Value
  0         10
  1         20
  2         30
  3         40
```

---

# DataFrame

A **DataFrame** is a two-dimensional data structure.

It resembles:

* A table.
* A matrix.
* An Excel spreadsheet.

A DataFrame can contain multiple columns with different data types.

For example:

```text
Name       Age       Marks
Rahul      20        85
Priya      21        91
Amit       19        78
```

---

## Characteristics of DataFrame

A DataFrame:

* Is two-dimensional.
* Can contain heterogeneous data.
* Can contain multiple columns.
* Can contain multiple rows.
* Allows labels for rows and columns.
* Can be modified.
* Can be used for mathematical and analytical operations.

---

# Series and DataFrame Comparison

| Feature    | Series                  | DataFrame            |
| ---------- | ----------------------- | -------------------- |
| Dimension  | One-dimensional         | Two-dimensional      |
| Structure  | Array-like              | Table/matrix-like    |
| Data types | Generally homogeneous   | Can be heterogeneous |
| Columns    | No multiple columns     | Multiple columns     |
| Rows       | Yes                     | Yes                  |
| Index      | Yes                     | Yes                  |
| Common use | Single-dimensional data | Tabular data         |

---

# Creating an Empty Series

The Pandas library must first be imported:

```python
import pandas as pd
```

An empty Series can then be created:

```python
s = pd.Series()
```

The resulting Series represents an empty Series.

Older Pandas versions may display a default data type such as:

```text
float64
```

---

# Creating a Series from a NumPy Array

Pandas can work together with NumPy arrays.

First import both libraries:

```python
import pandas as pd
import numpy as np
```

Create a NumPy array:

```python
data = np.array(['a', 'b', 'c', 'd'])
```

Create a Pandas Series:

```python
s = pd.Series(data)
```

The resulting Series automatically receives default index values:

```text
0    a
1    b
2    c
3    d
```

---

# Specifying Index Values

Custom index values can be supplied while creating a Series.

Example:

```python
s = pd.Series(
    data,
    index=['w', 'x', 'y', 'z']
)
```

The output becomes conceptually:

```text
w    a
x    b
y    c
z    d
```

The index values can therefore be explicitly specified.

---

# Creating a Series from a Dictionary

A Series can also be created from a Python dictionary.

Example:

```python
data = {
    'a': 10,
    'b': 20,
    'c': 30
}

s = pd.Series(data)
```

The dictionary keys become the Series index values.

Output:

```text
a    10
b    20
c    30
```

---

## Series from Dictionary with Explicit Index

An explicit index can also be supplied:

```python
s = pd.Series(
    data,
    index=['b', 'c', 'a']
)
```

The specified index determines the order of the resulting Series.

---

# Creating a Series from a Scalar Value

A Series can be created using a scalar value.

Example:

```python
s = pd.Series(5, index=[0, 1, 2, 3])
```

Since the scalar value is associated with multiple index positions, the value is repeated.

Conceptually:

```text
0    5
1    5
2    5
3    5
```

---

# Mathematical Operations with Series

Pandas Series support mathematical operations.

Consider two Series:

```python
a = pd.Series([1, 2, 3, 4])
b = pd.Series([1, 2, 3, 4])
```

Operations such as addition and multiplication can be performed.

```python
a + b
```

or:

```python
a * b
```

Operations are performed element by element according to corresponding index positions.

Therefore, matching indexes are important when performing arithmetic operations between Series.

---

# The `head()` Method

The `head()` method is used to display the first entries of a Pandas object.

Example:

```python
s.head()
```

By default, `head()` displays the first **five** entries.

A custom number can also be specified:

```python
s.head(3)
```

This displays the first three entries.

---

# The `tail()` Method

The `tail()` method is used to display the last entries of a Pandas object.

Example:

```python
s.tail()
```

By default, it displays the last five entries.

A custom number can be specified:

```python
s.tail(3)
```

This displays the last three entries.

---

# Accessing Series Data Using Indexing

Consider:

```python
s = pd.Series([1, 2, 3, 4, 5])
```

The individual values can be accessed using their index.

For example:

```python
s[0]
```

returns:

```text
1
```

The first value is located at index `0`.

---

# Series Slicing

Pandas Series support slicing.

Example:

```python
s[0:3]
```

This selects the values corresponding to the first three positions.

Negative indexing/slicing can also be used to work with values near the end of the Series.

Example:

```python
s[-3:]
```

This selects the last three values.

---

# Retrieving Data Using Labels

Series can use custom labels as indexes.

Example:

```python
s = pd.Series(
    [1, 2, 3, 4, 5],
    index=['a', 'b', 'c', 'd', 'e']
)
```

A value can then be retrieved using its label:

```python
s['c']
```

This returns:

```text
3
```

Multiple labels can also be used for selection.

---

# Data Selection in Pandas

Pandas provides several methods for selecting data.

Important methods include:

* `loc`
* `iloc`
* `ix`

---

# `loc`

`loc` is used for label-based selection.

It retrieves rows or columns using labels from the index.

Example:

```python
s.loc['c']
```

The selection is based on the label rather than the numerical position.

---

# `iloc`

`iloc` is used for position-based selection.

Example:

```python
s.iloc[3]
```

This retrieves the value at the fourth positional index.

For example:

```python
s.iloc[:3]
```

selects the first three positions.

---

# `ix`

The course material describes `ix` as a selection method that could behave similarly to `loc`, while falling back to `iloc` when a label was not present.

However, `ix` is **deprecated and removed from modern Pandas versions**.

The preferred modern methods are:

```python
loc
```

and:

```python
iloc
```

---

# DataFrame

A DataFrame is one of the most important objects in Pandas.

It is a two-dimensional structure containing:

* Rows.
* Columns.
* Row indexes.
* Column labels.

A DataFrame can contain different data types in different columns.

---

# Creating a DataFrame

The general form is:

```python
pd.DataFrame(data)
```

Additional parameters can include:

* `data`
* `index`
* `columns`
* `dtype`
* `copy`

Example:

```python
df = pd.DataFrame(data)
```

---

# Creating an Empty DataFrame

An empty DataFrame can be created using:

```python
df = pd.DataFrame()
```

This creates a DataFrame without rows or columns.

---

# Creating a DataFrame from a List

A DataFrame can be created from a Python list.

Example:

```python
data = [1, 2, 3, 4]

df = pd.DataFrame(data)
```

A two-dimensional list can also be used.

Example:

```python
data = [
    [1, 2],
    [3, 4],
    [5, 6]
]

df = pd.DataFrame(data)
```

This creates a two-dimensional DataFrame.

---

# Creating a DataFrame from a NumPy Array

NumPy arrays can also be used.

Example:

```python
import numpy as np
import pandas as pd

data = np.array([
    [1, 2],
    [3, 4]
])

df = pd.DataFrame(data)
```

---

# Adding Column Names

Column names can be specified while creating the DataFrame.

Example:

```python
df = pd.DataFrame(
    data,
    columns=['A', 'B']
)
```

The columns are then named:

```text
A
B
```

---

# Creating a DataFrame from a Dictionary

A dictionary can be used to create a DataFrame.

Example:

```python
data = {
    'Name': ['John', 'Rahul'],
    'Age': [20, 21]
}

df = pd.DataFrame(data)
```

The dictionary keys become the column names.

Output:

```text
    Name    Age
0   John     20
1   Rahul    21
```

---

# Creating a DataFrame from a Dictionary of Series

A dictionary can also contain Pandas Series as its values.

Example:

```python
data = {
    'A': pd.Series([1, 2, 3]),
    'B': pd.Series([4, 5, 6])
}

df = pd.DataFrame(data)
```

The dictionary keys become column names, while the Series values become column data.

---

# DataFrame from a Text File

Pandas provides functions for importing data from text files.

The `read_table()` method can be used to read tabular data.

Example:

```python
df = pd.read_table(
    'data.txt',
    delim_whitespace=True
)
```

The method can interpret whitespace-separated values and create a DataFrame.

Column names can also be specified when required.

---

# DataFrame from a CSV File

CSV stands for:

```text
Comma-Separated Values
```

Pandas provides the `read_csv()` method for importing CSV data.

Example:

```python
df = pd.read_csv('data.csv')
```

After loading the data, `head()` can be used to inspect the first entries:

```python
df.head()
```

---

# Editing a DataFrame

DataFrames can be modified after creation.

Common operations include:

* Adding columns.
* Deleting columns.
* Renaming columns.
* Adding rows.
* Deleting rows.

---

# Adding a Column

Suppose:

```python
df = pd.DataFrame({
    'A': [1, 2, 3],
    'B': [4, 5, 6]
})
```

A new column can be added:

```python
df['C'] = [7, 8, 9]
```

The DataFrame now contains:

```text
A    B    C
1    4    7
2    5    8
3    6    9
```

---

# Deleting a Column Using `del`

A column can be removed using the `del` statement.

Example:

```python
del df['C']
```

This removes column `C`.

---

# Deleting a Column Using `pop()`

The `pop()` method can also be used.

Example:

```python
df.pop('C')
```

This removes and returns the specified column.

---

# Renaming Columns

The `rename()` method can be used to rename columns.

Example:

```python
df.rename(
    columns={'A': 'NewA'},
    inplace=True
)
```

The column:

```text
A
```

becomes:

```text
NewA
```

---

# Adding Rows

Rows can be combined with another DataFrame.

For example:

```python
df1
```

and:

```python
df2
```

can be combined so that the rows of `df2` are placed after the rows of `df1`.

Modern Pandas commonly uses `pd.concat()` for this purpose:

```python
df = pd.concat([df1, df2])
```

---

# Dropping Rows

Rows can be removed using the `drop()` method.

Example:

```python
df.drop(0)
```

This removes the row with index `0`.

A modified DataFrame can be stored or the operation can be performed in place when appropriate.

---

# Iterating Over DataFrame Rows

Pandas allows rows of a DataFrame to be processed using a loop.

The `iterrows()` method returns:

* The row index.
* The row data as a Series.

Example:

```python
for index, row in df.iterrows():
    print(index)
    print(row)
```

Individual column values can then be accessed using the column name.

Example:

```python
for index, row in df.iterrows():
    print(row['Name'])
```

---

# `head()` and `tail()` with DataFrames

The `head()` and `tail()` methods also work with DataFrames.

By default:

```python
df.head()
```

returns the first five rows.

Similarly:

```python
df.tail()
```

returns the last five rows.

A custom number can be provided:

```python
df.head(2)
```

or:

```python
df.tail(2)
```

---

# Boolean Indexing

DataFrames can be accessed using Boolean values.

Boolean values are:

```text
True
False
```

For example, a DataFrame can contain a Boolean index.

A Boolean condition can then be used to select specific rows.

Example:

```python
df.loc[True]
```

or a Boolean condition can be applied to select rows satisfying a requirement.

Boolean indexing is particularly useful for filtering datasets.

---

# Basic Operations on DataFrames

Pandas supports mathematical operations between DataFrames.

Consider two DataFrames:

```python
x
```

and:

```python
y
```

The `add()` method can be used:

```python
x.add(y)
```

---

# The `axis` Parameter

Many Pandas operations support the `axis` parameter.

The commonly used values are:

```text
axis=0
axis=1
```

Conceptually:

```text
axis=0
    ↓
Operations along rows / index direction

axis=1
    ↓
Operations across columns
```

The exact behavior depends on the operation being performed.

---

# Merging or Joining DataFrames

Sometimes two DataFrames need to be combined to increase the feature size of the dataset.

Pandas provides the `merge()` method.

Example:

```python
pd.merge(left, right)
```

The merge operation can use one or more columns as keys.

Example:

```python
pd.merge(
    left,
    right,
    on='ID'
)
```

The common column:

```text
ID
```

is used to match records.

---

# Exporting a DataFrame to CSV

After processing a DataFrame, it can be exported to a CSV file.

Pandas provides the:

```python
to_csv()
```

method.

Example:

```python
df.to_csv('output.csv')
```

The DataFrame is written to:

```text
output.csv
```

---

## Controlling Index in CSV Output

The index can be included or excluded.

For example:

```python
df.to_csv(
    'output.csv',
    index=False
)
```

This prevents the DataFrame index from being written as an additional column.

---

# Data Visualization Using Pandas

Pandas also provides plotting functionality.

Visualization is useful because it helps interpret meaningful information from large datasets.

Python provides several popular plotting libraries, including:

* Matplotlib.
* Seaborn.
* Plotly.

Pandas DataFrames also provide plotting methods.

Common plots include:

* Scatter plots.
* Line plots.
* Bar plots.
* Histograms.

---

# Student Marks Case Study

The course uses a student-marks dataset as an example.

The dataset can contain information such as:

* Student name.
* Age.
* Gender.
* Marks.
* Mathematics marks.
* Physics marks.
* Chemistry marks.

A DataFrame can be created from a dictionary.

Example:

```python
import pandas as pd
import matplotlib.pyplot as plt

data = {
    'Name': ['A', 'B', 'C'],
    'Age': [20, 21, 19],
    'Math': [80, 75, 90],
    'Physics': [85, 78, 88],
    'Chemistry': [82, 80, 91]
}

df = pd.DataFrame(data)
```

The first five entries can be inspected using:

```python
df.head()
```

---

# Scatter Plot

A scatter plot represents the relationship between two variables.

For example, a scatter plot can compare:

```text
Math marks
```

and:

```text
Physics marks
```

A Pandas DataFrame can create a scatter plot using:

```python
df.plot(
    kind='scatter',
    x='Math',
    y='Physics'
)
```

Matplotlib can then display the plot:

```python
plt.show()
```

A title can be added using:

```python
plt.title('Math vs Physics')
```

---

# Line Plot

A line plot can be created using the DataFrame `plot()` method.

Example:

```python
df.plot(
    kind='line',
    x='Name',
    y='Math'
)
```

A line plot can be used to show how values vary across observations.

Multiple columns can also be plotted when appropriate.

---

# Bar Plot

A bar plot represents values using rectangular bars.

Example:

```python
df.plot(
    kind='bar',
    x='Name',
    y='Physics'
)
```

A title can be added:

```python
plt.title('Physics Marks')
```

The plot can then be displayed:

```python
plt.show()
```

---

# Common Pandas Plot Types

| Plot         | Purpose                                  |
| ------------ | ---------------------------------------- |
| Scatter plot | Shows relationship between two variables |
| Line plot    | Shows trends or changes                  |
| Bar plot     | Compares values                          |
| Histogram    | Shows distribution of values             |

---

# Important Pandas Methods

| Method         | Purpose                      |
| -------------- | ---------------------------- |
| `head()`       | Returns first rows           |
| `tail()`       | Returns last rows            |
| `loc[]`        | Label-based selection        |
| `iloc[]`       | Position-based selection     |
| `iterrows()`   | Iterates over DataFrame rows |
| `add()`        | Performs addition            |
| `merge()`      | Merges DataFrames            |
| `drop()`       | Removes rows or columns      |
| `pop()`        | Removes and returns a column |
| `rename()`     | Renames labels               |
| `read_csv()`   | Reads CSV data               |
| `read_table()` | Reads tabular/text data      |
| `to_csv()`     | Exports DataFrame to CSV     |
| `plot()`       | Creates plots                |

---

# Important Pandas Concepts

## Series

```text
One-dimensional data structure
```

---

## DataFrame

```text
Two-dimensional tabular data structure
```

---

## Index

An index identifies the position or label associated with data.

---

## Label-Based Selection

Use:

```python
loc
```

---

## Position-Based Selection

Use:

```python
iloc
```

---

## CSV Import

Use:

```python
pd.read_csv()
```

---

## CSV Export

Use:

```python
df.to_csv()
```

---

## DataFrame Iteration

Use:

```python
df.iterrows()
```

---

## DataFrame Merging

Use:

```python
pd.merge()
```

---

## DataFrame Visualization

Use:

```python
df.plot()
```

---

# Quick Reference

| Concept        | Description                                       |
| -------------- | ------------------------------------------------- |
| Pandas         | Python library for data analysis and manipulation |
| Series         | One-dimensional Pandas data structure             |
| DataFrame      | Two-dimensional tabular data structure            |
| `head()`       | Displays first entries                            |
| `tail()`       | Displays last entries                             |
| `loc`          | Label-based selection                             |
| `iloc`         | Position-based selection                          |
| `read_table()` | Reads tabular/text data                           |
| `read_csv()`   | Reads CSV files                                   |
| `to_csv()`     | Exports DataFrame to CSV                          |
| `iterrows()`   | Iterates over DataFrame rows                      |
| `drop()`       | Removes rows/columns                              |
| `pop()`        | Removes and returns a column                      |
| `rename()`     | Renames columns/index labels                      |
| `merge()`      | Combines DataFrames using matching keys           |
| `plot()`       | Creates visualizations                            |

---

# Common Knowledge Check Points

Remember:

```text
Python data-analysis library
        ↓
Pandas

One-dimensional structure
        ↓
Series

Two-dimensional structure
        ↓
DataFrame

First rows
        ↓
head()

Last rows
        ↓
tail()

Label-based selection
        ↓
loc

Position-based selection
        ↓
iloc

Read CSV
        ↓
read_csv()

Read text/table data
        ↓
read_table()

Export DataFrame to CSV
        ↓
to_csv()

Iterate over DataFrame rows
        ↓
iterrows()

Merge DataFrames
        ↓
merge()

Remove rows
        ↓
drop()

Remove a column and return it
        ↓
pop()

Rename columns
        ↓
rename()

Create plots
        ↓
plot()
```

---

# Practical Workflow

A typical Pandas data-analysis workflow can be summarized as:

```text
Install Anaconda
       ↓
Open Jupyter Notebook
       ↓
Import Pandas
       ↓
Load dataset
       ↓
Create Series/DataFrame
       ↓
Inspect data
       ↓
Use head() / tail()
       ↓
Select and filter data
       ↓
Clean and manipulate data
       ↓
Add / delete / rename columns
       ↓
Add / delete rows
       ↓
Perform calculations
       ↓
Merge datasets
       ↓
Visualize data
       ↓
Export processed data
```

---

# Example Complete Pandas Workflow

## Step 1: Import Libraries

```python
import pandas as pd
import matplotlib.pyplot as plt
```

---

## Step 2: Create a DataFrame

```python
data = {
    'Name': ['A', 'B', 'C'],
    'Age': [20, 21, 19],
    'Math': [80, 75, 90],
    'Physics': [85, 78, 88]
}

df = pd.DataFrame(data)
```

---

## Step 3: Inspect the Data

```python
df.head()
```

---

## Step 4: Select Data

Label-based selection:

```python
df.loc[0]
```

Position-based selection:

```python
df.iloc[0]
```

---

## Step 5: Add a Column

```python
df['Chemistry'] = [82, 80, 91]
```

---

## Step 6: Remove a Column

```python
df.drop('Chemistry', axis=1)
```

---

## Step 7: Iterate Through Rows

```python
for index, row in df.iterrows():
    print(row['Name'])
```

---

## Step 8: Create a Plot

```python
df.plot(
    kind='scatter',
    x='Math',
    y='Physics'
)

plt.show()
```

---

## Step 9: Export the Data

```python
df.to_csv(
    'output.csv',
    index=False
)
```

---

# Course Summary

This course introduced the fundamental concepts of **data analysis using Pandas**.

The major topics covered were:

* Introduction to Pandas.
* Features of Pandas.
* Pandas data structures.
* **Series**.
* **DataFrame**.
* Creating Series from:

  * NumPy arrays.
  * Dictionaries.
  * Scalar values.
* Series indexing and slicing.
* Series mathematical operations.
* `head()` and `tail()`.
* Label-based data selection.
* `loc`.
* `iloc`.
* The historical `ix` method.
* Creating DataFrames.
* Creating DataFrames from:

  * Lists.
  * NumPy arrays.
  * Dictionaries.
  * Dictionaries of Series.
* Reading text data using `read_table()`.
* Reading CSV data using `read_csv()`.
* Adding columns.
* Deleting columns.
* Renaming columns.
* Adding rows.
* Dropping rows.
* Iterating through DataFrame rows using `iterrows()`.
* Boolean indexing.
* DataFrame arithmetic operations.
* The `axis` parameter.
* Merging DataFrames.
* Exporting DataFrames to CSV.
* Data visualization using Pandas.
* Scatter plots.
* Line plots.
* Bar plots.
* Using Matplotlib with Pandas.

The overall concept can be summarized as:

```text
Raw Data
   ↓
Pandas
   ↓
Series / DataFrame
   ↓
Indexing & Selection
   ↓
Cleaning & Manipulation
   ↓
Analysis
   ↓
Visualization
   ↓
Export
```

After completing the course, you should be familiar with using Pandas to create, import, manipulate, analyze, visualize, and export structured datasets.

---

# Course Files

```text
Track11-Data-Analysis-Using-Pandas/
├── lecture.md
├── assessment.md
└── certificate.pdf
```
