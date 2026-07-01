# 📊 E-Commerce Sales Analytics Dashboard

A complete **Power BI Data Visualization Project** analyzing an e-commerce transaction dataset to uncover sales trends, customer behavior, and product performance through an interactive dashboard.


## 📷 Dashboard Preview


```
<img width="1481" height="842" alt="image" src="https://github.com/user-attachments/assets/193722e2-b29a-478d-9e49-cf93bddaba25" />

```
---

## 📌 Project Overview

This project analyzes an e-commerce transaction dataset using **Microsoft Power BI**. The objective was to clean, transform, visualize, and interpret the data to answer key business questions and provide actionable business insights.

The dashboard enables users to explore revenue trends, customer purchasing behavior, and product category performance through interactive visualizations.

---

## 🎯 Objectives

The project answers the following business questions:

- What is the distribution of transaction amounts?
- How does total revenue change over time?
- Which product categories generate the most revenue?
- What trends can be identified in customer purchasing behavior?

---

## 🛠️ Tools Used

- Microsoft Power BI
- Power Query
- DAX (for calculated measures)
- CSV Dataset

---

# Dataset

The dataset contains the following fields:

| Column |
|---------|
| TransactionNo |
| Date |
| ProductNo |
| Product |
| Price |
| Quantity |
| CustomerNo |
| Country |
| Category |

---

# Data Validation

The dataset was imported into Power BI using:

> **Get Data → Text/CSV**

Validation included:

- Verifying all required columns
- Confirming correct data types
- Ensuring the **Date** column was recognized as a Date field

---

# Data Cleaning

Several preprocessing steps were performed before analysis.

### ✅ Removed Cancelled Transactions

Transactions beginning with **"C"** in the **TransactionNo** column represented cancelled orders.

These records were removed.

---

### ✅ Removed Invalid Quantities

Negative quantities represented returned or cancelled items.

Filter applied:

```text
Quantity > 0
```

---

### ✅ Created Revenue Column

A custom column was created:

```text
Revenue = Price × Quantity
```

This became the primary metric used throughout the dashboard.

---

### ✅ Corrected Revenue Data Type

Initially, the Revenue column was imported as **Text**, preventing histogram creation.

The data type was changed to:

- Decimal Number

This enabled numeric binning for the transaction distribution visualization.

---

# Dashboard Visualizations

## 1. Revenue Distribution

### Business Question

> What is the distribution of transaction amounts?

### Visualization

- Histogram
- Revenue grouped into numeric bins

### Key Insights

- Most transactions fall into lower revenue ranges.
- High-value transactions occur much less frequently.
- Revenue is primarily generated through many small purchases.

---

## 2. Revenue Trend Over Time

### Business Question

> How does total transaction amount vary over time?

### Visualization

- Monthly Line Chart
- Sum of Revenue

### Improvements

Daily data produced a noisy visualization.

The chart was aggregated using the **Date Hierarchy (Month)** for better trend analysis.

### Key Insights

- Revenue remained relatively stable across months.
- Small declines were observed during February.
- Limited seasonality was detected.

---

## 3. Revenue by Product Category

### Business Question

> Which product categories generate the most revenue?

### Visualization

- Horizontal Bar Chart

### Key Insights

- **Home Accents** generated the highest revenue.
- **Office & Study** generated the lowest revenue.
- Home Accents contributed approximately twice the revenue of the second-highest category.

---

## 4. Customer Purchasing Behavior

### Business Question

> Can customer purchasing trends be identified?

### Visualization

- Monthly Active Customers
- Distinct Count of CustomerNo

### Key Insights

- Customer activity remained relatively stable.
- Consistent customer retention was observed.
- Revenue growth may depend more on increasing average order value than acquiring additional customers.

---

# Dashboard Features

The final interactive dashboard includes:

### KPI Cards

- Total Revenue
- Total Customers
- Total Transactions
- Average Transaction Value

### Visualizations

- Revenue Distribution
- Monthly Revenue Trend
- Revenue by Product Category
- Monthly Active Customers

### Interactive Filters

- Category
- Country
- Date

Users can dynamically explore the data using slicers.

---

# Business Insights

### 📈 Revenue

- Most purchases are low-value transactions.
- Revenue remains relatively stable over time.

### 🏠 Product Categories

- Home Accents is the strongest-performing category.
- Office & Study requires further investigation.

### 👥 Customer Behavior

- Customer engagement remained consistent.
- Stable active customer count suggests good customer retention.

---

# Recommendations

### 1. Invest Further in Home Accents

Continue prioritizing inventory and marketing efforts for the highest-performing category.

---

### 2. Investigate February Revenue Declines

Determine whether lower revenue is caused by seasonal demand or operational factors.

---

### 3. Increase Average Transaction Value

Introduce:

- Product bundles
- Cross-selling
- Upselling strategies

---

### 4. Improve Office & Study Performance

Evaluate:

- Pricing strategy
- Inventory availability
- Customer demand
- Promotional campaigns

---

# Challenges Encountered

During development several issues were resolved:

- Removing cancelled transactions
- Removing invalid quantities
- Correcting Revenue data type
- Aggregating daily data into monthly trends
- Creating histogram bins in Power BI

These preprocessing steps ensured accurate analysis and reliable dashboard insights.

---

# Conclusion

This project demonstrates a complete end-to-end Power BI analytics workflow, from data validation and cleaning to visualization and dashboard design.

The dashboard provides valuable insights into:

- Sales performance
- Revenue trends
- Customer purchasing behavior
- Product category performance

By combining interactive visualizations with business recommendations, the project showcases how Power BI can transform raw transactional data into actionable business intelligence.

---




## 👨‍💻 Author

**Priyanshu Joshi**

Data Analytics | Power BI  | Data Visualization

---
