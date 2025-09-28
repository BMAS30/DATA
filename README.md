# Data Analyst Job Market — SQL Insights

This repository explores the data analyst job market to find **top-paying roles**, **in-demand skills**, and the **sweet spot where high demand meets high salary**.

> **Stack**: PostgreSQL · SQL · Visual Studio Code  
> **Focus**: 1) Top salaries, 2) Required skills, 3) Demand, 4) Salary by skill, 5) Optimal skills (demand × salary)

---


## Background

This project was driven by the need to navigate the data analyst job market efficiently: identify top-paying roles, uncover the skills they require, and prioritize skills that balance **high demand** with **high pay**.


## Research Questions

1. What are the **top-paying data analyst jobs**?
2. What **skills** are required for these **top-paying jobs**?
3. What **skills are most in demand** for data analysts?
4. Which **skills are associated with higher salaries**?
5. What are the **most optimal skills to learn** (high demand × high salary)?


## Tools

- **SQL** — backbone of the analysis
- **PostgreSQL** — database engine
- **Visual Studio Code** — development environment


## Queries & Outputs

### Top-Paying Data Analyst Jobs

**Query 1:**

```sql
/* 
Question: What are the top-paying data analyst jobs?
-Identify the top 10 highest-paying Data Analyst roles that are available remotely.
-Focuses on job postings with specified salaries (remove nulls).
-Highlight the top-paying opportunities for Data Analysts.
*/

SELECT
    job_id,
    job_title,
    job_location,
    job_schedule_type,
    salary_year_avg,
    job_posted_date,
    name as company_name
FROM
    job_postings_fact
LEFT JOIN company_dim on job_postings_fact.company_id = company_dim.company_id
WHERE
    job_title_short = 'Data Analyst' and job_location = 'Anywhere' and salary_year_avg IS NOT NULL
ORDER BY
salary_year_avg DESC
LIMIT 10
```
**Example output (mock):**

| Job Title | Company | Avg Salary (USD) |
|---|---|---:|
| Senior Data Analyst | TechCorp | 145,000 |
| Lead Data Analyst | Finance Inc. | 138,500 |

![Top-Paying Roles](assets/top_paying_jobs.png)


## How to Run

1. Create a PostgreSQL database and load the job postings dataset (tables typically include `job_postings`, `job_skills`, and `skills`).  
2. Execute the queries in `/sql/` or from the provided `.sql` file.  
3. Export results (CSV) and regenerate visuals if desired.

> **Tip**: Keep an `assets/` folder for charts and reference them in the README.


## Key Takeaways

- **SQL, Python, and BI tools** (Tableau/Power BI) dominate demand.
- **Cloud and big data skills** (AWS, Snowflake, Spark) consistently align with higher salaries.
- Focus on skills that sit at the intersection of **high demand** and **high pay** to maximize ROI on learning time.


<details>
<summary>Full SQL file</summary>

```sql
/* 
Question: What are the top-paying data analyst jobs?
-Identify the top 10 highest-paying Data Analyst roles that are available remotely.
-Focuses on job postings with specified salaries (remove nulls).
-Highlight the top-paying opportunities for Data Analysts.
*/

SELECT
    job_id,
    job_title,
    job_location,
    job_schedule_type,
    salary_year_avg,
    job_posted_date,
    name as company_name
FROM
    job_postings_fact
LEFT JOIN company_dim on job_postings_fact.company_id = company_dim.company_id
WHERE
    job_title_short = 'Data Analyst' and job_location = 'Anywhere' and salary_year_avg IS NOT NULL
ORDER BY
salary_year_avg DESC
LIMIT 10
```
</details>
