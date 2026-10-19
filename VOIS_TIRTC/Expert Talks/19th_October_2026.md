# Expert Talk — Data Analytics, Decision-Focused Dashboards, AI & Career Readiness

**Date:** 19 October 2026<br>
**Session:** Decision-focused dashboards, responsible AI use and portfolio building<br>
**Speaker:** *Not specified in the summary*<br>
**Mode:** *Not specified in the summary*

---

## Core Thesis

> *"A data model should support decisions, not merely provide decoration."*

Every chart, metric and filter has to earn its place by answering a business question. The goal is not a polished dashboard. The goal is to help a stakeholder spot a problem and decide what to do next.

Knowing every tool does not make someone a data analyst. A person can know Excel, SQL and Power BI and still not be one if the dashboards look beautiful but fail to show the insight. What makes an analyst is the ability to make the dashboard show the real output.

---

## Session Structure

| Theme | Content |
|---|---|
| Build | Dataset to Power BI model, toolchain, dashboard design |
| Reason | Observation → insight → recommendation, evidence-to-action framework, analytics maturity |
| Responsibility | Using AI responsibly, validating output against evidence |
| Career | Portfolio, what recruiters look for, six-month roadmap |

---

## From Dataset to Power BI Model

**Workflow demonstrated:**

| Step | Action |
|---|---|
| 1. Import | Load the dataset |
| 2. Type check | Verify data types and data quality |
| 3. Measures | Calculate the important metrics |
| 4. Bands | Classify records into meaningful categories (e.g., resolution-time bands) |
| 5. Visuals | Represent findings through charts and KPIs |
| 6. Slicers | Allow interactive filtering |
| 7. Interpret | Translate results into business insight |

**Example dashboard metrics:**

| Metric | Value |
|---|---|
| Customers | 200 |
| Churn rate | 7.5% |
| High-risk customers | 5 |
| Average resolution time | 15.9 hours |

**Observation:** The sequence ends with *interpret*, not *visualize*. A dashboard that stops at charts has not yet done the analyst's job.

---

## How the Analytics Toolchain Works Together

**Principle:** Choose the simplest reliable tool for each task.

| Tool | Primary Purpose |
|---|---|
| Excel | Inspect and explore data |
| SQL | Extract and aggregate data |
| Python | Clean, analyse and automate |
| Power BI | Visualise and monitor results |
| AI | Draft queries, checks and summaries |
| Analyst | Validate evidence and context |
| Business stakeholders | Prioritise actions and KPIs |

**Q: Which tool should be selected first?**

Start with the business question, then select the tool that answers it reliably.

---

## Designing a Decision-Focused Dashboard

**Rule:** Every visual should answer a business question.

| Section | Content |
|---|---|
| Top row | Customer count, churn rate, high-risk customers, resolution time |
| Middle row | Customer segments, complaint counts, tenure |
| Bottom row | Resolution, customer experience, exceptions |
| Filters | Circle, plan, segment |

**In-session exercise:** Two charts were shown, with the question — *Which pattern should be investigated first, and what additional data would you request?*

The exercise tests three things: spotting a potentially meaningful pattern, prioritising it for investigation, and deciding what further evidence is needed before drawing any conclusion.

---

## Observation, Insight and Recommendation

Strong analytical communication separates three levels of reasoning.

| Level | Meaning | Example |
|---|---|---|
| Observation | What the data shows | Churn is higher in the 25–48-hour resolution band |
| Insight | What the pattern may mean | Longer resolution may identify customers requiring deeper investigation |
| Recommendation | What should happen next | Test targeted service recovery for an eligible group |

**Caution:** Do not present an observation as a proven explanation, and do not jump directly from a pattern to an action.

---

## Evidence-to-Action Framework

A responsible recommendation contains five elements:

| Element | Question It Answers |
|---|---|
| Evidence | What does the data show? |
| Insight | Why does it matter? |
| Action | What should be tested? |
| KPI | How will success be measured? |
| Limitation | What cannot be concluded? |

| Weak | Strong |
|---|---|
| Fix complaint resolution | Validate the pattern, define an eligible group, test targeted service recovery, and track churn, repeat complaints, resolution time and retained value |

The stronger version is measurable and openly acknowledges uncertainty.

---

## Student Challenge — Responsible Recommendation

**Task:** Use the dashboard to formulate a measurable, evidence-based recommendation.

**Model answer:**

| Element | Answer |
|---|---|
| Observation | Synthetic data shows higher churn alongside more complaints and longer resolution times |
| Pattern to investigate | Customers experiencing multiple complaints or prolonged resolution |
| Additional data | Further customer, complaint, resolution and retention information to validate the pattern |
| Insight | A service-experience group may require further investigation |
| Action | Validate the pattern and test targeted service recovery |
| Success KPIs | Churn, repeat complaints, resolution time |
| Limitation | The data is synthetic, and an association between variables does not establish causation |

---

## Descriptive to Prescriptive Analytics

Analytics grows more sophisticated as the business question changes.

| Type | Question | Telecom Example |
|---|---|---|
| Descriptive | What happened? | What was the churn rate? |
| Diagnostic | Why might it have happened? | Which indicators are associated with churn? |
| Predictive | What may happen next? | Which customers may churn next? |
| Prescriptive | What should be tested or done? | Which intervention should be evaluated? |

**Observation:** Match the sophistication of the method to the business question. Not every problem needs machine learning. Use the simplest reliable method that answers the question.

---

## AI-Assisted Analytics, Used Responsibly

