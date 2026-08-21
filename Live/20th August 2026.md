Large Language Models & Data Analytics — Day 2

Date: 20 August 2026
Program: VOIS FOR TECH LD AICTE Internship Program
Session: Data Analytics — Day 2
Mode: Live Lecture + Practical Session

1. Introduction to Language Models

The session began with an introduction to Language Models and how modern Artificial Intelligence systems learn from data.

A language model is an AI model that learns patterns from language and can use those patterns to predict or generate text.

The discussion then moved toward:

Language Models
Large Language Models (LLMs)
Small Language Models (SLMs)
Parameters
How models learn internally

The important idea was that an AI model does not learn in exactly the same way that a human memorizes information.

Instead, the model learns patterns and relationships from training data through its internal parameters.

2. What is an LLM?
LLM = Large Language Model

A Large Language Model is a language model containing a very large number of learned parameters and trained on large amounts of data.

LLMs can perform tasks such as:

Understanding text
Generating text
Answering questions
Summarizing information
Translating languages
Generating code
Analyzing text

Examples of applications include AI chatbots and coding assistants.

The session focused particularly on understanding what happens internally when these models learn.

3. How Does an LLM Learn?

One of the major discussions of the session was:

How does an LLM actually learn internally?

During training, the model processes large amounts of data.

It makes predictions and adjusts its internal values so that its future predictions become better.

These internal learned values are called:

Parameters

Therefore, parameters are an important part of how the model stores what it has learned about patterns in the training data.

A simplified representation is:

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
4. Understanding Parameters

A parameter is an internal value that is adjusted during the training of a machine learning model.

Large language models can contain millions, billions, or even more parameters.

These parameters allow the model to represent complex patterns learned from its training data.

Simple Analogy — IQ and Training

The instructor explained the concept using an analogy involving IQ and learning.

Imagine two people learning the same concept.

One person may understand the concept after a small amount of training.

Another person may require considerably more training.

Similarly, AI models have internal parameters that are adjusted during training to help them learn patterns.

The session used the simplified analogy:

More parameters → greater potential learning/model capacity

However, the number of parameters alone does not guarantee that a model will always be better. Training data, architecture, training quality, and other factors also matter.

5. Parameters and Model Capability

A model with more parameters can potentially represent more complex patterns.

For example:

Smaller Model
      ↓
Fewer Parameters
      ↓
Lower Model Capacity

Compared with:

Larger Model
      ↓
More Parameters
      ↓
Greater Potential Capacity

The important concept discussed was:

Parameters are the internal values through which the model learns and represents patterns.

6. SLM — Small Language Model

The session also introduced the concept of SLMs.

SLM = Small Language Model

An SLM is a smaller language model designed with fewer parameters compared with large language models.

A simplified comparison is:

Model Type	Meaning	General Characteristic
SLM	Small Language Model	Smaller and more lightweight
LLM	Large Language Model	Larger and more capable of handling complex patterns

Smaller models can be useful when efficiency, speed, resource requirements, or deployment constraints are important.

Therefore, not every AI application necessarily needs the largest possible model.

7. AI and Agriculture

After discussing language models and parameters, the session connected AI/data analysis concepts with agriculture.

Agriculture generates large amounts of data related to environmental and soil conditions.

Examples include:

Nitrogen
Phosphorus
Potassium
Temperature
Humidity
pH
Rainfall

These factors can be analyzed to understand agricultural conditions and support better decisions.

This led to the practical activity on:

Crop Recommendation Analysis

8. Practical — Crop Recommendation Analysis

The practical session focused on a Crop Recommendation Analysis dataset.

The dataset was provided during the session and analyzed using Google Colab.

The objective was to explore the agricultural data and understand the relationships and distributions of the different features.

The practical involved using:

Python
Pandas
DataFrames
Statistical analysis
Data visualization
Exploratory Data Analysis (EDA)
9. Google Colab

The practical work was performed using Google Colab.

Google Colab provides a browser-based environment where Python code can be executed.

It is useful for data analytics because libraries such as Pandas and visualization libraries can be used directly inside notebooks.

The practical workflow was broadly:

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
10. Pandas

Pandas is an important Python library used for data manipulation and analysis.

It provides data structures such as:

DataFrame

A DataFrame can be thought of as a table containing rows and columns.

For example:

import pandas as pd

A dataset can then be loaded into a DataFrame.

df = pd.read_csv("dataset.csv")

Here:

pd → Pandas
df → DataFrame containing the dataset
11. Understanding the DataFrame

