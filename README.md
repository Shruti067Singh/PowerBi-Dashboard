# Bank Loan Analysis & Interactive Dashboard

## Introduction

This project showcases a comprehensive analysis of bank loan data, sourced from Kaggle, visualized through an interactive Power BI dashboard. The primary objective is to delve into lending activities, understand applicant demographics, identify key trends in loan purposes, assess risk through loan status analysis (good vs. bad loans), and track financial performance metrics. This endeavor serves as a practical application of data analysis and visualization techniques for educational and demonstrative purposes, providing a clear view of the factors influencing the loan lifecycle.

## Process of Dashboard Development

The creation of this insightful dashboard involved a multi-stage process:

1. Data Sourcing & Understanding: The foundational data, a Kaggle dataset representing bank loan applications and their statuses, was acquired. An initial review was conducted to understand the variables, data types, and potential areas for cleaning and transformation.
### Dataset link: <a href= "https://github.com/Shruti067Singh/PowerBi-Dashboard/blob/main/BANK%20LOAN%20RAW%20DATA.csv">

3. Data Cleaning and Preparation (Conceptual - often in Excel/Power Query): While not explicitly detailed in the provided documents for Excel, typically, raw data like this would undergo cleaning. This might involve handling missing values, correcting data types (e.g., ensuring dates are recognized as dates, numerical values as numbers), removing duplicates, and standardizing categorical data for consistency. Power Query within Power BI is also a powerful tool for these steps.

4. Data Aggregation and KPI Calculation using SQL:
The core metrics and aggregated views for the dashboard were derived using MS SQL Server. A series of SQL queries were executed to calculate Key Performance Indicators (KPIs) and segment the data. As detailed in the MS Queries Doc link- <a href= "https://github.com/Shruti067Singh/PowerBi-Dashboard/blob/main/MS%20SQL%20BANK%20LOAN%20QUERIES.docx">, these queries included:

- Calculating total loan applications (38,576), total funded amount (approx. $435.8M), total amount received (approx. $473.1M), average interest rate (12.05%), and average Debt-to-Income (DTI) ratio (13.33%).
  
- Month-to-Date (MTD) and Previous Month-to-Date (PMTD) Metrics: Queries were designed to track performance for the current and previous months, enabling Month-over-Month (MoM) comparisons for loan applications, funded amounts, and received amounts. For instance, December 2021 saw 4,314 loan applications.

- Good vs. Bad Loan Analysis: SQL queries were used to segment loans into "Good Loans" (Fully Paid or Current) and "Bad Loans" (Charged Off). This involved calculating the percentage, number of applications, total funded amount, and total amount received for each category. For example, Good Loans constitute approximately 86% of applications, while Bad Loans are around 13-14%.
  
- Categorical Aggregations: Queries grouped data by various dimensions like loan status, month, state, loan term, employee length, purpose of the loan, and home ownership to provide data for the different charts and tables in the dashboard.

## Dashboard Design and Visualization in Power BI:
The processed and aggregated data from SQL Server was then imported into Power BI. The dashboard was designed with user experience in mind, organizing information into logical sections:
### Dashboard Link- <a href= "https://github.com/Shruti067Singh/PowerBi-Dashboard/blob/main/bank%20loan%20project(power%20BI).pdf">

1. Summary Page: Presents high-level KPIs like total loan applications, total funded amount, total amount received, average interest rate, and average DTI, along with MTD figures and MoM changes. It also features a clear distinction between "Good Loans" and "Bad Loans" metrics.

2. Overview Page: Provides visual breakdowns of loan applications by month, state, term, employee length, purpose, and home ownership, allowing for a deeper understanding of distribution patterns.

3. Details Page: Offers a granular view, likely a table listing individual or grouped loan details, including issue date, funded amount, interest rate, amount received, and installment amounts, which can be filtered by various criteria.

4. Interactive elements such as slicers for GRADE, STATE, and GOOD VS BAD LOAN were incorporated to allow users to dynamically filter the data and explore specific segments.

## Key Insights from the Dashboard

The dashboard reveals several significant insights into the bank loan portfolio:

1. Overall Performance: The bank has processed 38.6K loan applications, funding $435.8M and receiving $473.1M. The average interest rate stands at 12.05%, with an average DTI of 13.33%.

2. Growth Trends: There are positive Month-over-Month (MoM) increases in key metrics for the latest period shown: Total Loan Applications (+6.9%), Total Funded Amount (+13.04%), and Total Amount Received (+15.84%).

3. Loan Quality:

- A significant majority (86.2%) of loans are categorized as "Good Loans" (33.2K applications, $370.2M funded, $435.8M received).

- "Bad Loans" (Charged Off) account for 13.8% of the portfolio (5.3K applications, $65.5M funded, $37.3M received). This indicates that while most loans perform well, a notable portion results in losses.

4. Loan Characteristics & Distribution:

- Monthly Trends: Loan applications peak towards the end of the year, with December showing the highest volume (4.3K applications in the visualized data).

- Purpose of Loan: "Debt consolidation" is the most common reason for loan applications (18K), followed by "credit card" refinancing (5K) and "other" (4K).

- Applicant Profile (Employee Length): Applicants with "10+ years" of employment form the largest group (8.9K applications).

- Home Ownership: Applicants who are "Renting" (18K) or have a "Mortgage" (17K) constitute the majority of loan seekers.

- Loan Term: The 36-month term is overwhelmingly preferred, accounting for 73.2% of applications (28K), compared to 26.8% for 60-month terms (10K).

## Risk Indicators:

### When comparing "Fully Paid" loans to "Charged Off" loans:

1. Interest Rates: Charged Off loans had a higher average interest rate (13.88%) compared to Fully Paid loans (11.64%).

2. DTI: Charged Off loans also had a slightly higher average DTI (14.00%) compared to Fully Paid loans (13.17%). This suggests that higher interest rates and higher DTI ratios might be associated with increased risk of default.

### When comparing "Fully Paid" loans to "Charged Off" loans:

1. Interest Rates: Charged Off loans had a higher average interest rate (13.88%) compared to Fully Paid loans (11.64%).

2. DTI: Charged Off loans also had a slightly higher average DTI (14.00%) compared to Fully Paid loans (13.17%). This suggests that higher interest rates and higher DTI ratios might be associated with increased risk of default.
