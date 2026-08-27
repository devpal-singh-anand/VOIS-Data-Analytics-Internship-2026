# VOIS FOR TECH — Data Visualization

## Learning Objectives

The learning objective is to gain knowledge on:

At the end of this course, students will be able to:

* Learn the fundamentals of Python's **Matplotlib** library and its main features.
* Understand how to customize objects in Matplotlib.
* Understand how to create multiple plots in Matplotlib.
* Learn how to customize plots using annotations, labels, line styles, colors, and other attributes.
* Understand the different plot types available in the Matplotlib library.
* Understand how to communicate data-analysis results using visualizations.

---

# About the Course

This course guides students through techniques used to visualize data using the **Matplotlib** Python library.

The course explores:

* Main functionalities of Matplotlib.
* Customizing Matplotlib objects.
* Different plotting techniques.
* Multiple plots on a single canvas.
* Plot labels and titles.
* Line styles and colors.
* Bar graphs.
* Histograms.
* Scatter plots.
* Pie charts.
* Subplots.
* Annotations.
* Legends.
* Communicating analytical results through visualizations.

---

# Prerequisites

Basic knowledge of Python is required to start this course.

---

# What is Data Visualization?

**Data visualization** is the graphical representation of information and data.

It can be achieved using visual elements such as:

* Figures.
* Charts.
* Graphs.
* Maps.
* Other visual representations.

Data visualization tools provide a way to present figures and graphs.

When analyzing massive amounts of information, it is often essential to make **data-driven decisions**.

Data visualization helps convert complex data into an easy-to-understand representation.

---

# Matplotlib

**Matplotlib** is one of the most powerful tools for data visualization in Python.

It is an incredibly powerful and flexible plotting library.

Matplotlib:

* Is easy to use.
* Provides a large number of examples.
* Can be used to solve many different visualization problems.
* Provides several types of plots.
* Allows plots to be customized and manipulated.

To use Matplotlib in a Python script, the Matplotlib library needs to be imported.

A common import is:

```python
import matplotlib.pyplot as plt
```

The `pyplot` module is commonly imported using the alias:

```python
plt
```

If Matplotlib is not installed, it can be installed using the appropriate Python package-management command.

---

# Pyplot

`pyplot` is a collection of command-style functions that make Matplotlib work similarly to MATLAB in Python.

Each `pyplot` function makes some change to a figure.

Using Matplotlib, you can:

* Create plots.
* Edit plots.
* Modify plots.
* Manipulate plot attributes.
* Add labels.
* Add titles.
* Add legends.
* Customize colors and styles.

Matplotlib is built on NumPy and is designed to work with the broader Python scientific-computing ecosystem.

---

# Types of Matplotlib Plots

Using Matplotlib, you can generate several types of visualizations, including:

* Line graphs.
* Bar charts.
* Histograms.
* Pie charts.
* Scatter plots.
* Other graphical representations.

---

# Line Graphs

Line charts are used to represent the relationship between two variables, generally represented using the **x-axis** and **y-axis**.

To create a line graph, first import `pyplot`:

```python
import matplotlib.pyplot as plt
```

Then define the x and y values.

Example:

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]

plt.plot(x, y)
plt.show()
```

The x and y vectors are passed as arguments to the `plot()` function.

The `show()` function displays the generated plot.

---

# Plotting a Single Vector

If a single vector is passed to the `plot()` method, Matplotlib treats it as the y-axis values.

The x-axis values are generated automatically.

Example:

```python
import matplotlib.pyplot as plt

values = [1, 4, 9, 16, 25]

