# Telco CDR Analytics Dashboard

An end-to-end Business Intelligence (BI) project built with Power BI to transform raw telco Call Detail Records (CDR) into an interactive analytics dashboard for monitoring key performance indicators (KPIs), customer behavior, and churn analysis.

## 📊 Project Overview

This project demonstrates the full lifecycle of a BI solution:
- **Data Acquisition & Understanding:** Connected to a flat CDR table containing call, SMS, and data usage records.
- **Data Modeling:** Engineered a robust star schema with a central fact table (`FactCDR`) and related dimensions (`DimDate`, `DimTime`, `DimUserType`, `DimCallStatus`).
- **DAX & Measures:** Developed advanced measures for calculated KPIs like Churn Rate, ARPU, and MTD revenue.
- **Visualization:** Built an interactive report with pages for Executive Summary, Call Detail Analysis, and Churn Analysis.
- **Deployment & Security:** Published to Power BI Service and implemented Row-Level Security (RLS) for user-specific data access.

## 🚀 Features

- **Star Schema Data Model:** Optimized for performance and usability with slowly changing dimensions (Type 1).
- **Advanced DAX Formulas:** Time intelligence, churn analysis, and ratio calculations.
- **Dynamic Reporting:** Interactive filters, slicers, and tooltips for deep data exploration.
- **Row-Level Security (RLS):** Implemented security roles to control data access based on user profile.
- **End-to-End Documentation:** From project planning in Trello/Notion to deployment steps.

## 🗂️ Data Model

The solution uses a dimensional modeling approach:

See Project Docs

**Fact Table**
- `FactCDR`: Contains measured events (e.g., `call_duration`, `total_cost`, `data_usage_mb`, `sms_count`).

**Dimension Tables**
- `DimDate`: A full date table for time intelligence.
- `DimTime`: A time table for hourly/minute analysis.
- `DimUserType`: Contains user segments (e.g., 'Budget User', 'Premium User').
- `DimCallStatus`: Contains call outcomes (e.g., 'Answered', 'Busy').

## 📈 Key Metrics & KPIs

- **Total Revenue**
- **Total Calls & Average Call Duration**
- **Total Data Usage (GB)**
- **Distinct Customer Count**
- **Churn Rate** & **Churned Customers**
- **Average Revenue Per User (ARPU)**
- **Revenue Month-to-Date (MTD)**

## 🛠️ Built With

- **Microsoft Power BI Desktop** - Data modeling, DAX, and report development.
- **Power Query (M Language)** - ETL and data transformation.
- **Power BI Service** - Cloud deployment, sharing, and security.
- **Trello** - Project planning and task management.

## 📋 Project Steps

1.  **Planning:** Defined business questions and KPIs. Set up Trello/Notion for task tracking.
2.  **Data Modeling:**
    - Cleaned and transformed raw data in Power Query.
    - Created `DimDate` and `DimTime` tables using M code.
    - Established relationships in a star schema.
3.  **DAX:** Developed core and advanced measures for analysis.
4.  **Report Development:** Designed interactive visualizations and report pages.
5.  **Deployment:** Published to Power BI Service, configured RLS, and shared via an App.

## 🔒 Security

Row-Level Security (RLS) roles are configured to restrict data access:
- **Sales Role:** Can only view data for 'Premium Users'.
- **Network Admin Role:** Can view all data.


