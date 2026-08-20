# Data Analytics — Day 1

**Date:** 13 August 2026
**Program:** VOIS FOR TECH LD AICTE Internship Program
**Session:** Data Analytics — Day 1
**Mode:** Live Lecture

---

## 1. Introduction to Data Analytics

Data analytics is the process of examining data to understand what is happening, why it is happening, what may happen next, and what action should be taken.

The important point from the session was:

> Data analytics is not just about creating charts. The goal is to understand what the data means and use it to make better decisions.

### Business Example — Factory Machine

Imagine a factory machine suddenly stops.

* Machine stops.
* Production stops.
* Production loss occurs.
* Money and profit are lost.

Without analytics, the organization may only realize the problem after the machine has already failed.

With analytics, sensors can continuously provide machine data. If abnormal vibration is detected, maintenance can be performed before the machine completely fails.

Therefore:

> Analytics helps identify problems early so that action can be taken before a major loss occurs.

### Phone Battery Analogy

Analytics can be compared to a phone's battery warning.

For example:

* 20% → Plug in your charger.
* 15% → Warning.
* 5% → Urgent warning.
* 0% → Phone dies.

The warning gives us time to take action.

Similarly, analytics can provide information such as:

* Profit percentage
* Loss percentage
* Customer success rate
* Quarterly losses
* Business performance indicators

The purpose is to identify problems and opportunities early.

---

# 2. Data Analytics Process

A key point from the lecture was that data analytics should **start with a question**, not simply with a dataset.

### Basic Process

```text
Understand the Problem
        ↓
Collect Relevant Data
        ↓
Clean the Data
        ↓
Analyze the Data
        ↓
Visualize the Data
        ↓
Make a Decision
        ↓
Take Action
```

### Example — Student Performance

Instead of simply saying:

> "Let's analyze the student data."

We should ask a meaningful question:

> "Why are students failing in mathematics?"

Now the analysis has a specific purpose.

After analyzing the data, suppose a visualization shows that a large percentage of students are failing mathematics.

Possible actions could include:

* Extra classes
* Remedial teaching
* One-to-one sessions
* Additional guidance
* Identifying specific areas where students are struggling

The goal of analytics is therefore not simply to generate information.

It is:

> **Data → Insight → Decision → Action**

---

# 3. Primary and Secondary Data

## Primary Data

Primary data is data that **we collect ourselves** for a specific purpose.

### Example

Create a Google Form asking:

> "How many students use AI tools?"

The responses collected from that form are **primary data**.

## Secondary Data

Secondary data is data that **someone else has already collected** and made available.

### Examples

* Government datasets
* Population datasets
* Existing reports
* Public databases
* Existing research/data sources

### Easy Definition

> **Primary = I collect it.**
> **Secondary = Someone already collected it.**

| Type           | Meaning                           | Example               |
| -------------- | --------------------------------- | --------------------- |
| Primary Data   | Collected by us                   | Google Form responses |
| Secondary Data | Already collected by someone else | Government dataset    |

---

# 4. ETL

## ETL = Extract, Transform, Load

ETL is a process used to prepare raw data before it is used for analytics.

### Extract

Collect or retrieve the raw data.

Example:

> Collect sensor data from an IoT machine.

### Transform

Clean and modify the data so it can be used.

This may include:

* Cleaning data
* Handling missing values
* Changing formats
* Transforming values
* Organizing data

### Load

Store the transformed data in a location where it can be used for analysis.

### Food Preparation Analogy

The instructor explained ETL using food preparation.

```text
Extract
Get the ingredients
        ↓
Transform
Wash, cut and cook
        ↓
Load
Put the final food on the plate
```

Similarly:

```text
Raw Data
   ↓
Extract
   ↓
Clean / Transform
   ↓
Load
   ↓
Analytics
```

### Simple Definition

> **ETL prepares messy/raw data before serving it into analytics.**

---

# 5. Four Types of Data Analytics