plt.plot(values)
plt.show()
```

Here, the supplied values are treated as response/y values, while x-axis values are generated automatically.

---

# Plot Labels

Labels can be added to the axes using:

```python
plt.xlabel()
plt.ylabel()
```

Example:

```python
plt.xlabel("X Values")
plt.ylabel("Y Values")
```

The `ylabel()` method adds a label to the y-axis.

Similarly, `xlabel()` adds a label to the x-axis.

---

# Plot Title

A title can be added to a plot using:

```python
plt.title()
```

Example:

```python
plt.title("Sample Line Graph")
```

---

# Saving a Figure

A generated figure can be saved in the required format using:

```python
plt.savefig()
```

Example:

```python
plt.savefig("graph.png")
```

---

# Legend

A **legend** is used to identify different plots or data series displayed on a graph.

A legend can be added using:

```python
plt.legend()
```

Example:

```python
plt.plot(x, y, label="Data")
plt.legend()
```

The legend provides information about the different lines or data series in the plot.

---

# Clearing Plots

The `cla()` method can be used to clear the current axes.

Matplotlib provides functions that can be used to manipulate plots and axes.

---

# Example: Line Graph

Consider two lists containing x-axis and y-axis values.

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [10, 20, 15, 30, 25]

plt.plot(x, y)

plt.xlabel("X Values")
plt.ylabel("Y Values")
plt.title("Line Graph")

plt.show()
```

The x and y values are passed to `plot()`.

The axis labels describe the attributes represented by the axes.

The `title()` function provides a title.

The `show()` function displays the graph.

---

# Plotting Two Lines

Multiple lines can be plotted on the same graph.

Example:

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]

y1 = [1, 4, 9, 16, 25]
y2 = [1, 8, 27, 64, 125]

plt.plot(x, y1, label="Line 1")
plt.plot(x, y2, label="Line 2")

plt.legend()
plt.show()
```

The two lines are differentiated using their labels.

The rectangular box identifying the different lines and their associated information is called the **legend**.

---

# Customizing Plots

Plots can be customized using several attributes.

First import the `pyplot` module:

```python
import matplotlib.pyplot as plt
```

Then define the x and y values.

The size of the x and y data should be compatible when plotting corresponding coordinate values.

The values are passed to the `plot()` method.

Several attributes can be customized, including:

* Color.
* Line style.
* Line width.
* Marker.
* Marker face color.
* Marker size.

Example:

```python
plt.plot(
    x,
    y,
    color="red",
    linestyle="--",
    linewidth=2,
    marker="o",
    markersize=5
)
```

Matplotlib documentation can be used to identify and configure the available plotting attributes.

---

# Bar Graphs

A **bar graph** is another visualization technique available in Matplotlib.

The main difference between a bar graph and a line plot is that the x-axis in a bar graph is generally **categorical** rather than numerical.

The y-axis can contain numerical values.

To create a bar graph, use:

```python
plt.bar()
```

Example:

```python
import matplotlib.pyplot as plt

categories = ["A", "B", "C", "D"]
values = [10, 20, 15, 25]

plt.bar(categories, values)

plt.show()
```

The generated graph can be displayed using:

```python
plt.show()
```

The color of the bars can also be customized.

Example:

```python
plt.bar(categories, values, color="blue")
```

---

# Horizontal Bar Graph

A bar graph can also be displayed horizontally.

For a horizontal bar graph, use:

```python
plt.barh()
```

Example:

```python
import matplotlib.pyplot as plt

categories = ["A", "B", "C", "D"]
values = [10, 20, 15, 25]

plt.barh(categories, values)

plt.show()
```

In this case:

* The categorical variable is represented on the y-axis.
* The numerical variable is represented on the x-axis.

The orientation of the graph can therefore be changed depending on the problem scenario.

---

# Histogram

A **histogram** is a graphical representation of the distribution of data.

A histogram is represented by a set of adjacent rectangles.

Each bar represents the frequency of observations within a range.

The repetition of values in statistical data is known as **frequency**.

Frequency can be represented using a frequency distribution.

---

# Creating a Histogram

The Matplotlib function used to create a histogram is:

```python
plt.hist()
```

Example:

```python
import matplotlib.pyplot as plt

ages = [18, 20, 21, 22, 22, 23, 25, 26, 28, 30]

plt.hist(ages)

