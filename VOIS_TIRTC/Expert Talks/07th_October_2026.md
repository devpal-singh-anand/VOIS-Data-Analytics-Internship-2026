# Expert Talk — From Data to Decisions: Foundation, Tools & Business Analytics

**Date:** 7 October 2026<br>
**Program:** VOIS FOR TECH AICTE Internship Program<br>
**Session:** Expert Talk — Part 1<br>
**Speaker:** Mr. Anil Kumar Pande, VP Commercial, Vodafone Idea Limited<br>
**Mode:** Live Interactive Session (Zoom)

---

## Speaker Background

| Field | Detail |
|---|---|
| Role | VP Commercial, Vodafone Idea Limited |
| Experience | 25+ years across automotive, engineering, and telecom |
| Education | B.E. from NIT · MBA from Manipal University · DBN from SSBM |
| Doctoral Research | Role of AI and ML in supply chain management |

---

## Session Structure

| Part | Content |
|---|---|
| Part 1 (this session) | Analytics workflow, tool selection, telecom churn case study |
| Part 2 | Next session — Knowledge check on today's content (14th / 15th) |

**Duration:** ~45 min content + ~15 min Q&A

---

## Core Thesis

> *"Knowing the tool is not the differentiator. The differentiator is how you use your tools to solve the business problem."*

Depth in one tool matters more than surface familiarity with all tools. The relevant question is not *what tools do I know* — it is *which tool fits this problem, and can I apply it at sufficient depth to produce a useful result.*

---

## Two Knowledge Models

| Model | What It Covers |
|---|---|
| Tool Knowledge | SQL, Python, PowerBI, Excel, AI/ML — knowing how to operate them |
| Business Reasoning | Knowing *when*, *why*, and *to what depth* to apply a tool for a specific problem |

**Observation:** Tool knowledge without business reasoning produces output. Business reasoning is what makes that output useful.

---

## Analytics in Telecom — Case Study

**Dataset:** Synthetic — 1.5 lakh customers, 22 telecom circles, prepaid + postpaid mix<br>
**Problem domain:** Customer churn analysis

> All data used in the session is synthetic. Not actual Vodafone Idea customer data.

### Dataset Columns

| Column | Description |
|---|---|
| Customer ID | Unique identifier |
| Circle | Geographic telecom circle |
| Customer Segment | Prepaid / Postpaid |
| Tenure | Duration of association with the network |
| Monthly Data Usage | Data consumption pattern |
| Monthly Plan | Commercial plan type |
| Network Experience | Network quality score |
| Complaint Pending Days | Days a complaint has been open |
| Average Resolution Time | Time taken to resolve a complaint |
| Digital Engagement Score | Level of digital platform usage |
| Payment Delay | Payment behavior indicator |
| Drop Call Rate | Network call drop frequency |
| Churn Status | Whether the customer has churned (target field) |
| Churn Risk | Risk score |
| Churn Probability | Predicted probability of churn |

**Sample churn data by circle:**

| Circle | Churn % |
|---|---|
| Maharashtra | 4.7 |
| Gujarat | 4.6 |
| Madhya Pradesh | 4.5 |

---

## End-to-End Analytics Workflow

| Step | Action |
|---|---|
| 1. Define | Clarify the business problem and target decision *before* collecting data or building visuals |
| 2. Collect | Identify what data is needed |
| 3. Clean | Remove anomalies, handle missing values, standardize format |
| 4. Explore | EDA — single variable, relationships, segments, time |
| 5. Visualize | Build charts that answer the business question |
| 6. Recommend | Derive evidence-backed recommendations from analysis |
| 7. Monitor | Track outcomes after action is taken |

**Analogy:** Mirrors the PDCA cycle — Plan, Do, Check, Act.

---

## Step 1 — Define

**Why this step matters most:**
- A poorly defined problem produces misdirected analysis, regardless of how well the tools are applied.
- Without a clear definition, visuals and analysis have no decision to support.

**What a well-formed business question looks like:**

| Weak | Strong |
|---|---|
| Can you build a churn model? | Which customer segment and geography shows the highest churn, and which intervention should be tested first? |

**Formula:**
> *Which outcome varies across which dimensions, during which period, and for which decision?*

**Observation from DIY project review:** Most projects had solid analysis and visuals, but the problem definition was missing or disconnected. The analysis did not trace back to a specific decision.

---

## Step 3 — Clean: Data Quality

**Philosophy: GIGO — Garbage In, Garbage Out**

The quality of the output is a direct function of the quality of the input. Cleaning is the analyst's responsibility — not the tool's.

### Common Issues and Actions

| Issue | Action |
|---|---|
| Missing values | Treat based on meaning, missing pattern, distribution, and business context |
| Duplicate IDs | Identify and remove |
| Incorrect format | Standardize before analysis |
| Misfit entries | Investigate; exclude if irrelevant to the analysis |

