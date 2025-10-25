# 📊 Power BI Project Management Dashboard

![Project Management Dashboard - Cover](pm_1.png)

This repository contains the files and analysis for a comprehensive **Project Management Dashboard** built in **Microsoft Power BI**.  
This project was completed as part of my training with the **Digital Egypt Pioneers Initiative (DEPI)**.

**🧰 Tool:** Microsoft Power BI  
**🧠 Skills Demonstrated:** Data Cleaning (Power Query) · Data Modeling (Star Schema) · DAX · Data Visualization · Dashboard Design · Business Reporting

---

## 🔗 Live Dashboard
[![View Dashboard](https://img.shields.io/badge/View%20Dashboard-Power%20BI-yellow?style=for-the-badge&logo=power-bi)](https://app.powerbi.com/links/yE0Yz6J810?ctid=55f2965b-c160-40b8-90dc-52f4e06bb384&pbi_source=linkShare)

> Or open directly in your browser:  
> `https://app.powerbi.com/links/yE0Yz6J810?ctid=55f2965b-c160-40b8-90dc-52f4e06bb384&pbi_source=linkShare`

---

## 🧠 Project Overview

This project simulates a real-world business scenario for a company managing 100 projects.  
As a data analyst, my goal was to transform raw, multi-table project data into a structured, interactive dashboard.  
The final product delivers clear, actionable insights into project health, financial performance, and resource allocation — enabling stakeholders to make **data-driven decisions**.

---

## 🔧 Technical Components

### 🧹 Data Cleaning & Preparation (Power Query)
- Connected to the raw data source (Excel).  
- Used **Power Query Editor** to clean and transform data — standardizing formats, handling errors, and ensuring integrity before loading into the model.

### ⚙️ Data Modeling (Star Schema)
- Built a robust **Star Schema** linking the fact table (`ProjectManagement`) with dimension tables (`DimProject`, `DimProjectManager`, `Calendar`, `DimLocation`, etc.).  
- Ensured efficient relationships for performance and scalability.

### 📈 DAX Measures & Calculations
- Created advanced **DAX measures** to calculate key KPIs not available in the raw data.  
- Core measures include:
  - `[Task Completion %]`
  - `[Overdue Tasks]`
  - `[Profit]`
  - `[Cost vs. Budget by Month]` (Time Intelligence)

### 🎨 Dashboard Design & Visuals
- Designed a **two-page interactive report**:
  - **Page 1:** Executive summary (KPIs, Financial Overview, Project Status)
  - **Page 2:** Detailed breakdown of tasks, timelines, and manager performance

### 📊 Dashboard Components
- **Slicers:** Timeline (Gantt-style), Project Manager, Project Status  
- **KPI Cards:** Total Budget · Total Cost · Total Profit · Project Count · Task Count · Task Completion %  
- **Charts:**
  - Cost, Budget & Profit by Month (Line & Clustered Bar Chart)
  - Project Status (Donut Chart)
  - Tasks by Priority (Bar Chart)
  - Projects by Location (Map)
  - Manager Performance & Overdue Tasks (Matrix/Table)
  - Project & Task Timeline (Gantt Chart Visual)

---

## 📸 Report Previews

### Report — Executive Summary
![PM Report - Executive Summary](pm_1.png)

### Report — Detailed Tasks & Timeline
![PM Report - Tasks & Timeline](pm_2.png)

### Report — Manager Performance & Financials
![PM Report - Manager & Financials](pm_3.png)

---

## 💡 Key Business Insights

- **🚧 Project Bottleneck:** Only **25%** of projects are *On Track*, while **29%** are *Behind Schedule*. The low **29% task completion rate** reveals major operational delays.  
- **💸 Volatile Profitability:** A noticeable **financial loss in May** indicates profitability risks despite an overall profit of **$18K**.  
- **👥 Manager Workload Imbalance:** Two managers (Alice and Charlie) handle
