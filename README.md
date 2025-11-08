Global Supply Chain Analytics Dashboard – Power BI

### 🏢 Enterprise-Level BI Project | Designed by Sudhamsha Sagar

This project is a **complete Power BI analytics suite** built to analyze a **global supply chain dataset** from multiple perspectives — Executive, Regional, Supplier, and Product Performance.

The dashboard delivers **C-Suite level insights** using advanced DAX, professional design, and real business KPIs — aimed at demonstrating full-stack Power BI expertise.

---

## 🚀 Project Overview

### 🎯 Objective
To build an end-to-end BI solution that provides:
- Strategic business KPIs for executives  
- Regional revenue & profitability insights  
- Supplier efficiency & logistics intelligence  
- Product & category profitability analysis  

---

## 🧩 Data Model
**Tables Used:**
- `Orders` – Revenue, Cost, Profit, Discount, Dates  
- `Products` – Category, Subcategory, ProductID  
- `Suppliers` – Country, LeadTimeDays, OnTimeDeliveryRate, FreightCostPct  
- `Customers` – CustomerID, Segment, Country  
- `Regions` – Region, Manager, Country  
- `Date` – Continuous date table with Month, Quarter, Year, Day

### 🔗 Relationships
All relationships are **One-to-Many**, single direction:
- Date[Date] → Orders[OrderDate]  
- Products[ProductID] → Orders[ProductID]  
- Customers[CustomerID] → Orders[CustomerID]  
- Suppliers[SupplierID] → Orders[SupplierID]  
- Regions[Region] → Orders[RegionID]

---

## 🧮 Key DAX Measures

### 🔹 Financial Metrics

Total Revenue = SUM(Orders[Revenue])
Total Profit = SUM(Orders[Profit])
Profit Margin % = DIVIDE([Total Profit], [Total Revenue], 0)
Average Discount = AVERAGE(Orders[Discount])
Average Order Value = DIVIDE([Total Revenue], [Unique Customers], 0)

Avg Lead Time = AVERAGE(Suppliers[LeadTimeDays])
On-Time Delivery % = AVERAGE(Suppliers[OnTimeDeliveryRate])
Avg Freight Cost % = AVERAGE(Suppliers[FreightCostPct])
Supplier Efficiency Score =
DIVIDE(
    ([On-Time Delivery %] * 0.6) +
    ((1 - [Avg Freight Cost %]) * 0.3) +
    ((1 - [Avg Lead Time]/MAX(Suppliers[LeadTimeDays])) * 0.1), 1
)


Sales LY = CALCULATE(SUM(Orders[Revenue]), SAMEPERIODLASTYEAR('Date'[Date]))
Rolling 12M Sales = CALCULATE(SUM(Orders[Revenue]), DATESINPERIOD('Date'[Date], MAX('Date'[Date]), -12, MONTH))
YoY Growth % = DIVIDE(([Total Revenue] - [Sales LY]), [Sales LY])


📊 Dashboard Pages
1️⃣ Executive Overview

High-level KPIs: Revenue, Profit, Margin %, Efficiency, Rolling 12M, YoY %
Monthly revenue & profit trends
World map for total profit by region
Profit margin trend line
Gauge for YoY growth
Dynamic filters (Month, Region, Category)

2️⃣ Regional Performance

Revenue & Profit by Region
Profit ranking by region (bar chart)
Matrix with regional totals and average profit per order
Dynamic regional title ("Regional Performance – [Region]")
Conditional formatting for profit margin
Map upgraded to Azure Filled Map for premium look

3️⃣ Supplier Performance

KPIs: Avg Lead Time, On-Time %, Freight Cost %, Efficiency Score
Treemap: Profit by Supplier Country
Scatter: Supplier Efficiency vs Lead Time
Bar: Top 10 Suppliers by Efficiency (Top N filter)
Dynamic label: “Top Supplier by Efficiency”
Color-coded visuals

4️⃣ Product & Category Performance

KPIs: Avg Order Value, Avg Discount %, Avg Profit Margin %
Bar: Revenue by Category
Treemap: Profit & Margin % by Subcategory
Scatter: Discount vs Profit Margin %
Bar: Top 10 Products by Profit (conditional color scale)
Dynamic title: “Product Performance – [Category]”

5️⃣ Info / Documentation Page

Project summary
Data schema
Key KPIs
DAX categories used (Time Intelligence, Context Transition, Ranking)
Toolset and methodology

🧠 Concepts Demonstrated

Advanced DAX (CALCULATE, FILTER, SWITCH, RANKX, SAMEPERIODLASTYEAR, DATESINPERIOD)
Time Intelligence (YTD, Rolling 12M, YoY Growth)
Context Transition & Row Context understanding
Top N filters and Dynamic Titles
Data modeling best practices (Star schema)
Executive dashboard storytelling & design consistency

🧰 Tech Stack

Power BI Desktop
DAX for measures
Excel / CSV dataset (300K+ records)
Python (EDA) for pre-analysis (optional)

<img width="1122" height="646" alt="image" src="https://github.com/user-attachments/assets/9394a2f3-12d3-495d-b27f-0a917a6f4128" />
<img width="1120" height="623" alt="image" src="https://github.com/user-attachments/assets/349532c5-5783-4ca5-b2f3-1a50b8b60045" />
<img width="1122" height="630" alt="image" src="https://github.com/user-attachments/assets/3a600625-1fb7-4868-be8c-01a939204f02" />
<img width="1113" height="621" alt="image" src="https://github.com/user-attachments/assets/8c4227c2-034c-4dba-9ed9-3ade770e38cb" />