AI can speed up analytical work, but accountability stays with the human.

| AI Can Assist With | Analyst Remains Accountable For |
|---|---|
| Drafting SQL queries | Accuracy |
| Explaining DAX | Privacy |
| Suggesting data-quality checks | Bias |
| Generating exploratory questions | Assumptions |
| Summarising findings | Business context |
| Rewriting technical content | The final recommendation |

**In-session exercise:** Students were asked to identify an unsupported conclusion in an AI-generated response.

> *AI-generated output must be verified against evidence before it informs a decision.*

---

## Building an Industry-Ready Portfolio

A strong portfolio shows the complete decision journey, not just a list of tools.

**Journey:** Problem → Data cleaning → Analysis → Dashboard → Insight → Action → Limitation

**Required artefacts:**

| Artefact |
|---|
| Problem statement |
| Data dictionary or cleaned dataset |
| SQL or analysis file |
| Dashboard |
| One-page insight summary |
| Short presentation |
| Limitations |

**Portfolio test:** Can a recruiter understand the problem, verify the method, see the insight and follow the recommendation?

---

## What Recruiters Generally Look For in a Fresher's Projects

Depth, evidence and communication matter more than a long list of tools.

| Focus Area | What to Demonstrate | Expected Output |
|---|---|---|
| Depth over breadth | Use a few tools well, justify choices, show data-quality discipline | Cleaned-data and query project |
| Visible project | Connect a business question to cleaned data, analysis, dashboard, insight and measurable action | Dashboard and analysis notebook |
| Clear explanation | State assumptions and limitations, defend recommendations, connect work to business value | End-to-end business presentation |

**Poll in session:** When asked what the next portfolio project should prove, the chosen answer was a **hybrid** combining all three areas: technical depth, a visible end-to-end project and clear communication.

---

## Six-Month Career-Readiness Roadmap

The roadmap focuses on completing visible outputs in a practical sequence.

| Period | Focus | Output |
|---|---|---|
| Months 1–2 | Excel, data cleaning, statistics, SQL | Cleaned-data and query project |
| Months 3–4 | Power BI, Python, exploratory data analysis (EDA) | Dashboard and analysis notebook |
| Months 5–6 | Prediction, AI, communication | End-to-end business presentation |

**Central question:** Which visible output will you complete next?

---

## Q&A — Key Points

**Q: If I know Excel, SQL and Power BI and can build good-looking dashboards, am I a data analyst?**

Not necessarily. Someone can know every tool and still not be called a data analyst. If you can build professional, beautiful dashboards but cannot showcase the insight in them, you are not yet doing the analyst's job. Make sure your dashboards show the real output, not just decoration. A good test is whether a stakeholder can look at the dashboard, see the problem and know what to do next.

**Q: The dataset I got was messy, full of mixed things, and hard to work with. What should I do?**

Messy data is normal, and handling it well is part of the analyst's job. Don't start with charts. Start with the business question, then decide which columns the question actually needs. Check data types and quality, treat missing values based on what they mean rather than by one blanket rule, remove duplicates, standardise formats, and set aside entries that don't fit the problem. Note every cleaning decision in a data dictionary. Showing this discipline in a project counts for more than working with a perfect dataset.

**Q: How do I know which parts of a large, mixed dataset to use?**

Let the business question decide. If a column does not help answer the question or support the decision, it doesn't need to be in the analysis. A smaller, well-understood set of fields beats a large set used without a purpose.

**Q: Do I need machine learning for my project to be taken seriously?**

No. Match the method to the question. If a descriptive or diagnostic analysis answers it reliably, that is enough. Move to predictive or prescriptive methods only when the business question calls for them.

**Q: Can I use AI to build my project for me?**

AI can speed up the work, for example by drafting SQL, explaining DAX or suggesting data-quality checks. But the analyst stays accountable for accuracy, assumptions and the final recommendation. Verify every AI output against the evidence before using it.

**Q: How many tools should I show in my portfolio?**

Fewer, used well. Depth over breadth. A recruiter wants to see that you chose a tool for a reason and used it with discipline, not that you listed everything you have touched.

**Q: What if my data is synthetic or limited? Can I still make a recommendation?**

Yes, if you state the limitation. Frame the recommendation as something to test, not something proven, and say clearly what the data cannot show, such as the fact that an association does not establish causation.

**Q: I'm a beginner. Where do I start?**

Follow the roadmap. Spend the first two months on Excel, data cleaning, statistics and SQL, and finish a cleaned-data and query project before moving on to Power BI and Python.

---

## Closing Message — Foundations and Continuous Learning

No field stays static, and every field keeps advancing, so learning has no definitive endpoint. New technologies will keep building on the same basic blocks being studied today.

> *Learn the fundamentals deeply, apply them to practical problems, demonstrate your work through visible outputs, and keep adapting as technology evolves.*

---

## Key Concepts

| Concept | Description |
|---|---|
| Decision-focused dashboard | A dashboard where every visual answers a business question |
| Slicer | An interactive filter in Power BI |
| Observation / Insight / Recommendation | What the data shows / what it may mean / what should happen next |
| Evidence-to-Action | Evidence, Insight, Action, KPI, Limitation |
| Descriptive → Prescriptive | What happened → why → what next → what to do |
| Responsible AI use | AI assists; the analyst stays accountable for accuracy, privacy, bias, assumptions and the final call |
| Portfolio test | Can a recruiter follow the problem, method, insight and recommendation? |
| Depth over breadth | A few tools used well beats a long list used shallowly |
