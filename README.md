# 🍽️ SYSCO Sales & Operations Analytics Dashboard

<p align="center">
  <b>Enterprise Wholesale Foodservice Distribution, Order Fulfillment & Supply Chain Performance Intelligence</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black" alt="Power BI" />
  <img src="https://img.shields.io/badge/DAX-Time_Intelligence_&_YoY-blue?style=for-the-badge" alt="DAX" />
  <img src="https://img.shields.io/badge/Data_Modeling-Star_Schema-success?style=for-the-badge" alt="Star Schema" />
  <img src="https://img.shields.io/badge/Fulfillment-95.54%25_On--Time-orange?style=for-the-badge" alt="Fulfillment" />
  <img src="https://img.shields.io/badge/Sales_Growth-+158.71%25_YoY-brightgreen?style=for-the-badge" alt="YoY Growth" />
</p>

---

## 📌 Executive Overview
The **SYSCO Sales & Operations Analytics Dashboard** is an enterprise-grade commercial intelligence system built in Power BI to monitor B2B foodservice wholesale operations. Combining transactional line items, logistics fulfillment timelines, category catalog structures, and multi-tier commercial accounts, the system provides cross-functional visibility into revenue velocity, customer acquisition, operational fulfillment, and Year-over-Year (YoY) growth trajectories.

### 📊 Portfolio Key Performance Indicators (KPIs)
- 💰 **Gross Commercial Revenue:** **$1,265,339.00** across verified fulfillment records
- 📈 **Portfolio YoY Growth Rate:** **+158.71%** vs. prior year baseline ($489.10K target benchmark)
- 📦 **Total Orders Fulfilled:** **830 commercial delivery orders**
- 🛒 **Distinct Order Line Items:** **2,154 line transactions** (Average basket density: **2.60 lines/order**)
- 🏷️ **Average Order Value (AOV):** **$1,524.50** per purchase order
- 🚚 **Total Freight Logistics Cost:** **$64,942.69** (Average shipping transit: **7.45 days**, displayed rounded to **8 days**)
- ⏱️ **On-Time Delivery Rate:** **95.54%** (793 orders delivered on or before required date; only 37 late shipments)
- 🏢 **Enterprise Ecosystem:** **91 corporate client accounts**, **77 distinct products** across **8 categories**, **29 global suppliers**, and **9 sales representatives**

---

## 📈 Year-over-Year (YoY) & Temporal Growth Analysis

The system incorporates robust time intelligence DAX modeling (`dim_date`) to capture multi-year commercial trajectories:

| Calendar Year | Net Sales ($) | Orders | SPLY Baseline ($) | Nominal YoY % | Period Scope & Dynamics |
| :--- | :---: | :---: | :---: | :---: | :--- |
| **1996** | **$207,692.70** | 152 | *Baseline* | — | Operations commenced July 4, 1996 (H2 baseline only) |
| **1997** | **$617,022.43** | 408 | $207,692.70 | **+197.08%** | First full 12-month operational cycle; rapid market expansion |
| **1998** | **$440,623.87** | 270 | $617,022.43 | -28.59%* | Data window closes May 6, 1998 (~4.2 operating months) |

> 🔍 **Like-for-Like Run-Rate Growth (Jan 1 – May 6 Window):**  
> Comparing identical date intervals across years proves accelerating operational momentum:
> - **1997 (Jan 1 – May 6):** **$200,761.06**
> - **1998 (Jan 1 – May 6):** **$440,623.87**
> - **Like-for-Like YoY Run-Rate:** **+119.48%** (commercial volume more than doubled over the same period).
> - **Unfiltered Portfolio Gauge Benchmark:** **Total Sales $1.27M** vs. **SPLY Target $489.10K** yields an exact **+158.71%** portfolio outperformance.

---

## 🧮 Core DAX Measures & Formulas

All business logic is encapsulated in dedicated tabular DAX measures:

### 1. Revenue & Time Intelligence
```dax
Total Sales = 
SUM(fact_sales[CC Total Sales])

SPLY Total Sales = 
CALCULATE(
    [Total Sales],
    SAMEPERIODLASTYEAR(dim_date[Date])
)

YoY % = 
DIVIDE(
    [Total Sales] - [SPLY Total Sales],
    [SPLY Total Sales]
)

TYTD = 
TOTALYTD([Total Sales], dim_date[Date])

TQTD = 
TOTALQTD([Total Sales], dim_date[Date])

TMTD = 
TOTALMTD([Total Sales], dim_date[Date])
```

### 2. Operational & Supply Chain Metrics
```dax
# of Orders = 
DISTINCTCOUNT('dim_order'[Order Key])

AVG Ship Days = 
AVERAGE(dim_order[CC Ship Days])

Total Freight = 
SUM(dim_order[Freight])

SPLY Total Freight = 
CALCULATE(
    [Total Freight],
    SAMEPERIODLASTYEAR(dim_date[Date])
)

MAX Gauge = 
2000000
```

---

## 🥩 Category, Product & Operational Performance

