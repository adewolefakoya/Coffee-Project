# Coffee Sales Performance

> *End-to-End Sales Analytics, Customer Insights & Business Intelligence using Microsoft Excel*

---

## ⚙️ Project Type Flags
> 
 Microsoft Excel

---

## Table of Contents
1. [Project Overview](#1-project-overview)
2. [Objectives](#2-objectives)
3. [Project Scope & Tools](#3-project-scope--tools)
4. [Data Workflow](#4-data-workflow)
5. [Data Model & Schema](#5-data-model--schema)
6. [Analysis & Metrics](#6-analysis--metrics)
7. [Key Insights](#7-key-insights)
8. [Recommendations](#8-recommendations)
9. [Assumptions](#9-assumptions)
10. [Author](#10-author)

---

## 1. Project Overview

 The Coffee Sales Dashboard is an end-to-end Excel data analytics project designed to analyze coffee bean sales across different products, customers, countries, roast types, package sizes, and customer loyalty status.

The project starts with raw transactional order data and combines it with customer and product information. The data is then cleaned, transformed, enriched, analyzed using Pivot Tables, and visualized through an interactive Excel dashboard.

The final dashboard allows users to dynamically analyze sales performance using:

 Order-date timeline
 
 Coffee type
 
 Roast type
 
 Package size
 
 Country


The goal is to turn raw sales records into actionable business insights that can help management understand sales performance and customer behavior.


## 2. Objectives

  The main objective is to analyze coffee sales performance and build an interactive dashboard that allows users to easily identify sales trends and customer patterns.

Specific objectives

1. Analyze sales performance over time

Determine how total sales change by month and year.

This helps answer:

Are sales increasing, decreasing, or fluctuating over time?

2. Identify the best-performing coffee products

Analyze the performance of:

Arabica
Excelsa
Liberica
Robusta

This helps identify which coffee types generate the most revenue.

3. Analyze geographical performance

Compare sales across:

United States
Ireland
United Kingdom

This answers:

Which country generates the highest sales?

4. Identify high-value customers

Determine the Top 5 customers by sales.

This helps the business understand which customers contribute most to revenue.

5. Analyze customer behavior

Use the loyalty-card information to compare customers who have:

Loyalty cards
No loyalty cards

6. Analyze product characteristics

Evaluate sales based on:

Roast type
Package size
Coffee type

7. Create an interactive dashboard

Develop a dashboard where users can filter the data dynamically using slicers and a timeline.


## 3. Project Scope & Tools

### Scope

<!--
  WHAT GOOD LOOKS LIKE:
  In Scope: "Transaction-level data for Regions A–E, Jan 2023–Jun 2024.
             Analysis covers revenue, return rates, and product category performance."
  Out of Scope: "Customer demographics and marketing spend data were excluded -
                 demographic data was incomplete for two regions, and marketing
                 data sits in a separate system outside this engagement."

  WHAT TO AVOID:
  ❌ Leaving Out of Scope blank. This is the section that protects your credibility.
     If you don't define the fence, reviewers assume you missed things.
-->


### Tools & Technologies

The project covers the complete analytics process:

Raw Data → Data Gathering → Data Transformation → Data Validation → Analysis → Visualization → Dashboard → Insights

The analysis focuses primarily on sales performance and customer/product behavior.



| Category | Tool Used |
|----------|-------------|
| Data Storage | CSV files |
| Data Processing |  Excel |
| Analysis | Excel |
| Visualization | Excel |
| Version Control | GitHub |


---

## 4. Data Workflow

 The project follows a structured ETL-style workflow:
[Data Sources]
↓
[Data Ingestion / Collection]
↓
[Cleaning & Transformation]
↓
[Analysis / Modelling / Querying]
↓
[Output / Visualisation / Reporting]
1. **Source**

The project uses three Excel tables:
Orders: Order ID, Order Date, Customer ID, Product ID, Quantity
Customers: Customer ID, Customer Name, Email, Phone, Address, City, Country, Postal Code, Loyalty Card
Products: Product ID, Coffee Type, Roast Type, Size, Unit Price, Price per 100g, Profit

2. **Ingestion**
   
The data was provided in separate Excel worksheets and brought together within Microsoft Excel for analysis.

3. **Cleaning**

The data was checked for:
Duplicate records
Missing values
Inconsistent labels
Incorrect formats
Dates, currency, package sizes, and numeric fields were also standardized.

4. **Transformation**

XLOOKUP was used to retrieve customer information, while INDEX + MATCH was used to retrieve product information.
Additional fields were created, including:
Sales = Quantity × Unit Price
Coffee Type Name
Roast Type Name
Loyalty Card
Abbreviated values such as ROB, EXE, ARA, and LIB were converted to full coffee names.

5. **Analysis**

The cleaned dataset was converted into an Excel Table and analyzed using Pivot Tables and Pivot Charts.
Key analyses included:
Sales over time
Sales by country
Top 5 customers
Sales by coffee type
Sales by roast type
Sales by package size
Loyalty-card customer analysis

6. **Output**

The final output is an interactive Coffee Sales Dashboard containing:
Sales-over-time line chart
Sales-by-country bar chart
Top 5 customers bar chart
Order-date timeline
Roast Type slicer
Size slicer
Loyalty Card slicerk, processed CSV."

---

## 5. Data Model & Schema

  The project uses a relational-style data structure, although it is implemented within Excel rather than a dedicated database.
The main table is the:
Fact Table — Orders
Each row represents a customer order/transaction.
Important keys:
Order ID

Customer ID

Product ID

The Orders table connects to:
Customer Dimension

Customer ID → Customer information
and:
Product Dimension

Product ID → Product information

This structure resembles a star-schema approach, where the Orders table acts as the central transactional table and Customers/Products provide descriptive attributes.

### Dataset / Table: `CUSTOMER TABLE
             
             Customer ID
             
                  │
                  │
                  ▼
| ORDERS TABLE | PRODUCT TABLE |
|----------|-------------|
| Customer ID | Product ID |
|Product ID | Coffee Type |
| Order Date | Size |
|  Quantity  | Unit Price |
| Sales | Profit |
---



## 6. Analysis & Metrics

 The dashboard focuses on several important business metrics.

1. Total Sales

The primary metric is:

Total Sales = Σ(Unit Price × Quantity)

This measures the total revenue generated from coffee sales.

⸻

2. Monthly Sales

Sales are grouped by:

Year
Month

This allows the business to identify sales trends and seasonality.

The line chart displays sales over time by coffee type.

⸻

3. Sales by Coffee Type

The dashboard compares:

Arabica
Excelsa
Liberica
Robusta

This identifies which coffee products contribute most to revenue.

⸻

4. Sales by Country

Sales are analyzed by:

United States
Ireland
United Kingdom

This helps identify the strongest geographical market.

⸻

5. Top 5 Customers

Customers are ranked based on:

Total Sales

The dashboard displays the five customers generating the highest sales.

⸻

6. Sales by Roast Type

The dashboard allows analysis of:

Light
Medium
Dark

This can help identify customer preferences.

⸻

7. Sales by Package Size

The available package sizes include:

0.2 kg
0.5 kg
1 kg
2.5 kg

The slicer allows users to investigate how package size affects sales.

⸻

8. Loyalty Card Analysis

Customers are divided into:

Loyalty Card = Yes
Loyalty Card = No

This provides an opportunity to investigate whether loyalty customers contribute significantly to sales.

---

## 7. Key Insights

1. Identify the strongest coffee type

The sales-over-time chart allows management to see which coffee type consistently generates the most revenue.

For example, if Arabica consistently has the highest sales, the company may want to ensure sufficient inventory and marketing support for Arabica products.

⸻

2. Identify the strongest market

The Sales by Country chart identifies which geographic market generates the most revenue.

If the United States has the highest sales, it may represent the company’s most important market.

⸻

3. Identify high-value customers

The Top 5 Customers visualization highlights customers responsible for a significant portion of revenue.

These customers could be important for retention and relationship-management strategies.

⸻

4. Identify sales trends

The timeline and line chart allow users to identify:

Growth periods
Declining periods
Seasonal patterns
Strong and weak months

This can support sales forecasting and inventory planning.

⸻

5. Understand customer preferences

The slicers allow management to investigate whether customers prefer particular:

Roast types
Package sizes
Coffee types

⸻

6. Understand loyalty-card behavior

The Loyalty Card slicer can be used to compare purchasing behavior between loyalty and non-loyalty customers.

---

## 8. Recommendations

- Focus on high-performing coffee types

Increase marketing and inventory availability for coffee types that consistently generate the highest sales.

- Strengthen high-performing markets

If one country significantly outperforms others, consider:

Targeted marketing
Additional distribution
Local promotions
Market-specific product strategies

- Develop customer-retention strategies

The Top 5 customer analysis can help identify valuable customers.

The company could consider:

Loyalty rewards
Personalized promotions
Exclusive offers
Customer retention campaigns

 - Evaluate the loyalty program

Compare sales from loyalty-card customers against non-members.

If loyalty customers generate more revenue, expanding the loyalty program may be worthwhile.

- Optimize product sizes

Analyze which package sizes generate the most sales.

The company could prioritize inventory and promotions around the most popular sizes.

- Use sales trends for inventory planning

Historical sales patterns can help the business anticipate periods of high demand and avoid:

Overstocking
Stockouts
Excess inventory costs


## 9. Assumptions 

- Each Order ID represents a valid transaction.

- Customer ID is unique within the Customers table.

- Product ID is unique within the Products table.

- Customer and product information can be reliably connected to Orders using their respective IDs.
  
- Missing email addresses are treated as missing information rather than errors.
  
- The calculated Sales field represents revenue:

Sales = Unit Price × Quantity

- Unit prices are assumed to be accurate and applicable to the corresponding transactions.
  
- Currency values are assumed to be in US dollars, based on the dashboard formatting.

- Duplicate records identified during the data-validation stage are assumed to be unintended duplicates and can therefore be removed.
  
- Loyalty Card status is assumed to represent the customer’s membership status at the time of analysis.

**Analytical assumptions**

- Sales revenue is used as the primary measure of performance.

- The Top 5 Customers ranking is based on total sales, not profit.

- Country performance is evaluated based on sales revenue rather than number of orders.

- The analysis does not necessarily account for operating costs, marketing costs, shipping costs, or other expenses.

- Therefore, high sales do not necessarily mean high profitability.

- The dashboard is primarily descriptive rather than predictive; it explains historical performance rather than forecasting future sales.


---

## 10. Author

**Adewole Fakoya**

Data Analyst

- 🔗 (https://www.linkedin.com/in/adewole-fakoya-7484a5149)
- 📧 [Email - Adewolewa@gmail.com]

---

*Last updated: [Month YYYY]*
*If this template helped you, consider starring the repository.*