There are four main types of data analytics:

1. Descriptive Analytics
2. Diagnostic Analytics
3. Predictive Analytics
4. Prescriptive Analytics

### Easy Way to Remember

| Type             | Question           |
| ---------------- | ------------------ |
| **Descriptive**  | What happened?     |
| **Diagnostic**   | Why did it happen? |
| **Predictive**   | What might happen? |
| **Prescriptive** | What should I do?  |

---

# 6. Descriptive Analytics

Descriptive analytics tells us:

> **What happened?**

It describes past or current data.

### Example — College Placements

Suppose:

```text
CSE         → 85%
ECE         → 82%
Mechanical  → 78%
```

This tells us what happened.

Common visualization methods include:

* Bar charts
* Line charts
* Dashboards

### Screen-Time Example

Suppose your phone says:

> "You spent 6 hours 32 minutes on your phone today."

The data is telling you what happened.

Therefore, this is **descriptive analytics**.

---

# 7. Diagnostic Analytics

Diagnostic analytics asks:

> **Why did it happen?**

It investigates the possible reasons or root causes behind a problem.

### Example — College Placement

Suppose:

> College placement percentage decreased.

This is the observed problem.

Diagnostic analysis investigates why it happened.

Possible reasons:

* Fewer companies visited.
* Students lacked required skills.
* Fewer students were eligible.
* Interview performance was poor.

Therefore:

> Descriptive tells us the problem; diagnostic begins the investigation into why it happened.

### Phone Battery Example

Suppose your phone battery is draining quickly.

Diagnostic analysis might investigate:

* Excessive phone usage
* Gaming
* Heavy applications
* Battery health
* Possible malware/virus
* Background activity

The goal is to identify the root cause.

---

# 8. Predictive Analytics

Predictive analytics asks:

> **What might happen?**

It uses historical and current data to estimate possible future outcomes.

### Important Point

Prediction is **not 100% certain**.

It means estimating what is likely to happen based on available data.

### Machine Example

Suppose:

```text
Monday     → Normal vibration
Tuesday    → Normal vibration
Wednesday  → Increasing vibration
```

If the vibration continues increasing, machine failure may become more likely.

Therefore, analytics can predict a possible future failure.

### Other Examples

**Amazon:**

> What might you buy next?

**Netflix:**

> What movie might you watch next?

These are examples of predictive analytics.

### Key Point

> Predictive analytics estimates likely outcomes; it does not guarantee the future with 100% certainty.

---

# 9. Prescriptive Analytics

Prescriptive analytics asks:

> **What should I do?**

It goes beyond predicting a possible outcome and recommends an action.

### Machine Example

Predictive:

> "The machine may fail tomorrow."

Prescriptive:

> "Schedule maintenance tonight."

### Road Example

If analytics predicts that Road A will become congested, it can recommend:

> Take Road B instead.

Prescriptive analytics can involve:

* Optimization
* Decision support
* Recommendations
* Recommended actions

---

# 10. Four Types — Quick Revision

```text
Descriptive  → What happened?
Diagnostic   → Why did it happen?
Predictive   → What might happen?
Prescriptive → What should I do?
```

### Example

```text
Machine vibration increased.
        ↓
Descriptive:
What happened?
        ↓
Diagnostic:
Why did vibration increase?
        ↓
Predictive:
Machine may fail tomorrow.
        ↓
Prescriptive:
Schedule maintenance tonight.
```

---

# 11. Role of a Data Analyst

The instructor emphasized that the job of a Data Analyst is **not simply to create many charts**.

Creating 20 charts does not automatically make someone a good Data Analyst.

The important part is being able to explain:

> **What do these charts actually mean?**

The main responsibility discussed was:

> **Find and explain insights from data.**

A Data Analyst should be able to communicate the meaning of the analysis to decision-makers.

---

# 12. Skills Required for a Data Analyst

Important skills discussed:

* SQL
* Python / R
* Statistics
* Data Visualization
* Communication
* Curiosity
* Problem Solving

