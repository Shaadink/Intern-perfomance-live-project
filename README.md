#  Intern Performance Monitoring & Evaluation System
**End-to-End Data Analytics Project | Python · SQL · Power BI**
 <img src="https://github.com/Shaadink/Intern-perfomance-live-project/blob/main/backgroundphoto...png"/>
</p>

## Project Overview

This project delivers an **end-to-end analytics solution** for evaluating internship performance using:

- **Python** for data cleaning and transformation  
- **SQL** for normalization and semantic data modeling  
- **Power BI** for dashboards, insights, and reporting  

The system analyzes **weekly intern review data** to support **academic, operational, and management decision-making**.

Each record represents **one intern’s one-week evaluation**.

---

##  Business Objectives

- Monitor intern performance on a weekly basis  
- Identify **top-performing interns**
- Analyze **WeekBack decisions**
- Understand how **attendance influences performance**
- Provide **management-ready dashboards** for decision-making  

---

##  Key Business Questions Answered

- How does attendance impact overall performance?
- What patterns lead to WeekBack decisions?
- Who are the top-performing interns based on combined metrics?
- How does performance trend over time?
- What proportion of interns are WeekBack vs Non-WeekBack?

---

##  Tools & Technologies

| Layer | Tools |
|-----|------|
| Data Processing | Python (Pandas, NumPy) |
| Data Modeling | SQL (Normalization, Constraints) |
| Analytics | DAX |
| Visualization | Power BI |
| Documentation | Jupyter Notebook, GitHub |

---

##  Dataset Overview

The dataset contains weekly internship evaluation records including:

- Student details (batch, domain, qualification)
- Review score & task score
- Attendance & discipline
- WeekBack indicator
- Reviewer and advisor information
- Student status tracking

---

##  Project Workflow

### 1️ Python – Data Cleaning & Transformation

- Removed irrelevant and audit columns  
- Handled missing values  
- Converted correct data types  
- Created derived metrics:
  - `avgScore`
  - `remarks`
  - Standardized Student, Advisor & Reviewer IDs  
- Exported analytics-ready dataset  

 **Output:** `live_project.csv`

---

### 2️ SQL – Data Normalization (1NF → 3NF)

#### ✔ First Normal Form (1NF)
- Atomic values in all columns  
- No repeating groups  

#### ✔ Second Normal Form (2NF)
- Removed partial dependencies  
- Separated into dimension tables:
  - `students`
  - `advisors`
  - `reviewers`
- Created `reviews` as the **fact table**

#### ✔ Third Normal Form (3NF)
- No transitive dependencies  
- All non-key attributes depend only on primary keys  


## 3. Power BI Dashboard

###  Page 1 — Summary Overview
 <img src="https://github.com/Shaadink/Intern-perfomance-live-project/blob/main/Dashboard%20page%201.png"/>
</p>
This page provides a high-level snapshot of overall internship performance.

**Key KPIs**
- Total Students  
- Total Reviews  
- Average Review Score  
- Overall Performance Score  
- WeekBack Count  
- Average Attendance  
- Average Discipline  

**Visuals**
- Weekly Performance Trend (Line Chart)
- Top 5 Performers Table (Ranked by Overall Performance)
- WeekBack vs Non-WeekBack Distribution (Pie Chart)
- Student Status Indicator (Active / Placed / Dropped)

---

###  Page 2 — Attendance Impact Analysis
 <img src="https://github.com/Shaadink/Intern-perfomance-live-project/blob/main/Dashboard%20page%202.png"/>
</p>

This is the **key analytical page** focusing on attendance as a performance driver.

**Visuals**
- Scatter Plot:
  - Attendance vs Overall Performance Score
  - Colored by WeekBack status (True / False)
  - Trendline to show correlation
- WeekBack Percentage by Attendance Band (Column Chart)

**Purpose**
- Identify how attendance influences performance
- Understand WeekBack risk patterns across attendance levels

- ###  Page 3 — Discipline Impact Analysis
 <img src="https://github.com/Shaadink/Intern-perfomance-live-project/blob/main/Dashboard%20page%202.png"/>
</p>

---

##  Key Insights 

###  Descriptive Insights (What is happening?)

- The dataset contains **1,164 interns** with **15,000+ weekly reviews**.
- The **average overall performance score** is **6.71**, indicating moderate performance across interns.
- **Attendance (7.40)** and **discipline (7.28)** scores are relatively high on average.
- A significant number of interns (**3,294 cases**) have faced **WeekBack**, showing performance risk exists.
- Weekly performance trends show **fluctuations**, with sudden drops and recoveries over time.
- Top-performing interns consistently score **above 8.5**, showing stable and strong performance.

---

###  Diagnostic Insights (Why is it happening?)

- **Attendance has a strong positive relationship with performance**:
  - Interns with higher attendance consistently achieve higher performance scores.
  - Most WeekBack cases occur in the **lowest attendance band (0–2)**.
- **Discipline has an even stronger impact than attendance**:
  - Interns with poor discipline show significantly lower performance scores.
  - The **highest WeekBack risk (~90%)** is observed in the **lowest discipline band (0–2)**.
- Interns with good attendance but poor discipline still face performance risks, showing that **discipline is a critical factor**.
- Performance drops seen in weekly trends are likely caused by **temporary discipline or attendance issues**, not long-term capability.

---

###  Predictive Observations (What might happen next?)

- Interns with **low attendance and low discipline** are highly likely to face future WeekBack decisions.
- Sustained improvement in attendance and discipline leads to **consistent performance growth over time**.
- If discipline issues are not addressed early, WeekBack risk remains high even if attendance improves.
- Interns maintaining attendance and discipline above **6** are unlikely to face WeekBack.

---

###  Prescriptive Recommendations (What actions should be taken?)

- Implement **early warning systems** to flag interns with:
  - Attendance below **4**
  - Discipline below **4**
- Focus mentoring efforts more on **discipline improvement**, not only academic scores.
- Introduce **weekly monitoring dashboards** for attendance and discipline.
- Provide proactive interventions (mentoring, counseling, reminders) before WeekBack decisions.
- Shift from reactive WeekBack actions to **preventive performance management**.

---

###  Key Business Insight

> Intern performance and retention are driven more by **consistent discipline and attendance** than by individual review scores alone.  
> Improving these two factors can significantly reduce WeekBack risk and improve overall outcomes.


