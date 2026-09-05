# 🍕 Pizza Sales Analysis & Demand Prediction

## 📌 Project Overview

This project analyzes pizza sales data to understand customer demand, sales performance, revenue generation, inventory waste, and pricing patterns.

The project uses **Python, Pandas, NumPy, Matplotlib, Seaborn, and Scikit-learn** to perform data cleaning, exploratory data analysis (EDA), feature engineering, and machine learning.

The main objective is to convert raw pizza sales data into meaningful **business insights** and build a machine learning model that can predict pizza sales.

---

## 🎯 Objectives

The key objectives of this project are:

- Analyze overall pizza sales performance.
- Identify the best-selling pizzas.
- Identify pizzas generating the highest revenue.
- Compare Veg and Non-Veg pizza performance.
- Analyze pizza pricing and its relationship with sales.
- Identify pizzas with high unsold quantities.
- Understand sales and revenue patterns.
- Analyze sales trends over time.
- Identify relationships between numerical variables.
- Build a machine learning model to predict pizza sales.
- Provide actionable business recommendations.

---

## 📊 Dataset

The dataset contains pizza sales information with the following columns:

| Column | Description |
|---|---|
| `Date` | Date of the pizza sale |
| `Pizza_Name` | Name of the pizza |
| `Category` | Pizza category such as Veg or Non-Veg |
| `Pizza_Code` | Unique code assigned to the pizza |
| `Price_USD` | Price of the pizza in USD |
| `Sales` | Number of pizzas sold |
| `Unsold` | Number of unsold pizzas |
| `Revenue` | Revenue generated from pizza sales |
| `Rating` | Performance/rating category |

### Dataset Size

- **Rows:** 61
- **Columns:** 9

---

## 🛠️ Technologies Used

### Programming Language
- Python

### Libraries

- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

### Development Environment

- Jupyter Notebook
- VS Code / Anaconda

---

## 📁 Project Structure

```text
Pizza Sales
│
├── data
│   └── Pizza_Sales_Dataset_Extra_Rows.xlsx
│
├── notebook
│   ├── 01_Data_Cleaning.ipynb
│   ├── 02_EDA.ipynb
│   ├── 03_Feature_Engineering.ipynb
│   └── 04_Machine_Learning.ipynb
│
├── README.md
│
└── PowerBI
    └── Pizza_Sales_Dashboard.pbix
```

---

# 🔍 Exploratory Data Analysis

The EDA section focuses on understanding the dataset and identifying important business patterns.

### Key Analysis

1. Pizza-wise sales analysis
2. Pizza-wise revenue analysis
3. Unsold pizza analysis
4. Veg vs Non-Veg analysis
5. Price distribution
6. Sales distribution
7. Revenue distribution
8. Price vs Sales relationship
9. Sales vs Revenue relationship
10. Category-wise sales
11. Category-wise revenue
12. Rating distribution
13. Correlation analysis
14. Time-based sales analysis

---

## 📈 Visualizations

The project includes visualizations such as:

- Bar Charts
- Pie Charts
- Histograms
- Scatter Plots
- Line Charts
- Correlation Heatmaps

These visualizations help identify trends and relationships that are difficult to understand from raw data.

---

# 🤖 Machine Learning

After completing EDA, machine learning models will be used to predict pizza sales.

### Target Variable

```text
Sales
```

### Candidate Models

- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor

### Evaluation Metrics

The models will be evaluated using:

- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R² Score

The best-performing model will be selected based on its evaluation performance.

---

# 💡 Business Questions

This project attempts to answer questions such as:

### Sales

- Which pizza sells the most?
- Which pizza has the lowest sales?
- Which category has the highest sales?

### Revenue

- Which pizza generates the highest revenue?
- Which category contributes the most revenue?

### Inventory

- Which pizza has the highest unsold quantity?
- Which pizzas may require better inventory planning?

### Pricing

- Does pizza price affect sales?
- Is there a relationship between price and revenue?

### Customer Demand

- Are customers more likely to purchase Veg or Non-Veg pizzas?
- Which pizzas should receive more inventory?

---

# 📌 Business Recommendations

Based on the analysis, the business can:

- Focus marketing campaigns on high-performing pizzas.
- Maintain sufficient inventory for popular pizzas.
- Reduce production of pizzas with consistently high unsold quantities.
- Review pricing strategies for low-selling expensive pizzas.
- Promote pizzas with high ratings and strong sales performance.
- Use historical sales patterns to improve demand planning.
- Use machine learning predictions to support future inventory decisions.

---

# 📊 Power BI Dashboard

A Power BI dashboard can be created to provide an interactive business view of the pizza sales data.

### Dashboard KPIs

- Total Revenue
- Total Pizzas Sold
- Total Unsold Pizzas
- Average Pizza Price
- Average Rating

### Recommended Charts

- Sales by Pizza
- Revenue by Pizza
- Sales by Category
- Revenue by Category
- Unsold Pizzas by Pizza
- Sales Trend Over Time
- Price vs Sales
- Rating Distribution

### Interactive Filters

- Date
- Pizza Name
- Category
- Rating

---

# 🚀 Project Workflow

```text
Raw Dataset
     ↓
Data Loading
     ↓
Data Cleaning
     ↓
Exploratory Data Analysis
     ↓
Feature Engineering
     ↓
Data Visualization
     ↓
Machine Learning
     ↓
Model Evaluation
     ↓
Business Insights
     ↓
Power BI Dashboard
```

---

# ⚠️ Dataset Limitation

The current dataset contains only **61 records**, which is relatively small for machine learning.

Therefore, the predictive model should be considered a **learning and portfolio project**, rather than a production-ready demand forecasting system.

A larger dataset containing several months or years of pizza transactions would provide more reliable predictions.

---

# 🔮 Future Improvements

The project can be extended by:

- Using a larger real-world pizza sales dataset.
- Building time-series forecasting models.
- Adding customer-level transaction data.
- Predicting daily/weekly demand.
- Building an automated sales dashboard.
- Deploying the prediction model using Streamlit.
- Adding real-time sales data.
- Implementing advanced models such as Random Forest, XGBoost, or Gradient Boosting.

---

# 👨‍💻 Author

**Tejas Thete**

Data Science Project  
Python | Pandas | NumPy | Matplotlib | Seaborn | Scikit-learn | Power BI

---

## ⭐ Project Goal

> **Turn pizza sales data into actionable business insights and use machine learning to support better sales and inventory decisions.**