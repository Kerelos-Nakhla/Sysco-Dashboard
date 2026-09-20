# SYSCO Sales & Operations Analytics Dashboard

<p align="center">
  <b>Wholesale Foodservice Distribution, Order Fulfillment & Supply Chain Performance Intelligence</b>
</p>

---

## Executive Overview
The **SYSCO Sales & Operations Analytics Dashboard** is an enterprise B2B analytics platform developed in Power BI for foodservice distribution. Spanning hundreds of corporate accounts, diverse product categories, regional sales representatives, and global suppliers, the dashboard delivers granular operational insight into order velocities, product line margins, and fulfillment efficiency.

### Core Commercial Metrics (Calculated from Actual Dataset)
- **Net Sales Volume:** **$1,265,339.00** across verified fulfillment records
- **Total Orders Processed:** 830 commercial delivery orders
- **Distinct Order Line Items:** 2,154 product order line entries
- **Commercial Dimensions:** B2B restaurant and institutional customer accounts, international food suppliers, category managers, and regional sales representatives

---

## Business Problem & Key Findings
1. **Category Contribution & Margin Optimization:** Identifying high-revenue vs. high-margin food categories (Beverages, Dairy, Meat/Poultry, Produce) to optimize warehouse allocations and promotional pricing.
2. **Sales Representative Velocity:** Tracking individual account executive sales contributions, average discount concessions, and repeat order cycles.
3. **Supplier Fulfillment Reliability:** Monitoring supplier order volumes and delivery lead times to mitigate supply chain bottlenecks.

---

## Dashboard Visual Tour & Storytelling

### 1. Landing
<p align="center">
  <img src="./Dashboard%20Previews/Landing%20Page.jpg" alt="SYSCO Sales & Operations — Landing" width="95%">
</p>

### 2. Sales & Orders
<p align="center">
  <img src="./Dashboard%20Previews/Sales%20%26%20Orders%20Page.png" alt="SYSCO Sales & Operations — Sales & Orders" width="95%">
</p>

### 3. Category & Products
<p align="center">
  <img src="./Dashboard%20Previews/Categories%20%26%20Products%20Page.png" alt="SYSCO Sales & Operations — Categories & Products" width="95%">
</p>

### 4. Customers & Employees & Suppliers
<p align="center">
  <img src="./Dashboard%20Previews/Customers%20%26%20Employees%20%26%20Suppliers.png" alt="SYSCO Sales & Operations — Customers, Employees & Suppliers" width="95%">
</p>

---

## Data Architecture & Model
The data model is engineered as a dimensional Star Schema connecting order fulfillment and transactional sales to master business entities.

### Model Representation
<p align="center">
  <img src="./Dashboard%20Previews/Model.png" alt="SYSCO Sales & Operations Analytics — Power BI Data Model" width="95%">
</p>

- **Fact Table (`fact_sales`):** 2,154 transaction line items capturing Unit Price, Quantity, Discount rates, and calculated Total Sales.
- **Dimension Tables:**
  - `dim_order`: 830 commercial orders, order dates, required dates, and ship methods.
  - `dim_product`: Product catalog, unit packaging, and stock levels.
  - `dim_category`: Foodservice classifications (Beverages, Condiments, Confections, Dairy Products, Grains/Cereals, Meat/Poultry, Produce, Seafood).
  - `dim_customer`: Restaurant and hospitality client accounts.
  - `dim_employee`: Sales representatives and territory account executives.
  - `dim_supplier`: Food manufacturing and agricultural supply partners.
  - `dim_date`: Calendar dimensions for seasonality and trend analysis.

---

## Tools & Technologies
- **Business Intelligence:** Microsoft Power BI Desktop
- **Data Modeling:** Kimball Dimensional Design with referential integrity
- **DAX Measures:** Net Sales, Margin %, Average Order Value (AOV), Discount Variance, and Customer Retention Rates
- **ETL:** Power Query (M) for invoice reconciliation and master data management

---

## License & Usage
This repository is released under the [MIT License](LICENSE). Developed by **Kerelos Nakhla** — Data Analyst & BI Developer.
