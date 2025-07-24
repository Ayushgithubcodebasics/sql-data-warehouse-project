# Modern SQL Data Warehouse for Sales Analytics

A comprehensive, end-to-end data warehousing project that demonstrates the process of building a modern data warehouse from scratch using SQL Server. This repository showcases best practices in data architecture, ETL development, data modeling, and data cleansing, making it an ideal portfolio project for data professionals.

---

## 📖 Table of Contents
- [Project Goal](#-project-goal)
- [Key Concepts & Skills Demonstrated](#-key-concepts--skills-demonstrated)
- [Data Architecture](#-data-architecture)
- [Data Model (Star Schema)](#-data-model-star-schema)
- [Technology Stack](#-technology-stack)
- [Contact](#-contact)

---

## 🎯 Project Goal

The primary objective of this project is to develop a robust and scalable data warehouse that consolidates sales and customer data from two disparate source systems: **ERP** and **CRM**. The final data warehouse provides a single source of truth, enabling efficient analytical reporting and informed business decision-making.

The project involves:
1.  **Designing** a modern, layered data architecture.
2.  **Developing** ETL (Extract, Transform, Load) pipelines to ingest, clean, and integrate data.
3.  **Modeling** the data into a user-friendly Star Schema optimized for analytics.
4.  **Documenting** the entire process, from data lineage to the final data model.

---

## ✨ Key Concepts & Skills Demonstrated

This project covers a wide range of essential skills in the data engineering and analytics domain:

-   **Data Architecture**: Implementation of the **Medallion Architecture** (Bronze, Silver, Gold layers) to ensure data quality and progressive refinement.
-   **ETL Development**:
    -   **Extract**: Bulk inserting data from flat files (`.csv`) into the data warehouse.
    -   **Transform**: Performing extensive data transformations, including:
        -   **Data Cleansing**: Handling `NULL`s, duplicates, invalid values, and unwanted spaces.
        -   **Data Standardization & Normalization**: Mapping coded values to user-friendly descriptions (e.g., 'M' to 'Male').
        -   **Data Integration**: Combining data from multiple source systems into a unified view.
        -   **Derived Columns & Business Logic**: Creating new columns and applying business rules.
    -   **Load**: Using Stored Procedures for batch processing with full load patterns (Truncate & Insert).
-   **Advanced SQL**: Utilizing Window Functions, CTEs (Common Table Expressions), and complex `JOIN`s.
-   **Data Modeling**: Designing and implementing a **Star Schema** with Fact and Dimension tables, ideal for BI and reporting tools.
-   **Database Design**: Creating tables, views, schemas, and stored procedures.
-   **Project Management**: Following a structured project plan with clear phases and tasks.

---

## 🏗️ Data Architecture

This project implements the **Medallion Architecture**, a modern data design pattern that logically organizes data into three distinct layers. This approach ensures that data is progressively cleaned, refined, and modeled as it flows through the system.

<img width="6235" height="3216" alt="data_architecture" src="https://github.com/user-attachments/assets/f2f81de6-86c9-4fdc-ad96-1937edf75637" />

### 🥉 Bronze Layer (Raw Data)
-   **Purpose**: Serves as the initial landing zone for raw data from source systems. The data is stored "as-is" with no transformations.
-   **Objects**: Tables.
-   **Key Benefit**: Provides a historical archive of source data, enabling traceability and the ability to rebuild subsequent layers without re-extracting from the source.

### 🥈 Silver Layer (Cleansed & Standardized Data)
-   **Purpose**: Data from the Bronze layer is cleaned, conformed, and standardized. This is where data quality issues are addressed.
-   **Objects**: Tables.
-   **Key Benefit**: Provides a clean, reliable dataset for data analysts and data scientists to perform exploratory analysis.

### 🥇 Gold Layer (Business-Ready Data)
-   **Purpose**: Data is transformed into a business-centric model, ready for consumption by BI tools and analysts. This layer features the final, integrated data model.
-   **Objects**: Views.
-   **Data Model**: Star Schema.
-   **Key Benefit**: Delivers a highly performant, easy-to-understand data model that directly supports business reporting and analytics use cases.

---

## ⭐ Data Model (Star Schema)

The Gold layer is modeled as a **Star Schema**, which is optimized for querying and BI analytics. It consists of one central fact table surrounded by two dimension tables.

<img width="6033" height="2249" alt="data_model" src="https://github.com/user-attachments/assets/83c3a04c-5b19-4754-8fd5-9b73d7467aa6" />

-   **`fact_sales`**: Contains quantitative transactional data (the "facts"), such as sales amount and quantity. It includes foreign keys to the dimension tables.
-   **`dim_customers` & `dim_products`**: Contain descriptive attributes (the "dimensions") about customers and products, respectively. They provide the context for the facts.

---

## 💻 Technology Stack
-   **Database**: Microsoft SQL Server
-   **IDE**: SQL Server Management Studio (SSMS)
-   **Version Control**: Git & GitHub
-   **Documentation**: Markdown
---

## 📞 Contact
Mail - [ayushbutoliya22@gmail.com](mailto:ayushbutoliya22@gmail.com)

Project Link: [https://github.com/your-username/sql-data-warehouse-project](https://github.com/Ayushgithubcodebasics/sql-data-warehouse-project.git)
