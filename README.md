# San-Francisco-Intern-Salaries
This project analyse extracted data of salaries of San Francisco interns salaries from 2011 - 2014.

## Table of Contents

- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools](#tools)
- [Data Cleaning/Preparation](#data-cleaning-process)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Data Analysis](#data-analysis)
- [Results and Findings](#results-and-findings)
- [Recomendations](#recommendations)
- [Limitations](#limitations)
- [References](#references)


### Project Overview

This projects analyzes the employee data for San Francisco city workers from 2011 to 2014. The aim of this project is to explore compensation trends, differences across job titles and employment status and the impact of overtime pay, providing actionable insights for workforce management.


### Data Sources

Sales Data: The primary dataset used for this analysis is the "Salaries.csv" file, containing detailed information about employee compensation details fro SF city employess from 2011 to 2014. Full-time (FT) and part-time (PT) workers in a variety of occupations are represented in the dataset's 148,654 records. Reliability is ensured by the data's source, San Francisco's government transparency programs.

### Questions

1. What is the average Total Pay (excluding benefits) by Job Title for employees in San Francisco for each year, and how does it trend over time?

2. How does the distribution of Total Pay Benefits vary by Status (FT/PT) across different Agencies in 2011?

### Tools
- Excel (Data Cleaning)
- pgSQL (Data cleaning, querying and aggregation)
- Python (Numpy - Computations
          SciPy - statistical testing
          Panda - additional processing)
- Power BI - (Data visualization)

### Data Cleaning/Preparation Process

In the initial data preparation phase, we performed the following tasks:

1. Handled missiong values or inconsistent values: 'Not provided' was replaced with 'NULL' using Excel
2. Rows that had all null cells were deleted
3. Dataset were inspected fro missing or inconsistent values, particularly in Base Pay, Overtime Pay and Benefits columns which had null or zero entries
4. Ensured numerical columns (e.g., TotalPay, TotalPayBenefits) were float for accurate computations
5. All columns were checked to ensure that only the ones with contents were kept (especially the notes column)


### Data Extraction and Querying
1. Table Creation and Data Loading (csv file import)
   
<img width="366" alt="Screenshot 2025-06-18 at 04 47 58" src="https://github.com/user-attachments/assets/5397a439-66bd-4f60-911f-e125828ef3e6" />

3. Upper case strings
The Job_tile and Employee_name were set to upper case using SQL

<img width="452" alt="Screenshot 2025-06-20 at 10 18 34" src="https://github.com/user-attachments/assets/4201fbd8-4916-42f0-9a98-a25095feda12" />


3. Data Extraction using pgSQL

<img width="274" alt="Screenshot 2025-06-19 at 21 59 55" src="https://github.com/user-attachments/assets/e21a1b3d-9ae8-4ae4-9caa-1f405da75428" />

4. Handling missing data

<img width="563" alt="Screenshot 2025-06-20 at 13 02 56" src="https://github.com/user-attachments/assets/9fd2ad8d-e2f2-4af3-88d1-42399ff0783d" />


### Question 1: What is the average Total Pay (excluding benefits) by Job Title for employees in San Francisco for each year, and how does it trend over time?

1. Data Aggregation using SQL 
This query allows aggregation of the Total Pay by Job title and year showing how average pay changes over time for different roles.

<img width="520" alt="Screenshot 2025-06-20 at 15 06 41" src="https://github.com/user-attachments/assets/39073b64-bc57-46bb-8e7a-774aa0911717" /> 

2. Data Aggregation using Python 
Alternatively, pandas can be used for data grouping and aggregation




### Exploratory Data Analysis









