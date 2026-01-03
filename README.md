#  Internship Performance Evaluation Dashboard  
**End-to-End Data Analytics Project | Python · SQL · Power BI**

---

##  Project Overview

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

## 🛠️ Tools & Technologies

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

---

##  ER Diagram

```markdown
![ER Diagram](ER_Diagram.png)