The variable df was used to work with the dataset.

Simply displaying:

df

allows us to view the DataFrame.

This gives us an initial understanding of:

Rows
Columns
Values
Features
Dataset structure

Before performing analysis, it is important to first understand what data we actually have.

12. First Rows of the Dataset

The first few rows can be viewed using:

df.head()

This is useful for quickly checking:

Column names
Sample values
Data format
Whether the dataset loaded correctly

Similarly:

df.tail()

can be used to view the last few rows.

13. Dataset Shape

The dimensions of a DataFrame can be checked using:

df.shape

The result is represented as:

(rows, columns)

For example:

(1000, 8)

would mean:

1000 rows
8 columns

The important point is:

shape tells us the size of the dataset in terms of rows and columns.

14. Dataset Information — df.info()

The session also covered:

df.info()

This provides a structural overview of the DataFrame.

It can show:

Number of entries
Column names
Non-null counts
Data types
Memory usage

This is useful because before analyzing a dataset, we need to know what type of information each column contains.

15. Data Types

Different columns can contain different types of data.

For example:

Numerical Data

Examples:

Temperature
Humidity
Rainfall
pH

These contain numerical values.

Categorical Data

Examples:

Crop names
Categories
Labels

These represent groups or categories rather than continuous numerical measurements.

Understanding the data type is important because different types of data require different analysis and visualization techniques.

16. Statistical Summary — df.describe()

The session also covered:

df.describe()

This provides a statistical summary of numerical columns.

It can include:

Statistic	Meaning
count	Number of observations
mean	Average
std	Standard deviation
min	Minimum value
25%	First quartile
50%	Median
75%	Third quartile
max	Maximum value

This allows us to quickly understand the numerical characteristics of the dataset.

For example, looking at the minimum and maximum temperature can immediately show the range of observed temperatures.

17. Exploratory Data Analysis — EDA

A major part of the practical was Exploratory Data Analysis (EDA).

EDA = Exploratory Data Analysis

EDA is the process of exploring and understanding a dataset before making conclusions or building models.

The goal is to discover:

Patterns
Distributions
Relationships
Trends
Unusual observations
Outliers
Important variables

A simplified workflow is:

Dataset
   ↓
Understand Structure
   ↓
Statistics
   ↓
Visualization
   ↓
Relationships
   ↓
Outliers
   ↓
Insights
18. Univariate Analysis

The session covered Univariate Analysis.

The word:

Uni = One

Therefore, univariate analysis means analyzing one variable at a time.

Example

Suppose we analyze only:

Temperature

We may investigate:

Minimum temperature
Maximum temperature
Average temperature
Distribution of temperature
Potential outliers

Similarly, we could analyze only humidity.

Main Question

What does this one variable look like?

Histograms and other distribution visualizations can be useful for univariate analysis.

19. Bivariate Analysis

The session also covered Bivariate Analysis.

The word:

Bi = Two

Bivariate analysis studies the relationship between two variables.

For example:

Temperature
      ↕
Humidity

Or:

Rainfall
    ↕
Crop

The purpose is to understand whether two variables have some relationship or pattern.

Main Question

How are these two variables related?

Depending on the types of variables, visualizations such as scatter plots or bar charts can be used.

20. Multivariate Analysis

The third concept was Multivariate Analysis.

The word:

Multi = Many

Multivariate analysis involves analyzing multiple variables together.

In the crop recommendation dataset, multiple agricultural factors can be considered simultaneously.

For example:

Nitrogen
Phosphorus
Potassium
Temperature
Humidity
pH
Rainfall
      ↓
Crop Recommendation

This is useful because agricultural decisions generally depend on multiple factors rather than only one variable.

Main Question

How do multiple variables interact or relate to the outcome?

21. Univariate vs Bivariate vs Multivariate
Analysis	Number of Variables	Main Question
Univariate	1	What does this variable look like?
Bivariate	2	How are these two variables related?
Multivariate	3+	How do multiple variables interact?
Easy Way to Remember
Uni       → One
Bi        → Two
Multi     → Many
22. Histograms

Histograms were also used to understand the distribution of numerical data.

A histogram represents numerical values using ranges called bins.

For example, temperature data could be divided into:

10–15
15–20
20–25
25–30
30–35

The histogram then counts how many observations fall into each range.

23. What Are Bins?

A bin is a range or interval used to group numerical values in a histogram.

Suppose we have:

12, 14, 16, 18, 21, 22, 24, 27, 29