plt.show()
```

The data is passed to the `hist()` method.

The generated histogram can be displayed using:

```python
plt.show()
```

---

# Histogram Bins

The `bins` parameter allows the user to customize the number or boundaries of intervals in a histogram.

Example:

```python
plt.hist(ages, bins=5)
```

The number of bins affects how the distribution is divided and displayed.

---

# Histogram Transparency

The `alpha` parameter can be used to control the transparency of the histogram.

Example:

```python
plt.hist(ages, bins=5, alpha=0.5)
```

The `alpha` parameter controls the level of transparency of the plotted data.

---

# Scatter Plots

**Scatter plots** represent the relationship between two variables in a dataset.

They represent data points on a two-dimensional plane.

The:

* Independent variable or attribute is plotted on the **x-axis**.
* Dependent variable is plotted on the **y-axis**.

Scatter plots are also called:

* Scatter graphs.
* Scatter diagrams.

---

# Uses of Scatter Plots

Scatter plots can be used in situations such as:

* Working with numerical data.
* Representing multiple values of a dependent variable for a unique value of an independent variable.
* Determining relationships between variables.
* Identifying potential root causes of problems.
* Checking whether two apparently related products or variables actually have a relationship.

---

# Creating a Scatter Plot

The Matplotlib function used to create a scatter plot is:

```python
plt.scatter()
```

Example:

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [2, 4, 5, 8, 10]

plt.scatter(x, y)

plt.show()
```

The x and y coordinate values are passed to the `scatter()` method.

---

# Customizing Scatter Plots

The size of scatter-plot points can be controlled using the `s` parameter.

Example:

```python
plt.scatter(x, y, s=100)
```

The color can also be customized:

```python
plt.scatter(x, y, color="red")
```

Other attributes can be used to customize scatter plots.

These include:

* Marker style.
* Marker size.
* Labels.
* Colors.

Example:

```python
plt.scatter(
    x,
    y,
    marker="o",
    s=100,
    label="Data"
)

plt.legend()
plt.show()
```

Axis labels can also be added using:

```python
plt.xlabel("X Values")
plt.ylabel("Y Values")
```

---

# Pie Chart

A **pie chart** is a pictorial representation of data in the form of a circular chart.

The slices of the pie show the relative size or proportion of the data.

A list of numerical variables together with categorical variables can be used to represent data in a pie chart.

---

# Creating a Pie Chart

The Matplotlib function used to create a pie chart is:

```python
plt.pie()
```

Example:

```python
import matplotlib.pyplot as plt

activities = ["Sleeping", "Working", "Eating", "Exercise"]
slices = [8, 8, 3, 1]

plt.pie(slices, labels=activities)

plt.show()
```

The variables used in a pie chart can include:

* Activities/categories.
* Slice values.
* Labels.
* Colors.

---

# Pie Chart Colors

Colors can be specified using a list.

Example:

```python
colors = ["red", "blue", "green", "yellow"]

plt.pie(
    slices,
    labels=activities,
    colors=colors
)
```

---

# Pie Chart Starting Angle

The starting angle of the pie chart can be customized using:

```python
startangle
```

Example:

```python
plt.pie(
    slices,
    labels=activities,
    startangle=90
)
```

---

# Pie Chart Radius

The radius of a pie chart can be customized using:

```python
radius
```

Example:

```python
plt.pie(
    slices,
    labels=activities,
    radius=1.2
)
```

---

# Exploding Pie Chart Slices

The `explode` parameter can be used to offset selected slices from the center of the pie chart.

Example:

```python
explode = (0.1, 0, 0, 0)

plt.pie(
    slices,
    labels=activities,
    explode=explode
)
```

This can be used to emphasize a particular category.

---

# Pie Chart Legend

A legend can be added to a pie chart using:

```python
plt.legend()
```

Example:

```python
plt.pie(
    slices,
    labels=activities
)

plt.legend()
plt.show()
```

---

# Subplots

**Subplots** are a group of smaller axes where each axis contains a separate plot.

A figure can be thought of as a canvas that contains multiple plots.

Matplotlib provides the:

```python
plt.subplot()
```

function for creating multiple plots on a single canvas.

---

# Subplot Layout

The `subplot()` function takes three arguments:

```python
plt.subplot(rows, columns, index)
```

