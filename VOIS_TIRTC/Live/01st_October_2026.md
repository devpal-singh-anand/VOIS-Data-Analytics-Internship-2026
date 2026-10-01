# Consumer Electronics Sales Data Analytics — Live Session

**Date:** 1 October 2026<br>
**Program:** VOIS FOR TECH AICTE Internship Program<br>
**Session:** Consumer Electronics Sales Data Analytics — EDA Walkthrough<br>
**Mode:** Live Interactive Session (Zoom)

---

## Session Overview

This session was a hands-on, interactive EDA (Exploratory Data Analysis) walkthrough centered on a **Consumer Electronics Sales dataset**. The trainer (Ashwini) guided students through understanding the dataset structure, performing basic data operations, and building and interpreting multiple plot types — progressing from univariate to multivariate analysis.

Key emphasis was placed on thinking like a **business analyst** — not just plotting data, but deriving actionable decisions from it.

---

## Announcements

| Item | Details |
|---|---|
| DIY Project Deadline | 10 October 2026 |
| Next Session | 7 October 2026 (Wednesday) — **Mandatory Expert Talk** |
| Expert Talk Attendance | Attendance will be taken live; will **not** be reshared on Telegram |
| Attendance Form | Shared at the end of the session — submission is mandatory |
| IPython Notebook | Shared by trainer on Telegram after the session |
| Dataset | Consumer Electronics Sales dataset — shared on Telegram before/during session |

---

## Dataset: Consumer Electronics Sales

### Context

Students were asked to imagine themselves as analysts working for a company selling **smartphones, laptops, tablets, smartwatches, and headphones**. The company has thousands of customer and product records, and management wants answers to questions like:

- Who are our customers?
- What products are they interested in?
- Does price influence purchase decisions?
- Is customer satisfaction related to purchase intent?

### Columns

| Column | Type | Description |
|---|---|---|
| Product ID | Numerical (ID) | Unique identifier for each product/record |
| Product Category | Categorical | Type of product (smartphone, laptop, tablet, smartwatch, headphone) |
| Product Brand | Categorical | Brand associated with the product (e.g., Apple, Samsung, Dell, HP) |
| Product Price | Numerical | Price of the product (in INR) |
| Customer Age | Numerical | Age of the customer |
| Customer Gender | Categorical | Gender of the customer |
| Purchase Frequency | Numerical | How often the customer purchases |
| Customer Satisfaction | Numerical | Customer rating (1–5 scale) |
| Purchase Intent | Numerical/Binary | Whether the customer intends to purchase |

### Key Observations
- **No null values** in the dataset
- **9,000 records** total
- Mix of categorical and numerical columns

---

## Core Concept: Data Analytics — From Data to Decisions

> *"Data Analytics: From Data to Decisions"*

A key message of the session — data analytics is not just about building dashboards or charts. The goal is to:

1. Analyze the data
2. Find meaningful insights
3. **Take decisions** based on those insights

Example from the session: if laptop prices are very high and customers aren't buying, or if there are no offers on headphones and interest drops — these are business decisions that come from data analysis.

---

## Hands-On Task

Students were given **5 minutes** to independently load the dataset and perform basic operations:

```python
import pandas as pd

df = pd.read_csv('consumer_electronics_sales.csv')

df.head()       # Top 5 rows
df.tail()       # Last 5 rows
df.describe()   # Statistical summary
df.isnull().sum()  # Check for null values
```

**Result:** Zero null values confirmed. Dataset has 9,000 rows.

---

## EDA Walkthrough

### Types of EDA (Recap)

| Type | Columns Used | Purpose |
|---|---|---|
| Univariate | 1 column | Distribution of a single variable |
| Bivariate | 2 columns | Relationship between two variables |
| Multivariate | 3+ columns | Relationships across multiple variables |

---

### 1. Customer Age Distribution — Histogram (Univariate)

**Column used:** `Customer Age`

**Why a histogram?**
- Histograms are used for **numerical data** to show **distribution** — how values are spread across ranges.
- Instead of looking at 9,000 individual age values, the histogram groups ages into ranges (bins) and shows how many customers fall in each range.

**What it tells us:**
- X-axis: Customer age ranges (e.g., 20–30, 30–40, 40–50…)
- Y-axis: Number of customers in each range
- The height of each bar = number of customers in that age range
- Helps identify where customers are **concentrated** (e.g., if 34–40 has the tallest bar, most customers are in that range)

**Histogram vs Bar Chart:**
| Histogram | Bar Chart |
|---|---|
| Used for numerical data | Used for categorical data |
| Shows distribution | Shows counts/comparisons |
| Bars touch each other | Bars are separated |

