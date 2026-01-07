# Power BI Sales Summary Dashboard

##  Project Overview
This project presents an interactive **Power BI Sales Summary Dashboard** built using Excel as the data source.  
The dashboard provides a comprehensive view of sales performance, profitability, and regional trends to support data-driven business decisions. The solution is designed to help sales managers make **data-driven decisions** for inventory planning and business process optimization.

---

##  Business Context
Global Super Store operates worldwide and sells products across major categories:
- Furniture
- Office Supplies
- Technology

The goal is to:
- Monitor sales and profit trends
- Identify high- and low-performing regions
- Analyze category and sub-category performance
- Control data access using role-based security
  
---
    
##  Business Objectives
- Track overall sales and profit performance
- Analyze profitability across product categories and sub-categories
- Compare regional contribution to profit
- Monitor sales and profit trends over time
- Identify operational issues such as returned orders
- Build an interactive **Sales Summary dashboard**
- Enable natural language insights using **Power BI Q&A**
- Implement **Row-Level Security (RLS)** for managers
- Publish and share the report using **Power BI Service**

---

##  Tools Used
- **Power BI Desktop** – Data modeling, DAX, visualization
- **Microsoft Excel** – Data source & preprocessing
- **Power BI Service** – Publishing, sharing, security roles
- **GitHub** – Project documentation and version control

---

##  Data Preparation (Excel & Power BI)

### 🔹 Data Sources (Excel)
- Orders
- Returns
- People
- Date table

### 🔹 Excel Data Cleaning
Excel was used for initial data preparation:
- Removed duplicate records
- Checked for missing or invalid sales and profit values
- Standardized date formats
- Verified numeric consistency for sales, profit, and quantity fields

---

### 🔹 Power BI Data Transformation (Power Query)
- Promoted headers for Returns table
- Removed extra rows and promoted headers for People table
- Removed unnecessary columns (Ship Date, Postal Code, Product Name, etc.)
- Standardized data types (Date, Currency, Numeric)
- Optimized tables to reduce model size
---

### 🔹 Data Modeling
- Created relationships between:
  - Orders
  - Returns
  - People
  - Date
- Designed a **star-schema-style model** for efficient reporting
- Ensured correct granularity for time-based analysis


---

### 🔹 DAX Measures Created
Key metrics were calculated using DAX:
- **Total Sales**
- **Total Profit**
- **Profit Ratio**
- **Returned Orders Count**
- **Report As-Of Date**
- **UserPrincipalName (for RLS)**

These measures power the KPI cards and trend visuals in the dashboard.

---

## Dashboard Features

###  Sales Summary
Includes:
- KPI Cards (Total Sales, Total Profit, Profit Ratio)
- Total Sales by Year & Category (Clustered Column Chart)
- Sales & Profit Trends (Line Charts)
- Sales Contribution by Category (Donut Chart)
- Region Contribution in Profit (Table with Conditional Formatting)
- Returned Orders by Market
- Top Managers by Sales
- Bookmarks to toggle between **Sales vs Profit**

---

###  Q&A Analysis
- Map visualization showing **Total Sales by Country**

### Interactive Filters
- Market (Africa, Asia Pacific, Europe, LATAM, USCA)
- Year
- Month  

Filters allow users to dynamically explore performance across regions and time periods.

---

### Visuals Included
- Total Sales by Year and Category
- Sales & Profit Trend Over Time
- Sales, Profit & Profit Ratio by Sub-Category
- Total Sales by Category (Donut Chart)
- Region Contribution to Profit
- Returned Orders by Market
- Top 5 Regional Managers by Sales

---

## Row-Level Security (RLS)

### 🔹 Static Roles
- Market-based roles restricting data visibility by region

### 🔹 Dynamic RLS
- Implemented using:
  - `USERPRINCIPALNAME()`
  - Country Access mapping table
- Ensures users only see data for assigned countries

---

## ☁ Power BI Service Deployment
- Published report to Power BI Service
- Assigned users to security roles
- Tested roles using **View As Role**
- Shared report with users based on RLS permissions
- Pinned report to a live Power BI dashboard

---

## Key Insights
- Technology category generates the highest sales
- Certain regions show negative profit ratios
- Returned orders impact profitability across markets
- A small number of managers drive a large share of revenue
- Sales trends vary significantly by year and region

---

##  Repository Structure

superstore-sales-dashboard/
│
├── dashboard_screenshots/
│ └── sales_summary_dashboard.jpg
│ └──   Q&A_analysis_dashboard.jpg
├── powerbi/
│ └── superstore_sales_dashboard.pbix
├── data/
│ └── superstore_sales.xlsx
│ └──  date_table.xlsx
└── README.md

---

**Betcy Karukamalil Joy**
Data Analyst | Power BI | Excel | Data Visualization
