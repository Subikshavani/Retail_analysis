# Retail_analysis
🚀 Project Overview

This project analyzes retail sales data from a Superstore dataset to uncover business insights, sales trends, and profit drivers.
It follows a complete, industry-style data analytics pipeline:

✔ Data Cleaning

✔ Exploratory Data Analysis (EDA)

✔ SQL Querying

✔ Business Insights & Recommendations

This project demonstrates the full lifecycle of a data analyst’s workflow, making it ideal for portfolio and interviews.

🧰 Technologies Used
Area	Tools
Programming	Python (Pandas, NumPy, Matplotlib, Seaborn)
Development	Jupyter Notebook
Data Storage	CSV
Database	SQL
Version Control	Git & GitHub

Retail Sales Analysis/
│
├── data/
│   ├── SampleSuperstore_cleaned.csv
│   ├── region_summary.csv
│   ├── category_summary.csv
│   ├── region_summary-checkpoint.csv
│   └── SampleSuperstore.csv.zip
│
├── sql/
│   └── (SQL queries and scripts)
│
├── src/
│   └── (Helper scripts / modular Python code)
│
├── 01_EDA.ipynb               # Exploratory Data Analysis notebook
├── analysis.ipynb             # Additional analysis + visuals
├── requirements.txt           # Python dependencies
├── .gitignore                 # Ignored files and folders
└── README.md                  # Project documentation

📊 Dashboard Preview

(Add a screenshot named dashboard.png inside powerbi/ and use the line below)

📌 Interactive Power BI Dashboard


🧹 1. Data Cleaning

Performed steps:

Removed duplicates

Handled missing values

Checked data types

Standardized date formats

Created new fields (Month, Year, Profit Margin)

This ensures accurate analysis.

🔍 2. Exploratory Data Analysis (EDA)

Analysis includes:

📈 Sales Trends

Monthly and yearly trends

Category-wise performance

Seasonal patterns

🛒 Product Category Insights

Top-performing categories

Most profitable subcategories

🌍 Regional Performance

Sales by region

Profit comparison across states

🎯 Customer Segment Analysis

High-value customer segments

Returning vs new customer contributions

🧷 3. SQL Analysis

Sample queries used:

-- Total sales by category
SELECT Category, SUM(Sales)
FROM superstore
GROUP BY Category;

-- Monthly sales trend
SELECT DATENAME(MONTH, OrderDate) AS Month, SUM(Sales)
FROM superstore
GROUP BY DATENAME(MONTH, OrderDate);

-- Top 10 profitable products
SELECT TOP 10 ProductName, SUM(Profit)
FROM superstore
GROUP BY ProductName
ORDER BY SUM(Profit) DESC;


SQL is used to validate Python results & perform backend analysis.

📊 4. Power BI Dashboard Features

KPI cards: Total Sales, Total Profit, Orders Count

Region-wise performance map

Category and Subcategory filters

Monthly Trend Line

Profitability heatmap

The dashboard summarizes entire business performance.

💡 5. Key Insights
🔸 Business Insights

Technology category contributes the highest profit.

The West region has the strongest sales trend.

Furniture has low profit despite high sales → improvement needed.

Certain states show negative profit due to high discounting.

🔸 Recommendations

Reduce discount rates for loss-making states.

Promote high-margin subcategories via targeted campaigns.

Optimize logistics in Central & South regions.

Expand Technology product line due to strong performance.

🧪 Installation & Usage
1. Clone the Repository
git clone https://github.com/Subikshavani/retail_analysis.git

2. Install Requirements
pip install -r requirements.txt

3. Open Jupyter Notebook
jupyter notebook
