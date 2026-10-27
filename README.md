# E-commerce Sales & Profit Dashboard

An interactive Excel dashboard built on a star-schema data model, analyzing e-commerce sales and profit by region, category, segment, ship mode, and customer (2014 – 2017).

![Dashboard Preview](/images/dashboard.png.png)

## Project Overview
This project loads six related tables into Excel's Data Model using Power Query and analyzes 9,994 transactions from 5,009 orders and 793 customers. The dashboard includes 8 KPI cards, 6 charts, and slicers for year, month, and product category. All amounts are in SAR.

## Objective
Evaluate sales and profit performance and identify which regions, cities, product categories, customer segments, and shipping modes drive revenue.

## Dataset
- Six tables : transactions, customers, locations, products, segments, and ship modes
- Period : January 2014 to December 2017
- Source : a training dataset provided by the instructor of a data analysis training program as a practice exercise, shared with permission for portfolio use. 

## Tools & Techniques
- **Microsoft Excel**
- **Power Query** to load and transform the tables
- **Data Model** with a star schema: one transactions table linked to five lookup tables
- 24 PivotTables and 6 charts
- Slicers for year, month, and category

## Data Preparation
- Promoted headers and set data types for every table
- Removed empty columns from the transactions table and the postal code column from the locations table
- Removed duplicate products (by Product ID)
- Added calculated columns: Sales = Unit Price × Quantity, Costs = Unit Cost × Quantity, Profits = Sales − Costs, and delivery days = Ship Date − Order Date
- Counted distinct orders (5,009) instead of rows (9,994), because each order can contain several products

## Key Insights
- **Overall:** SAR 568,337 in sales, SAR 283,298 in costs, and SAR 285,039 in profit (about 50% margin).
- **Regions:** West led with SAR 184,188 (32% of sales); South was the lowest at SAR 93,120 (16%).
- **Categories:** Office Supplies drove 60% of sales, followed by Furniture (21%) and Technology (18%).
- **Segments:** Consumer accounted for 52% of sales, Corporate for 31%, and Home Office for 18%.
- **Shipping:** Standard Class represented 60% of sales; average delivery time is about 4 days.
- **Cities:** New York City (SAR 51,713) and Los Angeles (SAR 43,090) were the top two.
- **Growth:** Yearly sales rose from SAR 113K in 2014 to SAR 187K in 2017 (about +66%); use the year slicer to explore it.
- **Customers:** Sales are widely spread; the top 5 customers account for about 2% of total sales.

## How to Use
1. Download [ecommerce-sales-profit-dashboard.xlsx](ecommerce-sales-profit-dashboard.xlsx).
2. Open it in Microsoft Excel (desktop version recommended for slicers).
3. Open the **Dashboard** sheet and use the slicers to filter the KPIs and charts.

**Note :** The data model was loaded from the file in the `data` folder. You can explore the dashboard without refreshing. To refresh, point Power Query to a local copy of that file.
