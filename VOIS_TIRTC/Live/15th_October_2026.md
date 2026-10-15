# Cardiovascular Data Analysis — Live Session

**Date:** 15 October 2026<br>
**Program:** VOIS FOR TECH AICTE Internship Program<br>
**Session:** Cardiovascular Data Analysis — EDA Walkthrough<br>
**Mode:** Live Interactive Session (Zoom)

---

## Session Overview

This session was a hands-on, interactive EDA (Exploratory Data Analysis) walkthrough centered on a **Cardiovascular Risk Factors dataset** (based on the Framingham Heart Study). The trainer (Ashwini) guided students through understanding the medical domain, interpreting the dataset columns, and building multiple plot types to uncover patterns associated with coronary heart disease.

Key emphasis was placed on **domain knowledge** — understanding what the data represents medically before writing a single line of code — and on reading visualisations critically rather than just generating them.

---

## Announcements

| Item | Details |
|---|---|
| DIY Project Resubmission Deadline | 22 October 2026 |
| Next Session | 19 October 2026 (Monday) — **Mandatory Expert Talk (Part 2)** |
| Expert Talk Registration | Registration form already shared — fill it before Monday |
| Attendance Form | Shared at end of session — active until 8:00–8:30 PM only |
| IPython Notebook | Shared by trainer on Telegram after the session |
| Dataset | Cardiovascular dataset — shared by trainer on Telegram during session |

---

## Dataset: Cardiovascular Risk Factors (Framingham Heart Study)

### Context

The session opened with a scenario: *a 52-year-old person suddenly experiences chest discomfort, sweating, and breathlessness — you have 60 seconds to decide if it is a medical emergency.* Students were asked to interpret a patient profile and a diagram of the heart structure before touching any code.

The dataset is designed to help answer a central question:

> **Can we identify patterns in patient characteristics and health measurements associated with Coronary Heart Disease (CHD) over a 10-year period?**

**CHD (Coronary Heart Disease)** occurs when blood supply to the heart muscle becomes restricted — commonly due to plaque buildup in the coronary arteries (cholesterol and fatty deposits narrowing the artery walls over time).

### Columns

| Column | Type | Description |
|---|---|---|
| ID | Numerical (ID) | Serial number / unique record identifier |
| Age | Numerical | Patient's age in years |
| Education | Categorical | Education level of the patient |
| Is Smoking | Categorical | Smoking status (yes / no) |
| Cigs Per Day | Numerical | Number of cigarettes smoked per day |
| BP Meds | Binary | Blood pressure medication indicator |
| Prevalent Stroke | Binary | Indicator of a previous stroke |
| Prevalent Hyp | Binary | Indicator of pre-existing hypertension (high blood pressure) |
| Diabetes | Binary | Diabetes indicator |
| Total Chol | Numerical | Total cholesterol measurement |
| Sys BP | Numerical | Systolic blood pressure (the "120" in 120/80) |
| Dia BP | Numerical | Diastolic blood pressure (the "80" in 120/80) |
| BMI | Numerical | Body Mass Index |
| Heart Rate | Numerical | Heart rate in beats per minute |
| Glucose | Numerical | Blood glucose level |
| Ten Year CHD | Binary (Target) | 10-year CHD outcome — **0** = no recorded CHD, **1** = recorded CHD |

### Key Observations
- **Normal healthy BP** = 120/80 mmHg (120 → systolic, 80 → diastolic)
- **Target variable** is `Ten Year CHD` — 0 means no recorded outcome within the 10-year period, 1 means CHD was recorded
- Outcome distribution: approximately **85% no CHD (0)** and **15% CHD (1)** — the classes are imbalanced
- Missing values were present in several columns (glucose, education, BP meds, total cholesterol, cigarettes per day, BMI, heart rate) — these were handled before analysis
- No duplicate rows found

---

## Core Concept: Domain Knowledge is Non-Negotiable

> *"Nokia was the king of the mobile world from 2002 to 2010. Today we don't hear about Nokia. Samsung adopted technology. That's the difference."*

A key message of the session — data analysts must **adopt domain knowledge** regardless of their background. This is not a biology class, but to analyse a cardiovascular dataset meaningfully, you must understand what cholesterol, blood pressure, BMI, and glucose actually represent. Without that, patterns in the data have no meaning.

