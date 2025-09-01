# San-Francisco-Salaries
This project analyses extracted data of salaries of San Francisco administrative and personnel analysts including the senior roles salaries from 2011 - 2014.


## Table of Contents

- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools](#tools)
- [Data Cleaning and Preparation](#data-cleaning-and-preparation)
- [Data Extraction and Querying](#data-extraction-and-querying)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Results and Findings](#results-and-findings)
- [Recomendations](#recommendations)
- [Limitations](#limitations)
- [References](#references)


### Project Overview

This projects analyses the employee data for San Francisco city of specifed analysts from 2011 to 2014. The aim of this project is to explore administrative analyst and pesonnel analysts salaries from 2011 to 2014 

### Data Sources

Sales Data: The primary dataset used for this analysis is the "Salaries.csv" file, containing detailed information about employee compensation details fro SF city employess from 2011 to 2014. Full-time (FT) and part-time (PT) workers in a variety of occupations are represented in the dataset's 148,654 records. Reliability is ensured by the data's source, San Francisco's government transparency programs.


### Questions

1. What is the average Total Pay (excluding benefits) by Job Title for administrative analyst and personnel analysts in San Francisco for each year, and how does it trend over time?

### Tools
- Excel (Data Cleaning)
- pgSQL (Data cleaning, querying and aggregation)
- Python (Pandas - Data Aggregation)
          Matplotlib - Data visualization)

### Data Cleaning and Preparation

In the initial data preparation phase, we performed the following tasks:

1. Handled missiong values or inconsistent values: 'Not provided' was replaced with 'NULL' using Excel
2. Rows that had all null cells were deleted
3. Dataset were inspected for missing or inconsistent values, particularly in Base Pay, Overtime Pay and Benefits columns which had null or zero entries
4. Ensured numerical columns (e.g., TotalPay, TotalPayBenefits) were float for accurate computations
5. All columns were checked to ensure that only the ones with contents were kept (especially the notes column)


### Data Extraction and Querying
1. Table Creation and Data Loading (csv file import)
   
<img width="424" alt="Screenshot 2025-06-23 at 11 58 12" src="https://github.com/user-attachments/assets/7c264b5f-b98f-407a-a6bd-1d17a352a472" />

2. Handling missing data and sorting

<img width="565" alt="Screenshot 2025-06-23 at 12 44 08" src="https://github.com/user-attachments/assets/6280b96c-d4b4-4812-80a1-50e87f847b64" />

<img width="654" alt="Screenshot 2025-06-23 at 15 15 59" src="https://github.com/user-attachments/assets/1aec4ffe-88a1-4286-902c-ac9ce3aaafc7" />

3. Data extraction
- The cleaned csv dataset file is saved as a new file titled "cleaned_salaries.csv"

### Exploratory Data Analysis

i. Data Aggregation using SQL
- This query allows aggregation of the Total Pay for the administrative and personnel analysts only and year showing how average pay changes over time for different roles.

<img width="651" alt="Screenshot 2025-06-24 at 10 07 00" src="https://github.com/user-attachments/assets/75fb9c79-f065-4aaa-a023-2fb34d25d5ee" />

ii. Data Aggregation using Python 
- Alternatively, python using panda library is used to aggregate the cleaned dataset 'cleaned_salaries.csv'.

<img width="643" alt="Screenshot 2025-06-24 at 10 49 43" src="https://github.com/user-attachments/assets/ecbef707-c610-4e9e-b727-a0665620a94a" />

### Results and Findings
The result of the SQL query done from data agrregation is shown below and in the csv file named 'Salaries(Personnel_and_Administrative_Analysts).csv'

<img width="422" alt="Screenshot 2025-06-25 at 08 22 20" src="https://github.com/user-attachments/assets/9d5a7470-91b6-435d-91a3-b50ff4aa5e81" />

- The Python code using panda library is shown below and in the csv file named '(Python)Salaries(Personnel_and_Admonistrative_Analysts).txt'

![Personnel and Administrative analysts](https://github.com/user-attachments/assets/ed89e244-70af-475c-ba68-7641fee3167b)

### Recommendations
 Based on the analysis of the average Total Pay (excluding benefits) for Administrative and Personnel Analysts from 2011 to 2014, the following recommendations are proposed for SF's workforce management:

- Salary Adjustments and Reviews: Both job titles show an overall upward trend in average pay, likely reflecting cost of living changes, promotions or market pressures. However, a notable dip in Personnel Analysts' salary occured in 2012 which may reflect a market anomaly, inequitable compensation practices. To address this,
  i. SF can implement annual salary reviews to ensure compensation remains competitive and equitable, particularly for Personnel Analysts
  ii. Incorporate current SF market benchmarks in each review to maintain equity and proactively correct any emerging pay disparities, especially for Personnel analysts to boost retention and morale
These steps will stabilize compensation, prevent future dips and support fair competitive pay structure

- SF needs to investigate pay flunctuation as factors like changes in workforce composition or economic conditions may come to play.
- Budgeting for overtime controls or incentives to optimize costs, especially if overtime is a significant driver for either or both roles
- Targeted Acquisition Strategies: With pay increasing to around $78,000 by 2014 for both roles, benchmark against current market rates to attract qualified analysts. Also, consider targeted recruitment for underrepresented groups or skill development programs to build internal pipelines.

### Limitations
1. The current focus is just on Total Pay, incorporating overtime pay could further reveal the impact on overall compensation.
  
### References
The San Fransisco dataset was gotten from Kaggle
