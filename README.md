# 🏗️ SQL Data Warehouse & Analytics — End-to-End Project

> **Building a production-grade Data Warehouse from scratch using Medallion Architecture, Star Schema modeling, and 13-module EDA — entirely in SQL.**

---

## 📌 What This Project Is

This is a **full-lifecycle data engineering and analytics project** built on Microsoft SQL Server. Starting from raw, disconnected CRM and ERP data, I designed and implemented a complete analytical system — including ETL pipelines, data quality layers, dimensional modeling, and business-insight generation.

No drag-and-drop tools. No BI shortcuts. Pure SQL engineering.

---

## 🎯 What I Built

| Layer | What Happened Here |
|---|---|
| 🥉 **Bronze** | Raw ingestion from CRM + ERP — unchanged, traceable, auditable |
| 🥈 **Silver** | Cleansing, standardization, deduplication, business rule validation |
| 🥇 **Gold** | Star Schema dimensional model — analytics-ready, query-optimized |

---

## ⭐ Data Model — Star Schema

```
              ┌──────────────┐
              │  Dim Customer │
              └──────┬───────┘
                     │
┌─────────────┐      │      ┌─────────────┐
│  Dim Product ├──── Fact ────┤   Dim Date  │
└─────────────┘    Sales    └─────────────┘
```

The Gold Layer is built on a clean **Star Schema** with:
- `Fact_Sales` — transactional grain
- `Dim_Customer` — customer attributes + geography
- `Dim_Product` — product hierarchy, categories, subcategories
- `Dim_Date` — full calendar spine for time-intelligence queries

---

## 📊 Phase 2 — Exploratory Data Analysis (13 Modules)

After the warehouse was built, I ran a structured EDA across 13 analytical scripts:

| # | Module | What I Analyzed |
|---|---|---|
| 01 | Database Exploration | Schema inventory, table profiling, record counts |
| 02 | Dimensions Exploration | Customer geography, product hierarchy |
| 03 | Date Range Exploration | Temporal coverage, earliest/latest transactions |
| 04 | Measures Exploration | Revenue, orders, quantity, average selling price |
| 05 | Magnitude Analysis | Sales by category, region, and product |
| 06 | Ranking Analysis | Top/bottom customers and products via `RANK()`, `DENSE_RANK()` |
| 07 | Change Over Time | Monthly trends, revenue growth, seasonality |
| 08 | Cumulative Analysis | Running totals — revenue and orders |
| 09 | Performance Analysis | Product and customer performance vs. benchmarks |
| 10 | Data Segmentation | High / Medium / Low value customer tiers |
| 11 | Part-to-Whole Analysis | Category and customer revenue share % |
| 12 | Customer Report | Full customer behavioral report — revenue, orders, ranking |
| 13 | Product Report | Full product performance report — sales volume, category analysis |

---

## 🛠️ Technical Stack

| Area | Tools |
|---|---|
| **Database** | Microsoft SQL Server (Dockerized) |
| **Development** | VS Code + SQL Server Extension |
| **Containerization** | Docker Desktop |
| **Version Control** | Git + GitHub |
| **Design & Docs** | Draw.io, Notion, Markdown |

---

## 💡 SQL Skills Demonstrated

```sql
-- Representative techniques used across this project:

✅ CTEs (multi-step transformations)
✅ Window Functions — RANK(), DENSE_RANK(), ROW_NUMBER(), SUM() OVER()
✅ Stored Procedures (ETL automation)
✅ Joins — multi-table CRM + ERP integration
✅ Aggregations — SUM, AVG, COUNT with GROUP BY
✅ Conditional logic — CASE WHEN for segmentation
✅ Date functions — trend and period analysis
✅ Data Quality checks — duplicate detection, null handling
```

---

## 📂 Repository Structure

```
SQL-Project-1-Data-Warehousing/
│
├── datasets/                        # Source CRM + ERP data
│
├── docs/
│   ├── data_architecture.png        # Medallion architecture diagram
│   ├── data_flow.png                # ETL flow visualization
│   ├── data_model.png               # Star Schema diagram
│   └── eda_roadmap.png              # EDA module map
│
├── scripts/
│   ├── bronze/                      # Raw ingestion scripts
│   ├── silver/                      # Cleansing + transformation
│   └── gold/                        # Dimensional model creation
│
├── analytics/
│   ├── 01_database_exploration.sql
│   ├── 02_dimensions_exploration.sql
│   ├── 03_date_range_exploration.sql
│   ├── 04_measures_exploration.sql
│   ├── 05_magnitude_analysis.sql
│   ├── 06_ranking_analysis.sql
│   ├── 07_change_over_time_analysis.sql
│   ├── 08_cumulative_analysis.sql
│   ├── 09_performance_analysis.sql
│   ├── 10_data_segmentation.sql
│   ├── 11_part_to_whole_analysis.sql
│   ├── 12_report_customers.sql
│   └── 13_report_products.sql
│
├── README.md
└── LICENSE
```

---

## 🔍 Key Business Questions This Project Answers

- Who are the **top revenue-generating customers** and what's their share of total revenue?
- Which **product categories** drive the most sales — and which underperform?
- How has **revenue trended month-over-month** and where are the seasonal peaks?
- What does the **customer value distribution** look like across high/medium/low tiers?
- Which products are **consistently bottom performers** worth deprioritizing?

---

## 👨‍💼 About Me

**Varun Gautam** — MBA (HR + Business Analytics), IIM Ranchi

I'm an HR professional with a deep focus on analytics. This project reflects my conviction that the best business decisions come from well-engineered data — not gut feel. I built this end-to-end to sharpen my SQL and data engineering skills beyond the classroom.

📧 i.am.varungautam@gmail.com  
💼 [LinkedIn](https://www.linkedin.com/in/iamvarungautam/)  
💻 [GitHub](https://github.com/iamvarungautam)

---

> ⭐ If this project is interesting to you, let's connect.
