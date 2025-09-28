# Data Analyst Job Market — SQL Insights

This project explores the **Data Analyst** job market to identify:
- Top-paying roles  
- Skills those roles require  
- Skills most demanded by the market  
- Skills tied to higher salaries  
- The **optimal** skills to learn (where demand meets pay)

---

## Tools
SQL (PostgreSQL) · Visual Studio Code · Python (pandas, matplotlib)

---

## Q1 — Top-Paying Data Analyst Jobs
**Query goal:** Select the highest-paying remote (“Anywhere”) Data Analyst roles.

**Examples of top roles:**  
- Data Analyst — Mantys — **$650,000**  
- Director of Analytics — Meta — **$336,500**  
- Associate Director – Data Insights — AT&T — **$255,830**  
- Data Analyst, Marketing — Pinterest — **$232,423**  
- Data Analyst (Hybrid/Remote) — UCLA Health — **$217,000**  

**Takeaway:** Senior/lead titles and big-brand employers dominate the top salary range.

---

## Q2 — Skills Required for the Top-Paying Jobs
**Query goal:** Take the top 10 highest-paying jobs from Q1 and list their required skills.

**Most frequent skills among those jobs:**  
**SQL**, **Python**, **Tableau**, **R**, along with **Snowflake**, **Pandas**, **Excel**, and some cloud tools.

**Takeaway:** Core analytics stack (SQL + Python + BI) is essential even at the top end.

---

## Q3 — Most In-Demand Skills
**Query goal:** Rank skills by frequency across all Data Analyst postings.

**Top skills (ordered):**  
**SQL**, **Excel**, **Python**, **Tableau**, **Power BI**  

![Top 5 In-Demand Skills](assets_q3_top5.png)

**Takeaway:** The foundational toolkit (SQL/Excel/Python/BI) remains the market baseline.

---

## Q4 — Skills Associated with Higher Salaries
**Query goal:** Compute the average salary for each skill across roles with salary data.

**Highest-paying skills include:**  
**dplyr**, **solidity**, **couchbase**, **DataRobot**, **GitLab**, **Jira**, **Hadoop**, **Atlassian**, **Golang**, **Airflow**  

![Highest-Paying Skills — Top 10](assets_q4_top10.png)

**Takeaway:** Certain engineering-oriented and niche tools bring notable salary premiums.

---

## Q5 — Optimal Skills (High Demand × High Salary)
**Query goal:** On remote roles, identify skills that combine both demand and strong salaries.

**Optimal skills surfaced:**  
**Go**, **Confluence**, **Hadoop**, **Snowflake**, **Azure**, **BigQuery**, **AWS**, **Java**, **SSIS**, **Jira**, **Oracle**, **Looker**, **NoSQL**, **Python**, **R**  

![Optimal Skills — Demand vs Salary](assets_q5_scatter.png)

**Takeaway:** Pair the core stack with **cloud/big-data platforms** (Snowflake, Azure, AWS, BigQuery, Hadoop) to hit the sweet spot of **relevance + compensation**.

---

## Overall Conclusions
- **SQL is indispensable**: highest demand and present in top-paying roles.  
- **Python + BI (Tableau/Power BI)** form the must-have analyst toolkit.  
- **Cloud and Big Data** (Snowflake, Azure, AWS, BigQuery, Hadoop) deliver salary advantages.  
- Career roadmap: **master the core (SQL, Python, BI)** → add **1–2 premium platforms** to access top-tier opportunities.

---
