# 🚀 Superstore Sales Performance Dashboard | Power BI  
*Interactive analytics for sales trends, regional performance, and customer insights*

[![Power BI Dashboard](https://img.shields.io/badge/Power_BI-View_Full_Dashboard-blue)](https://app.powerbi.com/links/2Ptbku6hpH?ctid=55f2965b-c160-40b8-90dc-52f4e06bb384&pbi_source=linkShare)  
![Dashboard Overview](https://github.com/user-attachments/assets/8a3695f3-e870-48e8-a3cb-5ebb4ee13984)

---

## 📌 Business Challenge  
Superstore needs to:  
- Reverse declining sales (40% drop in orders YoY)  
- Optimize product mix (85% revenue from just 3 products)  
- Improve regional performance (West region dominates with 42% sales)  

---

## 🛠️ Technical Implementation  

### **Data Architecture**  
![Data Model](https://github.com/user-attachments/assets/f4c08ea1-9f84-4d9c-9d56-2cc2c38726d3)  
*Star schema with 1 fact table and 5 dimensions*

**Key Relationships**:  
![Relationships](https://github.com/user-attachments/assets/b6610c00-0728-49ce-a9fb-5efd08117355)  
- Sales_Fact → Dim_Product (ProductID)  
- Sales_Fact → Dim_Region (RegionID)  
- Sales_Fact → Calendar (Date)  

### **Core DAX Measures**  
```dax
AOV = DIVIDE([Total sales],([Orders]))
Sales color = IF([Growth Profit]>=0,"green","red")RETURN DIVIDE(CurrentSales - PriorSales, PriorSales)
sales color2 = IF([Total sales]>=100,"green","red")
Sales Previous Year = CALCULATE([Total sales],PREVIOUSYEAR('Calendar'[Date]))
AVg. sales = AVERAGE(Sales_Fact[Sales])
Total sales = sum(Sales_Fact[Sales])
