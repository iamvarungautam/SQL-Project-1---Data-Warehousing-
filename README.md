# 🚀 SQL Data Warehouse & Analytics Project

## 📌 Overview

This project demonstrates the end-to-end development of a modern Data Warehouse and Analytics solution using Microsoft SQL Server. The project covers the complete data lifecycle, from ingesting raw data from multiple source systems to transforming it into business-ready datasets and generating actionable insights through Exploratory Data Analysis (EDA).

The solution follows the **Medallion Architecture (Bronze → Silver → Gold)** framework and incorporates industry-standard practices in Data Engineering, Data Modeling, Data Quality Management, and Data Analytics.

---

## 🎯 Project Objectives

- Build a scalable Data Warehouse using SQL Server
- Integrate CRM and ERP datasets into a unified analytical model
- Develop ETL/ELT pipelines for data processing
- Perform data cleansing and quality validation
- Design dimensional models using Star Schema principles
- Conduct Exploratory Data Analysis (EDA)
- Generate business-ready insights for decision-making

---

# 🏗️ Phase 1 — Data Warehousing

## Data Architecture

![Data Architecture](docs/data_architecture.png)

The project follows a Medallion Architecture consisting of:

### Bronze Layer
- Raw data ingestion from source systems
- Preserves source data in its original format
- Supports auditability and traceability

### Silver Layer
- Data cleansing and standardization
- Data quality validation
- Business rule implementation
- Data enrichment and transformation

### Gold Layer
- Business-ready analytical datasets
- Dimensional modeling
- Optimized reporting and analytics structures

---

## 🔄 Data Flow

![Data Flow](docs/data_flow.png)

### ETL / ELT Workflow

1. Extract data from CRM and ERP source systems
2. Load raw data into Bronze Layer
3. Cleanse and standardize data in Silver Layer
4. Integrate business entities across systems
5. Create dimensional models in Gold Layer
6. Deliver analytics-ready datasets

---

## ⭐ Data Model

![Star Schema](docs/data_model.png)

The Gold Layer is designed using a Star Schema model optimized for analytical reporting.

### Fact Table
- Fact Sales

### Dimension Tables
- Dim Customer
- Dim Product
- Dim Date

This structure enables high-performance analytical querying and reporting.

---

## ⚙️ Data Engineering Components

### Data Architecture Design
- Medallion Architecture
- Layered Data Processing
- Separation of Concerns

### ETL / ELT Processing
- Data Extraction
- Data Loading
- Data Transformation

### Data Cleansing
- Duplicate Handling
- Missing Value Treatment
- Data Standardization
- Business Rule Validation

### Data Integration
- CRM + ERP Integration
- Business Key Reconciliation
- Master Data Alignment

### Data Modeling
- Dimensional Modeling
- Fact & Dimension Design
- Star Schema Implementation

---

# 📊 Phase 2 — Exploratory Data Analysis (EDA)

After building the Data Warehouse and Gold Layer, the next phase focused on analyzing curated business-ready data to uncover patterns, trends, and actionable insights.

## EDA Framework

![EDA Roadmap](docs/eda_roadmap.png)

---

## 1️⃣ Database Exploration

Objectives:
- Understand database structure
- Explore tables and schemas
- Validate dataset readiness

Deliverables:
- Database inventory
- Table overview
- Record counts

---

## 2️⃣ Dimensions Exploration

Analyzed business dimensions including:

### Customer Dimension
- Customer Distribution
- Geographic Analysis

### Product Dimension
- Product Categories
- Product Subcategories

Techniques:
- DISTINCT Analysis
- Category Exploration
- Data Profiling

---

## 3️⃣ Date Exploration

Analyzed temporal coverage of data.

Metrics:
- Earliest Transaction Date
- Latest Transaction Date
- Historical Coverage Period

---

## 4️⃣ Measures Exploration

Analyzed key business metrics:

- Total Sales
- Total Orders
- Quantity Sold
- Average Selling Price

SQL Functions Used:
- SUM()
- AVG()
- COUNT()

---

## 5️⃣ Magnitude Analysis

