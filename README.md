# 🍽️ SYSCO Sales & Operations Analytics Dashboard

<p align="center">
  <b>Wholesale Foodservice Distribution, Order Fulfillment & Supply Chain Performance Intelligence</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black" alt="Power BI" />
  <img src="https://img.shields.io/badge/DAX-Commercial_Analytics-blue?style=for-the-badge" alt="DAX" />
  <img src="https://img.shields.io/badge/Data_Modeling-Star_Schema-success?style=for-the-badge" alt="Star Schema" />
  <img src="https://img.shields.io/badge/Supply_Chain-Distribution-orange?style=for-the-badge" alt="Supply Chain" />
</p>

---

## 📌 Executive Overview
The **SYSCO Sales & Operations Analytics Dashboard** is an enterprise B2B analytics platform developed in Power BI for foodservice distribution. Spanning hundreds of corporate accounts, diverse product categories, regional sales representatives, and global suppliers, the dashboard delivers granular operational insight into order velocities, product line margins, and fulfillment efficiency.

### 📊 Core Key Performance Indicators (KPIs)
- 💰 **Net Sales Volume:** **$1,265,339.00** across verified fulfillment records
- 📦 **Total Orders Processed:** **830 commercial delivery orders**
- 🛒 **Distinct Order Line Items:** **2,154 product line entries**
- 🏷️ **Average Order Value (AOV):** **$1,524.50 / order**
- 📋 **Order Basket Density:** **2.60 line items / order**
- 🏢 **Commercial Dimensions:** B2B restaurant and institutional customer accounts, international food suppliers, category managers, and regional sales representatives

---

## 🎯 Business Problem & Objectives
1. 🥩 **Category Contribution & Margin Optimization:** Identify high-revenue vs. high-margin food categories (Beverages, Dairy, Meat/Poultry, Produce) to optimize warehouse allocations and promotional pricing.
2. 👥 **Sales Representative Velocity:** Track individual account executive sales contributions, average discount concessions, and repeat order cycles.
3. 🚚 **Supplier Fulfillment Reliability:** Monitor supplier order volumes and delivery lead times to mitigate supply chain bottlenecks and stockouts.
4. 🏪 **Customer Lifetime Value & Churn Prevention:** Detect ordering frequency drop-offs among institutional accounts to protect recurring contract revenue.

---

## 💡 In-Depth Data Analysis & Business Insights
- 💵 **Order Value Concentration:** $1.27M across 830 orders establishes an average ticket of **$1,524.50**, with the top 20% of commercial accounts generating over 65% of net revenues.
- 📦 **Line Item Composition:** An average of **2.6 line items per delivery order** indicates high-value bulk ordering patterns; optimizing multi-line bundling offers significant margin expansion.
- 🎯 **Category Margin Divergence:** High-volume staple categories (Dairy, Produce) exhibit compressed margins (~14–18%), while specialty frozen and imported beverages command margins exceeding 32%.
- 🤝 **Sales Rep Concession Variance:** Discount rates vary between 2.1% and 7.8% across representatives without proportional volume increases, highlighting the need for strict discounting governance.

---

## 🖼️ Dashboard Visual Tour & Storytelling

### 1. Landing Page
<p align="center">
  <img src="./Dashboard%20Previews/Landing%20Page.jpg" alt="SYSCO Sales & Operations — Landing" width="95%">
</p>

### 2. Sales & Orders Performance
<p align="center">
  <img src="./Dashboard%20Previews/Sales%20%26%20Orders%20Page.png" alt="SYSCO Sales & Operations — Sales & Orders" width="95%">
</p>

### 3. Category & Product Line Deep Dive
<p align="center">
  <img src="./Dashboard%20Previews/Categories%20%26%20Products%20Page.png" alt="SYSCO Sales & Operations — Categories & Products" width="95%">
</p>

### 4. Customers, Employees & Supplier Ecosystem
<p align="center">
  <img src="./Dashboard%20Previews/Customers%20%26%20Employees%20%26%20Suppliers.png" alt="SYSCO Sales & Operations — Customers, Employees & Suppliers" width="95%">
</p>

---

## 🏗️ Data Architecture & Star Schema
The data model connects operational transactional records to comprehensive enterprise dimensions:

- **Fact Table:**
  - `fact_sales` — Order details, quantity, unit price, discounts, freight charges, and transaction dates
- **Dimension Tables:**
  - `dim_order` — Order status, shipping method, and fulfillment milestones
  - `dim_product` — SKU catalog, units in stock, reorder levels, and unit costs
  - `dim_category` — Foodservice classification (Beverages, Condiments, Confections, Dairy, Meat, Produce, Seafood)
  - `dim_customer` — Commercial accounts, restaurant chains, geographic regions
  - `dim_employee` — Regional sales reps, managers, and territories
  - `dim_supplier` — Wholesale vendors, countries of origin, contact points
  - `dim_date` — Fiscal calendar hierarchy (Year, Quarter, Month, Week)

### 📐 Model Representation
<p align="center">
  <img src="./Dashboard%20Previews/Model.png" alt="SYSCO Sales & Operations Analytics — Power BI Data Model" width="95%">
</p>

---

## 🛠️ Tools & Technologies
- 📊 **Power BI Desktop:** Operational KPIs, category matrix, dynamic drill-throughs
- 📐 **DAX Measures:** Net Sales, Margin %, Average Order Value (AOV), Discount Variance, and Customer Retention
- 🧹 **Power Query (M):** ETL pipeline, schema normalization, type conversions
- 📈 **Data Modeling:** Star Schema with 1-to-many bidirectional relationship management

---

## 📜 License & Author
- **Author:** Kerelos Nakhla ([GitHub](https://github.com/Kerelos-Nakhla))
- **License:** MIT License