---

### 2. Customer Satisfaction by Product Category — Box Plot (Bivariate)

**Columns used:** `Customer Satisfaction`, `Product Category`

**Why a box plot?**
- Business question: *How does customer satisfaction differ across product categories?*
- A simple average (e.g., 3.2, 3.8, 4.0) doesn't tell the whole story.
- Box plots give a **compact view of the distribution** of a numerical variable across categories.

**What it shows:**
- **Median** — middle value of satisfaction ratings
- **Q1 and Q3** — first and third quartiles (interquartile range)
- **Outliers** — unusual values that fall far from the rest of the data (shown as individual points)

---

### 3. Purchase Frequency by Customer Gender — Bar Plot (Bivariate)

**Columns used:** `Purchase Frequency`, `Customer Gender`

**Observation:** Both male and female customers showed roughly equal purchase frequency across platforms.

---

### 4. Distribution of Product Category — Count Plot (Univariate)

**Column used:** `Product Category`

**Why a count plot and not a histogram?**
- `Product Category` is a **categorical column**, not numerical.
- Histograms are meant for **numerical/continuous data** — applying one to a categorical column won't yield meaningful insights.
- Count plots show **how many times each category appears** in the dataset.

**Observation:** Product counts were roughly equal across all categories, with a slight dip in headphones.

---

### 5. Distribution of Product Brand — Count Plot (Univariate)

**Column used:** `Product Brand`

- Same plot type as above, applied to brand instead of category.
- Shows which brands appear most frequently in the dataset.

---

### 6. Purchase Intent by Customer Satisfaction — Bar Plot with Error Bars (Bivariate)

**Columns used:** `Customer Satisfaction`, `Purchase Intent`

**What it shows:**
- Customers with higher satisfaction ratings (4–5) showed ~85% purchase intent.
- The small vertical black lines on top of each bar are **error bars**.

**What is an error bar?**
- Represents the **uncertainty/variability** around the estimated mean.
- A smaller error bar = the estimated mean is more precise.
- We shouldn't say "exactly 85% purchase intent" — the error bar shows how precise that estimate is.

---

### 7. Pair Plot — Multivariate Analysis

**Columns used:** `Product Price`, `Customer Age`, `Purchase Frequency`, `Customer Satisfaction`, `Purchase Intent`

**Why a pair plot?**
- Used to explore **relationships between several numerical variables simultaneously**.
- Data is divided by group (e.g., purchase intent 0 vs 1, shown in different colors).

**How to read it:**
- Each cell in the grid shows the relationship between two variables (scatter plot).
- The **diagonal cells** show the **distribution of each individual variable** (like a histogram for that variable alone).
- Color coding separates groups (e.g., blue = purchase intent 0, orange = purchase intent 1).

---

## Key Concepts Covered

| Concept | Description |
|---|---|
| Histogram | Distribution of a numerical variable across ranges |
| Box Plot | Distribution + outlier detection for numerical data, grouped by category |
| Count Plot | Frequency count of a categorical variable |
| Bar Plot | Comparison of a numerical value across categories |
| Error Bar | Represents uncertainty around an estimated mean value |
| Pair Plot | Grid of relationships between multiple numerical variables |
| Univariate Analysis | Analysis of a single variable |
| Bivariate Analysis | Relationship between two variables |
| Multivariate Analysis | Relationships across three or more variables |
| Distribution | How values of a variable are spread across ranges |

---

## Revision: Important Reminders

- Use **histograms for numerical columns** and **count plots for categorical columns** — don't mix them up.
- A box plot is not just for outlier detection — it's used to compare the **distribution** of a numerical variable across categories.
- The error bar on a bar plot indicates **uncertainty around the mean**, not an error in the data.
- Data analytics is not about plotting alone — it's about going **from data to decisions**.
- Domain knowledge (agriculture, banking, healthcare, electronics) is increasingly important for data analysts.
- Using AI tools like ChatGPT to generate full code defeats the purpose of learning — understand the dataset yourself first.

---

## DIY Project Reminder

- Project: **Healthcare Analytics for Doctor Visit**
- Submit on: **LMS** (DIY Project Submission tab) + **Google Form**
- Deadline: **10 October 2026**
- Dataset, PPT template, and reference video available on the LMS
- IPython notebook for today's session shared on Telegram by Ashwini sir

---

## Upcoming Session

| Detail | Info |
|---|---|
| Date | 7 October 2026 (Wednesday) |
| Session Type | Expert Talk — Industry Expert |
| Attendance | **Mandatory** — taken live, not reshared |
| Announcement channel | Telegram group |