Business performance across dimensions:

Examples:
- Sales by Product Category
- Revenue by Customer
- Orders by Region
- Quantity by Product

---

## 6️⃣ Ranking Analysis

Top and Bottom Performer Identification

Examples:

### Customers
- Top Revenue Customers
- Bottom Revenue Customers

### Products
- Best-Selling Products
- Lowest Performing Products

SQL Concepts:
- RANK()
- DENSE_RANK()
- ROW_NUMBER()

---

## 7️⃣ Change Over Time Analysis

Trend analysis including:

- Monthly Sales Trends
- Revenue Growth
- Seasonal Performance

---

## 8️⃣ Cumulative Analysis

Running calculations:

- Running Revenue
- Running Orders
- Cumulative Performance Tracking

---

## 9️⃣ Performance Analysis

Business performance evaluation:

- Product Performance
- Customer Performance
- Revenue Contribution

---

## 🔟 Data Segmentation

Customer and Product Segmentation

Examples:
- High Value Customers
- Medium Value Customers
- Low Value Customers

---

## 1️⃣1️⃣ Part-to-Whole Analysis

Contribution Analysis

Examples:
- Category Contribution %
- Product Contribution %
- Customer Revenue Share %

---

## 1️⃣2️⃣ Customer Report

Customer-focused business report including:

- Revenue
- Orders
- Purchase Behavior
- Customer Ranking

---

## 1️⃣3️⃣ Product Report

Product-focused business report including:

- Revenue
- Sales Volume
- Product Ranking
- Category Performance

---

# 📈 Sample Business Insights

### Customer Insights
- Identify top revenue-generating customers
- Analyze customer contribution to total revenue
- Segment customers by value

### Product Insights
- Best-performing products
- Underperforming products
- Revenue contribution by category

### Sales Insights
- Revenue trends over time
- Seasonal sales patterns
- Growth opportunities

---

# 🛠️ Technology Stack & Environment Setup

## Hardware

- Apple MacBook Air (M-Series)
- macOS

---

## Development Environment

- Visual Studio Code (VS Code)
- SQL Server Extension for VS Code
- Git
- GitHub

---

## Database Environment

- Microsoft SQL Server
- SQL Server Database Engine
- SQL Server running in Docker Container

---

## Containerization

- Docker Desktop
- Containerized SQL Server Environment

---

## Data Engineering Technologies

- SQL
- ETL / ELT
- Data Warehousing
- Data Integration
- Data Cleansing
- Data Validation
- Data Modeling
- Dimensional Modeling
- Star Schema Design

---

## Documentation & Collaboration

- Draw.io
- Notion
- Markdown
- GitHub

---

# 🎯 Skills Demonstrated

### Data Engineering
- Data Warehousing
- ETL / ELT Development
- Data Integration
- Data Architecture

### SQL Development
- Joins
- CTEs
- Window Functions
- Stored Procedures
- Query Optimization

### Data Modeling
- Star Schema
- Fact & Dimension Modeling

### Analytics
- Exploratory Data Analysis
- Trend Analysis
- Segmentation
- Business Reporting

### Professional Skills
- Documentation
- Version Control
- Problem Solving

---

# 📂 Repository Structure

```text
SQL-Project-1-Data-Warehousing/
│
├── datasets/
│
├── docs/
│   ├── data_architecture.png
│   ├── data_flow.png
│   ├── data_model.png
│   ├── eda_roadmap.png
│
├── scripts/
│   ├── bronze/
│   ├── silver/
│   └── gold/
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

# 👨‍💼 About Me

**Varun Gautam**

MBA (Human Resource Management), IIM Ranchi

HR Professional | Data Analytics Enthusiast | SQL Developer

I am passionate about combining business understanding with analytical capabilities to solve real-world business problems through data-driven decision-making.

---

# 📬 Connect With Me

📧 Email: i.am.varungautam@gmail.com

💼 LinkedIn: https://www.linkedin.com/in/iamvarungautam/

💻 GitHub: https://github.com/iamvarungautam

---

⭐ If you found this project useful, feel free to connect with me and explore my other projects.
