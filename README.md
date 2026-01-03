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

📁 **Output:** `live_project.csv`

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

### 🔹 Page 1 — Summary Overview

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

### 🔹 Page 2 — Attendance Impact Analysis

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

---

## 📈 Key Insights & Storytelling

### 📌 Descriptive Insights (What is happening?)
- Interns with higher attendance generally achieve higher overall performance scores.
- A significant proportion of WeekBack cases fall within the lowest attendance band (0–2).

### 📌 Diagnostic Insights (Why is it happening?)
- Attendance has a stronger impact on WeekBack decisions than individual review or task scores.
- Performance stability increases as attendance improves.

### 📌 Predictive Observations (What might happen next?)
- Interns with consistently low attendance are more likely to face future WeekBack decisions.
- Sustained attendance trends indicate improved long-term performance.

### 📌 Prescriptive Recommendations (What actions should be taken?)
- Implement early attendance monitoring mechanisms.
- Proactively flag interns in low attendance bands.
- Introduce intervention or mentoring before WeekBack decisions are required.

