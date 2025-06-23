# 🌍 Global Supply Chain Analytics Dashboard (Power BI)

This Power BI project simulates an enterprise-level global supply chain analytics solution by integrating production, forecast, inventory, and order data to provide actionable business insights across products and regions.

## 📊 Project Overview

The dashboard is designed to support strategic decision-making in supply chain and operations by analyzing key performance metrics across multiple dimensions.

## ✅ Key Features

- **Interactive, multi-page Power BI dashboard**
- Advanced **DAX measures** for:
  - Forecast Accuracy (MAPE)
  - Forecast Bias (Units and %)
  - Capacity Utilization
  - Inventory Turnover Ratio
  - Units Produced vs Units Sold
- **Dynamic filtering** with slicers for Product, Region, Month, and Quarter
- **Data modeling** with relationships between Forecast, Orders, Inventory, Production, and Calendar tables
- **Visualizations** include:
  - KPI Cards
  - Time Series Trend Lines
  - Regional Maps
  - Heatmaps by Product and Region
  - Forecast vs Actual Bar Charts (Monthly & Quarterly)
  - Sankey Chart for Revenue Flow by Customer Type

## 💡 Insights Uncovered

- Identified consistent over-forecasting patterns across all products (Forecast Bias > 250%)
- Analyzed production vs demand trends to detect potential stock imbalances
- Mapped regional forecast accuracy to uncover planning inefficiencies

## 🛠 Tools Used

- Power BI  
- Power Query  
- DAX (Data Analysis Expressions)

Few Snippets of dashboard are attached below:

![image](https://github.com/user-attachments/assets/f8fca287-e011-45f6-abf3-634d1e2d8aef)
![image](https://github.com/user-attachments/assets/aefa7805-1108-4395-b42a-c6d0f0fadfd8)


---

## 📁 Project Structure
📂 Global_Supply_Chain_Dashboard/
├── 📊 PowerBI_Dashboard.pbix
├── 📁 Sample_Datasets/
│ ├── Forecast.csv
│ ├── Orders.csv
│ ├── Inventory.csv
│ ├── Production.csv
│ └── Calendar.csv
└── 📄 README.md

