# Sales & Revenue Analysis Dashboard

An interactive Excel dashboard for analyzing sales and revenue data — tracks KPIs like total sales, revenue trends, and top-performing products, with dynamic charts and filters.

## Overview

This project simulates a full year (FY2025) of sales transaction data and turns it into a business-ready dashboard for tracking performance across regions, product categories, sales reps, and channels.

## Features

- **KPI Cards** — Total Net Revenue, Total Profit, Total Orders, and Units Sold, all calculated live from the underlying data
- **Region Filter** — a dropdown control that instantly recalculates all KPIs for a selected region (or "All")
- **Monthly Trend Chart** — line chart of net revenue and profit across all 12 months
- **Regional Breakdown** — bar chart comparing revenue by region
- **Category Breakdown** — pie chart showing revenue share by product category
- **Top Products** — bar chart of the 10 best-selling products by revenue
- **Sales Rep Performance** — bar chart ranking reps by revenue generated
- **Filterable Data Table** — the raw transaction data is an Excel Table with column filter dropdowns for detailed drill-down

## File Structure

The workbook (`SalesRevenueDashboard.xlsx`) contains three sheets:

| Sheet | Description |
|---|---|
| **Dashboard** | KPI cards, filter control, and all charts |
| **Raw Data** | 2,170 sample sales transactions (date, region, category, product, customer, rep, channel, quantity, price, discount, revenue, cost, profit) |
| **Summary Data** | Aggregated tables (by month, region, category, product, rep, channel) that feed the dashboard charts |

## How to Use

1. Open `SalesRevenueDashboard.xlsx` in Excel.
2. Go to the **Dashboard** sheet.
3. Use the **Region dropdown** (cell C6) to filter KPIs by region, or leave it set to "All."
4. To explore transaction-level detail, go to the **Raw Data** sheet and use the column filter dropdowns (Excel Table AutoFilter) on any field.
5. To use your own data, replace the rows in **Raw Data** — the KPI formulas and charts will recalculate automatically as long as column order is preserved.

## Tech Notes

- Built with Python (`openpyxl`, `pandas`) to generate realistic sample data and construct the workbook.
- All KPI values are driven by live Excel formulas (`SUMPRODUCT`), not hardcoded numbers.
- Zero formula errors — verified with a recalculation pass.

## Learning Outcomes

This project demonstrates:
- Data visualization and dashboard design in Excel
- KPI tracking and business performance monitoring
- Turning raw transactional data into actionable insights using charts, filters, and summary tables
