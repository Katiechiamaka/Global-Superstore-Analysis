# Global Superstore Analysis
![photo_5769413029257743609_y](https://github.com/user-attachments/assets/a5c4fc64-b380-4349-ba2b-6e1b904bee3a)

# Project Overview
This dataset contains transactional retail sales data covering customer orders, products, shipping, and profitability across different Countries and time periods. It is designed for sales performance analysis, customer segmentation, profitability evaluation, and operational insights.

# Business Objectives
This analysis was guided by the following business objectives:

- Monitor overall sales and profit trends to assess business performance
  
- Identify regions, products, and customers driving losses for targeted improvements

- Highlight top-performing products and customers to inform growth strategies

- Analyze discount strategies and their effect on profit margins

- Manage outstanding customer balances to strengthen cash flow and reduce risk

- Deliver actionable insights through data visualization for informed decision-making

# Dataset Overview

- **Source:** Kaggle
- **Dataset Name:** Global Superstore Sales Dataset
- **Description:** Contains transactional sales data for a Global retail superstore, including information about products, customers, regions, shipping, discounts, and profits.
- **Time Period:** January 2011 – December 2014
- **Number of Records:** 51,290 rows
- **Number of Columns:** 27
- **Key Variables:** Order ID, Customer ID, Region, Product Category and Sub-category, Sales, Profit, Discount, Shipping Mode
- **Purpose:** Used to analyze Sales performance, profitability, and operational efficiency.


# Tools and Techniques
### Tools Used
- **Microsoft Excel** – For data exploration, analysis, and visualization
- **Power Query** – For data cleaning and transformation
- **Power Pivot** – For data modeling and advanced calculations using DAX

### Techniques Applied
- **Data Cleaning and Transformation** – Handled missing values, removed duplicates, and formatted data
- **Data Modeling** – Created relationships between tables and calculated measures
- **Exploratory Data Analysis (EDA)** – Summarized key metrics and identified patterns in sales, profit, and customer behavior
- **Tables and Charts** – Used pivot tables, regular tables, and charts to visualize data and communicate insights
- **Visualization and Dashboarding** – Built charts and interactive dashboards to highlight insights
- **Profitability and Loss Analysis** – Identified loss-making products, regions, and customers
- **Operational Analysis** – Analyzed shipping modes, discount impacts, and regional performance


# Data Modeling
- **Model Type:** Star Schema
- **Fact Table:** Orders – Contains transactional data such as sales, profit, quantity, and discount
- **Dimension Tables:**
  - `Customer` – Contains customer details (ID, name, segment, region)
  - `Product` – Contains product details (ID, category, sub-category, price)
  - `Location` – Contains regional and country information
  - `Calendar` – Contains date-related fields (order date, month, quarter, year)
- **Relationships:**
  - Each dimension table is linked to the `Orders` fact table via a primary key → foreign key relationship
  - All relationships are one-to-many (1 dimension record → many orders)
- **Purpose:**
  - Enables efficient aggregation and analysis of sales, profit, and operational metrics
  - Supports slicing and dicing the data by customer, product, location, and time
  - Facilitates creation of measures and KPIs using Power Pivot (DAX)

<img width="946" height="453" alt="Data Model" src="https://github.com/user-attachments/assets/56a4d418-0b6f-47af-a42d-81046855a418" />




