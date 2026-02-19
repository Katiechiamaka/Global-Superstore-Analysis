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

# Dataset Description

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

# Data Cleaning And Preparation
To ensure accurate and reliable insights, the dataset underwent the following steps:
- Conducted data inspection to understand structure and relationships.
- Handled missing values, and checked for duplicate records.
- Standardized categorical data types.
- Cleaned inconsistent text entries (regions, product names, etc.).
- Created calculated metrics such as Profit Margin (%).
- Extracted Year and Month from Order Date and Shipment Date for time-based analysis.

# Data Modeling
- **Model Type:** Star Schema
- **Fact Table:** `Orders` – Contains transactional data such as Order Id, Order Priority, Sales, Profit, Quantity, and Discount
- **Dimension Tables:**
  - `Customer` – Contains customer details (Row ID, Customer ID, Customer Name, Segment)
  - `Product` – Contains product details (Product ID, Product Name, category, sub-category, price)
  - `Location` – Contains regional and country information
  - `Calendar` – Contains date-related fields (order date, month, quarter, year)

- **Relationships:**
  - Each dimension table is linked to the `Orders` fact table via a primary key → foreign key relationship
  - All relationships are one-to-many (1 dimension record → many orders)
- **Purpose:**
  - Enables efficient aggregation and analysis of sales, profit, and operational metrics
  - Facilitates creation of measures and KPIs using Power Pivot (DAX)

<img width="946" height="453" alt="Data Model" src="https://github.com/user-attachments/assets/56a4d418-0b6f-47af-a42d-81046855a418" />

# Key Questions And Analysis




# Key Insights (KPIS)


# DashBoard
### Global Superstore Dashboard Overview
<img width="932" height="412" alt="Global Superstore Dashboard Overview" src="https://github.com/user-attachments/assets/ae36a130-dbac-47ef-9ab3-07ab7317ed3b" />

### Sales And Profit Analysis
<img width="933" height="410" alt="Global Superstore Sales and Profit Analysis" src="https://github.com/user-attachments/assets/709216a7-5923-4413-ad39-d82fc1e70534" />

### Risk And Loss Analysis 
<img width="934" height="410" alt="Global Superstore Risk and Loss Analysis" src="https://github.com/user-attachments/assets/2b6efa3c-a7ee-4f71-a4ad-3a06b2de3fde" />

# Recommendation


#Challenges Faced And How it was Solved



# Conclusion



