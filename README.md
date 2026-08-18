**Why Are We Losing Customers? A Telco Churn Exploration**

A beginner-friendly exploratory data analysis (EDA) project built entirely in Excel, no coding required. This project walks through how to explore a real dataset, ask the right questions, and turn findings into a stakeholder-ready story.

If you're trying to break into data analytics and looking for a first project to build, feel free to fork/replicate this one,the full steps are below.

**1.) The Business Question**

Why are customers churning, and what should the business do about it?

This is the kind of open-ended question a stakeholder might actually ask,the goal of this project is to explore the data and turn it into a clear, actionable answer.

**2.)  Dataset**
- Source: Telco Customer Churn from Kaggle - link : https://www.kaggle.com/code/farazrahman/telco-customer-churn-logisticregression
- File: WA_Fn-UseC_-Telco-Customer-Churn.csv
- Size: 7032 customer records (after removing rows with missing values)
- Key columns used: tenure, MonthlyCharges, Contract, Churn
- Tools Used
Microsoft Excel (PivotTables, statistical functions, charts(no add-ins required))


**3.) Data Cleaning**
Before analyzing, I checked for missing values and data type issues:

Found ~11 blank values in TotalCharges (new customers with 0 tenure),exclude them from calculations
Verified Churn (Yes/No) and Contract fields were consistent, no whitespace or typos
Checked for duplicate customerID rows, none found

**4.) Key Findings**

i) Contract type is the strongest churn signal
Month-to-month customers churn at a dramatically higher rate than customers on 1-year or 2-year contracts. Flexibility for the customer means higher risk for the business?

![Contract Churn vs Non-Churn](contract-vs-churn.png)

ii) Churn happens early
Half of all customers who churn do so within their first 10 months (median tenure), while customers who stay have a median tenure of 38 months (more than 3 years).
There's also a solid group of long-term loyal customers who've stuck around for years (refer to the right end of histogram under non-churn), so the business has two very different types of customers,
and they probably need different strategies to retain existing customers and to reduce churn rate.

| | Count | Mean tenure | Median tenure |
|---|---|---|---|
| Non-Churn | 5,163 | 37.65 months | 38.00 months |
| Churned | 1,869 | 17.98 months | 10.00 months |

![Tenure Distribution](tenure-distribution.png)

iii) Churned customers pay more
On average, customers who churn pay about $13/month more than those who stay ($74.44 vs $61.31), this indicates price sensitivity plays the role for customers already on flexible, no-commitment plans.

| | Mean | Median |
|---|---|---|
| Non-Churn | $61.31 | $64.45 |
| Churned | $74.44 | $79.65 |

![Monthly Charges Mean vs Median](monthlycharges-mean-median.png)

**5.) Recommendation**

Retention efforts should prioritize two distinct groups, based on the data:

i) High-risk: new, month-to-month customers in their first year, especially those on higher-priced plans, this segment shows the highest combined churn risk.
   A targeted incentive (e.g. a discount for switching to an annual contract around month 3–6) could meaningfully reduce early churn.

ii) High-value: long-tenured customers (5+ years) this loyal segment represents low churn risk but high advocacy potential. Rather than discounting (which isn't needed to retain them), 
consider a loyalty recognition program e.g. an exclusive perk, early access to new plans/features, or a small "thank you" credit at each tenure milestone (3, 5, 7 years).
Loyal customers are also more likely to refer others or leave positive reviews, so investing in this group can drive word-of-mouth growth, not just retention.


*****************************************************************************************************

For those who interested to replicate this Project, please follow the steps below:

1.) Download the dataset from Kaggle (link above) and open it in Excel.

2.) Convert the range to a Table (Ctrl+T) for easier referencing.

3.) Check for missing values and inconsistent data types before analyzing anything.

4.) Build a PivotTable: Contract in Rows, Churn in Values (shown as % of Row Total) → this surfaces the #1 finding almost immediately.

5.) Get Mean and Median tenure by Churn status using a PivotTable (Average) plus a quick sort-and-MEDIAN() on the sorted blocks.

6.) Repeat step 5 for MonthlyCharges.

7.) Turn each finding into one simple chart, a bar chart, a histogram, or a grouped comparison chart.

8.) Write 2-3 sentences per finding explaining why it matters, not just what the number is.

9.) End with one clear, specific recommendation, this is what separates an analysis from a report.

📁 Files in This Repo
WA_Fn-UseC_-Telco-Customer-Churn.xlsx,the working Excel file (PivotTables, formulas, and charts included)
charts/ exported chart images used in this README

Part of my data analyst learning journey,follow along for more beginner-friendly projects :-)