The first argument represents:

```text
Number of rows
```

The second argument represents:

```text
Number of columns
```

The third argument represents:

```text
Index of the current plot
```

---

# Example of Subplots

A canvas can be divided into two sections:

```python
plt.subplot(1, 2, 1)
```

This creates the first plot in a layout containing:

```text
1 row × 2 columns
```

The second plot can be created using:

```python
plt.subplot(1, 2, 2)
```

Complete example:

```python
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(0, 5, 11)

y = x ** 2

plt.subplot(1, 2, 1)
plt.plot(x, y)

plt.subplot(1, 2, 2)
plt.plot(x, y)

plt.show()
```

The resulting figure contains two plots on the same canvas.

---

# `linspace()` with Subplots

The `numpy.linspace()` function can be used to generate evenly spaced values.

Example:

```python
import numpy as np

x = np.linspace(0, 5, 11)
```

This generates **11 equally spaced values** in the range from `0` to `5`.

These values can be used as input values for mathematical functions.

For example:

```python
y = x ** 2
```

creates a quadratic relationship between `x` and `y`.

---

# Plot Labels in Subplots

Each subplot can have its own:

* X-axis label.
* Y-axis label.
* Title.

Example:

```python
plt.subplot(1, 2, 1)

plt.plot(x, y)
plt.xlabel("X")
plt.ylabel("Y")
plt.title("First Plot")

plt.subplot(1, 2, 2)

plt.plot(x, y)
plt.xlabel("X")
plt.ylabel("Y")
plt.title("Second Plot")

plt.show()
```

---

# Annotation

The `annotate()` function in the `pyplot` module, or the `annotate()` method of the Axes class, is used to add explanatory text to a plot.

An annotation can include an arrow connecting the text to a particular point.

The annotation identifies a point using coordinate information.

---

# Basic Annotation

Example:

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [1, 4, 9, 16, 25]

plt.plot(x, y)

plt.annotate(
    "Important Point",
    xy=(3, 9),
    xytext=(4, 12),
    arrowprops=dict(arrowstyle="->")
)

plt.show()
```

The:

```text
xy
```

attribute represents the location of the point being annotated.

The:

```text
xytext
```

attribute represents the location where the annotation text is placed.

The annotation can therefore connect explanatory text with a particular point on the graph.

---

# Annotation with Mathematical Data

NumPy can be used to generate data for an annotated graph.

Example:

```python
import numpy as np
import matplotlib.pyplot as plt

x = np.arange(0, 5, 0.1)
y = x ** 2

plt.plot(x, y)

plt.title("Quadratic Function")
plt.xlabel("X")
plt.ylabel("Y")

plt.annotate(
    "Point",
    xy=(2, 4),
    xytext=(3, 8),
    arrowprops=dict(arrowstyle="->")
)

plt.show()
```

The plot title and axis labels are added using the corresponding Matplotlib functions.

---

# Legends with Annotations

A **legend** is an area describing the elements of a graph.

Matplotlib provides:

```python
plt.legend()
```

to place a legend on the axes.

The `loc` parameter can be used to specify the location of the legend.

---

# Legend Location

Common legend locations include:

```text
upper left
upper right
lower left
lower right
```

Example:

```python
plt.legend(loc="lower right")
```

This places the legend in the lower-right corner of the axes.

---

# Multiple Plots with Legends and Annotations

Multiple mathematical functions can be plotted on the same canvas.

Example:

```python
import numpy as np
import matplotlib.pyplot as plt

x = np.linspace(0, 5, 100)

y1 = x ** 2
y2 = x ** 3

plt.plot(x, y1, label="Quadratic")
plt.plot(x, y2, label="Cubic")

plt.annotate(
    "Quadratic",
    xy=(2, 4),
    xytext=(2.5, 10),
    arrowprops=dict(arrowstyle="->")
)

plt.annotate(
    "Cubic",
    xy=(2, 8),
    xytext=(3, 20),
    arrowprops=dict(arrowstyle="->")
)

plt.xlabel("X")
plt.ylabel("Y")
plt.legend(loc="lower right")

