# RFM Analysis in Fresh Mart Supermarket to Optimize Acceptance Campaign
This project analyzes customer purchasing behavior for a supermarket using RFM Analysis (Recency, Frequency, Monetary) to identify high-value customers and optimize marketing campaign strategies.
The goal is to turn raw customer data into actionable insights that help improve campaign acceptance, customer retention, and targeted marketing performance.

Business Objective
To help the supermarket:
- Identify and segment customers based on purchasing behavior
- Understand which customer groups are most valuable
- Improve campaign targeting using RFM and spending patterns
- Support data-driven marketing decisions
  
Project Overview
This repository includes:
- Data cleaning & preprocessing
- Data Understanding & Analysis
- Adding necessary columns to enrich data (Age, Total Spending, RFM Score, Segments, etc.)
- Outlier handling (Age, Income)
- Customer demographics visualization
- Correlation analysis
- RFM segmentation (Low, Medium, High)
- Heatmap, Histograms, and bar charts for customer insights
- Tableau dashboard

Data Cleaning Steps
Key steps performed:
1. Handling missing values (Income median imputation, cleaning categorical anomalies)
2. Fixing inconsistent labels
3. Removing/transforming outliers in Age & Income
4. Replacing invalid marital status values (“Absurd”, “Alone”, “YOLO”) → “Prefer not to say”

**RFM Calculation**

RFM Scores were computed using quantile ranking:
Recency → lower = better
Frequency → higher = better
Monetary → higher = better

Each score is scaled 1–5, producing:
R_score, F_score, M_score

RFM_Score (string)
RFM_Total (numeric)

Supermarket Customers Data Dictionary

People
- ID: Customer's unique identifier
- Year_Birth: Customer's birth year
- Education: Customer's education level
- Marital_Status: Customer's marital status
- Income: Customer's yearly household income
- Kidhome: Number of children in customer's household
- Teenhome: Number of teenagers in customer's household
- Dt_Customer: Date of customer's enrollment with the company
- Recency: Number of days since customer's last purchase
- Complain: 1 if the customer complained in the last 2 years, 0 otherwise

Products
- MntWines: Amount spent on wine in last 2 years
- MntFruits: Amount spent on fruits in last 2 years
- MntMeatProducts: Amount spent on meat in last 2 years
- MntFishProducts: Amount spent on fish in last 2 years
- MntSweetProducts: Amount spent on sweets in last 2 years
- MntGoldProds: Amount spent on gold in last 2 years

Promotion
- NumDealsPurchases: Number of purchases made with a discount
- AcceptedCmp1: 1 if the customer accepted the offer in the 1st campaign, 0 otherwise
- AcceptedCmp2: 1 if the customer accepted the offer in the 2nd campaign, 0 otherwise
- AcceptedCmp3: 1 if the customer accepted the offer in the 3rd campaign, 0 otherwise
- AcceptedCmp4: 1 if the customer accepted the offer in the 4th campaign, 0 otherwise
- AcceptedCmp5: 1 if the customer accepted the offer in the 5th campaign, 0 otherwise
- Response: 1 if the customer accepted the offer in the last campaign, 0 otherwise

Place
- NumWebPurchases: Number of purchases made through the company’s website
- NumCatalogPurchases: Number of purchases made using a catalog
- NumStorePurchases: Number of purchases made directly in stores
- NumWebVisitsMonth: Number of visits to the company’s website in the last month
