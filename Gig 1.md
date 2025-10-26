# 📊 Power BI Freelance Platform Dashboard

This repository contains the analysis for a **comprehensive Business Intelligence dashboard** built for a **freelance/gig platform**, focusing on a coffee shop client.  
The main goal was to analyze **sales trends, client behavior, and operational efficiency** to provide **data-driven recommendations** that enhance performance, loyalty, and resource optimization.

---

## 🚀 Live Interactive Dashboard

Click below to explore the live, interactive Power BI report:

👉 [**Open Live Power BI Dashboard**](https://app.powerbi.com/links/qZgu2OQ7v_?ctid=55f2965b-c160-40b8-90dc-52f4e06bb384&pbi_source=linkShare)

---

## 💾 Data Source

The dataset used for this project is an **Excel workbook** containing multiple sheets for sales, products, and sales channels.

📂 [View Raw `.xlsx` Data on GitHub](https://github.com/MostafaAyman11/Images-assets/blob/main/Gig.1%20Freelance%20Yard.xlsx)

---

## 🧭 Contents

- [💡 Actionable Insights & Recommendations](#-actionable-insights--recommendations)
- [🔍 Interactive Slicers & Filters](#-interactive-slicers--filters)
- [🔧 Technical Process & Data Model](#-technical-process--data-model)
- [🛠️ Skills & Tools](#️-skills--tools)
- [📸 Dashboard Previews](#-dashboard-previews)

---

## 💡 Actionable Insights & Recommendations

This dashboard is divided into **three analytical pages**, each answering a key business question and providing actionable insights.

---

### 1️⃣ Seasonal Promotions Strategy

**Business Goal:** Identify which drinks peak during specific months or seasons to plan targeted promotions.

**Insights:**
- "Pastries" are the most consistent high seller.
- "Cold Brew" sales spike around **April**, showing strong seasonality.
- "Espresso" maintains a steady but lower sales level.

**Recommendation:**  
Launch a **"Spring Bundle"** in late March–early April, pairing **Pastries** with **Cold Brew**.  
This leverages seasonal demand while boosting complementary sales.

---

### 2️⃣ Wholesale vs. Direct Channel Analysis

**Business Goal:** Evaluate the frequency and value of wholesale vs. direct sales channels.

**Insights:**
- Revenue is nearly evenly split:  
  - **Direct:** $270.02K  
  - **Wholesale:** $268.86K
- **Wholesale** clients place 1,009 orders — about 2.94 per day — indicating strong loyalty.
- Sales peak notably in **May** and **September**.

**Recommendation:**  
Implement a **tiered loyalty program** for wholesale customers:
- **Volume Discount:** 5% off for clients ordering above the monthly average.  
- **Frequency Bonus:** Free delivery for clients with 4+ monthly orders.

This strategy strengthens the wholesale segment, which contributes 50% of total revenue.

---

### 3️⃣ Operational Staffing & Footfall

**Business Goal:** Identify peak hours to optimize staffing schedules.

**Insights:**
- **Afternoon** is the busiest period, followed by **Morning**.  
- **Night shifts** show low activity.
- Sales are consistent across days, with slight peaks on **Monday** and **Saturday**.

**Recommendation:**  
- Increase staff during **afternoon hours (12 PM – 4 PM)**.  
- Maintain standard staff in mornings.  
- **Reduce night staff** and reallocate that time for cleaning/restocking tasks.

---

## 🔍 Interactive Slicers & Filters

To ensure flexibility and self-service analytics, multiple **interactive slicers** were added.

**Why They Matter:**  
Slicers empower decision-makers to answer questions like:  
> “How did Espresso sales perform in the Afternoon of February 2024?”  
in just a few clicks — without needing a new report.

**Slicers Implemented:**
- **Time-Based:** Year, Month, DayName, Time of Day  
- **Product-Based:** Category (Cold Brew, Espresso, Pastries)

This interactivity transforms the dashboard into a dynamic analytical tool for discovering hidden trends and patterns.

---

## 🔧 Technical Process & Data Model

**Data Connection & Modeling:**  
Connected the multi-sheet Excel file into Power BI, then built a clean **Star Schema** to optimize query performance.

**Model Structure:**
- **Fact Table:** Sales transactions (Quantity Sold, Profit, Cost)
- **Dimension Tables:**
  - `DimCategory` → Cold Brew, Pastries, Espresso  
  - `DimChannel` → Direct, Wholesale  
  - `DimReturn` → Returned Orders  
  - `Calendar` → Custom DAX table for time intelligence

**DAX Measures Developed:**
- `[Seasonal Drink Rank]` – ranks products by popularity  
- `[Total Revenue]`, `[Total Orders]`, `[Average Order Value]`, and more

---

## 🛠️ Skills & Tools

**Tool:** Microsoft Power BI  

**Skills Demonstrated:**
- Data Modeling (Star Schema Design)  
- DAX (Data Analysis Expressions)  
- Data Visualization & Dashboard Design  
- Business Analysis & Recommendations  
- UI/UX & Interactivity (Slicers, Filters, Navigation)

---

## 📸 Dashboard Previews

### 📍 Page 1: Main Report  
![Main Report](https://github.com/MostafaAyman11/Images-assets/raw/main/Gig%20image1.png)

---

### 📍 Page 2: Wholesale vs Direct Channel  
![Wholesale vs Direct](https://github.com/MostafaAyman11/Images-assets/raw/main/Gig%20image2.png)

---

### 📍 Page 3: Operational Staffing & Footfall  
![Staffing Report](https://github.com/MostafaAyman11/Images-assets/raw/main/Gig%20image3.png)

---

### 🧩 Data Model Overview  
![Data Model](https://github.com/MostafaAyman11/Images-assets/raw/main/Gig%20image4.png)

---

### ⭐ Author

**Mostafa Ayman Reda Ahmed**  
📍 Business Analyst | Power BI Developer | Data Enthusiast  
🔗 [LinkedIn](https://www.linkedin.com/in/mostafa-ayman-reda-ahmed)

---

