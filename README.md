# Project Overview
This project performs an end-to-end analysis of supermarket sales data using Power BI and KNIME.
It covers the full data analytics lifecycle: ETL, data modeling, business intelligence dashboards, exploratory data analysis (EDA), and machine learning regression models for sales prediction.
The goal of the project is to extract actionable insights from retail data and evaluate machine learning models for predicting sales performance.

# Dataset Description
Records: 9,800 sales transactions
Granularity: Each row represents one product sold within an order

## Data Includes:
- Order Information: Order ID, Order Date, Ship Date, Ship Mode
- Customer Information: Customer Name, Segment, City, State, Region
- Product Information: Category, Sub-Category, Product Name
- Sales: Revenue per product

## ETL Process (Power BI)
- Extraction
  Data loaded from an Excel file into Power Query Editor.
- Transformation
  Corrected data types across all columns
  Fixed incorrect date formats (Order Date & Ship Date)
  Replaced null Postal Codes with "Unknown"
  Created a Row ID column as a primary key
  Applied data normalization to improve performance and modeling
- Normalized Tables
  Customers Table (customer details and location)
  Products Table (category and product information)
  Order Details Table (transactional data and sales)
- Load
  Cleaned and modeled data loaded into Power BI for analysis and reporting.

## DAX Measures & Calculated Columns:
- Key DAX Measures:
  Total Sales
  Total Orders
  Total Customers
  Total Products
  Average Shipping Duration
- Calculated Columns:
  Shipping Days
  Year
  Month
  Quarter
These enable time-based analysis and performance tracking.

# Exploratory Data Analysis (KNIME)
- The following visualizations were created in KNIME:
  Category vs Sales (Pie Chart)
  Sub-Category vs Total Sales (Bar Chart)
  Order ID vs Sales (Scatter Plot)
  Sales Distribution (Histogram)
  Category vs Region (Heatmap)
  Sales vs Segment (Density Plot)
  These visuals helped identify sales patterns, top-performing categories, and regional behavior.

# Machine Learning Models
Two regression models were developed in KNIME to predict Sales.
- Input Features:
Ship Mode,Segment,Country,State,Region,Category
Sub-Category,Models Used

- Linear Regression
- Random Forest Regression

- Model Evaluation
Evaluation was performed using standard regression metrics:
R²
MAE (Mean Absolute Error)
MSE (Mean Squared Error)
RMSE
MAPE

# Results Summary
Both models showed negative R², indicating weak predictive performance
Linear Regression performed slightly better than Random Forest
High dependence on categorical features limited model accuracy

# Tools & Technologies
- Power BI (ETL, Data Modeling, DAX, Dashboards)
- KNIME (EDA, Visualization, Machine Learning)
- Excel (Data Source)