**Quiz from session:** *Should every missing numeric value be replaced with the average?*<br>
**Answer:** No. Treatment depends on why the value is missing and what the business context requires. No single method applies universally.

---

## Step 4 — Explore: EDA Dimensions

| Type | Telecom Example |
|---|---|
| Single variable | Churn by tenure |
| Relationship | Churn by average resolution time |
| Segment | Churn by customer type, age group, geography |
| Time | Churn rate this month vs. 1 month / 6 months out |

**Filters applicable to churn data:**
- Age group
- Geography (circle → city → specific area)
- Data usage level (high / low)
- Tenure bracket (< 3 months, < 6 months, > 1 year, > 5 years)

**Caution:** Association does not establish causation. Small subgroups require careful interpretation before drawing conclusions.

---

## Analysis Plan Template

| Element | Description |
|---|---|
| Business Question | What are we trying to solve? |
| Target Metric | What outcome are we measuring? |
| Dimensions | Along what axes do we segment? |
| Filters | What constraints narrow the scope? |
| Required Fields | Which columns are needed? |
| Quality Checks | What data gaps or anomalies exist? |
| Intended Visuals | What charts will answer the question? |
| Decision Supported | What action does this analysis enable? |

All eight elements must connect. Strong visuals (element 7) without a clear business question (element 1) or a supported decision (element 8) produce no actionable output.

---

## Tool Selection — Tool Chain Principle

**Don't rely on one tool:** A single tool rarely handles every aspect of a problem.<br>
**Don't apply all tools:** Using every available tool adds complexity without adding insight.

**Right approach:** Select the tool that fits the task within the problem.

| Task | Appropriate Tool |
|---|---|
| Querying and filtering structured data | SQL |
| Automating repetitive analysis | Python |
| Dashboards and visualization | PowerBI |
| Quick tabular analysis, formulas | Excel |
| Pattern recognition and prediction | AI/ML |

**Analogy from session:** Algebra, trigonometry, and geometry are all mathematics — but you don't apply all three to every problem. You use what the problem requires.

---

## DIY Project Review — Gaps Observed

| Project | Gap |
|---|---|
| Bike Sharing Demand Prediction | Missing link between stated goal and data used |
| Mental Fitness Tracker | Recommendations not validated against evidence |
| Sentiment Analysis for Restaurant Reviews | Recommendations not validated against evidence |
| Cardiovascular Risk Prediction | — |
| Credit Card Fraud Detection | — |
| Employee Burnout Analysis and Prediction | — |
| Telecom Customer Retention | — |

**Common pattern:** Visuals and analysis were generally solid. The recurring gap was in problem definition and in connecting recommendations back to what the data actually supported.

**On AI-generated output:** AI tools can assist with analysis, but output must be validated against real-world evidence before making any recommendation. Treating AI output as ground truth is not analysis.

---

## Q&A — Key Points

**Q: How do I master data science / data analytics?**

Tools will keep changing. What remains constant is the ability to ask the right question, select the appropriate method, analyze the data correctly, and produce a supported recommendation. That ability matters more than knowing any specific tool at an advanced level.

**Q: If everyone knows the same tools, how do I differentiate?**

Knowing the tool is not the differentiator. Knowing how to apply it to a specific business problem is.

**Q: I'm from a non-tech background. Can I do data analytics?**

Domain familiarity matters. Take a project on a subject you actually understand. Define your own problem statement. Find or build relevant data. Apply tools to it. Don't copy-paste other projects — run the analysis yourself.

**Q: I have a career gap. Will that be a problem?**

Staying current with business problems and industry trends matters more than unbroken employment. A relevant skill set paired with awareness of what's happening in the field is sufficient.

**Q: Is AI just hype?**

The hype is significant, but the underlying capability is real. Don't let the hype drive learning decisions. Start with problems you can observe and understand, define them clearly, and build from there.

---

## Key Concepts

| Concept | Description |
|---|---|
| GIGO | Garbage In, Garbage Out — data quality determines output quality |
| Churn | Customers leaving the network / organization |
| Tool Chain | Using the right combination of tools based on problem type |
| Business Reasoning | Knowing when and why to apply a tool, not just how to operate it |
| Evidence Validation | Checking AI or tool output against real-world evidence before recommending |
| PDCA | Plan → Do → Check → Act — mirrors the analytics workflow |
| Sentiment Analysis | Predicting customer behavior or intent before an event (e.g., pre-churn signals) |
| Knowledge Check | Quick recall quiz — tests how much of a session's content was retained |

---

## Announcements

| Item | Detail |
|---|---|
| DIY Project Deadline | 10 October 2026 |
| Submission | LMS (DIY Project tab) + Google Form |
| Next Session | 14th / 15th — dip check on today's content |
| Unanswered Q&A | Responses will be shared before the next session |
| Feedback Form | Shared at end of session — include remaining questions in remarks |
