# Unicorn Companies Dataset & Major Project Briefing — Day 4

**Date:** 3 September 2026<br>
**Program:** VOIS FOR TECH AICTE Internship Program<br>
**Session:** Data Analytics — Day 4<br>
**Mode:** Live Lecture + Practical Session + Major Project Briefing

---

## 1. Introduction

The fourth technical session moved into a new practical dataset — **Unicorn Companies** — covering dataset cleaning, univariate, bivariate and multivariate analysis.

The session then transitioned into a full briefing on the **Major Project**: Seasonal Agriculture Performance Analysis, including the problem statement, objectives, deliverables and deadline.

### Main topics covered

* Unicorn companies dataset
* Dataset exploration and cleaning
* Missing value handling
* Converting valuation/funding to numeric values
* Univariate, bivariate and multivariate analysis
* Major Project introduction and briefing

---

## 2. Unicorn Companies Dataset

**File:** `unicorn companies.xlsx`

The dataset contains information about high-value startup companies.

A startup is generally called a **unicorn** once its valuation reaches **$1 billion or more**.

### Clarification on valuation tiers

* $1B to below $5B → unicorn
* $5B and above → still unicorn
* $10B+ → commonly referred to as a **decacorn**

> **Unicorn = startup valued at at least $1 billion.**

---

## 3. Initial Dataset Exploration

### Libraries imported

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```

### Loading the dataset

The dataset was loaded from the Excel file into a Pandas DataFrame.

### First and last rows

```python
df.head()
df.tail()
```

### Shape

```python
df.shape
```

Used to identify the number of rows and columns.

### Column names

```python
df.columns
```

Used to inspect the available variables.

### Dataset information

```python
df.info()
```

Used to inspect:

* Number of entries
* Column names
* Data types
* Non-null counts
* Memory usage

### Statistical summary

```python
df.describe()
```

Used to obtain statistical summaries (count, mean, standard deviation, minimum, quartiles, maximum) for numeric columns.

---

## 4. Missing Value Analysis

Missing values were checked using:

```python
df.isnull().sum()
```

Null values were found in the categorical `city` column, and were filled using:

```python
df['city'] = df['city'].fillna('Unknown')
```

---

## 5. Converting Valuation to Numeric Values

The `valuation` column was stored as an object/string (e.g. `$5B`, `$750M`), and needed to be converted to plain numbers.

The requirement was to convert values **dynamically**, without depending on a particular currency symbol (`$`, `₹`, `€`, etc.).

### Examples

* `$5B` → `5000000000`
* `$2.5B` → `2500000000`
* `$750M` → `750000000`
* `$100K` → `100000`

### Conversion function

```python
import re

def convert_valuation(value):
    value = str(value).strip().upper()

    # Extract number and B/M/K
    match = re.search(r'(\d+(?:\.\d+)?)\s*([BMK]?)', value)

    if not match:
        return None

    number = float(match.group(1))
    unit = match.group(2)

    multiplier = {
        'B': 1_000_000_000,
        'M': 1_000_000,
        'K': 1_000
    }

    return number * multiplier.get(unit, 1)
```

### Applying the conversion

```python
df['valuation'] = df['valuation'].apply(convert_valuation)
```

---

## 6. Converting Funding to Numeric Values

The same conversion function was reused for the `funding` column:

```python
df['funding'] = df['funding'].apply(convert_valuation)
```

The `.apply()` method applies a custom function to every value in a Pandas column.

---

## 7. Rechecking Data After Conversion

Missing values and structure were re-verified after cleaning:

```python
df.isnull().sum()
df.info()
```

---

## 8. Univariate Analysis

**Univariate analysis** means analyzing one variable at a time.

Remaining null rows were removed:

```python
df = df.dropna()
```

### Example distribution plot

```python
sns.histplot(df['valuation'], kde=True)
plt.show()
```

---

## 9. Histogram Bins

A question was discussed about why bins are required in a histogram.

Bins divide continuous numerical data into intervals/ranges, and the histogram shows how many observations fall within each interval.

```python
sns.histplot(df['valuation'], bins=10, kde=True)
plt.show()
```

### Interpretation

* Too few bins → distribution may be oversimplified.
* Too many bins → plot may become noisy.
* A suitable number of bins helps reveal the distribution more clearly.

---

## 10. Bivariate Analysis

**Bivariate analysis** studies two variables together to understand their relationship or association.

### Funding vs Valuation

**Client-style question:** Does the amount of funding a startup receives have a relationship with its valuation?

```python
sns.scatterplot(data=df, x='funding', y='valuation')

plt.xlabel('Funding')
plt.ylabel('Valuation')
plt.title('Funding vs Valuation')

plt.show()
```

### Valuation by Industry

**Question:** Which industries have the highest-valued unicorn companies? / How does average valuation vary across industries?

```python
avg_valuation = df.groupby('industry')['valuation'].mean().sort_values(ascending=False)

sns.barplot(x=avg_valuation.index, y=avg_valuation.values)

