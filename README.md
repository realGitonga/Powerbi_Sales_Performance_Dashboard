# Sales Performance Dashboard (Power BI)

##  Project Overview
This project presents an **end-to-end Sales Performance Dashboard** developed in **Power BI**, covering the full analytics lifecycle: data integration, cleaning, modeling, DAX measure creation, and interactive dashboard design.

The dashboard enables stakeholders to monitor sales trends, profitability, customer performance, and regional insights through a clean, professional, and interactive interface.

---

##  Project Tasks & Implementation

### **Part 1: Data Preparation & Feature Engineering**

#### **a) Data Integration**
- Performed a **LEFT JOIN** between Sales Transactions and Product Master to retain all transactions, including those with missing product records
- Performed an **INNER JOIN** with Customer Information to include only completed transactions with valid customers
- Performed a **LEFT JOIN** with Sales Representatives, retaining all transactions and flagging orphaned records
- Investigated and resolved the missing `CustomerID` in **TXN004** using transaction pattern analysis

#### **b) Data Cleaning & Standardization**
- Standardized all date formats across datasets
- Cleaned pricing columns by removing `$`, handling `#ERROR#` and `#N/A`, and converting values to decimal format
- Standardized Discount% values (treated blanks as 0%, converted percentages to decimals)
- Created a hierarchical **Territory structure**:  
  `Region → Territory → Sales Representative`
- Validated and standardized Channel names (case consistency and naming variations)
- Generated **Customer Segments** based on Company Size and Credit Limit

#### **c) Calculated Columns**
- Net Sale Amount  
- Gross Profit  
- Profit Margin %  
- Commission Amount  
- Days Since Launch  

---

### **Part 2: Data Modelling & DAX Measures**

#### **a) Data Modelling**
- Designed a **star schema** with Sales Transactions as the fact table
- Created proper fact–dimension relationships
- Enabled **bidirectional filtering** where appropriate for customer analysis
- Built a dedicated **Calendar/Date dimension** containing:
  - Date, Year, Quarter, Month, Week, Day of Week
  - Fiscal Year (starting April 1st)
- Implemented many-to-many relationships where required
- Configured cross-filtering directions to balance performance and analytical flexibility

#### **b) DAX Measures**

**Core Measures**
- Total Sales  
- Total Profit  
- Average Order Value  
- Profit Margin %  

**Time Intelligence Measures**
- Sales MTD  
- Sales YTD (Fiscal Year)  
- Sales Previous Month  
- Sales Growth %  

---

### **Part 3: Dashboard Visualisation & Interactivity**

#### **a) Visuals**
1. Card – Total Sales  
2. Bar Chart – Sales by Product Category  
3. Line Chart – Sales by Month  
4. Table – Top Customers by Sales (Customer Name, Total Sales, Profit)  

#### **b) Interactivity**
- Enabled full cross-filtering between visuals
- Added a **Region slicer** to dynamically filter the dashboard

#### **c) Formatting & Design**
- Added dashboard title: **Sales Performance Dashboard**
- Formatted all monetary fields with `$` currency symbol
- Applied professional styling using consistent colors, spacing, and typography

---

##  Tools & Technologies
- **Power BI Desktop**
- **Power Query** (ETL & data cleaning)
- **DAX** (measures & time intelligence)
- CSV datasets

---

##  Dashboard Preview
![Dashboard Preview](dashboard_preview.PNG)

---

##  How to Use
1. Download the `.pbix` file from the `powerbi/` folder
2. Open it in **Power BI Desktop**
3. Use slicers and visuals to explore insights interactively

---

## Key Outcome
A **business-ready, interactive Power BI dashboard** demonstrating strong capabilities in:
- Data integration & cleaning
- Data modeling
- DAX and time intelligence
- Dashboard design and storytelling

## Author and Contributors
**Mathew Chalo** 

**Lawrence Gitonga**

**Abel Kiptoo**

