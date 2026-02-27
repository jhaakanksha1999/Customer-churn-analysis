# Customer-churn-analysis
📌 Project Overview

This project analyzes customer churn behavior to identify high-risk customers and uncover the key drivers behind churn.

The goal is to support data-driven retention strategies and reduce revenue loss.

The dashboard was built using Power BI with structured data and interactive slicers for dynamic business analysis.

🛠 Tools & Skills Used

Power BI

DAX (Calculated Measures & Columns)

Data Cleaning & Transformation

Data Modeling

KPI Development

Business Insight Generation

📊 Key Dashboard KPIs

Total Customers

Total Churn Customers

Churn Rate (%)

High Risk %

Revenue at Risk

Average Monthly Charges

📈 Key Business Insights (Based on Actual Analysis)

2-Year contract customers show the highest churn rate, which challenges common assumptions that shorter contracts churn more.

Long-term customers may churn due to:

Contract expiration

Competitive pricing offers

Service dissatisfaction over time

Customers with higher monthly charges show increased churn probability.

Customers without value-added services (Tech Support / Security) are more likely to churn.

A concentrated segment of high-risk customers contributes disproportionately to revenue at risk.

Tenure-based segmentation shows churn is not limited to new customers.

Revenue impact analysis highlights the financial cost of long-term customer loss.

🧠 Analytical Approach

Created risk segmentation logic using DAX

Calculated churn rate using:

Churn Rate % = 
DIVIDE([Total Churn Customers], [Total Customers])

Lost revenue = 
CALCULATE(SUM(customer_churn[MonthlyCharges]),customer_churn[Churn]= "Yes")

Risk score = 
VAR HighCharges = IF(customer_churn[MonthlyCharges]>90,1,0)
VAR HighTicket = IF(customer_churn[SupportTickets]> 5,1,0)
VAR LowTenure = IF(customer_churn[TenureMonths] <5 ,1,0)
RETURN
HighCharges + HighTicket + LowTenure

CLV = 
customer_churn[MonthlyCharges]*customer_churn[TenureMonths]

Built interactive slicers:

Risk Category

Contract Type

Tenure Group

Payment Method

Designed the dashboard for clarity, storytelling, and executive-level decision-making.

🎯 Business Implication

Since 2-Year contracts show higher churn, retention strategies should focus on:

Pre-renewal engagement campaigns

Loyalty benefits before contract expiry

Personalized pricing adjustments

Early dissatisfaction detection

This insight shifts the focus from short-term customers to contract renewal strategy.

Live Interactive Dashboard 
You can view the full dashboard here:
[Click here to view] https://app.powerbi.com/view?r=eyJrIjoiODExNjM3NzYtMTVjYi00Y2VlLWJkM2YtNmE1YmYxYjJkN2MyIiwidCI6IjQ2ZGY3MDk4LTRkNmEtNDJkNS1hYmFmLTJhNzRmMWY3Mjc1MyJ9

