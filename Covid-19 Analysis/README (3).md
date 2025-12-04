# 🦠 COVID-19 Analysis Dashboard  
### Power BI • SQL • Excel • Data Visualization

This project presents a complete **end-to-end COVID-19 data analysis**, covering global case trends, recovery & death rates, and country-wise comparisons.  
The analysis helps understand how the pandemic evolved across regions and highlights major insights using interactive dashboards.

---

## 📌 **Project Overview**

The goal of this project is to:

- Analyze worldwide COVID-19 cases, deaths, recoveries, and active cases  
- Build interactive Power BI dashboards with drilldowns  
- Identify worst-affected countries  
- Study growth trends & patterns  
- Create automated data pipelines using **SQL**  
- Perform data cleaning & preprocessing using **Excel**

This project is ideal for learning **data analytics**, **visualization**, and **BI reporting**.

---

## 📁 **Datasets Used**

The analysis uses two main datasets:

- **worldometer_data.csv**  
  - Country-wise statistics  
  - Columns include: Total Cases, New Cases, Total Deaths, Active Cases, Total Tests, Population, etc.

- **country_wise_latest.csv**  
  - Latest COVID-19 numbers  
  - Contains: Confirmed, Deaths, Recovered, Active, WHO Region

(Upload these files in your GitHub repo for reference.)

---

## 🛠️ **Tools & Technologies**

| Tool / Tech | Purpose |
|-------------|---------|
| **Power BI** | Dashboard creation, KPI cards, maps, trend visuals |
| **Excel** | Cleaning, removing nulls, transformation |
| **SQL** | Automated refresh, querying datasets |
| **DAX** | Calculating metrics & measures |
| **Power Query** | Data preprocessing |

---

## 📊 **Dashboards Created**

### **1️⃣ Overview Dashboard**
- Global Summary KPIs  
- Total Cases, Active Cases, Deaths  
- World Map showing case distribution  
- Top 10 most affected countries  
- Country slicer with drilldowns  

### **2️⃣ Trend Analysis Dashboard**
- Daily confirmed cases line chart  
- Death vs Recovery trends  
- Active vs Recovered comparison  
- Country-wise growth over time  

### **3️⃣ Country-wise Analysis Dashboard**
- Table of all countries with sorting  
- Metrics per million population  
- Test positivity rate  
- Mortality rate (DAX measure)  
- Recovery rate  

---

## 📐 **Key DAX Measures**

```DAX
Recovery Rate = DIVIDE(SUM(country_wise_latest[Recovered]), SUM(country_wise_latest[Confirmed])) * 100

Mortality Rate = DIVIDE(SUM(country_wise_latest[Deaths]), SUM(country_wise_latest[Confirmed])) * 100

Active Case Ratio = DIVIDE(SUM(country_wise_latest[Active]), SUM(country_wise_latest[Confirmed])) * 100
