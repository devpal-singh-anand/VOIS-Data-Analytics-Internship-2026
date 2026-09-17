# Healthcare Analytics DIY Project & IBM Bob — TIRTC Session

**Date:** 17 September 2026<br>
**Program:** VOIS FOR TECH TIRTC Integrated Session<br>
**Session:** Data Analytics — TIRTC Session<br>
**Mode:** Live Lecture + Practical Session + Tool Demonstration

---

## 1. Introduction

The session opened with announcements about the TIRTC extension program, then moved into a guided walkthrough of the new **DIY project — Healthcare Analytics for Doctor Visits**: dataset exploration, AI-assisted analysis in Google Colab, PPT preparation, and the two-place submission process (VOIS LMS and Google Form).

The final part introduced **IBM Bob**, an AI-assisted software development tool, with a live demonstration of running the same healthcare analysis from a single natural-language prompt.

### Main topics covered

* TIRTC program announcements (schedule, certificates, recordings)
* DIY project: Healthcare Analytics for Doctor Visits
* Accessing the project, dataset and PPT template on the VOIS LMS
* Problem statement and business questions
* Dataset exploration and the statistical summary
* Quartiles, IQR and box plots
* Univariate, bivariate and multivariate analysis with Gemini in Google Colab
* Preparing the project PPT
* Submitting on the VOIS LMS and through the Google Form
* IBM Bob: installation, setup and demonstration

---

## 2. TIRTC Announcements

### Program

* The session is part of the extension of the AICTE initiative, delivered as the **TIRTC** integrated sessions.
* Alongside the learning sessions, additional tool training, expert talks, mentoring and doubt sessions, and projects are planned for the coming weeks.
* Details about the TIRTC initiative, which runs in collaboration with the Department of Telecommunications, are available on the LMS.

### Schedule

* Two sessions were held that week: the day of this session and the day after.
* From the following week, mostly one session per week is planned, with extra sessions when an industry expert joins or another opportunity comes up.
* Updates are shared on the Telegram group.

### Certificates

* Students who only completed the AICTE internship (including the major project) receive the **AICTE certificate**.
* Students who take part in the extension learning receive **two certificates**: the AICTE certificate and a certificate from the **TIRTC initiative**.
* Completing this DIY project is important for receiving the TIRTC certificate.

### Recordings and attendance

* Session recordings are shared, but should be watched regularly and not left to pile up. Students are encouraged to make their own notes.
* Students should join on time and stay until the end, since doubts are discussed at the start and end of each session.
* The attendance form is shared separately on the Telegram group.

---

## 3. DIY Project Overview

**Project name:** Healthcare Analytics for Doctor Visits

This DIY project is separate from the AICTE major project and from the earlier DIY project. It is submitted in **two places**:

| Where | What |
| ----- | ---- |
| VOIS LMS portal | The project PPT, through the DIY project submission option |
| Google Form | The project PPT and student details, through a separate TIRTC DIY project submission form |

### Points to remember

* The Google Form is different from the AICTE major project form. It was described as the **green-colored** form, titled as the DIY project submission form for the AICT data analytics batch.
* Students who had already completed this DIY project on their own earlier must submit it again through the new Google Form, since earlier submissions are not counted.
* Only this project (Healthcare Analytics for Doctor Visits) has to be submitted. It is not necessary to complete every DIY project on the LMS.
* The form link and instructions are shared on the Telegram group. Students were asked to wait for that message before submitting.

---

## 4. Accessing the Project on the VOIS LMS

1. Log in to the VOIS LMS portal.
2. From the dashboard, open **DIY Project**.
3. Select **Data Analytics**.
4. Open the second project, **Healthcare Analytics for Doctor Visits**.
5. On first opening, click **Enroll Now**.
6. Download both:
   * the **dataset**
   * the **DIY project PPT template**

The dataset is available only on the VOIS LMS. Without downloading it from there, the project cannot be completed or submitted.

---

## 5. Problem Statement

**Turning patient visit data into actionable healthcare insight.**

The project is a practical data analysis exercise showing how healthcare data can become meaningful insight for hospitals, doctors and patients. The session focused on **data analysis, not machine learning**.

### Central question

> How can a hospital use patient visit data to understand demand, reduce waiting time and improve the patient experience?

### Role

Students imagine themselves as a **junior healthcare data analyst** working with a hospital management team.

### Business problems

1. Which patient groups have more recorded doctor visits?
2. How are illness and health status associated with the visits?
3. Do chronic conditions correspond to different visit patterns?
4. What should management investigate before making operational changes?

### Learning outcomes

* Understand a healthcare dataset and its columns
* Clean and prepare data using Python and Pandas
* Create meaningful visualizations using Matplotlib and Seaborn
* Compare doctor visit patterns across age groups, gender, illness and chronic conditions
* Communicate findings as recommendations for healthcare service improvement

