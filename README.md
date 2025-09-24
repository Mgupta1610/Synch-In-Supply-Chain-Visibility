# SynchIn: Supply Chain Visibility

### A Tableau dashboard to monitor inventory, supplier performance, and sales trends at a glance.

## Project Overview & Objectives
Build an interactive Warehouse Inventory & Sales Analytics dashboard using Tableau on a grocery dataset to:
- Monitor stock levels and product availability
- Evaluate supplier performance (pricing & delivery efficiency)
- Analyze sales trends and identify fast/slow-moving items

## Dataset Information
**Source:** Kaggle API — Grocery Inventory & Sales  
**Columns Used**
- **Product Details:** `Product_ID`, `Product_Name`, `Category`
- **Inventory:** `Stock_Quantity`, `Reorder_Level`, `Reorder_Quantity`, `Expiration_Date`
- **Supplier Details:** `Supplier_ID`, `Supplier_Name`
- **Sales:** `Sales_Volume`, `Inventory_Turnover_Rate`

## Data Preprocessing (Python • Pandas)
- **Date formatting:** converted `Date_Received`, `Last_Order_Date`, `Expiration_Date` to `datetime`
- **Unit price cleanup:** stripped currency symbols → numeric
- **Missing values:** checked & imputed where necessary
- **Category grouping:** mapped fine-grained items into broader categories

## Tableau Dashboards

### 1) Stock Level Monitoring 📊
**Purpose:** Track current stock levels; flag products needing restock  
**Key fields:** `Stock_Quantity`, `Reorder_Level`, `Expiration_Date`  
**Conditional formatting:**  
- **Green** → sufficient stock  
- **Orange** → low stock  
- **Red** → reorder needed

### 2) Supplier Performance Analysis 📦
**Purpose:** Compare suppliers on efficiency & availability  
**Key fields:** `Supplier_Name`, `Sales_Volume`, `Reorder_Quantity`  
**Insights:** Identify best-performing suppliers and optimize vendor relationships

### 3) Sales Trend Analysis 📈
**Purpose:** Find fast/slow movers & seasonality  
**Key fields:** `Sales_Volume`, `Category`, *Quarter* of `Last_Order_Date`  
**Insights:** Seasonal demand patterns and category-wise performance

## Deployment
- Published on **Tableau Public** for interactive exploration  
- Built-in filters for **Category**, **Supplier**, and **Sales Period** for drill-down analysis
