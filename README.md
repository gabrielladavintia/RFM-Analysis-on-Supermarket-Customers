# RFM Analysis in Fresh Mart Supermarket to Optimize Acceptance Campaign
This project analyzes customer purchasing behavior for a supermarket using RFM Analysis (Recency, Frequency, Monetary) to identify high-value customers and optimize marketing campaign strategies.
The goal is to turn raw customer data into actionable insights that help improve campaign acceptance, customer retention, and targeted marketing performance.

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

Business Objective
To help the supermarket:
- Identify and segment customers based on purchasing behavior
- Understand which customer groups are most valuable
- Improve campaign targeting using RFM and spending patterns
- Support data-driven marketing decisions

Data Cleaning Steps
Key steps performed:
1. Handling missing values (Income median imputation, cleaning categorical anomalies)
2. Fixing inconsistent labels
3. Removing/transforming outliers in Age & Income
4. Replacing invalid marital status values (“Absurd”, “Alone”, “YOLO”) → “Prefer not to say”

Creating additional customer features:
1. Age
2. Total Amount
3. Total Purchases
4. Total Spending
5. Median Segment
6. RFM Scores (R, F, M, RFM_Total)
7. 3-Level Spending Segment

RFM Calculation

RFM Scores were computed using quantile ranking:
Recency → lower = better
Frequency → higher = better
Monetary → higher = better

Each score is scaled 1–5, producing:
R_score, F_score, M_score

RFM_Score (string)
RFM_Total (numeric)
