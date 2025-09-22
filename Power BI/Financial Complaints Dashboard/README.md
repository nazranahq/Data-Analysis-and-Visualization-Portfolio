# 💳 Financial Complaints Dashboard

This **Power BI project** analyzes financial consumer complaint data to uncover **trends in complaint volume, response timeliness, resolution types, and dispute rates**.  
Stakeholders can explore complaint patterns by **issue, product, state, and time**, while evaluating the effectiveness of company responses.  
Key performance metrics—**Timely Response %**, **Disputed Rate**, and **Resolved at No Cost %**—provide actionable insights for improving **service quality, policy enforcement, and customer satisfaction**.

---

## 🧾 Business Context
Financial institutions receive thousands of consumer complaints each year across banking, credit cards, and mortgage products.  
Understanding **where, when, and why** complaints occur is essential to improve operations, meet regulatory standards, and maintain customer trust.

---

## 🎯 Project Objectives
- Clean and transform consumer complaint data for accurate analysis.  
- Track KPIs such as **Total Complaints**, **Timely Response %**, **Disputed Rate**, and **Resolved at No Cost %**.  
- Visualize trends by **state, product category, and issue type** to identify problem areas and regional patterns.

---

## 🛠️ Tools & Features
- **Power BI Desktop**  
- **Power Query Editor** for data profiling and type conversions  
- **DAX Measures** for KPI calculations  
- Interactive visuals: **Stacked Bar, Area Chart, ArcGIS Map, Treemap, Donut Chart, KPI Cards**  
- Custom **blue theme**, rounded corners, and consistent typography

---

## 🚀 Implementation Steps
1. **Data Import & Validation**  
   - Loaded financial consumer complaints from a pre-processed ![CSV](Data/Financial%20Consumer%20Complaints.csv).
   - Verified row counts for data integrity.  
   - Used *Column Quality, Distribution, and Profile* in Power Query to ensure **100% valid values** and **0% errors**.  
   - Converted `Date Received` and `Date Submitted` columns to **Date** type.

2. **DAX Measures**  
   - `Total Complaints = COUNTROWS('Financial Consumer Complaints')`  
   - `Timely Response % = CALCULATE(COUNTROWS('Financial Consumer Complaints'), 'Financial Consumer Complaints'[Timely response?] = "Yes") / [Total Complaints]`  
   - `In Progress`, `Consumer Disputed Complaints`, `Disputed Rate`, `Resolved at No Cost` calculated using `CALCULATE` with appropriate filters.

3. **Dashboard Construction**  
   - **Slicers:** Date Received, Media  
   - **KPI Cards:** Total Complaints, Timely Response %, Complaints In Progress, Disputed Rate %, Resolved at No Cost %  
   - **Visuals:**  
     - *Stacked Bar Chart* – Total Complaints by Issue  
     - *ArcGIS Map* – Complaints by State  
     - *Area Chart* – Monthly Trend of Total Complaints  
     - *Treemap* – Complaints by Product  
     - *Donut Chart* – % of Consumer Disputed  
   - Applied a **blue theme** with rounded corners and visual shadows for a clean, modern look.

---

## 📊 Key Findings

### 📌 KPI Highlights
- **Total Complaints:** **75,074** – overall volume of consumer dissatisfaction.
- **Timely Response %:** **98.05 %** – strong responsiveness from financial institutions.
- **Complaints in Progress:** **280** – a small portion of unresolved cases.
- **Disputed Rate:** **9.71 %** – nearly 1 in 10 complaints were disputed.
- **Resolved at No Cost:** **84.50 %** – most issues resolved without monetary relief.

### 🏷️ Complaints by Issue
- Top issues: **Managing an account (~8.8K)**, **Deposits & Withdrawals (~6.1K)**, **Payment Process (~3.5K)**.  
- Indicates **operational and account handling** as key consumer pain points.

### 🗺️ Complaints by State
- Highest volumes in **California, Texas, and Florida**, highlighting regions where service improvements are critical.

### 📆 Monthly Trend
- Peaks in **March (7.1K)**, **May (6.9K)**, and **October (6.8K)**.  
- Seasonal dips in **April** and **January** suggest post-holiday or reporting lags.

### 🏦 Complaints by Product
- Leading categories: **Credit Card (~19K)**, **Checking/Savings (~13K)**, **Mortgage (~12K)**.  
- Credit card services remain the largest source of complaints.

### 🔄 Consumer Disputes
- **Disputed:** **9.71 %**  
- **Not Disputed:** **41.27 %**  
- **Missing/NA:** **49.01 %** – highlights data gaps and potential follow-up issues.

---

## 🖼️ Dashboard View
![Financial Complaints Dashboard](Image/financial-complaints-dashboard.png)

---

## 🧠 Conclusion
The **Financial Complaints Dashboard** offers a **comprehensive, interactive view** of consumer issues in the financial services sector.  
By combining **clean data, robust DAX measures, and intuitive visuals**, it empowers regulators and financial organizations to:
- Monitor and reduce dispute rates,
- Enhance **timeliness and quality of responses**, and
- Identify regional or product-based problem areas for targeted improvements.

This scalable Power BI solution provides **actionable insights** that drive better customer service and stronger regulatory compliance.