plt.show()
```

The legend identifies the different plotted functions.

Annotations provide additional information at selected locations.

---

# Communicating Results Using Visualization

Data visualization helps communicate analytical results by converting numerical information into graphical representations.

Different plots can be selected according to the type of data and the objective of the analysis.

For example:

| Plot Type    | Typical Use                                  |
| ------------ | -------------------------------------------- |
| Line Graph   | Relationship or trend between variables      |
| Bar Graph    | Comparison of categorical values             |
| Histogram    | Distribution and frequency of numerical data |
| Scatter Plot | Relationship between two numerical variables |
| Pie Chart    | Proportions or composition                   |
| Subplots     | Multiple visualizations on one canvas        |

---

# Important Matplotlib Functions

| Function         | Purpose                             |
| ---------------- | ----------------------------------- |
| `plt.plot()`     | Create line plots                   |
| `plt.bar()`      | Create vertical bar graphs          |
| `plt.barh()`     | Create horizontal bar graphs        |
| `plt.hist()`     | Create histograms                   |
| `plt.scatter()`  | Create scatter plots                |
| `plt.pie()`      | Create pie charts                   |
| `plt.subplot()`  | Create multiple plots on one canvas |
| `plt.xlabel()`   | Add x-axis label                    |
| `plt.ylabel()`   | Add y-axis label                    |
| `plt.title()`    | Add plot title                      |
| `plt.legend()`   | Add a legend                        |
| `plt.annotate()` | Add annotations                     |
| `plt.savefig()`  | Save a figure                       |
| `plt.show()`     | Display a figure                    |

---

# Important Plot Customization Attributes

Common Matplotlib plot attributes include:

```text
color
linestyle
linewidth
marker
markersize
markerfacecolor
label
alpha
bins
startangle
radius
explode
loc
```

These attributes allow a plot to be customized according to the visualization requirements.

---

# Complete Visualization Workflow

A basic Matplotlib workflow is:

```text
Import Matplotlib
       ↓
Prepare Data
       ↓
Select Plot Type
       ↓
Pass Data to Plot Function
       ↓
Customize Plot
       ↓
Add Labels / Title / Legend
       ↓
Add Annotations if Required
       ↓
Display or Save Figure
```

Example:

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]

plt.plot(x, y, label="Data")

plt.xlabel("X")
plt.ylabel("Y")
plt.title("Data Visualization")

plt.legend()
plt.show()
```

---

# Course Completion

After completing this course, you should now be able to:

* Understand how to install and use Matplotlib.
* Understand the `pyplot` module.
* Call and pass parameters to the `plot()` method.
* Place axis labels and titles.
* Save figures using Matplotlib methods.
* Customize plots using colors, line styles, line widths, and markers.
* Create multiple plots on a single canvas.
* Create bar graphs using Matplotlib.
* Create horizontal bar graphs using `barh()`.
* Create histograms using the `hist()` method.
* Customize histograms using bins and transparency.
* Create scatter plots using numerical coordinate pairs.
* Customize scatter plots using markers, sizes, labels, and colors.
* Create pie charts.
* Customize pie charts using labels, colors, starting angle, radius, and explode parameters.
* Use the `subplot()` method to place different figures on a single canvas.
* Use `annotate()` to add explanatory text to plots.
* Use legends to identify different plotted data.
* Understand how visualization can help communicate data-analysis results.

---

# Knowledge Assessment

The course concludes with a knowledge assessment covering:

* Data visualization fundamentals.
* Matplotlib.
* Pyplot.
* Line graphs.
* Plot labels and titles.
* Plot customization.
* Bar graphs.
* Horizontal bar graphs.
* Histograms.
* Scatter plots.
* Pie charts.
* Subplots.
* Annotations.
* Legends.
* Communicating data-analysis results.

You must achieve **80%** to pass the assessment.

If you are not ready for the assessment, you can review the course material and attempt the assessment again.

---

## Course Files

```text
Track09-Data-Visualization/
├── lecture.md
├── assessment.md
└── certificate.pdf
```