AI tools such as ChatGPT, Gemini, and other LLM-based tools can assist with analysis, but they do not replace the fundamental skills of a Data Analyst.

---

# 13. Data Analyst vs Data Scientist vs Data Engineer

## Data Analyst

Main responsibility:

> Find and explain insights from data.

Focus:

* Data analysis
* Visualization
* Reporting
* Business insights

## Data Scientist

Main responsibility:

> Build advanced predictive models.

Focus:

* Predictive modeling
* Machine learning
* Advanced analytics

## Data Engineer

Main responsibility:

> Build data pipelines and infrastructure.

Focus:

* Data pipelines
* Data infrastructure
* Data processing

### Comparison

| Role           | Main Responsibility                     |
| -------------- | --------------------------------------- |
| Data Analyst   | Find and explain insights               |
| Data Scientist | Build advanced predictive models        |
| Data Engineer  | Build data pipelines and infrastructure |

---

# 14. Career Perspective

The instructor emphasized that students should not think:

> "I am a CSE student, so I must become a software developer."

There are multiple career paths in technology.

Students should develop transferable abilities such as:

* Logical thinking
* Problem decomposition
* Mathematical thinking
* System thinking

A degree does not limit someone to a single technology role.

---

# 15. Practical — Employee Attrition Analysis

The practical session focused on an **Employee Attrition Analysis** dataset.

### Dataset

The dataset contained:

* **1,480 employee records**
* **38 columns**

### Business Problem

The main problem statement was:

> **Why are employees leaving the organization, and which employee characteristics or workplace factors are associated with higher employee attrition?**

HR may have hundreds or thousands of employees but may not clearly understand:

* Which employees are more likely to leave?
* Which departments have higher attrition?
* Does overtime influence employee leaving?
* Does salary influence attrition?
* Does job satisfaction matter?
* Which jobs have higher employee turnover?
* Does work-life balance influence attrition?
* Do less-experienced employees leave more frequently?
* What workplace factors are associated with employee attrition?

Data analytics can help HR understand these patterns and improve the employee environment.

---

# 16. Google Colab

The practical was performed using **Google Colab**.

Google Colab provides a Python environment that can be used for:

* Python programming
* Data analysis
* Machine learning

One advantage discussed was that users can work with Python through Colab without needing to install Python locally for the basic workflow.

### Opening Colab

1. Open Google.
2. Search for **Google Colab**.
3. Open Colab.
4. Select **New Notebook**.
5. Upload the dataset.
6. Import required libraries.
7. Start analyzing the data.

---

# 17. Importing Pandas

Pandas was used for data analysis.

```python
import pandas as pd
```

A CSV file can be loaded into a DataFrame using:

```python
df = pd.read_csv("dataset.csv")
```

Here:

* `pd` represents Pandas.
* `df` represents the DataFrame.

---

# 18. Understanding the Dataset

Before performing analysis, we first need to understand the data.

## First Five Rows

```python
df.head()
```

This displays the first few rows.

## Last Five Rows

```python
df.tail()
```

This displays the last few rows.

These commands help us inspect the beginning and end of the dataset.

---

# 19. Dataset Shape

To determine the number of rows and columns:

```python
df.shape
```

The practical dataset returned:

```text
(1480, 38)
```

Meaning:

* **1480 rows**
* **38 columns**

---

# 20. Indexing

Python indexing starts from **0**.

Both positive and negative indexes can be used to access data.

The instructor demonstrated accessing rows and columns using indexes.

---

# 21. Statistical Information

To obtain statistical information about the dataset:

```python
df.describe()
```

This provides statistical information for numerical data, including values such as:

* Count
* Mean
* Standard deviation
* Minimum
* Quartiles
* Maximum

---

# 22. Null / Missing Values

Missing values need to be identified during data cleaning.

To check null values:

```python
df.isnull().sum()
```

This gives the number of null values in each column.

