# HR Analytics Employee Attrition &amp; Performance
## Overview
This project collects and analyses the factors that lead to employee attrition and explore important questions.
## File URL: https://github.com/oakindeji1/HR-Analytics-Employee-Attrition-amp-Performance/blob/main/WA_Fn-UseC_-HR-Employee-Attrition%20analysis.xlsx

## Data Collected
### The dataset includes the following key columns:

1 Education ('Below College', 'College','Bachelor','Master','Doctor')
  
2 EnvironmentSatisfaction ('Low','Medium', 'High','Very High') 

3 JobInvolvement ('Low', 'Medium' ,'High', 'Very High')

4 JobSatisfaction ('Low','Medium','High','Very High')

5 PerformanceRating ('Low','Good','Excellent','Outstanding')

6 RelationshipSatisfaction ('Low','Medium','High','Very High')

7 WorkLifeBalance ('Bad','Good','Better','Best') etc

## Project Objectives
This project was designed to address the following analysis goals:

## Overall Information
| Total Number of Employees |
|---------------------------|
|1470                       |

| Total Number of Department|
|---------------------------|
|3                          |
                
| Row Labels Count of Gender|
|---------------------------|
|Female	       40%          |
|Male	       60%          |


## Employee Attrition Analysis

### Objective: Identify factors related to employee attrition (i.e., why employees leave).
### Approach:
- Use Pivot Tables to analyze attrition rates across different departments, job roles, and age.
- Calculate attrition percentage by filtering the Attrition column, and then check for patterns based on age, gender, department, and job role.
  
## Initial Insights from the Data



### Overall Attrition Rate:
- The proportion of employees leaving the organization is noticeable, but the majority are retained. This provides a baseline for further analysis.
 ![image](https://github.com/user-attachments/assets/5fb450f0-08c8-4099-9cc6-5d11c6c07d28)
 
 
### Attrition by Department:
![image](https://github.com/user-attachments/assets/ada30c65-5fa8-468f-b0ad-5499e12183fe)

- Some departments experience higher attrition rates than others. For example, Sales might see more attrition compared to Research & Development, signaling potential areas for targeted retention strategies.

## Employee Satisfaction and Engagement Insights
### Objective: Evaluate levels of job satisfaction and Compensation Analysis
### Approach:
- Use Average and Count functions on satisfaction-related columns (e.g., JobSatisfaction and RelationshipSatisfaction).
- Conditional Formatting can visually highlight satisfaction levels across different departments or roles, helping to identify areas where improvements may be needed.
## Insights from Compensation and Satisfaction Analysis

### Attrition and Monthly Income:
Attrion	Average of MonthlyIncome	StdDev of MonthlyIncome2
No		6832.74				4818.21
Yes		4787.09				3640.21

Employees who leave generally have lower monthly income levels compared to those who stay. This suggests that compensation may be a key factor influencing retention.

### Attrition by Job Satisfaction:
![image](https://github.com/user-attachments/assets/860a6d05-3ee4-4cd5-a7dd-397111512169)

Lower job satisfaction levels are associated with higher attrition rates. Employees reporting high or very high satisfaction are less likely to leave, emphasizing the importance of maintaining engagement and morale.

## Demographic Analysis
### Objective: Understand workforce composition in terms of age, gender, education.
### Approach:
- Generate Demographic Profiles by analyzing columns such as Age, Gender, Education, and Department.
- Use Charts (e.g., pie charts) to visualize age distribution and departmental gender ratios.
- Pivot by EducationField to understand the educational backgrounds of your workforce and how these relate to job roles or satisfaction.

  ### Attrition by Age Group:
![image](https://github.com/user-attachments/assets/4437420a-0e8b-4e99-a2c0-6b49c931f6df)

Younger employees (e.g., 19-34 age group) exhibit higher attrition rates compared to older employees. This trend may reflect early-career exploration or dissatisfaction with growth opportunities.

### Attrition by Gender:
![image](https://github.com/user-attachments/assets/e236c387-775c-40b2-92fe-ca09b1e07d99)

- Employees with bachelor degrees tends to have a  different attrition patterns which higher. May be they are moving to have a greener pasture.
  
### Attrition by Education:
 
 ![image](https://github.com/user-attachments/assets/9f2c3ff0-0ee5-4d48-908f-74f9defe7852)

- Male and female employees exhibit slightly different attrition patterns. Exploring further could reveal if certain roles, job levels, or satisfaction metrics contribute to these differences.
  
## Work Experience and Tenure Analysis
### Objective: Assess employee tenure and promotion frequency.
### Approach:
- Calculate averages for YearsAtCompany, YearsInCurrentRole, YearsSinceLastPromotion, and YearsWithCurrManager to get insights into employee tenure.
- Pivot and filter by Attrition to see if shorter tenures correlate with higher turnover.
- Use Charts to illustrate the typical career progression (e.g., time between promotions or average years in current role) to help plan development initiatives.

### Attrition by Employee Tenure:
 ![image](https://github.com/user-attachments/assets/fe498545-44d1-4f4a-8656-e9833be5daf7)

- It was observed that employees with more than 10 years of service exhibit slightly different attrition patterns. In contrast, those with 1 to 10 years of tenure may not have fully established their footing within the organization, potentially leading to higher attrition rates.

### Attrition by Promotion Frequency:

![image](https://github.com/user-attachments/assets/e5e9dccf-ced1-4b15-9f87-8eb06a118efb)

 
  
- If employees promoted within the last five years exhibit higher attrition rates, it suggests that promotion might not necessarily be a factor driving them to leave.

## Formula Used
```   Formula:
Attrition Rate (%) = (Number of Employees Who Left / Total Number of Employees) × 100
```
- Age Grouping

    =CHOOSE(MATCH(A2,{0,19,35,50,65},1),"18 and Under","19-34","35-49","50-64","65 and Over")
  
- Attrition Encoded

    Find and Replace
  
- BusinessTravel Encoded

    =IF($E2="Travel_Rarely", 1, IF($E2="Travel_Frequently", 2, IF($E2="Non-Travel", 3,"")))
  
- Education

    =SWITCH(TRUE(),K2=1,"Below College",K2<=2,"College",K2=3,"Bachelor",K2=4, "Master","Doctor")
  
- JobInvolvement, JobSatisfaction Encoded, Performance Rating, and Relationship Satisfaction

    =IFS(P2=1,"Low",P2=2,"Medium",P2=3,"High",P2=4,"Very High",TRUE," ")

## Tools and Methods Used

- Data Analysis: The data was analyzed using Microsoft Excel, utilizing Pivot Tables to organize, summarize, and filter the data for easier interpretation.

- Data Visualization: Bar Charts were created in Excel to visually represent the key insights.

## Action Performed

- I put my data into a Table, removed all the formulaes by pasting real values and added it to a data model.
- I noticed my pivot Table was showing blank whereas i do not have any blank row; Solution applied was clean(trim(Cell))

## Dashboard
![image](https://github.com/user-attachments/assets/6bc05f61-9d3e-48fc-92f2-ad5076b54ebf)
			






