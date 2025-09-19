# Optimizing Portuguese Bank Marketing Campaigns through Data-Driven Insights: An Analysis of Customer Subscription to Term Deposits
## Table of Contents
- [Introduction](#Introduction)
- [Problem Statement](#Problem-Statement)
- [Data Dictionary](#Data-Dictionary)
- [Tools](#Tools)
- [Data Source](#Data-Source)
- [Data Cleaning & Transformation](#Data-Cleaning-&-Transformation)
- [Key Questions & Findings](#Key-Questions-&-Findings)
- [Insights](#Insights)
- [Data Storytelling Presentation](#Data-Storytelling-Presentation)
- [Recommendations](#Recommendations)

## Introduction
<p align = "justify"> 
The financial services sector is becoming increasingly competitive, with banks striving to design effective marketing campaigns that attract and retain customers. To remain profitable, banks need to identify the characteristics of customers who are most likely to subscribe to financial products such as term deposits. Traditional marketing campaigns often involve broad outreach strategies, which may lead to high costs, low conversion rates, and wasted resources.
The dataset under review comes from a Portuguese banking institution, where clients were contacted through telemarketing campaigns to promote term deposits. It contains demographic information, financial attributes, contact details, campaign-related variables, and the final outcome (whether the client subscribed or not). By analyzing this data, valuable insights can be derived to help optimize marketing strategies, improve customer targeting, and enhance return on investment.
</p>

## Business Challenge
<p align="justify">
UA Portuguese bank is facing a significant challenge in its direct marketing campaigns for term deposits. Despite a large customer base, the current strategy—relying on a broad, untargeted approach—is leading to inefficient marketing, low conversion rates, and a poor return on investment. The bank needs to shift from making random phone calls to making smart, data-driven decisions to increase subscriptions and reduce operational costs. As a data analyst, I was tasked with:
</p>
- Identify customer subscription patterns
- Profile high-potential customer groups
- Recommend data-driven marketing strategies

 dfg



## Tools 
|Tool | Purpose |
|----|----|
|SQL | Data cleaning and analysis |
|Excel | Visual storytelling and charts|
|PowerPoint | Final storytelling presentation |

## Problem Statement
<p align = "justify"> 
Despite significant efforts and costs, telemarketing campaigns in the banking sector often face low success rates. Many contacted clients decline to subscribe to the offered products, resulting in resource inefficiency and reduced profitability.
The central problem, therefore, is: <br>
<br>
<b> How can the bank identify the factors that influence customer subscription decisions and use this knowledge to improve campaign performance? </b> 
<br>
<br>
This project seeks to uncover the key drivers of customer response, differentiate between segments that are likely to subscribe versus those that are not, and provide actionable recommendations to reduce non-subscription and improve conversion rates.
</p>

## Data Dictionary
This section provides a detailed breakdown of the features and their characteristics to help guide your analysis.

### Client Demographics
- age: The client's age (numeric).
- job: The client's occupation (categorical).
- marital: The client's marital status (categorical: 'married', 'single', 'divorced').
- education: The client's education level (categorical).
- default: Does the client have a credit default? (categorical: 'yes', 'no', 'unknown').
- housing: Does the client have a housing loan? (categorical: 'yes', 'no', 'unknown').
- loan: Does the client have a personal loan? (categorical: 'yes', 'no', 'unknown').

### Campaign Interaction
- contact: The type of communication used for the last contact (categorical: 'cellular', 'telephone').
- month: The month of the last contact (categorical).
- day_of_week: The day of the week of the last contact (categorical).
- duration: The duration of the last contact in seconds (numeric). This feature is highly influential and should be analyzed carefully.
- campaign: The number of contacts performed during this campaign for this client (numeric).
- pdays: The number of days since the client was last contacted from a previous campaign (numeric). A value of 999 means the client was not previously contacted.
- previous: The number of contacts performed before this campaign for this client (numeric).
- poutcome: The outcome of the previous marketing campaign (categorical: 'failure', 'success', 'nonexistent').
### Economic & External Factors
- emp.var.rate: Employment variation rate (numeric): This is a measure of the change in the number of people employed over a period. A positive value indicates an increase in employment, while a negative value shows a decrease. This can affect consumer spending habits and their willingness to commit to new financial products.
- cons.price.idx: Consumer price index (numeric): The CPI measures the average change in prices paid by consumers for a basket of goods and services. It is a key indicator of inflation. A high CPI means prices are rising, which can reduce a consumer's purchasing power.
- cons.conf.idx: Consumer confidence index (numeric): This index measures the optimism of consumers about the state of the economy. When this index is high, consumers are more likely to spend money and make larger purchases, which could include a term deposit. A low index suggests economic uncertainty and may lead to less spending.
- euribor3m: Euribor 3-month rate (numeric): This is the interest rate at which European banks lend to one another. It's a key indicator for the cost of borrowing for banks. It directly influences the interest rates banks offer to their customers, which would impact the attractiveness of a term deposit.
- nr.employed: Number of employees (numeric).
This represents the number of employees in the bank's country. A higher number of employees generally signals a stronger economy, which can correlate with higher consumer confidence and a greater likelihood of subscription.
### Output Variable
- y: The target variable indicating whether the client subscribed to the term deposit (categorical: 'yes', 'no').