plt.xlabel('Industry')
plt.ylabel('Average Valuation')
plt.title('Average Unicorn Valuation by Industry')

plt.xticks(rotation=45)
plt.show()
```

This is bivariate because it involves one categorical variable (industry) and one numerical variable (valuation).

---

## 11. Multivariate Analysis

**Multivariate analysis** involves examining three or more variables together.

**Question:** How do funding, valuation, and industry together relate to unicorn company valuation?

### Preferred graph — Funding vs Valuation by Industry

* X-axis → Funding
* Y-axis → Valuation
* Hue/color → Industry
* Each point → one unicorn company

```python
sns.scatterplot(
    data=df,
    x='funding',
    y='valuation',
    hue='industry'
)

plt.xlabel('Funding')
plt.ylabel('Valuation')
plt.title('Funding vs Valuation by Industry')

plt.show()
```

This combines funding, valuation and industry into a single multivariate view.

---

## 12. Major Project Briefing

**Official project:** VOIS AICTE Batch 1 2026–2027

### Major Project Title

> **Seasonal Agriculture Performance Analysis**

---

## 13. Major Project — Introduction to Dataset

The project dataset represents agricultural activities carried out across:

* Different seasons
* Geographical areas
* Farming conditions

It contains information related to:

* Farming practices
* Environmental conditions
* Crop production
* Resource usage
* Economic performance

The dataset provides an opportunity to explore how agricultural performance changes across seasons and identify meaningful patterns and differences.

---

## 14. Major Project — Problem Statement

Agricultural activities are influenced by seasonal variations, environmental conditions, farming practices, resource availability and market conditions — so agricultural performance may differ from one season to another.

Raw agricultural data does not clearly explain how performance changes across seasons or what patterns exist within different seasonal conditions.

**Problem:** Analyze the given agricultural dataset and investigate seasonal differences in agricultural performance by identifying meaningful patterns, trends, relationships, variations and differences within the available data.

---

## 15. Importance of the Problem

Understanding seasonal patterns through Data Analytics can help stakeholders:

* Understand variations in agricultural performance
* Identify important seasonal trends
* Compare performance across different periods
* Understand changing environmental conditions
* Examine differences in resource usage
* Identify areas requiring further investigation
* Support evidence-based agricultural planning

For students, this provides a focused real-world Data Analytics problem rather than a generic analysis of the entire dataset.

---

## 16. Major Project — Objective

> **To analyze agricultural data from different seasons and identify meaningful patterns, trends, relationships and differences in agricultural performance.**

Students should independently:

* Explore and understand the dataset
* Clean and prepare the data
* Examine agricultural performance across seasons
* Identify important seasonal patterns and trends
* Investigate relationships between seasonal conditions and agricultural outcomes
* Compare relevant groups within different seasons
* Identify significant differences or unusual patterns
* Apply appropriate statistical and visualization techniques
* Interpret findings based on evidence
* Develop meaningful conclusions
* Provide data-driven recommendations

---

## 17. Expected Outcomes

* Understanding of seasonal agricultural data
* Appropriate data cleaning and preparation
* Identification of important seasonal patterns
* Comparison of agricultural performance across seasons
* Discovery of relationships and variations
* Appropriate selection of analytical and visualization techniques
* Correct interpretation of findings
* Identification of significant observations
* Evidence-based insights
* Appropriate recommendations
* Complete analysis documented in a Jupyter Notebook

---

## 18. Suggested Key Questions

The official project asks students to develop their own specific analytical questions after exploring the dataset. Possible areas include:

* How does agricultural performance vary across seasons?
* What major seasonal patterns can be observed?
* Which characteristics change between seasons?
* What differences exist between agricultural activities in different seasons?
* Are there noticeable variations in resource usage across seasons?
* Are there relationships between seasonal environmental conditions and agricultural performance?
* How do economic outcomes vary across seasons?
* Are some seasonal patterns consistent across different regions or categories?
* Are there unusual or unexpected seasonal patterns?
* What insights can be derived from observed seasonal differences?
* What conclusions can reasonably be drawn from the available data?
* How could findings support better seasonal agricultural planning?

**Important:** Final analytical questions should be selected only after inspecting the actual project dataset.

---

## 19. Major Project Deliverables

**1. Problem Statement** — the Seasonal Agriculture Performance Analysis problem statement supplied by VOIS/AICTE.

**2. Dataset** — the agricultural dataset used for the project.

**3. Jupyter Notebook / Code File**, containing:

* Dataset loading
* Dataset understanding
* Data cleaning
* Data preparation
* Exploratory Data Analysis
* Seasonal analysis
* Appropriate visualizations
* Statistical analysis where relevant
* Five key results
* Findings
* Conclusions
* Recommendations

**4. PPT**, communicating the project results, with:

* 5 results
* 5 result slides
* Future Scope

The exact graphs for the five results should be selected after inspecting the dataset and identifying the strongest evidence.

---

## 20. PPT Result Strategy

The five results should be:

* Meaningful
* Directly connected to the problem statement
* Supported by actual data
* Supported by appropriate graphs
* Consistent with the Jupyter Notebook
* Easy to explain during presentation

Do not invent values before the dataset is analyzed. The final PPT numbers, charts and conclusions must match the Jupyter Notebook.

---

## 21. Future Scope

A Future Scope section is required in the project presentation, based on the actual findings obtained from the agricultural dataset.

Potential areas can include:

* More detailed seasonal forecasting
* Larger datasets
* Additional environmental variables
* Regional-level analysis
* Crop-specific predictive models
* Weather integration
* Resource optimization
* Economic forecasting
* Machine Learning-based prediction

These should only be finalized after the actual analysis so they remain relevant to the project findings.

---

## 22. Project Analysis Workflow

```text
Dataset
   ↓