We could create bins such as:

10–15
15–20
20–25
25–30

The values are grouped into their corresponding ranges.

The histogram then displays the number of observations in each range.

Conceptually:

10–15    ███
15–20    ██
20–25    ███
25–30    ███

Therefore:

Bins divide continuous numerical data into ranges so that its distribution can be visualized.

24. Number of Bins

The number of bins affects how a histogram looks.

Fewer Bins
Large ranges
↓
Simpler visualization
↓
Less detail
More Bins
Smaller ranges
↓
More detail
↓
Potentially more noise

Therefore, selecting a suitable number of bins helps produce a useful representation of the data distribution.

25. Bar Chart vs Histogram

The session also discussed the difference between bar charts and histograms.

Although they look visually similar, they represent different types of information.

	Bar Chart	Histogram
Data	Mainly categorical	Numerical
X-axis	Categories	Numerical intervals/bins
Purpose	Compare categories	Show distribution
Bars	Usually separated by gaps	Normally touch
Example	Crop names	Temperature ranges
Bar Chart

A bar chart can be used to compare categorical values.

Example:

Rice     ███████
Wheat    █████
Maize    ███

The categories are independent.

Therefore, gaps between bars can be used.

Histogram

A histogram represents continuous numerical ranges.

10–15   ███
15–20   █████
20–25   ███████
25–30   ████

The bins represent connected numerical intervals.

Therefore:

Histogram bars normally touch because the numerical intervals are continuous.

26. Data Distribution

The histograms helped in understanding the distribution of different numerical features.

A distribution shows how the values of a variable are spread across its possible range.

For example, we can investigate the distribution of:

Temperature
Humidity
Rainfall
pH
Nutrient values

This helps identify where most observations are concentrated.

It can also help reveal unusual or extreme values.

27. Violin Plot

Another visualization covered during the session was the Violin Plot.

A violin plot combines information about the distribution of numerical data with the visual structure of a box-plot-like summary.

It can help us understand:

Distribution
Spread
Density
Central region of the data
Potential unusual observations

The width of the violin represents the density of observations at different values.

For example:

      ╭──╮
     ╭╯  ╰╮
    ╭╯    ╰╮
    │      │
    ╰╮    ╭╯
     ╰╮  ╭╯
      ╰──╯

A wider section indicates that more observations are concentrated around that region.

Why Violin Plots Are Useful

A box plot provides a compact summary, while a violin plot can provide additional information about the shape and density of the distribution.

Therefore:

Violin plots are useful for understanding the distribution and density of numerical data.

28. Outliers

The practical also involved identifying outliers.

An outlier is a value that is unusually far from the general pattern of the observations.

For example, if most temperature values are within a particular range but a few observations are extremely high or low, those observations may be potential outliers.

During the crop recommendation analysis, potential outliers were identified in:

Temperature
Humidity
29. Why Outliers Matter

Outliers can influence statistical analysis and visualizations.

For example, an extreme value can affect:

Mean
Range
Standard deviation
Distribution
Visualization

However:

An outlier does not automatically mean that the data is wrong.

An unusually high temperature or humidity value may represent a genuine environmental condition.

Therefore, outliers should be investigated before deciding what to do with them.

30. Outliers in the Crop Dataset

During the practical, the temperature and humidity distributions were examined to identify unusual observations.

The process can be summarized as:

Analyze Temperature
        ↓
Visualize Distribution
        ↓
Identify Potential Outliers
        ↓
Analyze Humidity
        ↓
Visualize Distribution
        ↓
Identify Potential Outliers

This demonstrated how visualization can help us notice unusual patterns that may not be obvious from looking at raw values alone.

31. Data Visualization in EDA

The practical demonstrated that different visualizations answer different questions.

Visualization	Useful For
Bar Chart	Comparing categories
Histogram	Numerical distribution
Violin Plot	Distribution and density
Box Plot	Spread and potential outliers

Choosing the correct visualization depends on the type of data and the question we want to answer.

32. Overall EDA Workflow

The practical work can be summarized as:

Load Dataset
      ↓
Create DataFrame
      ↓
Inspect Data
      ↓
df.head()
      ↓
df.shape
      ↓
df.info()
      ↓
df.describe()
      ↓
Understand Data Types
      ↓
EDA
      ↓
Univariate Analysis
      ↓
Bivariate Analysis
      ↓
Multivariate Analysis
      ↓
Visualization
      ↓
Histograms / Bins
      ↓
Bar Charts
      ↓
