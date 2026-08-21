# Large Language Models & Data Analytics — Day 2

**Program:** VOIS FOR TECH LD AICTE Internship Program
**Session:** Data Analytics — Day 2
**Date:** 20 August 2026
**Mode:** Live Lecture + Practical Session

---

## Table of Contents

1. [Introduction to Language Models](#1-introduction-to-language-models)
2. [What is an LLM?](#2-what-is-an-llm)
3. [How Does an LLM Learn?](#3-how-does-an-llm-learn)
4. [Understanding Parameters](#4-understanding-parameters)
5. [Parameters and Model Capability](#5-parameters-and-model-capability)
6. [SLM — Small Language Model](#6-slm--small-language-model)
7. [AI and Agriculture](#7-ai-and-agriculture)
8. [Practical — Crop Recommendation Analysis](#8-practical--crop-recommendation-analysis)
9. [Google Colab](#9-google-colab)
10. [Pandas](#10-pandas)
11. [Exploratory Data Analysis (EDA)](#17-exploratory-data-analysis--eda)
12. [Univariate / Bivariate / Multivariate Analysis](#18-univariate-analysis)
13. [Visualizations: Histograms, Bins, Bar Charts, Violin Plots](#22-histograms)
14. [Outliers](#28-outliers)
15. [Final Revision Sheet](#final-revision-sheet)

---

## 1. Introduction to Language Models

The session began with an introduction to Language Models and how modern Artificial Intelligence systems learn from data.

> A **language model** is an AI model that learns patterns from language and can use those patterns to predict or generate text.

Topics covered:

- Language Models
- Large Language Models (LLMs)
- Small Language Models (SLMs)
- Parameters
- How models learn internally

**Key idea:** An AI model does not learn in exactly the same way that a human memorizes information. Instead, the model learns patterns and relationships from training data through its internal parameters.

---

## 2. What is an LLM?

**LLM = Large Language Model**

A Large Language Model is a language model containing a very large number of learned parameters and trained on large amounts of data.

LLMs can perform tasks such as:

- Understanding text
- Generating text
- Answering questions
- Summarizing information
- Translating languages
- Generating code
- Analyzing text

**Examples of applications:** AI chatbots, coding assistants.

---

## 3. How Does an LLM Learn?

During training, the model processes large amounts of data, makes predictions, and adjusts its internal values so that future predictions improve. These internal learned values are called **parameters**.

```
Training Data
      ↓
Model processes patterns
      ↓
Predictions
      ↓
Adjust Parameters
      ↓
Better Predictions
      ↓
Learned Model
```

---

## 4. Understanding Parameters

A **parameter** is an internal value that is adjusted during the training of a machine learning model. Large language models can contain millions, billions, or even more parameters, allowing them to represent complex patterns learned from training data.

### Analogy — IQ and Training

Imagine two people learning the same concept:

- One person may understand it after a small amount of training.
- Another may require considerably more training.

Similarly, AI models have internal parameters adjusted during training to help them learn patterns.

> **More parameters → greater potential learning/model capacity**

⚠️ However, more parameters alone does not guarantee a better model. Training data, architecture, and training quality also matter.

---

## 5. Parameters and Model Capability

```
Smaller Model → Fewer Parameters → Lower Model Capacity
Larger Model  → More Parameters  → Greater Potential Capacity
```

**Core concept:** Parameters are the internal values through which the model learns and represents patterns.

---

## 6. SLM — Small Language Model

**SLM = Small Language Model** — a smaller language model designed with fewer parameters compared with large language models.

| Model Type | Meaning | General Characteristic |
|---|---|---|
| SLM | Small Language Model | Smaller and more lightweight |
| LLM | Large Language Model | Larger and more capable of handling complex patterns |

Smaller models are useful when efficiency, speed, resource requirements, or deployment constraints matter — not every application needs the largest possible model.

---

## 7. AI and Agriculture

Agriculture generates large amounts of environmental and soil data, including:

- Nitrogen, Phosphorus, Potassium
- Temperature, Humidity
- pH
- Rainfall

These factors can be analyzed to support better agricultural decisions — leading into the practical: **Crop Recommendation Analysis**.

---

## 8. Practical — Crop Recommendation Analysis

The practical focused on a Crop Recommendation Analysis dataset, analyzed in Google Colab using:

- Python
- Pandas / DataFrames
- Statistical analysis
- Data visualization
- Exploratory Data Analysis (EDA)

---

## 9. Google Colab

Google Colab is a browser-based environment for executing Python code, useful for data analytics since libraries like Pandas and visualization tools can run directly in notebooks.

```
Open Google Colab
       ↓
Load Dataset
       ↓
Import Pandas
       ↓
Create DataFrame
       ↓
Explore Dataset
       ↓
Perform EDA
       ↓
Visualize Data
       ↓
Analyze Patterns
       ↓
Identify Outliers
```

---

## 10. Pandas

**Pandas** is a Python library for data manipulation and analysis, providing the **DataFrame** structure (a table of rows and columns).

```python
import pandas as pd

df = pd.read_csv("dataset.csv")
```

- `pd` → Pandas
- `df` → DataFrame containing the dataset

### 10.1 Viewing the DataFrame

```python
df           # view full DataFrame
df.head()    # first few rows
df.tail()    # last few rows
```

### 10.2 Dataset Shape

```python
df.shape     # (rows, columns), e.g. (1000, 8)
```

### 10.3 Dataset Information

```python
df.info()
```

Shows: number of entries, column names, non-null counts, data types, memory usage.

### 10.4 Data Types

- **Numerical data** — e.g. Temperature, Humidity, Rainfall, pH
- **Categorical data** — e.g. Crop names, categories, labels

### 10.5 Statistical Summary

```python
df.describe()
```

| Statistic | Meaning |
|---|---|
| count | Number of observations |
| mean | Average |
| std | Standard deviation |
| min | Minimum value |
| 25% | First quartile |
| 50% | Median |
| 75% | Third quartile |
| max | Maximum value |

---

## 11. Exploratory Data Analysis (EDA)

**EDA** = the process of exploring and understanding a dataset before making conclusions or building models.

Goal: discover patterns, distributions, relationships, trends, unusual observations, outliers, and important variables.

```
Dataset → Understand Structure → Statistics → Visualization
        → Relationships → Outliers → Insights
```

### 11.1 Univariate Analysis (*Uni = One*)

Analyzing **one** variable at a time (e.g. Temperature: min, max, average, distribution, outliers).
**Main question:** What does this one variable look like?

### 11.2 Bivariate Analysis (*Bi = Two*)

Studies the relationship between **two** variables (e.g. Temperature ↕ Humidity, Rainfall ↕ Crop).
**Main question:** How are these two variables related?

### 11.3 Multivariate Analysis (*Multi = Many*)

Analyzing **multiple** variables together (e.g. Nitrogen, Phosphorus, Potassium, Temperature, Humidity, pH, Rainfall → Crop Recommendation).
**Main question:** How do multiple variables interact or relate to the outcome?

### 11.4 Summary Table

| Analysis | Number of Variables | Main Question |
|---|---|---|
| Univariate | 1 | What does this variable look like? |
| Bivariate | 2 | How are these two variables related? |
| Multivariate | 3+ | How do multiple variables interact? |

**Easy way to remember:** Uni → One, Bi → Two, Multi → Many

---

## 12. Visualization Techniques

### 12.1 Histograms

Represents numerical values grouped into ranges called **bins**, showing how many observations fall into each range.

### 12.2 Bins

A **bin** is a range/interval used to group numerical values in a histogram.

Example data: `12, 14, 16, 18, 21, 22, 24, 27, 29`

```
10–15    ███
15–20    ██
20–25    ███
25–30    ███
```

**Number of bins effect:**

| Fewer Bins | More Bins |
|---|---|
| Large ranges | Smaller ranges |
| Simpler visualization | More detail |
| Less detail | Potentially more noise |

### 12.3 Bar Chart vs Histogram

| | Bar Chart | Histogram |
|---|---|---|
| Data | Mainly categorical | Numerical |
| X-axis | Categories | Numerical intervals/bins |
| Purpose | Compare categories | Show distribution |
| Bars | Usually separated by gaps | Normally touch |
| Example | Crop names | Temperature ranges |

**Bar Chart example:**
```
Rice     ███████
Wheat    █████
Maize    ███
```

**Histogram example:**
```
10–15   ███
15–20   █████
20–25   ███████
25–30   ████
```

### 12.4 Data Distribution

A **distribution** shows how a variable's values are spread across its possible range — useful for identifying where observations are concentrated and revealing extreme values. Examined for: Temperature, Humidity, Rainfall, pH, nutrient values.

### 12.5 Violin Plot

Combines distribution information with a box-plot-like summary, showing distribution, spread, density, central region, and potential unusual observations. Wider sections = more concentrated observations.

```
      ╭──╮
     ╭╯  ╰╮
    ╭╯    ╰╮
    │      │
    ╰╮    ╭╯
     ╰╮  ╭╯
      ╰──╯
```

**Why useful:** A box plot gives a compact summary, while a violin plot adds information about shape and density.

### 12.6 Visualization Use Cases

| Visualization | Useful For |
|---|---|
| Bar Chart | Comparing categories |
| Histogram | Numerical distribution |
| Violin Plot | Distribution and density |
| Box Plot | Spread and potential outliers |

---

## 13. Outliers

An **outlier** is a value unusually far from the general pattern of observations.

**During the crop recommendation analysis**, potential outliers were identified in:
- Temperature
- Humidity

### 13.1 Why Outliers Matter

Outliers can influence:
- Mean
- Range
- Standard deviation
- Distribution
- Visualization

⚠️ An outlier does **not** automatically mean the data is wrong — it may represent a genuine environmental condition. Outliers should be investigated before deciding what to do with them.

### 13.2 Outlier Detection Process

```
Analyze Temperature → Visualize Distribution → Identify Potential Outliers
Analyze Humidity     → Visualize Distribution → Identify Potential Outliers
```

---

## 14. Overall EDA Workflow

```
Load Dataset → Create DataFrame → Inspect Data
     → df.head() → df.shape → df.info() → df.describe()
     → Understand Data Types → EDA
     → Univariate → Bivariate → Multivariate
     → Visualization
     → Histograms/Bins → Bar Charts → Violin Plots
     → Outlier Analysis (Temperature & Humidity)
     → Interpret Insights
```

---

## 15. AI/ML and Agriculture

```
Soil/Nutrient Conditions + Temperature + Humidity + pH + Rainfall
                              ↓
                  Crop Recommendation Analysis
```

This shows how data analytics and machine learning can be applied to real-world domains such as agriculture.

---

## 16. Key Pandas Commands Reference

```python
import pandas as pd

df = pd.read_csv("dataset.csv")

df              # view DataFrame
df.head()       # first rows
df.tail()       # last rows
df.shape        # (rows, columns)
df.info()       # structure & data types
df.describe()   # statistical summary
```

---

## Quick Revision

### EDA
```
EDA → Understand the Dataset → Check Structure → Check Statistics
    → Visualize Data → Find Patterns → Find Relationships
    → Identify Outliers → Generate Insights
```

### Analysis Types
- **Univariate** → One variable → Analyze individual distribution
- **Bivariate** → Two variables → Analyze relationships
- **Multivariate** → Multiple variables → Analyze complex relationships

### Visualization
- **Bar Chart** → Categorical comparison
- **Histogram** → Numerical distribution
- **Bins** → Numerical ranges in a histogram
- **Violin Plot** → Distribution + density
- **Box Plot** → Spread + potential outliers

### LLM Concepts

```
Language Model → Learns patterns from data
              → Parameters are adjusted during training
              → Learned parameters represent patterns
              → Model can make predictions / generate output
```

- **LLM** — Large Language Model
- **SLM** — Small Language Model
- **Parameter** — An internal value adjusted during model training to help the model learn patterns

### LLM vs SLM

| Feature | SLM | LLM |
|---|---|---|
| Full Form | Small Language Model | Large Language Model |
| Model Size | Smaller | Larger |
| Parameters | Fewer | More |
| Resource Requirement | Generally lower | Generally higher |
| Use | Lightweight/specific applications | More complex language tasks |

**Key idea:** Model size and parameters relate to potential capacity, but more parameters alone do not guarantee better performance.

---

## Final Session Takeaways

- **Language Models** learn patterns from data and use those patterns to generate or predict language.
- **Parameters** are internal values adjusted during training that allow a model to learn patterns.
- **SLMs** provide a more lightweight alternative to large models.
- **Data Analytics** requires understanding the dataset before drawing conclusions.
- **Pandas** provides powerful tools for inspecting and analyzing structured data.
- **EDA** helps discover patterns, distributions, relationships, and unusual observations.
- **Visualization** — different charts suit different data types and questions.
- **Outliers** should be investigated rather than automatically removed.
- **Agriculture** — data analytics can support crop recommendation and decision-making.

---

## Final Revision Sheet

| Topic | Remember |
|---|---|
| Language Model | Learns patterns from language data |
| LLM | Large Language Model |
| SLM | Small Language Model |
| Parameter | Internal value adjusted during training |
| Model Capacity | Ability to represent complex patterns |
| Crop Recommendation | Practical agricultural data-analysis task |
| Pandas | Python library for data analysis |
| DataFrame | Table-like data structure |
| `df` | DataFrame containing the dataset |
| `df.head()` | First rows |
| `df.tail()` | Last rows |
| `df.shape` | Rows and columns |
| `df.info()` | Dataset structure and data types |
| `df.describe()` | Statistical summary |
| EDA | Exploratory Data Analysis |
| Univariate | One variable |
| Bivariate | Two variables |
| Multivariate | Multiple variables |
| Bar Chart | Categorical comparison |
| Histogram | Numerical distribution |
| Bin | Numerical range in a histogram |
| Violin Plot | Distribution and density |
| Outlier | Unusually distant observation |
| Temperature | Outliers identified/analyzed |
| Humidity | Outliers identified/analyzed |

---

## Complete Practical Flow

```
                    CROP RECOMMENDATION ANALYSIS
                              │
                              ↓
                       Google Colab
                              │
                              ↓
                           Pandas
                              │
                              ↓
                         DataFrame
                              │
               ┌──────────────┼──────────────┐
               ↓              ↓              ↓
           df.shape       df.info()     df.describe()
               │              │              │
               └──────────────┼──────────────┘
                              ↓
                     Understand Dataset
                              ↓
                  Exploratory Data Analysis
                              │
             ┌────────────────┼────────────────┐
             ↓                ↓                ↓
        Univariate         Bivariate       Multivariate
             │                │                │
             └────────────────┼────────────────┘
                              ↓
                       Data Visualization
                              │
             ┌────────────────┼─────────────────┐
             ↓                ↓                 ↓
          Bar Chart        Histogram        Violin Plot
                              │
                              ↓
                            Bins
                              │
                              ↓
                       Distribution Analysis
                              ↓
                        Outlier Detection
                              │
                    ┌─────────┴─────────┐
                    ↓                   ↓
               Temperature          Humidity
                    │                   │
                    └─────────┬─────────┘
                              ↓
                       Interpret Insights
                              ↓
                    Crop Recommendation
```
