# Manufacturing Downtime Analysis  
**From raw machine sensor data to operational insight and predictive maintenance readiness**

## Overview

Unplanned downtime is one of the most expensive problems in manufacturing. It disrupts production schedules, increases maintenance costs, reduces equipment availability, and can quietly erode operational efficiency over time.

This project analyzes a raw manufacturing downtime dataset containing machine identifiers, assembly lines, timestamps, and multiple process/sensor measurements. The goal is to move beyond simple reporting and build a complete analytics workflow that:

- cleans and standardizes messy operational data,
- identifies the conditions associated with machine failure,
- surfaces business-relevant insights for maintenance and production teams,
- and prepares the data for predictive maintenance use cases.

Rather than treating this as a basic EDA exercise, the project is designed as a real business analytics case: **What patterns drive machine failure, which assets are most at risk, and how can operations act earlier?**

---

## Problem Statement

Manufacturing environments generate large volumes of machine and process data, but raw data alone does not reduce downtime. To be useful, it must be transformed into structured information that can answer operational questions such as:

- Which machines fail most often?
- Which production lines are riskier?
- Are there measurable warning signals before failure?
- What operating conditions appear unsafe?
- Can machine failure be predicted early enough to support preventive action?

This project addresses those questions by combining data cleaning, exploratory analysis, KPI design, visualization, and predictive modeling preparation.

---

## Objectives

The main objectives of this project are to:

1. **Clean and standardize** the raw manufacturing dataset.
2. **Build a clear analytical structure** through a data dictionary and business logic.
3. **Measure downtime patterns** across machines, assembly lines, and time.
4. **Identify the variables most strongly associated with machine failure.**
5. **Design dashboards** that communicate insights to operational stakeholders.
6. **Prepare the dataset for predictive maintenance modeling.**

---

## Dataset Summary

The dataset contains observations related to manufacturing equipment, including:

- **Date**
- **Machine ID**
- **Assembly Line**
- **Hydraulic Pressure**
- **Coolant Pressure**
- **Air System Pressure**
- **Coolant Temperature**
- **Hydraulic Oil Temperature**
- **Spindle Bearing Temperature**
- **Spindle Vibration**
- **Tool Vibration**
- **Spindle Speed**
- **Voltage**
- **Torque**
- **Cutting Force**
- **Downtime Status** (`Machine Failure` / `No Machine Failure`)

This is a **raw dataset**, which means it includes real-world data quality issues such as:

- inconsistent machine and line naming,
- mixed text formatting,
- duplicate records,
- missing values,
- invalid placeholder values,
- mixed date formats,
- inconsistent target labels.

These issues make the project more realistic and better suited for demonstrating practical data analysis skills.

---

## Analytical Focus

This project is built around two core ideas:

### 1. Downtime understanding
Understand how machine failure is distributed across assets, lines, and time, and determine which operational conditions are most associated with failure.

### 2. Downtime prevention
Use sensor and process measurements to identify patterns that could support earlier intervention, preventive maintenance, and future failure prediction systems.

---

## Key Business Questions

The analysis is designed to answer questions that matter in real manufacturing operations:

- Which machine has the highest failure rate?
- Which assembly line is associated with the most failures?
- Do failure patterns change over time?
- Which sensor readings differ most between failure and non-failure cases?
- Are pressure, temperature, vibration, or load useful early warning indicators?
- Are all machines failing under similar conditions, or does each machine show a different risk pattern?
- Can safe operating ranges be inferred from the data?
- Is the dataset strong enough to support a predictive maintenance model?

---

## Project Scope

This repository covers the full analytics workflow:

- raw data assessment
- data cleaning and standardization
- exploratory data analysis
- business KPI generation
- dashboard design
- modeling preparation

The project is intentionally structured to reflect how a real analyst would approach an industrial operations problem, not just how a student would complete an assignment.

---

## Tools & Technologies

This project can be developed using the following stack:

- **Python** — data cleaning, EDA, feature engineering, and modeling
- **SQL** — structured querying, KPI generation, and analysis-ready tables
- **Excel** — quick validation, pivoting, and business-friendly checks
- **Power BI** — interactive dashboards and stakeholder reporting
- **Tableau** — visual storytelling and operational analytics

---

## Proposed Workflow

### 1. Data Cleaning & Preparation
The first stage focuses on converting the raw dataset into an analysis-ready one.

Tasks include:

- standardizing column names,
- cleaning categorical text fields,
- unifying machine IDs and assembly line names,
- handling missing values and invalid placeholders,
- converting numeric fields to proper types,
- parsing dates,
- removing duplicate records.

### 2. Exploratory Data Analysis
Once cleaned, the data is explored to understand patterns in machine failure.

This includes:

- failure vs. non-failure comparisons,
- machine-level and line-level failure analysis,
- trend analysis over time,
- distribution analysis of sensor variables,
- relationship and correlation analysis between operational indicators.

### 3. Business Insight Generation
This stage translates technical findings into business language.

Examples:

- identifying risky machines,
- flagging abnormal conditions,
- highlighting variables most associated with downtime,
- defining candidate thresholds for monitoring.

### 4. Dashboard Development
Interactive dashboards are designed for both executive and operational users.

Planned dashboard sections include:

- executive overview,
- machine performance,
- downtime trends,
- sensor diagnostics,
- data quality monitoring.

### 5. Predictive Maintenance Readiness
The final stage prepares the dataset for supervised learning use cases such as failure classification and risk scoring.

Potential techniques include:

- logistic regression,
- decision trees,
- random forest,
- gradient boosting.

The goal is not only to predict failure, but to explain which conditions increase failure risk.

---

## Expected Deliverables

This repository is intended to produce:

- a cleaned and standardized dataset,
- a documented data dictionary,
- exploratory analysis notebooks,
- SQL queries for KPI extraction,
- dashboards in Power BI or Tableau,
- and a predictive-maintenance-ready analysis dataset.

---

## Repository Structure

```bash
manufacturing-downtime-analysis/
│
├── data/
│   ├── raw/              # Original dataset
│   └── cleaned/          # Cleaned and analysis-ready data
│
├── notebooks/
│   ├── 01_data_cleaning.ipynb
│   ├── 02_exploratory_analysis.ipynb
│   └── 03_modeling_preparation.ipynb
│
├── sql/
│   └── downtime_kpis.sql
│
├── dashboards/
│   ├── powerbi/
│   └── tableau/
│
├── reports/
│   └── findings_summary.md
│
├── images/
│   └── dashboard_screenshots/
│
└── README.md