Understand Dataset
   ↓
Shape / Columns / Info
   ↓
Missing Values / Duplicates
   ↓
Data Cleaning
   ↓
Data Type Conversion
   ↓
Exploratory Data Analysis
   ↓
Univariate Analysis
   ↓
Bivariate Analysis
   ↓
Multivariate Analysis
   ↓
Statistical Analysis
   ↓
Identify 5 Strong Results
   ↓
Insights
   ↓
Conclusion
   ↓
Recommendations
   ↓
PPT
   ↓
Future Scope
```

---

## 23. Important Analysis Principle

Do not choose graphs first and then force the data into them. Instead:

```text
Business / Agricultural Question
        ↓
Variables involved
        ↓
Type of analysis
        ↓
Appropriate graph/statistical method
        ↓
Observation
        ↓
Insight
```

### Example

* **Question:** Does funding relate to valuation?
* **Variables:** Funding + Valuation
* **Analysis:** Bivariate
* **Graph:** Scatter plot

---

## 24. Deadline

**Major Project submission deadline: 10 September 2026**

The project should be completed and checked before the deadline.

*Later extended to 15 September 2026, and then to 20 September 2026.*

---

## 25. Final Project Package

```text
Seasonal Agriculture Performance Analysis
│
├── Problem Statement
├── Agricultural Dataset
├── Jupyter Notebook (.ipynb)
│   ├── Data Loading
│   ├── Data Cleaning
│   ├── EDA
│   ├── Seasonal Analysis
│   ├── Visualizations
│   ├── Statistical Analysis
│   ├── 5 Key Results
│   ├── Findings
│   ├── Conclusions
│   └── Recommendations
│
└── PPT
    ├── 5 Results / 5 Result Slides
    └── Future Scope
```

---

## 26. Key Takeaways

* **Unicorn** — a startup valued at $1 billion or more.
* **Data Cleaning** — converting text-based valuation/funding values (e.g. `$5B`) into numeric form using a dynamic regex-based function.
* **Univariate** — one variable at a time (e.g. distribution of valuation).
* **Bivariate** — two variables together (e.g. funding vs valuation, valuation by industry).
* **Multivariate** — three or more variables together (e.g. funding, valuation and industry via scatter plot with hue).
* **Major Project** — Seasonal Agriculture Performance Analysis, due **10 September 2026** (later extended to 20 September 2026), requiring a Jupyter Notebook and a PPT with 5 results and a Future Scope.
* **Working principle** — start from the question, not the graph; never invent numbers before the dataset is analyzed.

---

## 27. Final Revision Sheet

| Topic                  | Remember                                                  |
| ----------------------- | ---------------------------------------------------------- |
| Unicorn                 | Startup valued at $1B+                                     |
| Decacorn                | Startup valued at $10B+                                    |
| `fillna('Unknown')`     | Fill missing categorical values                            |
| Valuation/Funding Clean | Convert `$5B`/`$750M`/`$100K` strings to numeric via regex |
| Univariate              | One variable                                                |
| Bivariate               | Two variables (e.g. funding vs valuation)                  |
| Multivariate            | Three+ variables (e.g. funding, valuation, industry)       |
| Histogram Bins          | Intervals grouping numeric data; too few/many distort the view |
| Major Project Title     | Seasonal Agriculture Performance Analysis                  |
| Deliverables            | Problem Statement, Dataset, Jupyter Notebook, PPT           |
| PPT Requirement         | 5 Results, 5 Slides, Future Scope                            |
| Deadline                | 10 September 2026 (later extended to 20 September 2026)     |

---

## Session Reflection

The fourth session moved from a fully guided practical — cleaning and analyzing the Unicorn Companies dataset — into the start of independent project work with the Seasonal Agriculture Performance Analysis brief.

The unicorn dataset practical reinforced the univariate → bivariate → multivariate progression already introduced in earlier sessions, this time applied to real cleaning problems (inconsistent valuation strings, missing city values) rather than an already-tidy dataset.

The shift into the Major Project briefing marks a change in mode: the sessions so far have been concept-plus-practical, but from here the work is self-directed, against a fixed dataset and a 10 September deadline, with the explicit rule to let findings — not assumptions — drive the five results and the Future Scope.
