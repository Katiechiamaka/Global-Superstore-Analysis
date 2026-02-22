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

# Key Business Questions Answered
## Time-Based Sales Performance Analysis
- How has overall sales performance evolved over the past years?

<img width="736" height="404" alt="Screenshot 2026-02-21 192849" src="https://github.com/user-attachments/assets/b00dc955-11d1-4152-9381-fda26ae58efb" />

#### Insights
- Sales increased consistently every year, from 2011 to 2014, sales grew by $2.04M overall. That represents nearly 90% total growth over four years.

### Monthly Trend Analysis
- Which months consistently generate the highest sales?
- How does monthly sales growth fluctuate?
- Which months generate the highest profit?

<img width="1470" height="558" alt="Screenshot 2026-02-21 193909" src="https://github.com/user-attachments/assets/142d1387-626f-4a97-8ef8-2d251eed3a52" />

#### Insights
- Q3 (July - Sep) and Q4 (Oct - Dec) are high-performance periods. July appears to be a recurring risk month with a decrease in sales and profit.
- July shows both sales decline and profit drop. However, profit steadily improves toward Q4.
- While December has the most sales, November generates the highest overall profit at $175.4K, followed closely by December ($170.7K) and September ($170.4K).

## Market Performance Analysis
### Regional Sales & Profit Margin Across Market
- Which region generates the highest profit?
- Which regions are underperforming in profit despite moderate or high sales?
- Which region has the highest Profit Margin?
<img width="1546" height="496" alt="Screenshot 2026-02-21 204418" src="https://github.com/user-attachments/assets/ac5f3399-7b73-49ec-9e51-abeb7d04a201" />

#### Insights
- The Central region generates the highest total profit ($311.4K) driven by the largest sales volume (41.8K units), though its margin is moderate (11%).
- South and Southeast Asia underperform due to low profit margins despite maintaining moderate to high sales volumes.
- Canada has the highest profit margin at 26.6%, making it the most efficient and profitable region relative to revenue.


## Product Category and Sub-category Analysis
### Product Performance
- Which of the top 10 best-selling products are also among the top 10 most profitable?
- Which products have strong sales volume but relatively low profitability?
- Are there products that generate high profit despite not being top sellers?

<img width="1804" height="510" alt="Screenshot 2026-02-22 185136" src="https://github.com/user-attachments/assets/7bc4ee74-14aa-4060-affa-9d08ad9b4ff0" />

#### Insights
- Cisco Smart Phone (Full Size), Motorola Smart Phone (Full Size), Nokia Smart Phone (Full Size), Canon imageCLASS 2200 Advanced Copier, and Nokia Smart Phone (with Caller ID) appears to be both high sellling and profit generating, indicating strong profit alignment.
- Apple Smart Phone (Full Size) leads in sales but does not add to profitability, suggesting thinner margins.
- The Canon imageCLASS 2200 generates the highest profit but ranks fifth in revenue, showing strong margin efficiency.


### Category and Sub-Category Performance
- Which category contributes the highest overall profit?
- Which sub-category generates the highest profit?
- Which sub-categories have strong sales but weak margins?
- Are any sub-categories showing signs of profitability risk?

<img width="1442" height="498" alt="Screenshot 2026-02-22 013237" src="https://github.com/user-attachments/assets/f68e1336-8581-49a0-841e-14447093bf9a" />

#### Insights
- Technology is the most profitable category, generating approximately $663.8K, making it the primary profit driver.
- Copiers ($258.6K) generate the highest profit, followed by Phones ($216.7K).
- Tables show moderate sales ($757K) but generate a loss (-$64.1K), indicating serious margin issues.
- Yes. Machines generate approximately $58.9K profit on $779K in sales, indicating a relatively low profit to sales ratio and suggesting potential margin pressure that requires close monitoring and cost optimization review.

## Risk and Loss Analysis
### Customer Performance
- Which customer is responsible for the most ouststanding balance?
- What is driving outstanding balances among the top owing customers?
<img width="1587" height="405" alt="Screenshot 2026-02-22 000406" src="https://github.com/user-attachments/assets/d9fba595-616d-41ac-b1f5-26bb1e113277" />

