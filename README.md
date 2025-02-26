# Loan Performance and Recovery Analytics

## Overview
This repository contains a comprehensive analysis of Non-Performing Loans (NPLs) and revenue collection trends based on data from a pilot project initiated in August 2023 and concluded in August 2024. The project focuses on understanding key performance metrics such as the NPL ratio, aging of loans, repayment/collection trends, and revenue patterns to inform risk management and enhance loan recovery strategies.

## Project Objective
The primary objective of this analysis is to assess the performance of our loan portfolio by:
- Calculating and tracking the overall NPL ratio and its monthly trends.
- Conducting an aging analysis by categorizing loans into buckets (0-30, 31-60, 61-90, >90 days past due).
- Evaluating repayment/collection trends over time.
- Analyzing revenue collection trends to identify potential shortfalls or gains.

## Key Analysis Areas
- **NPL Ratio Analysis:** Assessing the percentage of loans in default and monitoring monthly changes.
- **Aging Analysis:** Categorizing loans based on the number of days past due to highlight risk exposures.
- **Repayment/Collection Trend Analysis:** Tracking borrower repayment behaviors and collection efficiency.
- **Revenue Collection Trend Analysis:** Evaluating the trends in revenue generated from interest, fees, and repayments.

## Data Features
The analysis utilizes both original and engineered data features. Key features include:
- **Original Features:** `loan_id`, `agent_id`, `loan_amount`, `loan_balance`, `amount_paid`, `outstanding_principle`, `outstanding_daily_interest`, `outstanding_setup_fees`, `outstanding_penalty_fees`, `interest_earned`, `penalty_fees_repayment`, `daily_interest_repayment`, `status_id`, `defaulted`, `eligible_amount`, `created_at`, `due_date`, `last_repayment_date`, `days_interest_calculated`, `age`.
- **Engineered Features:**  
  - `is_npl`: Binary indicator for non-performing loans.  
  - `created_month`, `due_month`, `last_repayment_month`: Temporal markers for monthly trend analysis.  
  - `days_since_last_repayment`: Days elapsed since the last repayment.  
  - `days_past_due`: Number of days a payment is overdue.  
  - `aging_bucket`: Categorization of loans based on overdue duration.  
  - `collection_rate`: Percentage of the eligible amount that has been repaid.  
  - `revenue_earned`, `outstanding_revenue`, `revenue_per_loan`: Metrics reflecting revenue performance.

## Methodology
- **Data Cleaning & Preparation:** Ensuring accuracy and consistency across all data points.
- **Descriptive & Trend Analysis:** Using time-series analysis to observe trends over time.
- **Aging Categorization:** Grouping loans into predefined aging buckets.
- **Visualization:** Creating charts and graphs to effectively communicate key trends and insights.

## Key Insights
- The overall NPL ratio was found to be 5.24%, with monthly variations ranging from 0% to 10%.
- Significant differences exist in repayment behaviors across various aging buckets, highlighting a concerning trend for loans collected after 60 days.
- Revenue analysis indicates that 52.4% of the total expected revenue remains outstanding, emphasizing the need for enhanced recovery strategies.
- High-value loans exhibit a near 100% default rate, suggesting that stricter lending criteria may be necessary.

## Recommendations & Next Steps
- **Enhanced Risk Mitigation:** Apply stricter scrutiny on high-value loans and those exceeding 60 days in repayment delay.
- **Targeted Recovery Strategies:** Focus on improving collection efforts for segments with high outstanding revenue i.e. offering incentives such as discounts for early fees payment, increasing loan affordability for clients whose repayment trends outperform the norm.
- **Predictive Modeling:** Develop early warning systems for loan defaults and explore additional machine learning models (e.g., binary classification for default prediction, revenue forecasting).

## Repository Structure
|-- data viz/                                 # Folder containing data visualizations generated from the jupyter notebook

|-- data/                                     # Folder containing dataset that is analysed in the jupyternotebook

|----- Turbo-aug-23-24-npl-analysis.pdf       # PDF version of jupyter notebook  

|----- Turbo_Aug_23_24_NPL_Analysis.ipynb     # Jupyter notebook containing detailed analysis and visualizations

|----- Turbo_Project_Performance_Report.pptx  # Powerpoint presentation summarizing results and findings

|----- requirements.txt                       #List of all required Python packages


## Author Contact Info:
David Kirianja
- dmkirianja@gmail.com
- www.linkedin.com/in/david-mutugi-dmk007n