Violin Plots
      ↓
Outlier Analysis
      ↓
Temperature & Humidity
      ↓
Interpret Insights
33. AI/ML and Agriculture

The agricultural practical demonstrated how data can be used to understand conditions related to crop selection.

Agricultural parameters such as:

Soil/Nutrient Conditions
        +
Temperature
        +
Humidity
        +
pH
        +
Rainfall
        ↓
Crop Recommendation Analysis

This shows how data analytics and machine learning can be applied to real-world domains such as agriculture.

34. Key Concepts Covered in the Practical

The practical brought together several important data-analysis concepts.

DataFrame

A table-like data structure used by Pandas to store and analyze data.

df.info()

Provides structural information about the dataset.

df.describe()

Provides statistical summaries of numerical data.

df.shape

Returns the number of rows and columns.

Histogram

Shows the distribution of numerical values.

Bin

A numerical interval used to group values in a histogram.

Bar Chart

Used mainly to compare categorical values.

Violin Plot

Shows the distribution and density of numerical data.

Outlier

An unusually distant observation that requires investigation.

35. Important Pandas Commands Covered
import pandas as pd


df = pd.read_csv("dataset.csv")


df
df.head()
df.tail()


df.shape


df.info()


df.describe()

These commands form some of the basic building blocks of dataset exploration using Pandas.

36. Quick Revision — EDA
EDA
↓
Understand the Dataset
↓
Check Structure
↓
Check Statistics
↓
Visualize Data
↓
Find Patterns
↓
Find Relationships
↓
Identify Outliers
↓
Generate Insights
37. Quick Revision — Analysis Types
Univariate
→ One variable
→ Analyze individual distribution


Bivariate
→ Two variables
→ Analyze relationships


Multivariate
→ Multiple variables
→ Analyze complex relationships
38. Quick Revision — Visualization
Bar Chart
→ Categorical comparison


Histogram
→ Numerical distribution


Bins
→ Numerical ranges in a histogram


Violin Plot
→ Distribution + density


Box Plot
→ Spread + potential outliers
39. Quick Revision — LLM Concepts
Language Model
      ↓
Learns patterns from data
      ↓
Parameters are adjusted during training
      ↓
Learned parameters represent patterns
      ↓
Model can make predictions / generate output
LLM

Large Language Model

SLM

Small Language Model

Parameter

An internal value adjusted during model training to help the model learn patterns.

40. LLM vs SLM
Feature	SLM	LLM
Full Form	Small Language Model	Large Language Model
Model Size	Smaller	Larger
Parameters	Fewer	More
Resource Requirement	Generally lower	Generally higher
Use	Lightweight/specific applications	More complex language tasks

The session's key idea was that model size and parameters are related to the model's potential capacity, but more parameters alone do not guarantee better performance.

41. Final Session Takeaways
Language Models

Language models learn patterns from data and use those learned patterns to generate or predict language.

Parameters

Parameters are internal values adjusted during training that allow a model to learn patterns.

SLM

Small Language Models provide a more lightweight alternative to large models.

Data Analytics

Data analysis requires understanding the dataset before drawing conclusions.

Pandas

Pandas provides powerful tools for inspecting and analyzing structured data.

EDA

Exploratory Data Analysis helps discover patterns, distributions, relationships, and unusual observations.

Visualization

Different charts are appropriate for different types of data and analytical questions.

Outliers

Unusual values should be investigated rather than automatically removed.

Agriculture

Data analytics can be applied to agricultural parameters to support crop recommendation and decision-making.

42. Final Revision Sheet
Topic	Remember
Language Model	Learns patterns from language data
LLM	Large Language Model
SLM	Small Language Model
Parameter	Internal value adjusted during training
Model Capacity	Ability to represent complex patterns
Crop Recommendation	Practical agricultural data-analysis task
Pandas	Python library for data analysis
DataFrame	Table-like data structure
df	DataFrame containing the dataset
df.head()	First rows
df.tail()	Last rows
df.shape	Rows and columns
df.info()	Dataset structure and data types
df.describe()	Statistical summary
EDA	Exploratory Data Analysis
Univariate	One variable
Bivariate	Two variables
Multivariate	Multiple variables
Bar Chart	Categorical comparison
Histogram	Numerical distribution
Bin	Numerical range in a histogram
Violin Plot	Distribution and density
Outlier	Unusually distant observation
Temperature	Outliers identified/analyzed
Humidity	Outliers identified/analyzed
43. Complete Practical Flow
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