The practical demonstrated identifying columns containing missing values and discussed filling missing values using appropriate methods.

Depending on the data, techniques such as **mean** or **mode** may be used.

---

# 23. Dataset Information

To obtain information about all columns:

```python
df.info()
```

This provides information such as:

* Column names
* Non-null counts
* Data types
* Number of entries
* Memory usage

The instructor discussed different data types including:

* Integer
* Float
* Object/String
* Categorical data

---

# 24. Numerical and Categorical Columns

The dataset contained:

* **26 numerical columns**
* **12 categorical/string columns**

Understanding data types is important because different types of data require different analysis techniques.

---

# 25. Data Distribution

The practical demonstrated creating histograms/distributions for numerical features.

The purpose of a distribution plot is to understand how values are spread across a dataset.

Selected numerical columns can be analyzed separately rather than analyzing every column at once.

---

# 26. Selecting Specific Columns

Specific columns can be selected for focused analysis.

Example:

```python
selected_columns = [
    "column1",
    "column2",
    "column3"
]

df1 = df[selected_columns]
```

Now `df1` contains only the selected columns.

This allows analysis to focus on specific variables.

---

# 27. Outliers

An **outlier** is a data point that is unusually far away from the general pattern of the dataset.

Outliers can affect analysis and therefore may need to be investigated.

### Example

The instructor demonstrated checking columns such as monthly income for possible outliers.

---

# 28. Box Plot

A **box plot** can be used to identify potential outliers.

Example:

```python
import matplotlib.pyplot as plt

plt.boxplot(df1["MonthlyIncome"])
plt.show()
```

The box plot helps visually identify values that are unusually high or low.

---

# 29. IQR Technique

The instructor demonstrated the **Interquartile Range (IQR)** technique for handling outliers.

### Formula

```text
IQR = Q3 − Q1
```

Where:

* `Q1` = First Quartile
* `Q3` = Third Quartile

A commonly used method for detecting potential outliers is:

```text
Lower Bound = Q1 − 1.5 × IQR

Upper Bound = Q3 + 1.5 × IQR
```

Values outside these boundaries can be considered potential outliers.

The practical demonstrated:

1. Identify outliers.
2. Apply the IQR technique.
3. Remove/handle the outliers.
4. Create the plot again.
5. Check whether the outliers were removed.

---

# 30. LLMs in Data Analytics

The instructor introduced the use of **LLMs** for assisting with data analysis.

## LLM

**LLM = Large Language Model**

LLMs can assist with:

* Generating Python code
* Explaining code
* Finding possible insights
* Suggesting analysis techniques
* Creating visualizations
* Working with data-analysis prompts

The session demonstrated using **Gemini 2.5** as an example.

### Important

AI tools should be treated as assistants.

A Data Analyst still needs to understand:

* The business problem
* The dataset
* The analysis
* The generated code
* The results
* Whether the results make sense

---

# 31. Julius AI

Another AI-based data-analysis tool introduced was **Julius AI**.

The instructor demonstrated uploading the same dataset and providing a prompt similar to:

> "Build our best insights with this dataset and clean the data."

Julius AI can assist with:

* Data cleaning
* Python code generation
* Data analysis
* Visualization
* Insight generation
* Dashboards

It can automatically generate Python code and visualizations based on the dataset and prompt.

The session also mentioned that Julius AI provides a limited number of credits per day.

### Important Principle

> AI tools can assist with data analysis, reporting, and narration, but they are not a replacement for a Data Analyst.

---

# 32. Attendance Form

Attendance instructions were provided at the end of the session.

Students were asked to fill the attendance form carefully because mistakes had occurred in previous sessions.

### Information Required

The form included fields such as:

* Full Name
* AICT Student ID
* Gender
* Person with Disability information, where applicable
* Session Date
* College Name
* College State
* College City
* Course Name
* Stream
* Branch
* Semester
* AICT Email ID
* LMS Email ID
* Contact Number
* Feedback
* Session Rating

