# 📊 Databel Case Study - Power BI Dashboard

## 🧠 Project Overview
This Power BI project analyzes **customer churn** for the telecommunications company **Databel**.  
The goal is to uncover insights behind customer attrition, identify churn drivers, and suggest potential business strategies to improve customer retention.

The project consists of three interactive dashboards:
- **Overview** – High-level churn metrics and customer distribution
- **Age Groups** – Customer behavior and churn by demographic segments
- **Insights** – Service usage, charges, and churn correlation analysis

---

## 🗂️ Files Included
- **Case Study - Databel.pbix** → Main Power BI project file  
- **Screenshots**
  - Screenshot 2025-10-20 014203.jpg 


---

## 📈 Dashboard Sections

### 🔹 1. Databel - Overview
**Key Metrics**
- 🧾 Total Customers: **6,687**
- 📉 Churn Rate: **26.86%**
- 👥 Churned Customers: **1,796**

**Visuals**
- Bar chart: Top churn reasons  
- Map: Churn rate by U.S. state  
- Pie charts: Contract types & churn categories  

---

### 🔹 2. Databel - Age Groups
**Insights by Age Segment**
- Histogram of customers & churn rate by age bins  
- Correlation between **monthly charges** and **churn rate**  
- Interactive slicer for **account length (months)**  

---

### 🔹 3. Databel - Insights
**Performance Indicators**
- Avg. Extra International Charges → **$33.64**  
- Avg. Extra Data Charges → **$3.37**  
- Avg. Customer Service Calls → **0.92**  
- Total Customer Service Calls → **6,123**

**Visuals**
- Churn rate map by state  
- Line chart: Customer service calls vs. churn label  

---

## 🧩 Data Model

The **Databel data model** integrates multiple tables into a **star schema** for optimized analysis and performance.

**Tables Used**
- `Customer` → Customer demographics and account info  
- `Churn` → Churn status and churn reason  
- `Contract` → Contract details (Month-to-Month, One Year, Two Year)  
- `Services` → Data, phone, and internet services  
- `Charges` → Monthly and total charges  

**Relationships**
- `CustomerID` serves as the **primary key** connecting all tables  
- One-to-many relationships link `Customer` to `Contract`, `Services`, and `Charges`

**Model Type:** Star Schema  
**Storage Mode:** Import  

---

## 🧮 Key DAX Measures

| **Measure** | **Formula** | **Description** |
|--------------|-------------|-----------------|
| **Total Customers** | `Total Customers = COUNT(Customer[Customer ID])` | Counts the number of active customers |
| **Total Churned** | `Churned Customers = CALCULATE(COUNT(Customer[Customer ID]), Customer[Churn Label] = "Yes")` | Counts customers who churned |
| **Churn Rate** | `Churn Rate = DIVIDE([Churned Customers], [Total Customers], 0)` | Calculates overall churn percentage |
| **Avg Monthly Charge** | `Avg Monthly Charge = AVERAGE(Charges[Monthly Charges])` | Computes the average customer monthly charge |
| **Avg Customer Service Calls** | `Avg Service Calls = AVERAGE(Services[Customer Service Calls])` | Average number of service calls per customer |
| **Churn by Category** | `Churn by Category = CALCULATE([Churned Customers], VALUES(Customer[Churn Category]))` | Breaks down churn by predefined categories |

---

## 💡 Key Insights
- **High churn (26.86%)** mainly due to **competitor offers** and **customer support dissatisfaction**.  
- Customers on **month-to-month contracts (51%)** show the highest churn.  
- **Older age groups (60+)** exhibit increased churn rates.  
- Frequent **customer service calls** strongly correlate with churn probability.  

---

## 🧰 Tools & Technologies
- **Power BI Desktop**
- **DAX (Data Analysis Expressions)**
- **Data Modeling (Star Schema)**
- **Bing Maps Integration**
- **Interactive Filters & Slicers**

---

## 🚀 How to Use
1. Download the `.pbix` file from this repository.  
2. Open it using **Power BI Desktop**.  
3. Navigate between the interactive dashboards:
   - **Overview**
   - **Age Groups**
   - **Insights**  

---

## 🧰 Requirements
- Power BI Desktop (latest version recommended)
- Basic understanding of DAX and Power BI visuals

---

## 👤 Author
**Mai Hasan Zayan**  
📅 *Created: October 2025*  
🔗 [GitHub Repository](#) *(Add your repository link here)*  

---

## 📜 License
This project is licensed under the **MIT License** – feel free to use, modify, and share with attribution.

---

## 🖼️ Dashboard Previews

### Databel - Overview
![Overview Dashboard](Screenshot%202025-10-20%20014203.jpg)

### Databel - Age Groups
![Age Groups Dashboard](Screenshot%202025-10-20%20014243.jpg)

### Databel - Insights
![Insights Dashboard](Screenshot%202025-10-20%20014328.jpg)

