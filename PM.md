# 📊 Power BI Project Management Dashboard

![Project Management Dashboard - Cover](https://raw.githubusercontent.com/MostafaAyman11/Images-assets/refs/heads/main/PM%201.png)

This repository contains the files and analysis for a comprehensive **Project Management Dashboard** built in **Microsoft Power BI**. This project transforms raw, multi-table project data into an interactive report that delivers clear, actionable insights into project health, financial performance, and resource allocation.

This project was completed as part of my training with the **Digital Egypt Pioneers Initiative (DEPI)**.

**🧰 Tool:** Microsoft Power BI  
**🧠 Skills Demonstrated:** Data Cleaning (Power Query) · Data Modeling (Star Schema) · DAX · Data Visualization · Dashboard Design · Business Reporting

---

## 🚀 Live Interactive Dashboard

[![View Dashboard](https://img.shields.io/badge/View%20Dashboard-Power%20BI-yellow?style=for-the-badge&logo=power-bi)](https://app.powerbi.com/links/yE0Yz6J810?ctid=55f2965b-c160-40b8-90dc-52f4e06bb384&pbi_source=linkShare)

> Or open directly in your browser:  
> `https://app.powerbi.com/links/yE0Yz6J810?ctid=55f2965b-c160-40b8-90dc-52f4e06bb384&pbi_source=linkShare`

---

## Contents

- [Key Business Insights](#💡-key-business-insights)
- [Dashboard Previews](#📸-dashboard-previews)
- [Project Objective](#🎯-project-objective)
- [My Technical Process](#🔧-my-technical-process)
- [Skills & Tools](#🛠️-skills--tools)

---

## 💡 Key Business Insights

This dashboard answers critical business questions by identifying key trends and risks:

- **🚧 Project Bottleneck:** Only **25%** of projects are *On Track*, while **29%** are *Behind Schedule*. The low **29% task completion rate** reveals major operational delays.
- **💸 Volatile Profitability:** A noticeable **financial loss in May** indicates profitability risks, despite an overall profit of **$18K** for the period.
- **👥 Manager Workload Imbalance:** Two managers (Alice and Charlie) are responsible for **84 overdue tasks (≈40% of all overdue tasks)**, highlighting potential resource strain and a need for workload review.

---

## 📸 Dashboard Previews

### Page 1: Executive Summary & Financial Overview
![Report - Executive Summary](https://raw.githubusercontent.com/MostafaAyman11/Images-assets/refs/heads/main/PM%201.png)

### Page 2: Detailed Task & Timeline Breakdown
![Report - Tasks & Timeline](https://raw.githubusercontent.com/MostafaAyman11/Images-assets/refs/heads/main/PM%202.png)

### Data Model: Star Schema
![Data Model - Star Schema](https://raw.githubusercontent.com/MostafaAyman11/Images-assets/refs/heads/main/PM%203.png)

---

## 🎯 Project Objective

This project simulates a real-world business scenario for a company managing 100 projects. As a data analyst, my goal was to execute a full Business Intelligence workflow to enable stakeholders to make **data-driven decisions** regarding project health and financial performance.

---

## 🔧 My Technical Process

I followed a four-step process from raw data to a finished BI product.

### 1. Data Cleaning & Preparation (Power Query)
- Connected to the raw data source (Excel).
- Used the **Power Query Editor** to clean and transform the data. This involved standardizing formats, handling null values and errors, and ensuring data integrity before loading it into the model.

### 2. Data Modeling (Star Schema)
- Built a robust **Star Schema** to create an efficient and scalable data model.
- Linked the central fact table (`ProjectManagement`) with multiple dimension tables (`DimProject`, `DimProjectManager`, `Calendar`, `DimLocation`, etc.).

### 3. DAX Measures & Calculations
- Wrote advanced **DAX measures** to calculate essential KPIs that were not available in the raw data.
- Core measures include:
  - `[Task Completion %]`
  - `[Overdue Tasks]`
  - `[Profit]`
  - `[Cost vs. Budget by Month]` (using Time Intelligence functions)

### 4. Dashboard Design & Visualization
- Designed a **two-page interactive report** to serve different business needs:
  - **Page 1 (Executive Summary):** High-level KPIs, financial overview, and project status for stakeholders.
  - **Page 2 (Detailed View):** Granular breakdown of tasks, timelines, and manager performance for project managers.
- Implemented a variety of visuals, including slicers, KPI cards, line & clustered bar charts, donut charts, and a map visual for project locations.

---

## 🛠️ Skills & Tools

- **Tool:** Microsoft Power BI
- **Skills Demonstrated:**
  - Data Cleaning & ETL (Power Query)
  - Data Modeling (Star Schema)
  - DAX (Data Analysis Expressions)
  - Data Visualization & Dashboard Design
  - Business Reporting & Analysis