#### Insights
- Cindy Stewart with an outstanding balance of (-$6,151). 
- Customers with large negative balances suggest delayed payments or extended credit terms.

### Country Performance
- Which countries are contributing the most to overall losses?
- Are the losses due to high shipping costs?
<img width="654" height="574" alt="Screenshot 2026-02-22 000959" src="https://github.com/user-attachments/assets/e792b1eb-f539-47f6-b63d-ff9ff126aa83" />

#### Insights
- Countries such as Turkey is the largest source of financial drain with a loss of -$98.4K, followed closely by Nigeria at -$80.8K, making these two countries the primary targets for urgent cost-cutting and strategy shifts.
- Large losses in these countries suggest that logistics and shipping to these specific regions may be significantly eating into revenue.

### Product Performance
- Which products are consistently generating losses?
- Which Subcategory is generating loss?
- Should loss-making products (e.g., 3D printers, furniture items) be discontinued, repriced, or cost-optimized?
<img width="1165" height="471" alt="Screenshot 2026-02-22 000910" src="https://github.com/user-attachments/assets/f7bfef61-9b25-4875-8963-36ab800cab03" />

#### Insights
- The largest loss comes from the Cubify CubeX 3D Printer Double Head Print (-$8,879.97).
- Tables is the only loss-making sub-category, generating a negative profit (−$64.1K)
- Tables and storage products particularly from the Bevis and Rogers brands, consistently generate losses, indicating potential issues with pricing strategy, excessive discounting, or an unfavorable cost structure.
  
  However, loss making products should first be reviewed for pricing errors, high cost of goods, or excessive discounting before discontinuation.


## Shipping mode and Discount Analysis

<img width="1188" height="461" alt="Screenshot 2026-02-22 225616" src="https://github.com/user-attachments/assets/606b8c7d-1df8-4ef6-8527-41ab1fbe2081" />

# Key KPIS 
- **Total Revenue:** $12.64M
- **Total Orders:** 25,035
- **Total Quantity Sold:** 175K
- **Average Order Value:** $505
- **Profit Margin:** 11.61%
- **Total Customer Debt:** -$65.51K
- **Total Countries Debt:** -$447.9K

# DashBoard
### Global Superstore Dashboard Overview
<img width="932" height="412" alt="Global Superstore Dashboard Overview" src="https://github.com/user-attachments/assets/ae36a130-dbac-47ef-9ab3-07ab7317ed3b" />

### Sales And Profit Analysis
<img width="933" height="410" alt="Global Superstore Sales and Profit Analysis" src="https://github.com/user-attachments/assets/709216a7-5923-4413-ad39-d82fc1e70534" />

### Risk And Loss Analysis 
<img width="934" height="410" alt="Global Superstore Risk and Loss Analysis" src="https://github.com/user-attachments/assets/2b6efa3c-a7ee-4f71-a4ad-3a06b2de3fde" />

# Recommendation
1. Review Discount Strategy

Implement controlled discount thresholds.

Avoid high discounts on already low-margin products.

2. Reprice or Discontinue Loss Products

Re-evaluate pricing for Cubify printers and Tables.

Consider discontinuing consistently loss-generating items.

3. Focus on High-Margin Markets

Invest more in Canada and North Asia.

Improve operational efficiency in Southeast Asia.

5. Strengthen Credit Management

Improve customer payment policies.

Reduce outstanding debt exposure.


# Challenges Faced And How it was Solved
- **Data Quality Issues:** Missing values and inconsistent formatting.
    - Solved by data cleaning and standardization.
- **Profit Distortion Due to Discounts:** Difficult to identify true profit drivers.
    - Solved by isolating discounted vs non-discounted performance.
- **Multi-Dimensional Analysis:** Complex relationships across regions, categories, and time.
    - Solved by implementing a Star Schema data model.
- **Identifying True Loss Drivers:** Sales did not equal profit.
    - Used sub-category and product-level drilldowns


# Conclusion
The Global Superstore demonstrates strong revenue growth and expanding operations. However, profitability is being eroded by:
  - Excessive discounting
  - Loss-making furniture sub-categories (Tables)
  - Low-margin markets
By optimizing discount policies, refining product mix, and focusing on high-margin markets, the business can significantly improve its overall profit margin beyond the current 11.61%.


