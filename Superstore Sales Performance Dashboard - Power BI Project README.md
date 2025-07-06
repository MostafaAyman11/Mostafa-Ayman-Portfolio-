# Superstore Sales Performance Dashboard - Power BI Project

## 💡 Project Overview

This project focuses on developing a comprehensive and interactive Power BI dashboard to analyze and optimize sales performance of a superstore dataset. The goal is to deliver meaningful insights through clear visualizations, advanced data modeling, and time intelligence for stakeholders including business managers, sales executives, and data analysts.

📊 **Live Dashboard**: [View Dashboard](https://app.powerbi.com/links/2Ptbku6hpH?ctid=55f2965b-c160-40b8-90dc-52f4e06bb384&pbi_source=linkShare)

---

## 🔢 Objectives

* Build a data-driven Power BI dashboard with dynamic filters and visuals.
* Track and visualize total sales, shipping efficiency, and customer segmentation.
* Analyze order trends, best-selling categories, and regional performance.
* Provide executive-friendly and drill-down analytical views.
* Giving some recommendations.

---

## 🗕️ Project Planning & Management

### ✉️ Project Proposal

* **Scope**:

  * **Sales Performance**: Products, categories, monthly/quarterly/yearly trends.
  * **Customer Insights**: Segmentation, frequency, and purchasing behavior.
  * **Shipping Analysis**: Mode, speed, and delivery trends.
  * **Geographical Trends**: Comparison across states and regions.

### ✅ Project Plan

| Phase                             | Tasks                                                           |
| --------------------------------- | --------------------------------------------------------------- |
| 1. Data Collection                | Import sales, customer, and shipping datasets                   |
| 2. Data Cleaning & Transformation | Handle nulls, fix formats, parse dates, standardize columns     |
| 3. Data Analysis & Metrics        | Create KPIs, customer segments, shipping insights               |
| 4. Dashboard Development          | Build Power BI report visuals and interactive components        |
| 5. Review & Refinement            | QA checks, visual refinement, user testing                      |
| 6. Presentation & Documentation   | Final report, README, dashboard export, stakeholder walkthrough |

### 🛠️ Resources Used

* Microsoft Excel (initial data)
* Power Query Editor
* Power BI Desktop

### ⚠️ Risk Assessment

| Risk                      | Mitigation Strategy                                |
| ------------------------- | -------------------------------------------------- |
| Data format inconsistency | Apply locale-specific parsing and validations      |
| Slow performance          | Optimize data models and use efficient DAX queries |

### 📈 KPIs Tracked

* Total Sales
* Sales by Category, Sub-Category, and Region
* Total Customers
* Average Order Value (AOV)
* Orders by Ship Mode
* Average Delivery Time
* Monthly and Year-over-Year Sales

---

## 📖 Literature Review

* Stakeholder feedback led to enhancements in layout, filter experience, and summary visuals.
* Key improvements include tooltips, customer drilldowns, and consistent regional segmentation.
* Evaluation criteria: **accuracy**, **storytelling**, **interactivity**, **load time**, and **visual quality**.

---

## 📊 Requirements Gathering

### Stakeholders

* Sales Managers
* Business Executives
* Regional Analysts

### User Stories

> "As a sales manager, I want to track monthly and regional sales trends to identify peak seasons."

### Functional Requirements

* Time-based filtering and visuals.
* Regional and category-level sales insights.
* Drill-down capabilities to customer level.

### Non-Functional Requirements

* Dashboard should load in <5 seconds.
* All visuals should be clear, labeled, and context-aware.

---

## 📝 System Analysis & Design

### ⚠️ Problem Statement

Manual reporting is inefficient and lacks granularity. Automating data analysis using Power BI enables better performance monitoring and strategic decision-making.

### △ Use Case Summary

* **Admin**: Update data & manage source files.
* **Analyst**: Build and enhance visuals and insights.
* **Business User**: Navigate dashboard and make decisions.

### ▴ Architecture

* Source: Excel/CSV
* ETL: Power Query in Power BI
* Output: Interactive dashboard deployed via Power BI Service

---

## 📁 Database & Data Modeling

### ✍️ ER Design

* **Fact Table**: `Sales_Fact`
* **Dimensions**: `Dim_Product`, `Dim_Region`, `Dim_Customer`, `Dim_Ship`, `Calendar`

### ⚖️ Relationships

* Many-to-One relationships:

  1. `Dim_Customer` → `Dim_Region` via Region_ID
  2. `Sales_Fact` → `Dim_Customer` via Customer ID
  3. `Sales_Fact` → `Calender` via Date
  4. `Sales_Fact` → `Dim_Country` via Postal Code
  5. `Sales_Fact` → `Dim_Product` via Product ID
  6. `Sales_Fact` → `Dim_Region` via Region_ID
  7. `Sales_Fact` → `Calender` via Date
  8. `Sales_Fact` → `Dim_Region` via ShipModeID

![Data Modeling Diagram](https://github.com/user-attachments/assets/f4c08ea1-9f84-4d9c-9d56-2cc2c38726d3)

![Relationships View](https://github.com/user-attachments/assets/b6610c00-0728-49ce-a9fb-5efd08117355)

---

## 🧰 Order Date Parsing: Power Query Documentation

### 🔹 Problem:

Power BI couldn't parse dates in DD/MM/YYYY format due to locale mismatch. Example error:
`DataFormat.Error: We couldn't parse the input provided as a Date value. Details: 15/04/2018`

### ✅ Solution:

1. Converted `Order Date` to **Text** to avoid auto-parsing.
2. Created custom column with M code:

```m
try
    let
        cleanText = Text.Trim([Order Date]),
        parts = Text.Split(cleanText, "/")
    in
        if List.Count(parts) = 3 then
            #date(Number.FromText(parts{2}), Number.FromText(parts{1}), Number.FromText(parts{0}))
        else null
otherwise null
```

3. Converted new column to type `Date`.
4. Removed or renamed original column.
5. Clicked **Close & Apply** to load changes.

---

## 🔄 DAX Measures

### Aggregates & Calculations

```DAX
AOV = DIVIDE([Total sales], [Orders])
Sales Previous Year = CALCULATE([Total sales], PREVIOUSYEAR('Calendar'[Date]))
Growth Profit = DIVIDE([Total sales] - [Sales Previous Year], [Sales Previous Year])
Sales Color = IF([Growth Profit] >= 0, "green", "red")
Sales Color 2 = IF([Total sales] >= 100, "green", "red")
Avg. Sales = AVERAGE(Sales_Fact[Sales])
Total Sales = SUM(Sales_Fact[Sales])
```

---

## 📃 Dashboard Structure (Pages)

### Page 1: Executive Overview

![Sales Performance Overview](https://github.com/user-attachments/assets/8a3695f3-e870-48e8-a3cb-5ebb4ee13984)

* **November recorded the highest total sales**, significantly outperforming February by a margin of 489.78%, confirming a strong end-of-year performance.
* **Furniture led category sales in 2017**, followed by Office Supplies and Technology, contrary to claims that Technology was the top performer.
* **Sub-category sales ranged between 42K and 82K**, with Chairs and Phones leading figures outside this range are not reflected in the 2017 data.
* **Q4 delivered the highest total sales across all categories**, but Technology's contribution did not account for 14.04% this figure is not supported by the visualized data.

### Page 2: Sales Analysis

![State Sales Performance](https://github.com/user-attachments/assets/62353722-6571-4f16-88de-a1446d5f27a3)

* **Total sales reached 2.26M**, generated from **10K orders** across **793 customers**, with an **Average Order Value (AOV) of $230.8**.
* **November was the strongest sales month (0.35M)**, followed by **December (0.32M) and September (0.30M)**, showing a consistent Q4 peak.
* **California led all states with 200K in total sales**, followed by **New York (118K) and Texas (91K)**.
* The **lowest-performing months were February (0.06M) and January (0.09M)**, indicating potential seasonality in demand.
* The **map visualization confirms broad nationwide sales coverage**, with larger concentrations across coastal and urban states.

### Page 3: Customer & Regional Insights

![Customer & Region Insights](https://github.com/user-attachments/assets/6e24f53e-ede4-47ea-8943-b04b25e5b4ac)

* **Total sales reached 2M across 10K orders**, with the **West region leading at 391K**, followed by **East (343K) and Central (298K)**.
* **The West region dominated across all segments**, especially Corporate (190K) and Home Office (120K), highlighting strong business demand.
* **Furniture was the top-selling category in every region**, particularly in the West (270K), where it outperformed Office Supplies and Technology.
* **California led state-level sales (83K), with San Diego, Los Angeles, and San Francisco** being the top-performing cities.
* **Customer distribution was highest in the West (32%)**, followed by the South (27.7%) and Central (23.2%), indicating strong brand presence in western and southern markets.

### Page 4: Order & Shipping Details

![Order and Shipping Details](https://github.com/user-attachments/assets/a5c96160-eb87-4cae-b9be-55b7e9a4f776)

* Total orders reached 10,000, serving 793 customers over the analyzed period.
* Standard Class shipping dominated, accounting for nearly 60% of sales and the majority of orders.
* Sales and order volumes are highest at the start of the year, then steadily decline month by month.
* Second Class and First Class shipping modes contributed significantly less, with Same Day being the least utilized.
* The data highlights a clear customer preference for Standard Class shipping and reveals a need to address declining monthly order trends.

### Page 5: Summary Report

![Summary Report](https://github.com/user-attachments/assets/7ed81e7e-00de-4628-8c66-cad782313172)

* Adrian Barton (West, Consumer) is the top customer with 14,474 in sales.
* Adam Bellavance (East, Home Office) and Alan Dominguez (Central, Home Office) follow with 7,756 and 6,107 respectively.
* High-value customers are distributed across West, East, and Central regions.
* Both Consumer and Corporate segments are strongly represented among top customers.

Sales are spread throughout the year, with no single month or segment dominating.
---

## 📖 Report Design Guidelines

* Professional layout with consistent Visualizations using Power BI
* Use of slicers for interactivity and filtering
* Color-coded segments and categories
* Time filter standardization across all visuals

---

## 🚀 Deployment & Testing

* Data Source: CSV (Excel export)
* Excel Dataset: ![Excel Preview](https://github.com/user-attachments/assets/ce262ada-3701-4a39-b6b8-c46dbace541e)
* Excel File Link: [Download Excel File](https://docs.google.com/spreadsheets/d/149BCm8p2eFRYamqlQWPyGHqKe9dtfDz8/edit?usp=sharing&ouid=104502612719527840097&rtpof=true&sd=true)
* Environment: Power BI Desktop & Service
* Deployment Plan: Publish to Power BI Workspace
* QA: Tested for data accuracy, load speed, and filter responsiveness

---

## 📍 Summary & Conclusion

This Power BI report offers a complete analytical experience covering:

* High-level KPIs for decision makers
* In-depth sales and shipping insights
* Regional and customer analysis
* Clean, optimized design for fast and error-free reporting

By resolving locale-related date parsing issues and applying strong modeling principles, the dashboard delivers actionable insights that improve sales strategy and operational performance.

### 🔧 Summary of Priority Actions

* Boost sales in underperforming regions
* Focus on high-gross profit product categories
* Optimize inventory for best-selling items
* Target marketing efforts by customer segment
* Monitor sales trends to adjust pricing and promotions

---

## 📢 Contact

**Mostafa Ayman**
📧 Email: [mostafaayman112005@gmail.com](mailto:mostafaayman112005@gmail.com)
📞 Phone: 01020258416
🔗 [LinkedIn](https://linkedin.com/in/mostafa-ayman5)

> This project was my graduation capstone for the **DEPI 300-hour program offered by the Ministry of Communication**, where I was awarded a degree of **excellence**. It is part of my Data Analytics Portfolio and demonstrates my end-to-end proficiency in Power BI, including data transformation, modeling, and visualization.
