Lending Club Case Study
> Outline a brief description of your project.


## Table of Contents
* [General Info](#general-information)
* [Approach](#Approach)
* [Conclusions](#conclusions)
* [Technologies Used](#technologies-used)

<!-- You can include any other section that is pertinent to your problem -->

## General Information
 Problem Statement
   
    - The Consumer Finance Company specializes in lending various types of loans to urban customers
    - When the company receives a loan application, the company has to make a decision for loan approval based on the applicant’s profile
    - If the applicant is likely to repay the loan, then not approving the loan results in a loss of business to the company
    - If the applicant is not likely to repay the loan, , then approving the loan may lead to a financial loss for the company
    - The company needs a framework to evaluate the loan applications, to improve the profitability of the business

Objective of the Analysis
  - To identify the key drivers impacting the default behaviour of borrowers
  - Also understand the interrelationship between variables that impact default behaviour
  - To identify the key drivers impacting the recoveries from defaulted loans
  - To prioritize the drivers in terms of their impact, and suggest ways to assess loan application to maximize business profitability

## Approach
- **Data Cleaning**
    - **Outlier treatment** - Identify and treat outliers by calculating IQR (Q3-Q1), then remove data points outside 1.5 * IQR from Q1 and Q3
    - **Data conversion** – ‘%’ symbol is removed from variables such as ‘int_rate’ and ‘revol_util’ columns to treat them as float
- To understand the default behaviour, only closed loans are analyzed - 'Charged Off’ and 'Fully Paid’ loans
    - ‘Current’ loans are excluded because their default status cannot be determined yet.
- **Derived metrics** such as default rate and recovery rate are calculated to understand their relationship with other variables
- **Default rate** has been calculated as ‘Charged Off’ loans as percentage of total closed loans
- **Default rate** has been calculated in terms of both:
    - Count of loans defaulted
    - Amount of loans defaulted
- **Recovery Rate** has been calculated as ‘recoveries’ as percentage of defaulted amount
    - Defaulted amount is considered as ‘loan_amnt’ minus ‘total_rec_prncp’, which denotes the principal amount that has been charged off
- **Univariate, Bivariate and Multivariate analysis** analysis is performed to explain relationship among variables
    - **Interdependency of variables** is also analyzed avoid any misleading conclusion regarding any variable driving default rate
- **Correlation and Regression** techniques have been applied to establish relationship among variables


 

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Conclusions

  - Caution must be exercised in granting lower grade loans, especially graded ‘D’ and below, which experience more than 20% default rate
  - Additional measures such as physical verification, income documentation, etc should be taken for such loans
  - Loans graded ‘D’ and below should be charged even higher interest rates to compensate for substantially higher chances of default
  - High income group borrowers (typically above $90k) should be incentivized to apply for more loans due to better risk-adjusted returns, given the low
    default rate
  - Debt to Income (DTI) ratio is a primary indicator of default that must be considered and verified in granting loans
  - Higher DTI increases the chances of default
  - If an applicant has made multiple inquiries in the last 6 months, loan is likely to have some defect due to which it was probably rejected
  - Such loans should go through an extra layer of due diligence
  - Loans with large installment sizes (typically higher than 200 USD) should be regularly monitored, and if required restructuring plans should be considered
    to reduce incidences of default due to budget related burden on borrowers
  - Lower rates of interest should be offered for 3 yr loans in view of lower defaults in this bucket


<!-- You don't have to answer all the questions - just the ones relevant to your project. -->


## Technologies Used
  Python 3.13 
  - Matplotlib 3.9.2
  - Numpy 2.1.2
  - Pandas 2.2.3
  - Seaborn 0.13.2
<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Contact
Created by [@DarKk10] - feel free to contact me!
- Submmited by Pratham Desai and Prashant Saxena


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->