Risk factors for heart disease discussed:
- Age
- Smoking
- High blood pressure
- High cholesterol
- Obesity (BMI)
- Diabetes (glucose levels)
- Poor diet and stress
- Genetic history

---

## Hands-On Task

Students were asked to download the dataset from Telegram, import the required libraries, and perform initial analysis:

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

df = pd.read_csv('cardiovascular_data.csv')

df.head()             # Top 5 rows
df.tail()             # Last 5 rows
df.describe()         # Statistical summary
df.isnull().sum()     # Missing value count per column
df.duplicated().sum() # Check for duplicate rows
df.shape              # Rows and columns
```

**Results:**
- Missing values found in several columns (not zero — requires cleaning)
- No duplicate rows
- Dataset shape confirmed before and after cleaning

---

## EDA Walkthrough

### Types of EDA (Recap)

| Type | Columns Used | Purpose |
|---|---|---|
| Univariate | 1 column | Distribution of a single variable |
| Bivariate | 2 columns | Relationship between two variables |
| Multivariate | 3+ columns | Relationships across multiple variables |

---

### 1. Age Distribution — Histogram (Univariate)

**Column used:** `Age`

**Why a histogram?**
- `Age` is a **numerical (continuous)** variable.
- A histogram groups ages into **bins** (intervals) and shows how many patients fall in each interval.
- With `bins=20`, the age range is divided into 20 equal intervals — the height of each bar shows how many observations fall within that age range.

**Key question asked:** *Does the histogram look symmetrical, or are most observations concentrated in a particular age range?*

**Answer:** The distribution is **not symmetrical** — it is **slightly right-skewed**.
- Peak concentration is around ages **39–45**.
- Frequency generally declines toward older ages, extending into the late 60s.
- The distribution is not a mirror image on both sides of its peak.

**What are bins?**
- Bins are the intervals used to group numerical data in a histogram.
- `bins=20` means the full age range is divided into 20 equal intervals.
- Each bar represents one bin, and its height = number of patients in that interval.

---

### 2. Average Health Measurements by CHD Outcome — Grouped Bar Chart (Bivariate)

**Columns used:** `Ten Year CHD` (group), `Age`, `Cigs Per Day`, `Total Chol`, `Sys BP`, `Dia BP`, `BMI`, `Heart Rate`, `Glucose`

**Why a grouped bar chart?**
- Business question: *Which health measurements differ between patients who develop CHD and those who don't?*
- A grouped bar chart places bars for both outcome groups (0 and 1) side by side for each measurement — making comparison direct and immediate.

**How it was built:**
```python
df.groupby('TenYearCHD')[numerical_features].mean().T
```
- Records are grouped by CHD outcome (0 or 1)
- The mean of each selected measurement is calculated separately for each group
- The table is transposed so measurements appear as rows and outcome groups as columns
- X-axis labels are rotated 35° to avoid overlap

**Key observation:** Total cholesterol showed notably higher averages in the CHD group — suggesting an association between cholesterol levels and CHD outcome. Smoking (cigarettes per day) also showed a higher average in the CHD group.

> **Important note:** Different measurements use different units (age in years, cholesterol in concentration units, heart rate in beats per minute). Do not compare bar heights *across* different variables — compare the two outcome groups *within* each variable only.

---

### 3. Smoking Status and CHD Outcome — Bar Chart (Bivariate)

**Columns used:** `Is Smoking`, `Ten Year CHD`

**How it was built:**
- A **cross-tabulation** was created between smoking status and CHD outcome.
- Proportions were calculated within each smoking status group (`normalize='index'`), then multiplied by 100 to get percentages.
- Percentage values were rounded to 2 decimal places for display.

**Key question asked:** *Does the percentage of recorded CHD outcome differ between smoking groups?*

**Answer:** The cross-tabulation describes the difference — however, smoking alone does not establish causation. Age, medical history, cholesterol, blood pressure, and other variables may all contribute. Smoking is one factor among many.

---

### 4. Blood Pressure Comparison — Grouped Bar Chart (Bivariate)

**Columns used:** `Sys BP` (systolic), `Dia BP` (diastolic), `Ten Year CHD`

**How it was built:**
```python
df.groupby('TenYearCHD')[['sysBP', 'diaBP']].mean().T
```
- Averages of systolic and diastolic BP are calculated for both outcome groups
- Displayed as a grouped bar chart with readable axis labels

**Observations from the chart:**

| Measurement | No CHD (0) | CHD (1) |
|---|---|---|
| Systolic BP (Sys BP) | ~131 mmHg | ~144 mmHg |
| Diastolic BP (Dia BP) | ~82 mmHg | ~87 mmHg |

Both average blood pressure measurements are **higher in the CHD group**. This suggests an **association between elevated blood pressure and CHD** in this dataset.

> **Caveat:** This shows averages, not the full distribution. It does not prove causation, and it does not establish individual risk. Whether these differences are statistically significant requires further testing.

---

### 5. Key Summary — Descriptive Statistics

A final summary section collected important descriptive statistics in one place:

```python
# Total records
print(f"Total records: {len(df)}")

