# E-Commerce Customer Segmentation & Sales Analytics

## Overview
This project analyzes customer purchasing behavior and product bundling opportunities using the **UCI Online Retail Dataset**.  
The goal is to uncover actionable insights for churn prevention, customer segmentation, and sales optimization through a combination of:
- Exploratory Data Analysis (EDA)
- RFM Segmentation
- Market Basket Analysis
- Interactive Power BI Dashboard

## Objectives
- Identify revenue trends across time periods and customer groups.
- Segment customers using **RFM (Recency, Frequency, Monetary)** analysis to detect high-value and churn-risk segments.
- Discover product bundling opportunities via **Market Basket Analysis (Apriori Algorithm)**.
- Build a **Power BI dashboard** to visualize customer behavior, revenue patterns, and product affinities.

## Dataset
**Source:** UCI Machine Learning Repository  
**Link:** [Online Retail Dataset](https://archive.ics.uci.edu/dataset/352/online+retail)  
**Size:** 500,000+ transaction records  

**Features:**  
`InvoiceNo`, `StockCode`, `Description`, `Quantity`, `InvoiceDate`, `UnitPrice`, `CustomerID`, `Country`

## Tech Stack
- **Python**: Pandas, NumPy, Seaborn, Matplotlib, mlxtend
- **Power BI**: Data modeling, DAX measures, interactive dashboard design

## Models & Analysis

### RFM Segmentation
Customers were scored on Recency, Frequency, and Monetary value (1–5) and mapped into the following segments:

Mapped numeric RFM codes to **clear, human-readable customer segments** for easier interpretation in the dashboard.

| Segment Name        | RFM Code Example(s) | Description |
|---------------------|--------------------|-------------|
| **Champions**       | 555, 554, 545      | Purchased recently, frequently, and with high spend |
| **Loyal Customers** | 45X, 44X           | Frequent repeat buyers with good monetary value |
| **Potential Loyalists** | 5X3, 4X4, 5X2   | Recent buyers who need more engagement to become loyal |
| **At Risk**         | 3X2, 2X3           | Used to buy often, but haven’t purchased recently |
| **Lost Customers**  | 1X1, 1X2           | No recent activity, low frequency, low spend |
| **Others**          | All remaining combinations | Mixed buying behavior |

*(X indicates any score for that position)*

This conversion allowed the dashboard slicers and visuals to use descriptive labels like **"Potential Loyalists"** instead of raw codes like `511`.

---

### Market Basket Analysis
Applied the **Apriori algorithm** to uncover strong product pairings based on **lift** and **support**.

- **Lift**: Measures the strength of a rule relative to random chance (Lift > 1 indicates a strong association).  
- **Support**: Indicates how frequently the paired products appear together.

**Example:**  
`"REGENCY MILK JUG PINK"` → `"REGENCY SUGAR BOWL GREEN"` had one of the highest lifts, meaning customers who buy one are very likely to buy the other.

**Use Case:**  
Insights from these rules can guide **cross-selling** strategies and promotional bundles to boost revenue.

---

## Dashboard Story
This dashboard was designed for a UK-based online retailer, analyzing **revenue drivers**, specifically **Product Pairings**, **Customer Segments**, and **Overall Revenue Trends**. The dashboard allows stakeholders to filter by customer segment, country, and date range, enabling interactive exploration of revenue trends, product affinities, and customer profiles.

### 1. Overall Dashboard
![Overall Dashboard](screenshots/Online-Retail-Dashboard-Analytics.png)

### 2. United Kingdom View
![UK View](screenshots/Online-Retail-Dashboard-Analytics-UK.png)

### 3. Potential Loyalists Segment
![Potential Loyalists](screenshots/Online-Retail-Dashboard-Analytics-Potential-Loyalists-Customer-Segment.png)

### 4. Top 10 Highest-Lift Product Pairings
![Product Pairings](screenshots/Online-Retail-Dashboard-Analytics-Product-Pairings.png)

## Workflow
1. **Data Cleaning** – Removed invalid entries, filtered canceled orders, standardized formats, and filled missing product descriptions using the most frequent (mode) description for each StockCode.
2. **Exploratory Analysis** – Identified revenue trends, top countries, and best-selling products.
3. **Customer Segmentation** – Applied RFM analysis and mapped numeric scores to descriptive segment names.
4. **Product Pairing Analysis** – Used Apriori algorithm to find high-lift product associations.
5. **Dashboard Creation** – Built an interactive Power BI dashboard with KPIs, trend charts, and segment-based filters.

**Key Findings:**
- The online retailer generated **$8.89M in revenue**, with over **18.53K orders** from **4.34K customers**, averaging **$479.53 per order**.
- Revenue showed an **upward trend throughout 2011**, peaking in November before experiencing a sudden drop in December.
- The **United Kingdom accounted for the majority of total revenue**, likely due to the retailer’s domestic market presence.
- Customer segmentation revealed that **Potential Loyalists** (recent purchasers with moderate frequency and spend) and **"Other"** customers (mid-range across RFM scores) made up the majority of the customer base.
- **Potential Loyalists generated the highest share of revenue**, indicating strong retention opportunities.
- Market Basket Analysis identified high-lift product pairings, such as **“Regency Milk Jug Pink” with “Regency Sugar Bowl Green”** and **“Poppys Playhouse Kitchen” with “Poppys Playhouse Bedroom”**, suggesting bundling opportunities.

## Business Recommendations
- **Focus on the UK market** for marketing campaigns and product promotions, given its revenue dominance.
- **Launch loyalty and rewards programs** targeting Potential Loyalists to convert them into high-value repeat buyers.
- **Create product bundles** based on top high-lift pairings to increase average order value.
- **Investigate December revenue drop** to determine if it was caused by seasonality, stock issues, or marketing gaps.
- **Nurture “Other” customers** through personalized offers to push them toward higher engagement segments.
- **Apply targeted churn prevention** for Lost Customers by offering discounts or win-back campaigns.

## Author
Rishi Vangala

