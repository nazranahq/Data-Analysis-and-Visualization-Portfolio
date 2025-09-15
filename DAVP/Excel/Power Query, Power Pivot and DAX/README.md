# 🧮 Data Preparation and Analysis with Power Query, Power Pivot & DAX (Excel)

This project demonstrates the **end-to-end process of data preparation, modeling, and analysis** in Excel using **Power Query**, **Power Pivot**, and **DAX**.  
The goal was to consolidate and analyze **customer, sales, and product data** stored in different formats and across multiple sources.

---

## 🧾 Business Context
Customer and sales information was scattered across multiple regional CSV files, each with inconsistent formats.  
A robust and automated process was required to clean, integrate, and analyze the data for company-wide reporting.

---

## 🎯 Project Objectives
- Consolidate multiple regional CSV files into a **single, clean dataset**.  
- Create a **data model** linking Customers, Sales, and Products for relational analysis.  
- Use **DAX measures** for reusable, context-aware calculations such as profit margin.

---

## 🛠️ Key Steps

1. **Data Import & Consolidation**  
   - Used **Get Data ➜ From Folder** in Excel to import all regional customer CSV files at once.  
   - Automatically combined them in **Power Query**, eliminating manual file-by-file merges.

2. **Data Cleaning & Transformation (Power Query)**  
   - Removed unnecessary columns (e.g., source file names).  
   - Corrected data types, converting postal codes to *text* since they are identifiers.  
   - Added a new calculated column **Age Category** with conditional logic:  
     - *Young* (< 35), *Middle* (35–60), *Senior* (> 60).

3. **Data Modeling (Power Pivot)**  
   - Enabled the Power Pivot add-in and added the **Customer**, **Sales**, and **Product** tables to the **Data Model**.  
   - Created relationships on shared keys (e.g., *Customer ID*, *Product ID*), enabling relational analysis across tables.

4. **Pivot Table Analysis**  
   - Built Pivot Tables that combined fields from multiple tables—for example, **Age Category-wise Sales** using the Customer and Sales tables.

5. **Advanced Calculations with DAX**  
   - **Calculated Column:** *State Type* to flag key states (California, New York, Texas) as **Top** and others as **Others**.  
   - **Measure:** *Profit Margin* to provide a consistent, reusable KPI across all Pivot Tables.

---

## 📊 Outcomes & Insights
- Achieved a **single source of truth** for all customer and sales data, refreshed automatically when new CSVs are added.  
- Enabled **dynamic, interactive reporting** by age category, state grouping, and profit margin.

---

## 🧠 Key Learnings
- **Power Query** streamlines repetitive data-cleaning tasks into a refreshable pipeline.  
- **Power Pivot** turns Excel into a relational database, supporting complex cross-table analysis.  
- **DAX measures** ensure accurate, context-aware metrics across different reports.

---

This project highlights how Excel, when combined with **Power Query**, **Power Pivot**, and **DAX**, can deliver enterprise-grade data modeling and analytics without external BI tools.
