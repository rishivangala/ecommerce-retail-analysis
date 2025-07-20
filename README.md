# Online Retail Customer Segmentation and Sales Analytics
## Overview
This project analyzes customer purchasing behavior and product bundling opportunities using the UCI Online Retail Dataset. The goal is to uncover actionable insights for churn prevention, customer segmentation, and sales optimization through a combination of exploratory data analysis, RFM segmentation, and Market Basket Analysis.

## Objectives
Identify revenue trends across time periods and customer groups.

Segment customers using RFM (Recency, Frequency, Monetary) analysis to detect high-value and churn-risk segments.

Discover product bundling opportunities via Market Basket Analysis (Apriori Algorithm).

Build a Power BI dashboard to visualize customer behavior, revenue patterns, and product affinities.

## Dataset (Important)
Source: UCI Machine Learning Repository

Link: [Online Retail Dataset](https://archive.ics.uci.edu/dataset/352/online+retail)

Size: 500,000+ transaction records

Features: InvoiceNo, StockCode, Description, Quantity, InvoiceDate, UnitPrice, CustomerID, Country

## Tech Stack
Python (Pandas, NumPy, Seaborn, Matplotlib, mlxtend)

Market Basket Analysis: Apriori Algorithm (mlxtend)

Customer Segmentation: RFM Analysis

Visualization: Power BI (KPI cards, trend charts, segmentation visuals)

## Exploratory Analysis
Key areas explored:

Revenue Trends: Monthly and daily sales patterns

Product Patterns: Top-selling products by quantity and revenue

Customer Behavior: Purchase frequency, monetary value, recency

Order Patterns: Weekday and hourly trends in transactions

## Models & Analysis
### RFM Segmentation
Segmented customers into categories such as High-Value, New Buyers, and At-Risk (Churn-Prone)

Focused on 511 & 411 segments (high recency but low frequency & value) for churn prevention strategies

### Market Basket Analysis
Used the Apriori Algorithm to identify product pairings with high lift (>50)

Found actionable bundling insights (e.g., Regency kitchenware, Playhouse sets, party supplies)

Built a Network Graph to visualize co-purchase relationships

### Key Results
40% of customers are recent one-time buyers, highlighting churn risk if not re-engaged

Product bundles with highest lift include kitchenware sets and party accessories

RFM segmentation identified top-spending segments and retention opportunities

Power BI Dashboard includes KPIs, revenue trends, customer segmentation visuals, and market basket rules

## Next Steps
Integrate AI agents for real-time product recommendation simulations

Expand Market Basket Analysis with deeper product categorization

Deploy dashboard insights for sales strategy optimization

## Author
Rishi Vangala

