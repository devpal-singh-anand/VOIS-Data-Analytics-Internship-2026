# VOIS FOR TECH — Data Analysis Using NumPy

## Learning Objectives

The learning objective is to gain knowledge on:

* understanding NumPy.
* installing NumPy.
* understanding and use statistical functions of NumPy.
* generating random numbers using Python and NumPy.
* creating scalars using NumPy.
* creating vectors using NumPy.
* performing operations on vectors.
* understanding NumPy arrays.
* sorting NumPy arrays.
* understanding broadcasting of arrays.
* creating and work with matrices using NumPy.
* accessing values of a matrix.
* performing matrix multiplication.
* understanding measures of central tendency using NumPy.

---

# Introduction to NumPy

NumPy is an open-source Python library used for working with arrays.

It also provides functions for working in domains such as:

* Linear algebra.
* Fourier transforms.
* Matrices.
* Mathematical operations.
* Statistical operations.

**NumPy** stands for **Numerical Python**.

NumPy is a Python library written partially in Python. However, most of the parts that require fast computation are written in **C or C++**.

---

# Why NumPy?

NumPy can be used for the following operations:

* Arithmetic operations.
* Statistical operations.
* Bitwise operations.
* Copying and viewing arrays.
* Sorting arrays.
* Linear algebra.
* Mathematical operations.

NumPy provides an array object that can be significantly faster and more efficient than traditional Python lists for numerical operations.

---

# Installing the NumPy Module

NumPy can be installed using the command prompt or terminal.

## Using pip

The following command can be used to install NumPy:

```bash
pip install numpy
```

## Using Conda

NumPy can also be installed using Conda:

```bash
conda install numpy
```

---

# Statistical Functions in NumPy

NumPy provides several statistical functions.

Some commonly used functions are:

| NumPy Function    | Purpose                                              |
| ----------------- | ---------------------------------------------------- |
| `np.min()`        | Minimum value of the elements along a specified axis |
| `np.max()`        | Maximum value of the elements along a specified axis |
| `np.mean()`       | Mean value of the dataset                            |
| `np.median()`     | Median value of the dataset                          |
| `np.ptp()`        | Range of values along an axis                        |
| `np.std()`        | Standard deviation                                   |
| `np.var()`        | Variance                                             |
| `np.average()`    | Weighted average                                     |
| `np.percentile()` | Percentile of the data along the specified axis      |

---

# Statistics: Mean, Median and Range

NumPy provides functions for calculating common statistical measures.

## Mean

The function:

```python
np.mean()
```

computes the arithmetic mean along the specified axis.

---

## Median

The function:

```python
np.median()
```

computes the median along the specified axis.

---

## Range

The function:

```python
np.ptp()
```

computes the range along the specified axis.

`ptp` stands for **peak-to-peak**.

---

# Statistics: Standard Deviation and Variance

## Standard Deviation

Standard deviation is the square root of the average of squared deviations from the mean.

The NumPy function used for calculating standard deviation is:

```python
np.std()
```

---

## Variance

Variance is the average of squared deviations from the mean.

The NumPy function used for calculating variance is:

```python
np.var()
```

Standard deviation is the square root of variance.

---

# Statistics: Quartiles

Quartiles divide a dataset into four parts.

There are three main quartiles:

1. First quartile — Q1
2. Second quartile — Q2
3. Third quartile — Q3

## First Quartile — Q1

The first quartile is defined as the middle number between the smallest number and the median of the dataset.

---

## Second Quartile — Q2

The second quartile is the **median** of the given dataset.

```text
Q2 = Median
```

---

## Third Quartile — Q3

The third quartile is the middle number between the median and the largest value of the dataset.

---

## Quartiles Using NumPy

NumPy can be used to calculate quartiles using:

```python
np.percentile()
```

---

# Random Numbers in Python

Python defines a set of functions that are used to generate or manipulate random numbers through the `random` module.

The functions in the `random` module rely on a **pseudo-random number generator**.

---

# `random()` Function

The `random()` function generates a random floating-point number between:

```text
0.0 and 1.0
```

The generated value is generally within the half-open interval:

```text
0.0 <= value < 1.0
```

These types of functions are used in applications requiring random number generation, such as:

* Games.
* Lotteries.
* Simulations.
* Other applications requiring random values.

---

# `randint()` Function

The `randint()` function is used to generate a random integer.

It is available through Python's `random` module.

Example:

```python
random.randint(a, b)
```

This returns a random integer in the inclusive range:

```text
a <= N <= b
```

Both endpoints are included.

---

# Random Arrays

We can work with arrays and use random-number generation methods to create random arrays.

NumPy provides methods that can generate arrays containing random values.

For example, a random array can contain five random integers in a specified range.

---

# `randrange()` Function

Python provides a function named:

```python
randrange()
```

in the `random` package.

It can produce random numbers from a given range while also allowing a step value to be specified.

Example:

```python
random.randrange(start, stop, step)
```

The function can be used to randomly select integers from a range with a specified step.