---

# 33. AICT Student ID

The AICT Student ID can be found by logging into the **AICT portal** and opening the profile section.

The ID begins with:

```text
STU...
```

Students need to enter the **complete ID**.

A sample screenshot was also shared during the session to show where the ID could be found.

---

# 34. Email Information

The attendance form asks for:

### AICT Email ID

The email address used while applying for the AICT internship.

### LMS Email ID

The email address used for LMS registration.

If the same email was used for both, the same email can be entered.

If different emails were used, the appropriate email should be entered in each field.

---

# 35. Attendance Feedback

The attendance form also contains feedback questions.

Students were asked to provide feedback regarding:

* Overall session experience
* Three things they liked about the session
* Other feedback questions
* Session rating

After completing all information:

> Submit the form to confirm attendance.

---

# 36. Session Task

The task given at the end of the session was to:

1. Explore the Data Analytics elements.
2. Complete the relevant Data Analytics certificates.
3. Explore the available learning material.
4. Continue learning before the next session.

The instructor mentioned that the certificate link would be shared.

Students were encouraged to explore as much of the material as possible.

---

# 37. Key Takeaways

### Data Analytics

> Data analytics helps turn data into useful insights that support decisions and actions.

### Analytics Process

```text
Question
   ↓
Data
   ↓
Cleaning
   ↓
Analysis
   ↓
Visualization
   ↓
Decision
   ↓
Action
```

### Primary vs Secondary

```text
Primary   → I collect
Secondary → Someone already collected
```

### ETL

```text
Extract → Transform → Load
```

### Four Types

```text
Descriptive  → What happened?
Diagnostic   → Why did it happen?
Predictive   → What might happen?
Prescriptive → What should I do?
```

### Career Roles

```text
Data Analyst
→ Find and explain insights

Data Scientist
→ Build advanced predictive models

Data Engineer
→ Build data pipelines and infrastructure
```

### Practical Workflow

```text
Upload Dataset
      ↓
Import Libraries
      ↓
Read CSV
      ↓
head() / tail()
      ↓
shape
      ↓
describe()
      ↓
isnull().sum()
      ↓
info()
      ↓
Check Data Types
      ↓
Analyze Distributions
      ↓
Detect Outliers
      ↓
IQR
      ↓
Visualization
      ↓
Insights
```

---

# 38. Important Commands Covered

```python
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv("dataset.csv")

df.head()
df.tail()

df.shape

df.describe()

df.isnull().sum()

df.info()

df.dtypes
```

For visualization and outlier analysis:

```python
plt.boxplot(df["MonthlyIncome"])
plt.show()
```

---

# 39. Final Revision Sheet

| Topic                      | Remember                                 |
| -------------------------- | ---------------------------------------- |
| Data Analytics             | Turning data into insights for decisions |
| Primary Data               | Data collected by us                     |
| Secondary Data             | Data already collected by someone else   |
| ETL                        | Extract → Transform → Load               |
| Descriptive                | What happened?                           |
| Diagnostic                 | Why did it happen?                       |
| Predictive                 | What might happen?                       |
| Prescriptive               | What should I do?                        |
| Data Analyst               | Finds and explains insights              |
| Data Scientist             | Builds advanced predictive models        |
| Data Engineer              | Builds data pipelines/infrastructure     |
| `head()`                   | First rows                               |
| `tail()`                   | Last rows                                |
| `shape`                    | Rows and columns                         |
| `describe()`               | Statistical summary                      |
| `isnull().sum()`           | Null-value count                         |
| `info()`                   | Dataset/column information               |
| Box Plot                   | Identify potential outliers              |
| IQR                        | Outlier detection/handling technique     |
| LLM                        | Large Language Model                     |
| Julius AI                  | AI-assisted data analysis tool           |
| Dataset                    | 1,480 rows × 38 columns                  |
| Numerical Columns          | 26                                       |
| Categorical/String Columns | 12                                       |

---
