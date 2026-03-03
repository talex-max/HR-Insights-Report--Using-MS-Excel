## HR Analytics Project – Attrition, Engagement and Workforce Optimization-Using-MS-Excel
Data analysis using MS Excel  to discover insights on employee attrition, compensation alignment, engagement, and workforce distribution.
### Table of Contents
- [1.	Project Overview](1.-project-overview)
- [2.	Business Problem](2.-business-problem)
- [3. Specific Questions](3.-specific-questions)
- [4. Tools and Technologies](4.-tools-and-technologies)
- [5. Data Modeling Approach](5.-data-modeling-approach)
- [6. Analysis](6.-analysis)
- [7. Key Insights](7.-key-insights)
- [8. Dashboard Features](8.-dashboard-features)
- [9. Business Impact](9.-business-impact)
- [10.	Demonstrated Skills](10.-demonstrated-skills)
- [11.	Future Improvements](11.-future-improvements)

### 1. Project Overview
This project analyzes employee attrition, compensation alignment, engagement, and workforce distribution using a structured HR dataset (CSV format).
The goal was to design a scalable HR analytics solution using **Excel, Power Pivot, and DAX** to generate executive-level insights and KPI dashboards that support data-driven HR decision-making.
### 2. Business Problem
The organization previously experienced a **33.80% attrition rate**, later reduced to **17.54%**.
Despite improvement, turnover remained a strategic risk impacting: Talent retention, Payroll efficiency, Workforce stability and Organizational performance.
This project identifies key attrition drivers and quantifies relationships between:
Tenure, Overtime, Compensation, Training frequency, Job satisfaction and Work-life balance
### 3. Specific Questions
**3.1 Attrition 1**
  - What is the overall employee attrition rate?
  - Which departments have the highest attrition rates?
  - Are employees with shorter tenure more likely to leave? 
  - Does overtime increase the likelihood of attrition? 
  - Is there a relationship between monthly income and attrition? 
  - Are high-performing employees more likely to stay? 
  - How does job satisfaction affect attrition? 
  - Are trained employees less likely to leave? 
  - Does work-life balance impact job satisfaction? 
  - Does training frequency improve performance ratings?

**3.2 Attrition 2**
  - Does attrition differ by job level?
  - Does attrition differ by job role?
  - What is the gender distribution across departments?
  - What is the average monthly income by department?
  - How does income differ by job level?
  - Which departments have the highest payroll cost?
  - How satisfied are employees across departments?
  - How does environment satisfaction relate to attrition?

### 4. Tools and Technologies
  - **Microsoft Excel**
  - **Power Pivot (Data Model)**
  - **DAX (Data Analysis Expressions)**
  - CSV Data Source
  - Interactive Excel Dashboards
### 5. Data Modeling Approach
    a. Imported HR CSV dataset into Excel Data Model - Data Grain: One row per employee
    b. Cleaned and standardized categorical variables
    c. Created calculated columns e.g.:
      - Tenure Bands
      - Income Bands
    d. Built relational structure in Power Pivot (employee-level grain)
    e. Developed reusable DAX measures for KPIs
    f. Designed executive dashboards with slicers for dynamic analysis
### 6. Analysis
First created bins (buckets) using the conditional column functionality in power query - ** Key DAX Measures **

  - ``` total_income =  SUM(hranalytics[MonthlyIncome]) ```     
  - ``` initial_headcount = DISTINCTCOUNT(hranalytics[EmployeeNumber]) ```
  - ``` % of trained employees = DIVIDE([no_employees_trained], [initial_headcount], 0) ```
  - ``` attrition_number = CALCULATE(COUNTROWS(hranalytics),hranalytics[Attrition] = "Yes") ```
  - ``` attrition_rate = DIVIDE([attrition_number], ([initial_headcount] + ([initial_headcount] - [attrition_number])) / 2) ```
  - ``` avg_job_satisfaction = AVERAGEX(hranalytics,hranalytics[JobSatisfaction]) ```
  - ``` avg_monthly_income = AVERAGEX(hranalytics,hranalytics[MonthlyIncome]) ```
  - ``` avg_performance_rate = AVERAGEX(hranalytics, hranalytics[PerformanceRating]) ```
  - ``` no_employees_trained = CALCULATE(COUNTROWS(hranalytics), hranalytics[TrainingTimesLastYear] > 0) ```
  - ``` overtime_number =  CALCULATE(COUNTROWS(hranalytics), hranalytics[OverTime] = "Yes") ```

### 7. Key Insights
The Exploratory Data Analysis (EDA) under the column of the EmplyeeNumber (PK), it was discovered that some Employee numbers were missing indicating that there was an initial attrition before this one which is currently being analysed. The last EmployeeNumber is 2068 indicating that the company had 2068 employees before with an attrition number of 598 employees hence attrition rate of 33.80% (**by considering the average number of employees at the end of the season**).
#### 7.1 Attrition and Tenure
  - Attrition reduced from **33.80%** to **17.54%**
  - Higher turnover among short-tenure employees
#### 7.2 Overtime and Burnout
  - Employees working overtime show higher attrition probability
#### 7.3 Compensation Alignment
  - Lower income bands correlate with higher turnover
  - Pay varies by job level and department
#### 7.4 Training and Development
  - Employees with frequent training show:
    - Higher performance ratings
    - Lower attrition rates
#### 7.5 Engagement and Satisfaction
  - Job satisfaction strongly predicts retention
  - Work-life balance influences engagement levels
  - Environment satisfaction impacts turnover likelihood
### 8. Dashboard Features
Interactive Excel dashboard includes for page: 

**Attrition 1:**
  - KPIs like Attrition Rate, Average job satisfaction, Average monthly income and the % of trained employees, Slicers.
  - Attrition by Department, Attrition by Job Level, Payroll Cost by Department, Income Distribution, Satisfaction vs Attrition Trends, and Training Frequency vs Performance.

**Attrition 2:**
  - KPIs like Attrition Rate, Average Job Satisfaction, Average Monthly Income and the % of trained employees, Slicers.
  - Attrition Rates by Job Level, Attrition Analysis by Job Function, Gender Diversity by Department, Mean Monthly Income per Department, Income Distribution by Career Level, Total Payroll Expenditure by Department, Employee Satisfaction Scores by Department and The Correlation between Workplace Environment and Retention.
### 9. Business Impact
This solution enables:
  - Poactive attrition monitoring
  - Data-driven compensation strategy
  - Workload risk identification
  - Training ROI analysis
  - Workforce planning optimization
### 10.	Demonstrated Skills
  - Data Cleaning and Transformation
  - Data Modeling (Power Pivot)
  - DAX Measure Development
  - KPI and Dashboard Design
  -	HR and Workforce Analytics
  - Executive Insight Communication
  - Business Problem Translation into Data Solutions
### 11.	Future Improvements
  - Build predictive attrition model (Logistic Regression / Machine Learning)
  - Automate reporting in Power BI (extended into Power BI for predictive attrition modeling and automated HR reporting)
  - Implement row-level security for HR managers
  - Integrate employee engagement survey data















  
  


