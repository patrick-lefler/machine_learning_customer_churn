# machine_learning_customer_churn

Executive Overview
This repository contains a comprehensive data science project aimed at identifying, analyzing, and predicting customer attrition within a consumer credit card division. Leveraging a dataset of over 10,000 historic records, the project moves beyond basic reporting to provide actionable risk intelligence.

The final output is a high-level Quarto HTML report designed for senior bank executives. It bridges the gap between complex statistical modeling and strategic decision-making by utilizing "Executive Note" callouts to explain the business intuition behind the data.

Key Objectives
Identify Drivers: Use Logistic Regression to isolate the "Risk Multipliers" that lead to account closure.

Predict Risk: Deploy a Random Forest machine learning model to score existing customers on their probability of churn.

Analyze Lifecycle: Utilize Survival Analysis to map the "Customer Life Expectancy" and identify critical tenure milestones.

Tactical Action: Generate a prioritized outreach list of at-risk active customers for the retention team.

Repository Contents
version7.qmd: The primary Quarto Markdown file containing the full analysis, R code, and executive narrative.

bank_attrition_data.xlsm: The source dataset containing customer demographics, credit limits, and behavioral metrics.

README.md: This project documentation.

Technical Methodology
The project utilizes the tidymodels ecosystem in R to ensure a rigorous and reproducible workflow:

Exploratory Data Analysis (EDA): Faceted ggplot2 visualizations and plotly interactive charts to identify behavioral "Danger Zones."

Statistical Inference: Logistic Regression to calculate Odds Ratios for factors like inactivity and transaction velocity.

Machine Learning: A Random Forest classifier (using the ranger engine) with importance scores based on Gini Impurity.

Tenure Analysis: Kaplan-Meier survival curves to visualize the retention probability over the customer lifecycle.

Strategic Insights
Behavioral Signatures: The analysis proves that transaction frequency and revolving balance are the primary indicators of health, far outweighing demographic factors like age or income.

The 36-Month Milestone: Survival curves indicate a significant "Risk Milestone" at the 3-year mark, suggesting a need for refreshed loyalty incentives at that anniversary.

Proactive Prevention: By filtering the predictive model for existing customers, we provide a "lead list" of individuals who have not yet left but show a 30%+ probability of attrition.

Requirements
To render the report, the following R libraries are required:

R
install.packages(c("tidyverse", "tidymodels", "readxl", "plotly", 
                   "kableExtra", "vip", "survival", "survminer"))
How to Use
Clone this repository.

Ensure bank_attrition_data.xlsm is in the root directory.

Open version7.qmd in RStudio or your preferred IDE.

Click Render to generate the version7.html executive report.

Note: This analysis was developed to simulate a real-world scenario within a financial technology/banking environment, focusing on the transition from data points to executive strategy.