---

# `random()` Function for Floating-Point Values

The `random.random()` function returns random floating-point values in the half-open interval:

```text
0.0 <= value < 1.0
```

---

# Creating Scalars in NumPy

In NumPy, a **scalar** is a single value.

It is similar to the concept of a scalar in linear algebra, where a scalar is an element of a field used to define a vector space.

An array can contain values having a particular data type.

For example, one scalar may have type:

```text
int32
```

while another scalar may have type:

```text
int64
```

---

# `np.asscalar()`

The transcript introduces the NumPy scalar conversion concept using the `asscalar` function.

The purpose is to convert an array of size one to its scalar equivalent.

The returned data type is the same type as that returned by the input.

Example concept:

```python
np.asscalar()
```

This can be used to convert an array containing a single value into a scalar representation.

---

# Creating a Vector in NumPy

A **vector** is built from components that are ordinary numbers.

A vector can be thought of as a list of numbers, with vector algebra consisting of operations performed on those numbers.

In NumPy, a vector can be represented using a one-dimensional array.

---

# Creating a Vector Using `np.array()`

To create a vector, we can use the NumPy `array()` method.

Example:

```python
import numpy as np

v = np.array([1, 2, 3, 4])
```

The list of numbers is converted into a NumPy array.

---

# NumPy Arrays

NumPy aims to provide an array object that can be significantly faster than traditional Python lists for numerical operations.

A NumPy array is a contiguous block of memory used to store data of the same type.

When the type of data to be stored is determined, the memory layout and stride information can be determined accordingly.

---

# Sorting an Array

NumPy provides functionality for sorting arrays.

The sorting operation returns a sorted copy of an array.

Example:

```python
np.sort(array)
```

This can be used to sort the values contained in an array.

---

# Broadcasting of an Array

**Broadcasting** describes how NumPy treats arrays with different shapes during arithmetic operations.

The smaller array is broadcast across the larger array so that they have compatible shapes.

Broadcasting allows arithmetic operations to be performed between arrays of compatible but different shapes.

---

# Addition of Two Vectors

Vector addition takes place in an **element-wise manner**.

This means that addition happens element by element.

For example:

```text
[1, 2, 3]
+
[4, 5, 6]
-----------
[5, 7, 9]
```

The vectors must have compatible dimensions for the operation.

### Syntax

```python
vector1 + vector2
```

A program can create two vectors and add them together using this syntax.

---

# Vector Dot Product

The **vector dot product** is performed between two vectors of the same length and returns a single value.

NumPy provides a method for performing the dot product:

```python
np.dot()
```

For example:

```python
import numpy as np

list1 = [1, 2, 3]
list2 = [4, 5, 6]

v1 = np.array(list1)
v2 = np.array(list2)

result = np.dot(v1, v2)
```

The dot product is calculated by multiplying corresponding elements and adding the results.

Conceptually:

```text
(1 × 4) + (2 × 5) + (3 × 6)
```

---

# Matrix in NumPy

A matrix in NumPy is a two-dimensional structure.

The course introduces the NumPy `matrix` class for working with matrices.

The NumPy matrix functionality can be used to convert an array-like object into a two-dimensional matrix representation.

---

# Creating a Matrix

The syntax for creating a matrix is:

```python
np.matrix(data, dtype, copy)
```

where:

* `data` represents the input data.
* `dtype` specifies the data type.
* `copy` controls whether the input data is copied.

Example:

```python
import numpy as np

matrix = np.matrix([[1, 2], [3, 4]])
```

This creates a two-dimensional matrix.

---

# Accessing Values of a Matrix

Values of a matrix can be accessed using row and column indexing.

For example:

```python
import numpy as np

matrix = np.matrix([[1, 2], [3, 4]])

print(matrix[0, 0])
```

The indexing allows individual elements of the matrix to be accessed.

---

# Matrix Multiplication Operator

The `@` symbol is known as the **matrix multiplication operator** in Python.

It can be used to perform matrix multiplication.

Example:

```python
result = matrix1 @ matrix2
```

The `@` operator performs matrix multiplication rather than ordinary element-wise multiplication.

---

# Measure of Central Tendency Using NumPy

Mathematically, **central tendency** means measuring the center or location of the values of a dataset.

It gives an idea of the average or central value of the data in a dataset and provides an indication of how the values are distributed around the center.

There are three main measures of central tendency:

1. Mean
2. Median
3. Mode

---

# Mean

The **mean** is the average value of the data.

It is calculated by dividing the sum of the values by the number of values.

Conceptually:

```text
Mean = Sum of values / Number of values
```

NumPy provides:

```python
np.mean()
```

to calculate the mean.

---

# Median

The **median** is the middle value in a distribution when the values are arranged in ascending or descending order.

NumPy provides:

```python
np.median()
```

to calculate the median.

---

# Mode

The **mode** is the most commonly occurring value in a distribution.

The three measures can therefore be summarized as:

| Measure | Meaning                       |
| ------- | ----------------------------- |
| Mean    | Average value                 |
| Median  | Middle value                  |
| Mode    | Most commonly occurring value |

---

# Median Using NumPy

The NumPy function:

```python
np.median()
```

is used to calculate the median.

Example:

```python
import numpy as np

data = np.array([10, 20, 30, 40, 50])

median = np.median(data)

print(median)
```

The function calculates the median of the array.

---

# Practical Example: Runs Scored by Sachin, Dravid and Team India

Consider a dataset consisting of runs scored by **Sachin, Dravid and Team India** across a subset of matches.

The dataset covers:

```text
15 matches
```

The objective is to analyze the dataset and answer statistical questions.

---

# Loading the Dataset

The dataset is first loaded into the Python/NumPy environment.

The data can then be divided into its individual components.

The individual components represent the relevant data for:

* Sachin.
* Dravid.
* Team India.

---

# Calculating Mean and Median

NumPy functions can be used to calculate the mean and median of the data.

The functions used are:

```python
np.mean()
```

and:

```python
np.median()
```

These functions can be applied to the data for Sachin, Dravid and Team India.

---

# Creating a Statistics Function

A function named:

```text
stats
```

can be created to calculate and return the mean and median of the data passed to it.

Conceptually, the function:

1. Receives data as input.
2. Calculates the mean.
3. Calculates the median.
4. Returns the mean and median.

The function can therefore be used to obtain the mean and median scores for:

* Sachin.
* Dravid.
* Team India.

---

# Course Summary

In this course, the following concepts were covered:

* Introduction to NumPy.
* Installation of NumPy.
* Statistical functions in NumPy.
* Mean.
* Median.
* Minimum.
* Maximum.
* Range.
* Standard deviation.
* Variance.
* Weighted average.
* Percentile.
* Quartiles.
* Random number generation.
* Scalars.
* Vectors.
* NumPy arrays.
* Sorting arrays.
* Broadcasting.
* Vector addition.
* Vector dot product.
* Matrices.
* Accessing matrix values.
* Matrix multiplication.
* Measures of central tendency.
* Practical statistical analysis using NumPy.

---

# Important NumPy Functions

| Function          | Purpose                             |
| ----------------- | ----------------------------------- |
| `np.mean()`       | Calculates the arithmetic mean      |
| `np.median()`     | Calculates the median               |
| `np.min()`        | Finds the minimum value             |
| `np.max()`        | Finds the maximum value             |
| `np.ptp()`        | Calculates the range                |
| `np.std()`        | Calculates standard deviation       |
| `np.var()`        | Calculates variance                 |
| `np.average()`    | Calculates average/weighted average |
| `np.percentile()` | Calculates percentile               |
| `np.sort()`       | Sorts an array                      |
| `np.dot()`        | Calculates dot product              |
| `np.array()`      | Creates a NumPy array               |
| `np.matrix()`     | Creates a matrix representation     |

---

# Important Concepts to Remember

## NumPy

```text
NumPy = Numerical Python
```

It is an open-source Python library designed for numerical computing and array operations.

---

## Basic Statistical Functions

```text
np.mean()
np.median()
np.min()
np.max()
np.ptp()
np.std()
np.var()
np.average()
np.percentile()
```

---

## Random Number Generation

Python's `random` module provides functions such as:

```python
random.random()
random.randint()
random.randrange()
```

---

## Vectors

Vectors can be represented using NumPy arrays:

```python
np.array([1, 2, 3])
```

Vector addition is performed element-wise.

The dot product can be calculated using:

```python
np.dot()
```

---

## Matrices

Matrices can be represented using NumPy's matrix functionality.

Matrix multiplication can be performed using:

```python
@
```

---

## Central Tendency

The three major measures are:

```text
Mean   → Average
Median → Middle value
Mode   → Most frequently occurring value
```

---

# Course Completion

Well done! You have completed the course.

After completing this course, you should now be able to:

* Understand NumPy.
* Install the NumPy module.
* Use NumPy statistical functions.
* Generate random numbers using Python.
* Create and work with NumPy arrays.
* Create scalars and vectors.
* Perform vector operations.
* Sort arrays.
* Understand broadcasting.
* Create matrices.
* Access matrix values.
* Perform matrix multiplication.
* Understand measures of central tendency.
* Calculate mean and median using NumPy.
* Apply NumPy functions to a practical dataset.

---

# Knowledge Assessment

The course concludes with a knowledge assessment.

The assessment checks your understanding of the concepts covered in the course, including:

* NumPy fundamentals.
* NumPy installation.
* Statistical functions.
* Random number generation.
* Scalars.
* Vectors.
* Vector operations.
* Arrays.
* Broadcasting.
* Matrices.
* Matrix operations.
* Measures of central tendency.

You must achieve **80%** to pass the assessment.

If you are not ready for the assessment, you can review the course material before attempting it again.

---

## Course Files

```text
Track08-Data-Analysis-Using-NumPy/
├── lecture.md
├── assessment.md
└── certificate.pdf
```
