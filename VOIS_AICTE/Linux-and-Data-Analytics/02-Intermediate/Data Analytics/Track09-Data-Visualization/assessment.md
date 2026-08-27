# VOIS Assessment — Data Visualization

## Questions and Answers

### 1. The interface of Matplotlib used for data visualization is:

* Seaborn
* Anaconda
* Matlab
* Pyplot

**Answer:** Pyplot

---

### 2. Which of the following does not support Pyplot?

* Histogram
* Boxplot
* Pie
* All are correct

**Answer:** All are correct

> **Note:** The question is somewhat ambiguously worded. Pyplot supports plotting functions for histogram, box plots, and pie charts, so none of options 1–3 is correct as a "does not support" answer. The intended answer is **All are correct**.

---

### 3. The plot used to present a statistical overview is:

* Bar
* Pie
* Histogram
* Box plot

**Answer:** Box plot

---

### 4. Matplotlib is ________ plotting library.

* 1D
* 2D
* 3D
* All of the above

**Answer:** 2D

> **Important:** Matplotlib is primarily described as a **2D plotting library**. It also has support for 3D plotting through `mpl_toolkits.mplot3d`, but the standard course/MCQ answer is **2D**.

---

### 5. The most effective real-time illustration of data visualization is:

* Percent of population by age group in India
* Google Analytics
* Solar System Drawing
* Both A and B

**Answer:** Google Analytics

> **Reason:** Google Analytics provides real-time visualization of website/app activity and user behavior. Population by age group is a data visualization, but it is not inherently real-time.

---

# Assessment Topics

The assessment is based on the following topics covered in the course:

* Data visualization fundamentals
* Matplotlib
* Pyplot
* Installing Matplotlib
* Importing `pyplot`
* Line graphs
* Plot labels and titles
* Legends
* Plot customization
* Colors
* Line styles
* Line widths
* Markers
* Bar graphs
* Horizontal bar graphs using `barh()`
* Histograms
* Scatter plots
* Pie charts
* Subplots
* Annotations
* Matplotlib axes
* Saving figures
* Multiple plots on a single canvas

---

# Important Matplotlib Concepts

## Importing Pyplot

```python
import matplotlib.pyplot as plt
```

`pyplot` provides the interface commonly used to create and customize Matplotlib plots.

---

## Basic Line Plot

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4]
y = [10, 20, 15, 25]

plt.plot(x, y)
plt.show()
```

---

## Labels and Title

```python
plt.xlabel("X Axis")
plt.ylabel("Y Axis")
plt.title("My Plot")
```

---

## Legend

```python
plt.legend()
```

A legend describes the different elements or plotted datasets in a graph.

---

## Bar Graph

```python
plt.bar(x, y)
plt.show()
```

A bar graph commonly uses categorical values on one axis.

---

## Horizontal Bar Graph

```python
plt.barh(x, y)
plt.show()
```

`barh()` creates a horizontal bar graph.

---

## Histogram

```python
plt.hist(data)
plt.show()
```

A histogram represents the **distribution of data** using intervals/bins.

---

## Scatter Plot

```python
plt.scatter(x, y)
plt.show()
```

A scatter plot represents the relationship between two variables using data points.

---

## Pie Chart

```python
plt.pie(values, labels=labels)
plt.show()
```

A pie chart represents proportions of a whole using circular slices.

---

## Subplots

Matplotlib's `subplot()` function allows multiple plots to be placed on a single canvas.

Basic syntax:

```python
plt.subplot(rows, columns, index)
```

Example:

```python
plt.subplot(1, 2, 1)
plt.plot(x, y)

plt.subplot(1, 2, 2)
plt.plot(x, y)

plt.show()
```

---

## Annotation

The `annotate()` function is used to add text and an arrow pointing to a particular location on a plot.

Example:

```python
plt.annotate("Point", xy=(2, 4), xytext=(3, 5))
```

---

# Quick Revision

| Concept              | Matplotlib Function |
| -------------------- | ------------------- |
| Line plot            | `plt.plot()`        |
| Bar graph            | `plt.bar()`         |
| Horizontal bar graph | `plt.barh()`        |
| Histogram            | `plt.hist()`        |
| Scatter plot         | `plt.scatter()`     |
| Pie chart            | `plt.pie()`         |
| Subplot              | `plt.subplot()`     |
| Title                | `plt.title()`       |
| X-axis label         | `plt.xlabel()`      |
| Y-axis label         | `plt.ylabel()`      |
| Legend               | `plt.legend()`      |
| Annotation           | `plt.annotate()`    |
| Display plot         | `plt.show()`        |
| Save figure          | `plt.savefig()`     |

---

# Key Points to Remember

* **Matplotlib** is a Python plotting library primarily used for **2D data visualization**.
* **Pyplot** is the commonly used Matplotlib interface for creating plots.
* `plt.plot()` creates line plots.
* `plt.bar()` creates bar graphs.
* `plt.barh()` creates horizontal bar graphs.
* `plt.hist()` creates histograms.
* `plt.scatter()` creates scatter plots.
* `plt.pie()` creates pie charts.
* `plt.subplot()` allows multiple plots on one canvas.
* `plt.annotate()` adds annotations to plots.
* `plt.legend()` displays plot legends.
* `plt.xlabel()` and `plt.ylabel()` label axes.
* `plt.title()` adds a title.
* `plt.show()` displays the figure.
* `plt.savefig()` saves a figure.

---