**Note:** The dataset is a record of observations. It is not a live hospital appointment system.

---

## 6. The Dataset

The dataset describes doctor visits along with patient characteristics, illness, health status and healthcare coverage.

* **Rows:** 5,190
* **Columns:** 13

### Columns discussed

| Column | Meaning |
| ------ | ------- |
| `visits` | Number of recorded doctor visits |
| `gender` | Patient gender |
| `age` | Encoded age group value |
| `income` | Encoded income value |
| `illness` | Illness measure / score |
| `reduced` | Number of days of reduced activity |
| `health` | Health status measure |
| `private` | Private insurance indicator |
| `freepoor` | Free care indicator for low-income patients |
| `nchronic` | Indicator for non-limiting chronic conditions |
| `lchronic` | Indicator for limiting chronic conditions |

A further free-care indicator column was also mentioned in the session but not described in detail.

---

## 7. Practical — Exploring the Data in Google Colab

A new Google Colab notebook was created and named after the project. The dataset was added to the Colab session and loaded with Pandas.

### Libraries

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```

**Matplotlib** provides the core plotting functions, and **Seaborn** builds on it to make statistical plots easier to create.

### Loading the dataset

```python
df = pd.read_csv("file_name.csv")
```

### Inspecting the data

```python
df.head()        # first five rows
df.tail()        # last five rows
df.shape         # (5190, 13)
df.info()        # column names, data types, non-null counts
df.describe()    # statistical summary of numeric columns
df.isnull().sum()  # missing values per column
```

### Observations

* The dataset has **5,190 rows and 13 columns**.
* `df.info()` showed the data types: integers, floats and object (string) columns.
* `df.isnull().sum()` returned **zero** missing values in every column.

---

## 8. Quartiles, IQR and Box Plots

`df.describe()` reports the 25%, 50% and 75% values of each numeric column:

| Value | Name | Meaning |
| ----- | ---- | ------- |
| 25% | Q1, first quartile | 25% of values fall below this |
| 50% | Q2, second quartile | The median |
| 75% | Q3, third quartile | 75% of values fall below this |

### Why quartiles are useful

* They divide the data into four equal parts.
* They show how doctor visits are spread across patients.
* They help identify unusual patterns.
* The **interquartile range (IQR)** is used to detect outliers, meaning noisy values far from the rest of the data.
* A **box plot** is used to visualize the quartiles and outliers.

The median (Q2) is not shown separately by `describe()`, but it appears as the 50% row.

---

## 9. AI-Assisted Analysis with Gemini in Colab

Google Colab includes a built-in Gemini assistant (Gemini 2.5 Flash was used in the session). It can generate plots from a plain-language prompt: the generated code is reviewed and then run with **Accept and run**.

### Univariate analysis

Prompt used: *create three univariate plots on this dataset.*

The plots included the distribution of gender and the distribution of doctor visits.

### Bivariate analysis

* **Doctor visits by gender:** the data was grouped by gender to get the count, mean and median of visits, and then plotted.

```python
df.groupby('gender')['visits'].agg(['count', 'mean', 'median'])
```

* **Illness score versus doctor visits:** as the illness score increases, doctor visits also increase.

### Multivariate analysis

Prompt used: *create a multivariate plot on this dataset.*

Gemini inspected the dataset and produced plots combining several variables, such as doctor visits by gender.

### Important point

AI can build the plots, but basic knowledge of the dataset, Python and the libraries is still needed. It makes it possible to notice and correct wrong output. The recommendation was to **integrate AI into the work, not depend on it blindly**.

---

## 10. Preparing the Project PPT

The PPT template is downloaded from the DIY project page on the VOIS LMS. Its sections were filled in as follows:

| Slide | What to add |
| ----- | ----------- |
| Title | Project name and your own name (for example, "Healthcare Doctor Visit TIRTC") |
| Problem statement | The problem the project solves, in your own words |
| Project description | What the project does and how it is used |
| End users | Who benefits from the project |
| Technology used | Python, Pandas, NumPy, Matplotlib and Seaborn |
| Results | Screenshots of the Colab outputs. Duplicate the slide to add more results |

### File name format

```text
YourName_ProjectName_DIY Project
```

The file name should start with your name, followed by the project name, then "DIY Project".

---

## 11. Submitting on the VOIS LMS

1. Open the project on the LMS and click **DIY Project Submission** (Data Analytics DIY Project 2, Healthcare Analytics for Doctor Visits).
2. Click **Choose file**, select the PPT, and click **Submit**.
3. A confirmation appears once the upload succeeds.
4. The course progress bar moves to **75%** after the project is submitted.
5. Fill in the **feedback** and **rating** as well to complete the remaining requirements.

---

## 12. Submitting Through the Google Form

The separate Google Form asks for:

* Full name
* Gender
* Disability information, if applicable
* College full name (short names are not accepted)
* College state and city
* Course (for example B.Tech, BCA or MBA), stream/branch and semester
* Email ID used for the TIRTC batch on the VOIS LMS
* AICTE email ID
* Student ID (starts with `STU`)
* Contact number
* Project title: *Healthcare analytics for doctor visits*
* Project PPT upload
* A few words about the LMS
* Upload of any Data Analytics certificate you have completed
* Feedback (or "NA")

Other points:

* A GitHub link can be added if available. The demo link can be skipped.
* Uploading any Data Analytics certificate in the form is acceptable.
* The deadline was not fixed in the session. It will be announced on the Telegram group.

---

## 13. IBM Bob

**IBM Bob** was introduced as an AI-assisted software development tool that works from natural-language instructions. Using it for the DIY project is **not mandatory**. It was presented as an additional tool to learn, and completing the related certificate was recommended.

### Getting started

1. Search for **IBM Bob** and open the official page.
2. Log in first (Google, GitHub or email), then click **Download Bob**. Versions are available for Mac, Windows and Linux.
3. Run the installer (about 219 MB on Windows), accept the agreement and complete the installation.
4. Launch IBM Bob, create and open a project folder, and choose **Trust** when asked about restricted mode.
5. Click **Login to IBM Bob**, sign in through the browser and return to the app.

New accounts receive around **50 Bob coins**. After they are used, further usage has to be purchased.

### Demonstration

1. A folder was created for the healthcare project and the dataset was copied into it.
2. A single natural-language prompt was given, asking for data understanding, pre-processing, analysis and good insights with a story for every plot.
3. The tasks proposed by Bob were approved (there is an *Always approve* option).
4. In roughly five minutes Bob wrote about **507 lines of code**, generated the plots, and produced a report and a dashboard as HTML files, each with storytelling for the plots and key insights.

### IBM Bob compared with VS Code

| Aspect | VS Code | IBM Bob |
| ------ | ------- | ------- |
| Main purpose | Code editing and development | AI-assisted software development |
| Instructions | Manual coding with suggestions | Natural-language instructions |
| Workflows | Extensions and manual planning | Built-in workflows, dedicated plan mode |
| Debugging | Extensions and debuggers must be installed | Debugging and code explanation built in |
| Scope | Single files and manual steps | Multi-file tasks and agent workflows |

IBM Bob is built on the VS Code editor, which is why a `.vscode` folder appears in the project. It is aimed at enterprise modernization, and the recommendation was to explore it hands-on before judging it.

---

## 14. Questions Discussed

* **Can a Data Analytics certificate be uploaded in the submission form?** Yes.
* **Is the healthcare dataset covered up to multivariate analysis?** Yes.
* **How long do Bob coins last?** Around 30 days, and they are used up sooner with heavy use.
* **Will recordings be shared?** Yes, and instructions and links will be posted on the Telegram group.

---

## 15. Key Takeaways

* **TIRTC** — an extension of the AICTE initiative, with a separate certificate.
* **DIY project** — Healthcare Analytics for Doctor Visits, submitted on the VOIS LMS and through the separate Google Form.
* **Dataset** — 5,190 rows and 13 columns, with no missing values.
* **Business questions** — which groups visit more, how illness and health status relate to visits, chronic conditions and visit patterns, and what management should investigate.
* **Quartiles and IQR** — divide the data into four parts and help detect outliers, using box plots.
* **AI assistance** — Gemini in Colab generates plots from prompts, but the analyst must understand and check the output.
* **IBM Bob** — generates the full analysis, plots, storytelling, report and dashboard from one prompt. It is an optional tool.

---

## 16. Final Revision Sheet

| Topic | Remember |
| ----- | -------- |
| TIRTC certificate | Second certificate for extension learners |
| DIY project | Healthcare Analytics for Doctor Visits |
| Submission | VOIS LMS and a separate Google Form |
| Dataset size | 5,190 rows and 13 columns |
| Missing values | None (`df.isnull().sum()`) |
| Q1 / Q2 / Q3 | 25th percentile / median / 75th percentile |
| IQR | Used to detect outliers, shown in a box plot |
| Gemini in Colab | Generates plots from prompts, review before running |
| PPT sections | Problem statement, description, end users, technology, results |
| File name | YourName_ProjectName_DIY Project |
| IBM Bob | AI-assisted software development tool, optional |

---

## Session Reflection

This TIRTC session followed the same pattern as the AICTE sessions: a guided dataset walkthrough (shape, info, describe, missing values) followed by univariate, bivariate and multivariate analysis, this time on healthcare data.

The main difference was the submission process. Unlike the AICTE projects, this DIY project has to be submitted in two places, with its own Google Form, so the steps for the LMS, the PPT naming format and the form fields are worth revisiting before submitting.

The IBM Bob demonstration continued the AI-assisted theme from the earlier sessions (Gemini in Colab and Julius AI): AI can produce analysis, plots and reports quickly, but understanding the data and checking the output remain the analyst's job.
