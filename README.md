<div align="center">

# SQL Data Warehouse & Analytics
### End-to-End Data Engineering & Business Intelligence Project

*Medallion Architecture · Star Schema · 13-Module EDA · Pure SQL*

<br>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Varun%20Gautam-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/iamvarungautam/)
[![GitHub](https://img.shields.io/badge/GitHub-iamvarungautam-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/iamvarungautam)
[![Email](https://img.shields.io/badge/Email-i.am.varungautam%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:i.am.varungautam@gmail.com)

<br>

![SQL Server](https://img.shields.io/badge/Microsoft%20SQL%20Server-CC2927?style=flat-square&logo=microsoft-sql-server&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![VS Code](https://img.shields.io/badge/VS%20Code-007ACC?style=flat-square&logo=visual-studio-code&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)

</div>

---

## 📌 What This Project Is

A **full-lifecycle data engineering and analytics project** built on Microsoft SQL Server. Starting from raw, disconnected CRM and ERP data, I designed and implemented a complete analytical system — ETL pipelines, data quality layers, dimensional modeling, and 13 structured EDA modules delivering actionable business insights.

> No drag-and-drop tools. No BI shortcuts. Pure SQL engineering.

---

<br>

# 🏗️ Phase 1 — Data Warehousing

<br>

## Data Architecture

<p align="center">
  <img src="docs/data_architecture.png" width="900">
</p>

<br>

The project follows a **Medallion Architecture** — three distinct zones with clear separation of responsibility:

<div align="center">

| &nbsp; | Layer | Purpose |
|:---:|---|---|
| 🥉 | **Bronze** | Raw ingestion from CRM + ERP — unchanged, traceable, auditable |
| 🥈 | **Silver** | Cleansing, standardization, deduplication, business rule validation |
| 🥇 | **Gold** | Star Schema dimensional model — analytics-ready, query-optimized |

</div>

---

## 🔄 Data Flow

<p align="center">
  <img src="docs/data_flow.png" width="900">
</p>

<br>

The pipeline integrates CRM and ERP datasets through a structured ETL/ELT workflow:

```
CRM + ERP Sources  →  Bronze (Raw)  →  Silver (Clean)  →  Gold (Model)  →  Analytics
```

1. Extract data from CRM and ERP source systems
2. Load raw data into Bronze Layer
3. Cleanse and standardize data in Silver Layer
4. Integrate and reconcile business entities across systems
5. Build dimensional models in Gold Layer
6. Deliver analytics-ready datasets for reporting

---

## ⭐ Data Model — Star Schema

<p align="center">
  <img src="docs/data_model.png" width="900">
</p>

<br>

The Gold Layer is built on a clean **Star Schema** optimized for analytical reporting:

<div align="center">

| Table | Type | Description |
|---|:---:|---|
| `Fact_Sales` | Fact | Core transactional grain — revenue, quantity, orders |
| `Dim_Customer` | Dimension | Customer attributes, geography, categories |
| `Dim_Product` | Dimension | Product hierarchy, categories, subcategories |

</div>

> This structure enables high-performance slicing across customers, products, and time — the three axes every sales analytics question reduces to.

---

## ⚙️ Data Engineering Components

<details>
<summary><b>🔧 ETL / ELT Pipeline</b></summary>
<br>

- Data extraction from heterogeneous source systems
- Staged loading with full auditability
- Incremental and full-load transformation logic

</details>

<details>
<summary><b>✅ Data Quality Management</b></summary>
<br>

- Duplicate detection and handling
- Missing value treatment
- Standardization rules and business rule enforcement
- Data enrichment and validation checks

</details>

<details>
<summary><b>🔗 Data Integration</b></summary>
<br>

- CRM + ERP business key reconciliation
- Master data alignment across systems
- Unified customer and product entities

</details>

<details>
<summary><b>📐 Dimensional Modeling</b></summary>
<br>

- Fact table design at transactional grain
- Conformed dimensions for consistent reporting
- Star Schema implementation for query performance

</details>

<br>

---

<br>

# 📊 Phase 2 — Exploratory Data Analysis


After building the warehouse, I ran a **structured 13-module EDA** on the Gold Layer — moving from database validation all the way to reusable business reports.

---

## 🔬 Foundational EDA — Modules 1 to 6

<details open>
<summary><b>1️⃣ Database Exploration</b></summary>
<br>

Validated the analytical dataset before any analysis:
- Database inventory and schema review
- Table structure and record count verification
- Data completeness checks and readiness assessment

</details>

<details open>
<summary><b>2️⃣ Dimension Exploration</b></summary>
<br>

Profiled the business entities available for slicing:

**Customer Dimension** — distribution, geographic spread, customer categories  
**Product Dimension** — category hierarchy, subcategory breakdown, product distribution

Techniques: `DISTINCT` analysis, category profiling, data distribution checks

</details>

<details open>
<summary><b>3️⃣ Date Exploration</b></summary>
<br>

Established the temporal boundaries of the dataset:
- Earliest and latest transaction dates
- Total historical coverage period
- Time span available for trend analysis

</details>

<details open>
<summary><b>4️⃣ Measures Exploration</b></summary>
<br>

Established baseline KPIs across the business:

| Metric | SQL Function |
|---|:---:|
| Total Sales Revenue | `SUM()` |
| Total Orders | `COUNT()` |
| Total Quantity Sold | `SUM()` |
| Average Selling Price | `AVG()` |

</details>

<details open>
<summary><b>5️⃣ Magnitude Analysis</b></summary>
<br>

Evaluated business performance scale across dimensions:
- Sales by Product Category
- Revenue by Customer
- Orders by Country / Region
- Quantity Sold by Product

Identified major revenue drivers, high-volume categories, and customer contribution patterns.

</details>

<details open>
<summary><b>6️⃣ Ranking Analysis</b></summary>
<br>

Identified top and bottom performers using window functions:

**Customer Rankings** — Top and bottom revenue contributors  
**Product Rankings** — Best-selling and lowest-performing products

```sql
ROW_NUMBER() OVER (ORDER BY revenue DESC)
RANK()       OVER (PARTITION BY category ORDER BY sales DESC)
DENSE_RANK() OVER (ORDER BY orders DESC)
```

</details>

---

## 📈 Advanced Analytics — Modules 7 to 11

<details open>
<summary><b>7️⃣ Change Over Time Analysis</b></summary>
<br>

- Monthly and quarterly sales trends
- Revenue growth patterns over the analysis period
- Seasonal performance identification

</details>

<details open>
<summary><b>8️⃣ Cumulative Analysis</b></summary>
<br>

- Running revenue totals using `SUM() OVER(ORDER BY date)`
- Cumulative order tracking
- Progressive performance benchmarking

</details>

<details open>
<summary><b>9️⃣ Performance Analysis</b></summary>
<br>

- Year-over-Year revenue comparison
- Product performance vs. category average
- Customer performance vs. overall average

</details>

<details open>
<summary><b>🔟 Data Segmentation</b></summary>
<br>

Classified customers and products into value tiers using `CASE WHEN` logic:

| Segment | Criteria |
|---|---|
| 🟢 High Value | Top revenue contributors |
| 🟡 Medium Value | Mid-range performance |
| 🔴 Low Value | Bottom contributors |

</details>

<details open>
<summary><b>1️⃣1️⃣ Part-to-Whole Analysis</b></summary>
<br>

Revenue contribution analysis:
- Category revenue share as % of total
- Product contribution % within category
- Customer revenue share across the base

</details>

---

## 📋 Business Reports — Modules 12 & 13

<details open>
<summary><b>1️⃣2️⃣ Customer Report — <code>report_customers.sql</code></b></summary>
<br>

A reusable, comprehensive customer analytics report covering:
- Total revenue per customer
- Order volume and purchase frequency
- Customer ranking by revenue tier
- Segmentation classification

</details>

<details open>
<summary><b>1️⃣3️⃣ Product Report — <code>report_products.sql</code></b></summary>
<br>

A reusable product performance report covering:
- Revenue and sales volume by product
- Category-level performance analysis
- Product ranking within and across categories
- Identification of star performers and laggards

</details>

---

## 🧠 SQL Concepts Applied

```sql
-- Techniques demonstrated across this project

✅ CTEs                 →  Multi-step transformations, readable logic
✅ Window Functions     →  RANK(), DENSE_RANK(), ROW_NUMBER(), SUM() OVER()
✅ Stored Procedures    →  ETL automation and reusable report logic
✅ Multi-table JOINs    →  CRM + ERP integration across fact and dimensions
✅ Aggregate Functions  →  SUM, AVG, COUNT with GROUP BY / HAVING
✅ CASE WHEN            →  Segmentation and conditional classification
✅ Date Functions       →  Trend analysis, period calculations
✅ Subqueries           →  Nested analytical logic
✅ Data Quality Checks  →  Duplicate detection, null handling, validation
```

---

<br>

## 🔍 Business Questions This Project Answers

> - Who are the **top revenue-generating customers** and what % of total revenue do they represent?
> - Which **product categories** drive the most sales — and which consistently underperform?
> - How has **revenue trended month-over-month** and where are the seasonal peaks?
> - What does the **customer value distribution** look like across high/medium/low tiers?
> - Which products should be **deprioritized** based on sustained low performance?

---

<br>

# 🛠️ Technology Stack

<div align="center">

| Area | Tools |
|---|---|
| **Database** | Microsoft SQL Server |
| **Infrastructure** | Docker Desktop (containerized SQL Server) |
| **Development** | VS Code + SQL Server Extension |
| **Version Control** | Git + GitHub |
| **Design & Docs** | Draw.io, Notion, Markdown |
| **Hardware** | Apple MacBook Air (M-Series), macOS |

</div>

---

# 📂 Repository Structure

```text
data-warehouse-project/
│
├── datasets/                          # Source CRM + ERP data (CSV)
│
├── docs/
│   ├── data_architecture.png          # Medallion architecture diagram
│   ├── data_flow.png                  # ETL pipeline flow
│   ├── data_model.png                 # Star Schema diagram
│   ├── eda_roadmap.png                # EDA module map
│   ├── data_catalog.md                # Field definitions and metadata
│   └── naming_conventions.md         # Naming standards used
│
├── scripts/
│   ├── bronze/                        # Raw ingestion scripts
│   ├── silver/                        # Cleansing + transformation
│   └── gold/                          # Dimensional model creation
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
├── tests/
├── README.md
├── LICENSE
└── .gitignore
```

---

<br>

<div align="center">

## 👨‍💼 About Me

**Varun Gautam**

MBA (HR + Business Analytics) · IIM Ranchi

*HR Professional · People Analytics · SQL Developer*

I built this project end-to-end to go beyond classroom SQL — architecture design, pipeline development, quality management, and business analysis in one cohesive system. My goal is to sit at the intersection of business, data, and decision-making.

<br>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/iamvarungautam/)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/iamvarungautam)
[![Email](https://img.shields.io/badge/Email-Reach%20Out-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:i.am.varungautam@gmail.com)

<br>

*⭐ If this project resonates with you — star the repo and let's connect.*

</div>
