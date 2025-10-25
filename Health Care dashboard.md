# 🏥 Power BI Hospital ER Dashboard

This repository holds the Power BI analysis for a Hospital Emergency Room (ER) Dashboard. The project's goal was to analyze operational performance, patient demographics, and wait times to identify key bottlenecks and areas for improvement.

The final report transforms raw visit data into a powerful interactive tool, enabling hospital administrators to make data-driven decisions to enhance patient flow and satisfaction.

---

## 🚀 Live Interactive Dashboard

Click the badge below to open and interact with the live Power BI report.

[![View Dashboard](https://img.shields.io/badge/View%20Dashboard-Power%20BI-yellow?style=for-the-badge&logo=power-bi)](https://app.powerbi.com/links/ap3dfR0b1H?ctid=55f2965b-c160-40b8-90dc-52f4e06bb384&pbi_source=linkShare)

> Or open directly in your browser:  
> `https://app.powerbi.com/links/ap3dfR0b1H?ctid=55f2965b-c160-40b8-90dc-52f4e06bb384&pbi_source=linkShare`

---

## 💾 Data Source

The analysis is based on a single, clean CSV file containing anonymized patient visit records.  

[View the Raw .csv Data on GitHub](https://github.com/MostafaAyman11/Images-assets/blob/main/Hospital%20ER.csv)

---

## Contents

- [Key Business Insights](#💡-key-business-insights)
- [Interactive Features & Slicers](#🔍-interactive-features--slicers)
- [Dashboard Previews](#📸-dashboard-previews)
- [My Technical Process](#🔧-my-technical-process)
- [Skills & Tools](#🛠️-skills--tools)

---

## 💡 Key Business Insights

This dashboard answers critical questions about ER operations:

📈 **Patient Volume:** The ER processed 9,000 patients with an average satisfaction score of **5.00**.

⏱️ **Waiting Times:** The average patient wait time is **35.25 minutes**. The "Avg Waiting by Department Referral" chart clearly shows that **Neurology** and **Physiotherapy** have the longest wait times, indicating they are primary bottlenecks.

🕒 **Peak Hours:** The patient visit heatmap shows that visits peak during midday hours (**10 AM - 2 PM**) and are highest on weekdays, especially **Mondays and Tuesdays**. This insight is crucial for optimizing staff schedules.

👥 **Patient Demographics:** The dashboard allows for a deep dive into patient volume by **age** and **gender**, revealing which groups visit the ER most frequently.

---

## 🔍 Interactive Features & Slicers

A key goal was to make this dashboard **highly interactive**.  
I implemented several slicers and filters to allow users to explore data from multiple perspectives.

### 🧩 Why Slicers and Filters Matter
Slicers and filters transform the report from a static snapshot into a **dynamic analytical tool**.  
They empower hospital managers and analysts to move seamlessly from a high-level view (overall hospital performance) to granular insights (specific departments, patient groups, or time periods).

### 🎛️ Features Implemented
- **Time Slicers (Year & Month):**  
  Allow administrators to analyze seasonal patterns, compare year-over-year performance, and isolate high-traffic months.

- **Demographic Filters (Gender, Race, Age):**  
  Help uncover whether specific patient groups (e.g., “Adult” vs. “Old”) experience different waiting times or satisfaction levels.

- **Department Filter:**  
  Enables users to evaluate performance, patient load, and average waiting times per department, identifying operational bottlenecks.

- **Cross-Filtering:**  
  The entire report is interactive. Selecting a department or patient group automatically updates all visuals to show context-specific data.

- **Patient Summary Drill-Through Page:**  
  A secondary page allows staff to search for individual patients and review their visit history and outcomes in detail.

### 💡 Impact of Interactivity
By adding slicers and filters, this dashboard:
- Enhances **decision-making precision** by allowing targeted exploration.  
- Supports **what-if analysis**, helping staff simulate different timeframes or departments.  
- Improves **usability and engagement**, making it easier for non-technical users to interact with insights visually.

---

## 📸 Dashboard Previews

### Page 1: Main Operations Dashboard
![Main Report](https://github.com/MostafaAyman11/Images-assets/blob/main/HC%201.png)

### Page 2: Patient Summary & Search
![Patient Summary](https://github.com/MostafaAyman11/Images-assets/blob/main/HC%202.png)

### Data Model: Star Schema
![Data Model](https://github.com/MostafaAyman11/Images-assets/blob/main/HC%203.png)

---

## 🔧 My Technical Process

### 1. Data Connection & Modeling
Connected to the **Hospital ER.csv** dataset and built an efficient **Star Schema** by linking the main hospital fact table to a **Calendar dimension**.  
This design ensures optimized performance and supports **Time Intelligence** functions in DAX.

### 2. DAX Measures
Developed key **DAX calculations** to extract critical KPIs, including:  
- `[Number of Patients]`  
- `[Avg Waiting Time]`  
- `[Avg Satisfaction]`  

### 3. Data Visualization & Design
Created a clean, two-page interactive dashboard:
- **Page 1 (Main):** Shows overall KPIs, patient flow heatmap, and departmental performance.  
- **Page 2 (Summary):** Allows search and drill-through for individual patient records.  
Added **navigation buttons** to move between pages seamlessly.

---

## 🛠️ Skills & Tools

**Tool:** Microsoft Power BI  

**Skills Demonstrated:**
- Data Modeling (Star Schema)  
- DAX (Data Analysis Expressions)  
- Data Visualization & Dashboard Design  
- UI/UX Design (Slicers, Navigation, Readability)  
- Operational & Business Analysis  

---