# CHD outcome counts
print(df['TenYearCHD'].value_counts())

# Average measurements by outcome group
df.groupby('TenYearCHD')[selected_columns].mean().round(2)
```

- `len(df)` returns the number of rows in the clean analysis dataset
- f-strings embed calculated values directly into printed text
- `.sum()` with a condition counts matching records for each outcome group
- `.round(2)` rounds displayed results to 2 decimal places
- This section is intended to make it easy to pull figures directly into a project report

---

## Key Concepts Covered

| Concept | Description |
|---|---|
| CHD (Coronary Heart Disease) | Restriction of blood supply to the heart muscle due to arterial plaque buildup |
| Systolic BP | Blood pressure during heart contraction (the top number — e.g., 120 in 120/80) |
| Diastolic BP | Blood pressure between heartbeats (the bottom number — e.g., 80 in 120/80) |
| Histogram | Distribution of a numerical variable; bars represent ranges (bins) |
| Bins | Intervals used to group numerical data in a histogram |
| Grouped Bar Chart | Compares averages of two outcome groups side by side for the same variable |
| Cross-Tabulation | Table of frequencies/percentages across two categorical variables |
| Group By + Mean | Splits data by a category and calculates the average of selected columns per group |
| Skewness (Right-Skewed) | Distribution where most values are on the left and the tail extends to the right |
| Domain Knowledge | Understanding the medical/business meaning of the data before analysis |
| Class Imbalance | When one outcome group (e.g., no CHD = 85%) is far larger than the other (CHD = 15%) |

---

## Revision: Important Reminders

- **Understand the dataset before writing code** — column names, units, and what each variable actually means medically or contextually.
- **Domain knowledge is not optional** — you don't need a biology degree, but you must know what cholesterol, blood pressure, and glucose mean in the context of heart disease.
- A **histogram** is for numerical/continuous data; a **count plot** is for categorical data — do not apply a histogram to a categorical column.
- A **grouped bar chart** is used when you want to compare the same measurement across two or more groups simultaneously.
- When comparing bar heights across different variables in a grouped bar chart, be cautious — each variable has **different units and scales**.
- The **right-skewed age distribution** means most patients in this dataset are in their early 40s, with fewer older patients — this must be considered when interpreting results.
- Showing that two groups have different averages is **not the same as proving causation** — other variables may be involved.

---

## DIY Project Reminder

- Project: **TI RTC DIY Project**
- Resubmission opportunity open for those whose projects were not accepted (check the feedback document shared by Ashwini sir)
- Also open for those who submitted on LMS but missed the Google Form submission
- Submit on: **LMS** + **Google Form**
- Deadline: **22 October 2026**
- Feedback and names available in the shared document (names on page 1, feedback in the same row on page 2)
- IPython notebook for today's session shared on Telegram by Ashwini sir

---

## Upcoming Session

| Detail | Info |
|---|---|
| Date | 19 October 2026 (Monday) |
| Time | 6:30 PM – 7:30 PM |
| Session Type | Expert Talk — Part 2 (continuation of Anil sir's session) |
| Attendance | **Mandatory** — taken live for certification eligibility |
| Action Required | Fill the expert talk registration form (link shared on Telegram) |
| Announcement channel | Telegram group |
