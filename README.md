# 🚀 SQL Data Warehouse & Analytics Project

## 📌 Project Overview

This project demonstrates the design and implementation of a modern **Data Warehouse and Analytics Solution** using Microsoft SQL Server. The objective was to build an end-to-end data warehousing pipeline capable of integrating data from multiple business systems, transforming raw data into trusted business information, and delivering analytics-ready datasets for reporting and decision-making.

The solution follows the **Medallion Architecture (Bronze → Silver → Gold)** framework and showcases industry-standard practices in Data Engineering, Data Modeling, Data Quality Management, and Analytics.

---

## 🏗️ Data Architecture

<p align="center">
  <img src="docs/data_architecture.png" width="900">
</p>

The project follows a layered Medallion Architecture:

### Bronze Layer

* Raw data ingestion from source systems
* Preserves source data in its original format
* Supports auditability and traceability

### Silver Layer

* Data cleansing and standardization
* Data quality validation
* Business rule implementation
* Data enrichment and transformation

### Gold Layer

* Business-ready analytical datasets
* Dimensional modeling
* Optimized reporting and analytics structures

This architecture ensures scalability, maintainability, and clear separation of responsibilities across the data pipeline.

---

## 🔄 Data Flow

<p align="center">
  <img src="docs/data_flow.png" width="900">
</p>

The data pipeline integrates CRM and ERP datasets through a structured ETL/ELT workflow:

1. Data Extraction from source systems
2. Raw Data Loading into Bronze Layer
3. Data Cleansing & Transformation in Silver Layer
4. Data Integration & Modeling
5. Creation of Analytics-Ready Gold Layer
6. Business Reporting & Insights

---

## ⭐ Data Model (Star Schema)

<p align="center">
  <img src="docs/data_model.png" width="900">
</p>

The Gold Layer is designed using a **Star Schema** model to support analytical reporting and high-performance querying.

### Fact Table

* Fact Sales

### Dimension Tables

* Dim Customer
* Dim Product
* Dim Date

This dimensional model enables efficient reporting on customer behavior, product performance, and sales trends.

---

# 🎯 Project Objectives

The primary objectives of this project were:

* Build a scalable Data Warehouse using SQL Server
* Integrate CRM and ERP datasets into a unified analytical model
* Implement ETL/ELT pipelines for data processing
* Perform data cleansing and quality validation
* Design dimensional models using Star Schema principles
* Generate business-ready datasets for analytics and reporting

---

# ⚙️ Key Components

## 1. Data Architecture Design

Designed a Medallion Architecture consisting of Bronze, Silver, and Gold layers to support data ingestion, transformation, and analytics.

---

## 2. ETL / ELT Pipeline Development

Developed SQL-based ETL/ELT processes to:

* Extract data from source systems
* Load raw datasets into staging environments
* Cleanse and standardize business data
* Integrate data across systems
* Build analytical models

---

## 3. Data Quality Management

Implemented:

* Duplicate handling
* Missing value treatment
* Data validation
* Standardization rules
* Data enrichment
* Business rule enforcement

These processes improved the reliability and consistency of analytical outputs.

---

## 4. Data Integration

Integrated customer, product, and sales information from multiple systems by:

* Reconciling business keys
* Mapping source entities
* Aligning master data
* Consolidating datasets

Resulting in a centralized and trusted source of business information.

---

## 5. Dimensional Modeling

Designed analytical structures using:

* Fact Tables
* Dimension Tables
* Star Schema Design

Optimized for reporting and business intelligence use cases.

---

## 6. Analytics & Reporting

Generated SQL-based analytical insights related to:

* Customer Behavior
* Product Performance
* Sales Trends
* Revenue Analysis
* Business KPIs

The final Gold Layer delivers analytics-ready datasets that can be consumed by reporting and visualization tools.

---

# 🛠️ Technology Stack & Environment Setup

## Hardware

* Apple MacBook Air (M-Series)
* macOS