### 1. Product Categories Performance
- 🍹 **Beverages:** **$267,868.18** (21.17% of revenue) — Leading category, driven by high-ticket imports
- 🧀 **Dairy Products:** **$234,507.28** (18.53% of revenue) — Core daily high-velocity staple
- 🍖 **Meat/Poultry:** **$163,022.36** (12.88% of revenue) — High average unit ticket items
- 🍬 **Confections:** **$167,357.23** (13.23% of revenue)
- 🐟 **Seafood:** **$131,261.74** (10.37% of revenue)
- 🌾 **Grains/Cereals:** **$95,744.59** (7.57% of revenue)
- 🥫 **Condiments:** **$106,047.08** (8.38% of revenue)
- 🥦 **Produce:** **$99,923.83** (7.90% of revenue)

### 2. Top SKUs by Revenue
1. 🍷 **Côte de Blaye:** **$141,396.74** (Leading commercial beverage)
2. 🌭 **Thüringer Rostbratwurst:** **$80,368.67**
3. 🧀 **Raclette Courdavault:** **$70,977.85**
4. 🧀 **Camembert Pierrot:** **$46,825.50**
5. 🥩 **Tarte au sucre:** **$47,234.97**

### 3. Logistics & Carrier Distribution
- 🚚 **Speedy Express:** 326 orders (39.28%) | Average fulfillment: 7.2 days
- 🚚 **United Package:** 255 orders (30.72%) | Average fulfillment: 7.6 days
- 🚚 **Federal Shipping:** 249 orders (30.00%) | Average fulfillment: 7.7 days

---

## 🖼️ Dashboard Visual Tour & Storytelling

### 1. Landing & Navigation Hub
High-impact visual portal providing quick navigation across executive verticals with real-time operational status.
<p align="center">
  <img src="./Dashboard%20Previews/Landing%20Page.jpg" alt="SYSCO — Landing Hub" width="95%">
</p>

### 2. Sales & Orders Performance Page
Executive dashboard tracking revenue pacing, YoY % performance (+158.71%), carrier volumes, regional map distributions, and monthly sales trends.
<p align="center">
  <img src="./Dashboard%20Previews/Sales%20%26%20Orders%20Page.png" alt="SYSCO — Sales & Orders Performance" width="95%">
</p>

### 3. Categories & Products Deep Dive
Catalog analytics breaking down SKU velocities, inventory reorder alerts, stock availability (69 active vs. 8 discontinued), and category revenue shares.
<p align="center">
  <img src="./Dashboard%20Previews/Categories%20%26%20Products%20Page.png" alt="SYSCO — Categories & Products" width="95%">
</p>

### 4. Customers, Employees & Supplier Ecosystem
Stakeholder analysis correlating account volume concentrations, sales representative achievements, and international supplier lead reliability.
<p align="center">
  <img src="./Dashboard%20Previews/Customers%20%26%20Employees%20%26%20Suppliers.png" alt="SYSCO — Stakeholders Ecosystem" width="95%">
</p>

---

## 🏗️ Data Architecture & Star Schema
The semantic model is engineered as a clean Star Schema optimized for performance and filter propagation:

```
                      +-------------------+
                      |     dim_date      |
                      +-------------------+
                               | 1
                               | 
                               | *
+------------------+ 1       * +-------------------+ *       1 +------------------+
|   dim_customer   |-----------|    fact_sales     |-----------|   dim_product    |
+------------------+           +-------------------+           +------------------+
                               | *               | *                    | *
                               |                 |                      | 1
                               | 1               | 1           +------------------+
                      +-------------------+      |             |   dim_category   |
                      |     dim_order     |      |             +------------------+
                      +-------------------+      |                      | *
                               | *               |                      | 1
                               | 1               |             +------------------+
                      +-------------------+      +-------------|   dim_supplier   |
                      |   dim_employee    |                    +------------------+
                      +-------------------+
```

### 📐 Physical Star Schema Diagram
<p align="center">
  <img src="./Dashboard%20Previews/Model.png" alt="SYSCO Sales & Operations Analytics — Power BI Data Model" width="95%">
</p>

---

## 🛠️ Technology Stack & Methods
- 📊 **Power BI Desktop & Service:** Dynamic KPI cards, gauge benchmarks, interactive geospatial mapping, and automated drill-throughs
- 📐 **DAX (Data Analysis Expressions):** Time Intelligence (`SAMEPERIODLASTYEAR`, `TOTALYTD`), dynamic ratio calculations, and filter context manipulation
- 🧹 **Power Query (M):** Multi-table ETL, date dimension generation, data type casting, key harmonization
- 📐 **Data Modeling:** Formal Star Schema with 1-to-many single-direction relationships to avoid circular filter traps

---

## 📜 Author & Portfolio
- **Author:** Kerelos Nakhla
- **GitHub:** [@Kerelos-Nakhla](https://github.com/Kerelos-Nakhla)
- **Portfolio:** [Kerelos Nakhla Portfolio](https://github.com/Kerelos-Nakhla/Portofolio)
- **License:** MIT License
