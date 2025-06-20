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

The SF city employee dataset (2011-2014) is used in this project to look at budget allocation for interns, pay component allocations, wage trends and possible gender-based pay discrimination. The major aim of the project is to find trends in pay among various categories, evaluate inequalities and offer information on intern budget allocation.


### Data Sources

Sales Data: The primary dataset used for this analysis is the "Salaries.csv" file, containing detailed information about employee compensation details fro SF city employess from 2011 to 2014

### Tools

- Excel (Data Cleaning)
- pgSQL (Data cleaning, querying and aggregation)
- Python (Numpy - Computations
          SciPy - statistical testing
          Panda - additional processing)
- Tableau Public - Data visualization)

### Data Cleaning Process

In the initial data preparation phase, we performed the following tasks:
1. Database creation
2. Handled missiong values: 'Not provided' was replaced with 'NULL'
3. Rows that had all null cells were deleted
4. Handled negative values: Negative values were replaced with 0
5. Data loading and inspection
6. Removed unnecessary empty spaces
7. Ensure proper calculation of the "Total Pay Benefits"
8. Ensure the years are restricted to 2011 - 2014

<img width="366" alt="Screenshot 2025-06-18 at 04 47 58" src="https://github.com/user-attachments/assets/76aed1ea-7853-414e-bcd5-dfe381263f2d" />


### Data Extraction and Querying
1. Table Creation and Data Loading (csv file import)
   
<img width="366" alt="Screenshot 2025-06-18 at 04 47 58" src="https://github.com/user-attachments/assets/5397a439-66bd-4f60-911f-e125828ef3e6" />

2. Upper case strings
The Job_tile and Employee_name were set to upper case using SQL

<img width="452" alt="Screenshot 2025-06-20 at 10 18 34" src="https://github.com/user-attachments/assets/4201fbd8-4916-42f0-9a98-a25095feda12" />


3. Data Extraction using pgSQL

<img width="274" alt="Screenshot 2025-06-19 at 21 59 55" src="https://github.com/user-attachments/assets/e21a1b3d-9ae8-4ae4-9caa-1f405da75428" />

4. 

### Exploratory Data Analysis









