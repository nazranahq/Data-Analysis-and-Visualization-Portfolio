# 📈 Advanced Data Modeling and KPI Analysis with Power Pivot

This project showcases how **Power Pivot** can be used to build a robust data model, create cross-table relationships, perform advanced calculations with **DAX**, and evaluate performance using **Key Performance Indicators (KPIs)**.

---

## 🧾 Business Context
The objective was to analyze staff performance by integrating transaction, employee, and salary data into a single model.  
Power Pivot enabled relational analysis and KPI-driven insights without leaving Excel.

---

## 🎯 Project Objectives
- Build a relational **Power Pivot data model** from multiple Excel worksheets.  
- Use **DAX** to create calculated columns and measures for profit analysis.  
- Develop **KPIs** to assess staff performance against defined targets.

---

## 🛠️ Key Steps

1. **Data Import & Model Setup**  
   - Opened a new Excel workbook and launched **Power Pivot ➜ Manage**.  
   - Used **Get External Data ➜ From Other Sources ➜ Excel File** to import three worksheets, ensuring the first row served as headers.

2. **Creating Relationships (Diagram View)**  
   - Linked tables by dragging fields to form relationships:  
     - `Staff ID` (Transactions → Employee).  
     - `Employee Level` (Salary → Employee).

3. **Calculated Columns & DAX Measures**  
   - Added a **Profit** calculated column using a custom formula.  
   - Created a DAX **measure** named **Total Profit** to aggregate profits across employees.

4. **Dynamic Lookups**  
   - Used the `RELATED` function to pull **Employee Name** from the Employee table based on linked `Staff ID`.

5. **Performance Analysis via Pivot Tables**  
   - Inserted a Pivot Table based on the Power Pivot model.  
   - Combined fields from multiple tables—e.g., **Employee Name** (Employee table) with **Sum of Profit** (Transactions table)—to compare individual and level-wise performance.

6. **Key Performance Indicators (KPIs)**  
   - Defined a **KPI** on the **Total Profit** measure with a target threshold (e.g., `$20,000`).  
   - Added KPI status to the Pivot Table to visually identify employees meeting or falling short of the target.

---

## 📊 Insights
- **High-performing junior employees** were highlighted when combining Profit with Employee Level.  
- The KPI indicator made it easy to track who exceeded the $20K target in real time.

---

## 🧠 Key Learnings
- **Power Pivot** turns Excel into a true relational database for analysis.  
- **DAX measures** provide reusable, context-aware calculations.  
- **KPIs** deliver clear, actionable performance insights without external BI tools.

---

This task demonstrates the full power of **Power Pivot + DAX**, transforming static Excel sheets into an **interactive, performance-driven analytics model**.
