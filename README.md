# Bank-Churn-Analysis
**Objective**
      The objective of this project is to analyze customer churn patterns using demographic, account, and credit-related information. This analysis helps identify the factors influencing customer exits and supports strategies to improve retention and overall customer satisfaction.
**Project Highlights**

**This project focuses on key areas that impact churn including:**
      Customer activity status Credit card usage Customer exit trends Gender-wise and credit-type-wise churn distribution Monthly movement in customer engagement These insights help the bank understand which customer segments are at higher risk of churn and where to improve retention strategies.
**Dashboard Visualization**

**DASHBOARD**

The dashboard presents a complete overview of customer churn performance using KPIs, charts, and slicers for flexible filtering.

**Dashboard Insights**

1. Total Customers Overview
The top KPI cards show:
Total customers
Active members
Inactive members
Credit card holders
Non–credit card holders
Exit customers
Retained customers
These metrics provide a quick summary of customer behavior at a glance.
2. Total Customers – Active vs Inactive
This chart compares the number of active and inactive customers month-wise. It helps understand engagement patterns and highlights months where activity drops or increases.
3. Exit Customers by Month
This line chart shows monthly customer exits. It reveals high-churn and low-churn months, helping find patterns in customer dropout behavior.
4.bExit Customers by Gender Category
This donut chart visualizes the male vs female exit distribution. It indicates which gender group contributes more to churn and can help target retention strategies accordingly.
5. Exit Customers by Credit Type
This bar chart categorizes churned customers based on their credit ratings (Excellent, Good, Fair, Poor, etc.). It helps identify which credit score groups are more likely to exit and which are more stable.
**DAX Formulas Used**

Max_Credit = MAX(Bank[CreditScore])
Totalcustomer = COUNT(Bank[CustomerId])
Active Member = CALCULATE( COUNT(Bank[IsActiveMember]), KEEPFILTERS(Bank[IsActiveMember] = 1) )
Inactive Member = CALCULATE( COUNT(Bank[IsActiveMember]), KEEPFILTERS(Bank[IsActiveMember] = 0) )
Credit Holder = CALCULATE( COUNT(Bank[HasCrCard]), KEEPFILTERS(Bank[HasCrCard] = 1) )
Not Credit Holder = CALCULATE( COUNT(Bank[HasCrCard]), KEEPFILTERS(Bank[HasCrCard] = 0) )
Retain Customers = CALCULATE( COUNT(Bank[Exited]), KEEPFILTERS(Bank[Exited] = 0) )
Exit Customers = CALCULATE( COUNT(Bank[Exited]), KEEPFILTERS(Bank[Exited] = 1) )
**Conclusion** 

This analysis provides deep insights into customer churn behavior. Based on the findings, the bank can:
Strengthen customer engagement programs, especially for inactive customers
Improve service experience for customers at risk of leaving
Design targeted retention plans for customers with lower credit scores
Analyze monthly churn spikes and address root causes
Personalize communication to increase long-term loyalty