---

## Development Environment

* Visual Studio Code (VS Code)
* SQL Server Extension for VS Code
* Git
* GitHub

---

## Database Environment

* Microsoft SQL Server
* SQL Server Database Engine
* SQL Server running in Docker Container
* Relational Database Management System (RDBMS)

---

## Containerization & Infrastructure

* Docker Desktop
* Containerized SQL Server Environment
* Local Development Environment

---

## Data Engineering Technologies

* SQL
* ETL / ELT Processing
* Data Warehousing
* Data Architecture
* Data Integration
* Data Transformation
* Data Cleansing
* Data Validation
* Data Quality Management
* Data Modeling
* Dimensional Modeling
* Star Schema Design

---

## Data Sources

* CRM Dataset
* ERP Dataset
* CSV Files

---

## Documentation & Collaboration Tools

* Draw.io
* Notion
* Markdown
* GitHub

---

# 🎯 Skills Demonstrated

### Data Engineering

* Data Warehousing
* ETL / ELT Development
* Data Integration
* Data Architecture
* Data Transformation

### SQL Development

* Stored Procedures
* Joins
* CTEs
* Window Functions
* Data Validation
* Query Optimization

### Data Modeling

* Dimensional Modeling
* Star Schema Design
* Fact & Dimension Modeling

### Analytics

* Business Analytics
* KPI Development
* Trend Analysis
* Performance Analysis

### Professional Skills

* Documentation
* Version Control
* Project Structuring
* Problem Solving

---

# 📂 Repository Structure

```text
data-warehouse-project/
│
├── datasets/
│
├── docs/
│   ├── data_architecture.png
│   ├── data_flow.png
│   ├── data_model.png
│   ├── data_catalog.md
│   └── naming_conventions.md
│
├── scripts/
│   ├── bronze/
│   ├── silver/
│   └── gold/
│
├── tests/
│
├── README.md
├── LICENSE
└── .gitignore
```

---

# 🌱 Career Objective

My long-term objective is to build expertise at the intersection of **Business, Human Resources, Analytics, and Technology**.

As an MBA graduate from IIM Ranchi and a professional currently working with DS Group, I am particularly interested in leveraging data to improve decision-making, optimize business processes, and drive organizational performance.

Areas of interest include:

* HR Analytics
* People Analytics
* Workforce Analytics
* Business Analytics
* Data Analytics
* Business Intelligence
* Consulting
* Data-Driven HR Strategy

Projects like this help me strengthen both technical and analytical capabilities while applying business understanding to real-world problems.

---

# 👨‍💼 About Me

**Varun Gautam**

MBA (Human Resource Management) | IIM Ranchi

HR Professional | Data Analytics Enthusiast | SQL Developer

---

# 📬 Connect With Me

📧 Email: [i.am.varungautam@gmail.com](mailto:i.am.varungautam@gmail.com)

💼 LinkedIn: https://www.linkedin.com/in/iamvarungautam/

💻 GitHub: https://github.com/iamvarungautam

---

# 📁 Project Resources

### Architecture & Design

* Data Architecture Diagram:
  https://github.com/iamvarungautam/SQL-Project-1---Data-Warehousing-/blob/main/docs/data_architecture.png

* Data Flow Diagram:
  https://github.com/iamvarungautam/SQL-Project-1---Data-Warehousing-/blob/main/docs/data_flow.png

* Data Model (Star Schema):
  https://github.com/iamvarungautam/SQL-Project-1---Data-Warehousing-/blob/main/docs/data_model.png

### Documentation

* ETL Documentation:
  https://github.com/iamvarungautam/SQL-Project-1---Data-Warehousing-/blob/main/docs/naming_conventions.md

### Dataset

* Dataset Source:
  https://github.com/iamvarungautam/SQL-Project-1---Data-Warehousing-/tree/main/datasets

---

## ⭐ If you found this project useful, feel free to star the repository and connect with me on LinkedIn.
