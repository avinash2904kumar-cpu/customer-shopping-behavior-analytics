# Customer Shopping Behavior Analytics

## 📌 Project Overview

An end-to-end data analytics project focused on understanding customer purchasing behavior, spending patterns, and business performance.

The project takes raw customer transaction data through **data cleaning, exploratory analysis, SQL-based business analysis, and Power BI visualization** to generate actionable insights.

### 🔄 End-to-End Workflow

```text
Raw CSV Data
     ↓
Python & Pandas
     ↓
Data Cleaning & EDA
     ↓
PostgreSQL
     ↓
SQL Business Analysis
     ↓
Power BI
     ↓
Interactive Dashboard
     ↓
Business Insights
```

---

## 🎯 Business Objective

The objective of this project was to analyze customer shopping behavior and answer key business questions related to:

* Customer spending patterns
* Product and category performance
* Customer segmentation
* Subscription behavior
* Payment methods
* High-value customers
* Revenue contribution
* Purchasing trends

The analysis was designed to convert raw transactional data into insights that could support **customer retention, marketing, and revenue-focused decisions**.

---

## 📊 Dataset

The dataset contains approximately **3,900 customer transaction records** with **18 attributes** covering customer demographics, purchasing behavior, product information, payment methods, subscription status, and transaction details.

Key attributes include:

* Customer ID
* Age
* Gender
* Item Purchased
* Category
* Purchase Amount
* Location
* Size
* Color
* Season
* Review Rating
* Subscription Status
* Payment Method
* Shipping Type
* Discount Applied
* Previous Purchases
* Frequency of Purchases
* Purchase-related information

---

## 🛠️ Tools & Technologies

| Tool                 | Purpose                                 |
| -------------------- | --------------------------------------- |
| **Python**           | Data cleaning and pre-processing        |
| **Pandas**           | Data manipulation and transformation    |
| **Matplotlib**       | Data visualization                      |
| **Seaborn**          | Exploratory data analysis               |
| **PostgreSQL**       | Database storage and SQL analysis       |
| **SQL**              | Business queries and KPI generation     |
| **Power BI**         | Interactive dashboard and visualization |
| **Jupyter Notebook** | Data analysis environment               |

---

## 🧹 Data Cleaning & Preparation

The raw CSV dataset was imported into **Jupyter Notebook** and analyzed using Pandas.

Key preprocessing steps included:

* Inspected dataset structure and data types
* Identified and handled missing values
* Checked for duplicate records
* Standardized column names
* Validated categorical and numerical fields
* Created additional analytical features where required
* Prepared the cleaned dataset for database analysis

The cleaned dataset was then loaded into **PostgreSQL** for structured querying and business analysis.

---

## 🔎 Exploratory Data Analysis

EDA was performed using **Pandas, Matplotlib, and Seaborn** to understand customer and purchasing behavior before performing SQL analysis.

The analysis explored:

* Customer demographics
* Purchase amount distribution
* Category performance
* Customer purchasing frequency
* Subscription behavior
* Payment methods
* Product-level patterns
* Spending behavior across customer segments

---

## 🗄️ SQL Business Analysis

After loading the processed data into PostgreSQL, SQL queries were developed to answer business-focused questions.

Examples include:

### Top 10 Highest-Value Customers

```sql
SELECT
    customer_id,
    SUM(total_charges) AS lifetime_value
FROM customer_churn
GROUP BY customer_id
ORDER BY lifetime_value DESC
LIMIT 10;
```

### Revenue by Contract Type

```sql
SELECT
    contract_type,
    SUM(total_charges) AS total_revenue
FROM customer_churn
GROUP BY contract_type;
```

### Average Monthly Charges by Plan

```sql
SELECT
    plan_tier,
    ROUND(AVG(monthly_charges), 2) AS avg_monthly_charge
FROM customer_churn
GROUP BY plan_tier;
```

> The SQL layer was used to transform the cleaned dataset into business-oriented metrics rather than simply retrieving raw records.

---

## 📈 Power BI Dashboard

The final dataset was connected to **Power BI** to create an interactive analytical dashboard.

The dashboard provides:

* KPI overview
* Customer segmentation
* Revenue analysis
* Category-level performance
* Customer purchasing behavior
* Subscription analysis
* Payment method analysis
* Interactive filtering and exploration

The dashboard allows users to move from a high-level business overview to more detailed customer and category-level analysis.

---

## 💡 Key Insights

The analysis was used to identify:

* High-value customer segments
* Major revenue-contributing categories
* Differences in purchasing behavior
* Subscription-related customer patterns
* Frequently used payment methods
* Customer groups with stronger spending potential

These insights can support **targeted marketing, customer retention strategies, and revenue optimization**.

---

## 📁 Repository Structure

```text
Customer-Shopping-Behavior-Analytics/
│
├── Data/
│   └── customer_shopping_behavior.csv
│
├── Notebook/
│   └── customer_behavior_analysis.ipynb
│
├── SQL/
│   └── business_queries.sql
│
├── PowerBI/
│   └── customer_behavior_dashboard.pbix
│
├── Images/
│   └── dashboard.png
│
└── README.md
```

---

## 🚀 Future Improvements

The project can be extended by adding:

* Customer churn prediction
* Customer lifetime value prediction
* Customer segmentation using clustering
* Machine learning models for purchase prediction
* Automated Power BI data refresh
* Advanced customer recommendation systems

---

## 👤 Author

**Avinash Kumar**

B.Tech – Chemical Engineering
Birla Institute of Technology, Mesra

### Skills Demonstrated

`Python` `Pandas` `SQL` `PostgreSQL` `Power BI` `Excel` `EDA` `Data Visualization`

---

## ⭐ Project Objective

This project demonstrates the complete analytics workflow of transforming **raw transactional data into structured business insights**, combining Python-based data preparation, SQL analysis, and Power BI visualization.

