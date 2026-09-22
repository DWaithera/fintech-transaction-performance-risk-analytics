# 💳 Fintech Transaction Performance & Risk Analytics

> **Business analytics on synthetic mobile-money transactions — turning transaction data into insights on performance, customer behavior, and financial risk.**

**Python · SQL · DuckDB · Power BI · Pandas · Jupyter**

---

## 📌 Project Overview

Financial transaction platforms generate millions of transactions, but raw transaction data does not directly answer business questions.

This project analyzes a synthetic mobile-money transaction dataset to investigate:

* **Transaction performance** — volume, value, transaction mix, and trends
* **Customer behavior** — transaction patterns and customer activity
* **Risk & fraud** — suspicious transaction patterns and fraud exposure
* **Business KPIs** — metrics that can support operational monitoring and decision-making
* **Data quality** — validation of transaction and balance data before analytical use

The end product will combine **Python-based analysis, SQL transformations, DuckDB analytics, and an interactive Power BI dashboard.**

---

## 🎯 Business Questions

| Area                  | Key Questions                                                      |
| --------------------- | ------------------------------------------------------------------ |
| **Performance**       | How much transaction value and volume flows through the platform?  |
| **Transaction Mix**   | Which transaction types drive activity and value?                  |
| **Customer Behavior** | How do customers transact across the platform?                     |
| **Risk**              | What transaction patterns are associated with fraudulent activity? |
| **Operations**        | When and where does transaction activity concentrate?              |
| **Decision Support**  | Which KPIs should management monitor regularly?                    |

---

## 📊 Dataset

### PaySim — Financial Mobile Money Simulator

**Source:** [Kaggle — PaySim](https://www.kaggle.com/datasets/ealaxi/paysim1)

PaySim is a **synthetic financial dataset** that simulates mobile-money transactions based on patterns observed in African mobile-money activity.

The dataset contains transaction-level information including:

* Transaction type
* Transaction amount
* Originating customer
* Destination customer
* Customer balances
* Fraud indicators
* Transaction time step

> ⚠️ **Data note:** PaySim is synthetic. Findings from this project should therefore be interpreted as analytical patterns within the simulation, not as direct measurements of real-world mobile-money behavior.

### Data handling

Raw transaction data is stored locally in:

```text
data/raw/
```

Raw CSV files are intentionally excluded from Git because of their size.

---

## 🏗️ Project Architecture

```text
                    ┌─────────────────────┐
                    │      PaySim Data    │
                    │   Synthetic Raw CSV │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   Data Profiling    │
                    │      Python         │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Data Quality &      │
                    │ Validation          │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ SQL / DuckDB        │
                    │ Analytical Models   │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Business KPIs       │
                    │ & Risk Analytics    │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │    Power BI         │
                    │ Executive Dashboard │
                    └─────────────────────┘
```

---

## 🛠️ Technology Stack

| Layer                     | Technology                    |
| ------------------------- | ----------------------------- |
| **Data Analysis**         | Python, Pandas, NumPy         |
| **Exploration**           | Jupyter Notebook              |
| **Analytics Engineering** | SQL, DuckDB                   |
| **Visualization**         | Power BI, Matplotlib, Seaborn |
| **Version Control**       | Git, GitHub                   |

---

## 📁 Repository Structure

```text
fintech-transaction-performance-risk-analytics/
│
├── data/
│   ├── raw/                 # Original source data — not committed
│   └── processed/           # Clean analytical datasets
│
├── notebooks/
│   └── 01_data_profiling.ipynb
│
├── sql/                     # Analytical SQL models
│
├── dashboard/               # Power BI dashboard assets
│
├── docs/                    # Documentation & data dictionary
│
├── src/                     # Reusable Python transformation logic
│
├── README.md
├── requirements.txt
└── .gitignore
```

---

## 🔎 Analytical Workflow

### 01 — Data Profiling

Understand the structure and characteristics of the raw dataset.

**Outputs**

* Dataset dimensions
* Data types
* Transaction distributions
* Time coverage
* Missing-value analysis
* Duplicate analysis
* Initial data-quality observations

### 02 — Data Quality Validation

Validate assumptions and identify anomalies before analytical modeling.

### 03 — Transaction Performance

Develop KPIs covering:

* Transaction volume
* Transaction value
* Average transaction value
* Transaction-type mix
* Time-based activity

### 04 — Customer Behavior

Analyze:

* Customer activity
* Transaction frequency
* Transaction values
* Originator vs recipient behavior
* Customer concentration

### 05 — Risk & Fraud Analytics

Investigate:

* Fraud frequency
* Fraud transaction value
* Fraud by transaction type
* Temporal fraud patterns
* Suspicious transaction characteristics

### 06 — SQL & DuckDB Analytical Layer

Transform validated data into reusable analytical datasets.

### 07 — Power BI Dashboard

Build an interactive business dashboard for transaction performance and risk monitoring.

---

## 📈 Planned KPI Framework

| KPI Category                | Example Metrics                                                 |
| --------------------------- | --------------------------------------------------------------- |
| **Transaction Performance** | Transaction Count, Transaction Value, Average Transaction Value |
| **Customer Activity**       | Active Customers, Transactions per Customer                     |
| **Transaction Mix**         | Type Distribution, Value by Transaction Type                    |
| **Risk**                    | Fraud Rate, Fraud Value, Fraud by Transaction Type              |
| **Time**                    | Hourly/Step Activity, Transaction Trends                        |
| **Operational Monitoring**  | High-value Transactions, Anomalous Patterns                     |

---

## 🧠 Key Analytical Principle

> **Profile first. Validate second. Transform third. Analyze fourth. Visualize last.**

The project deliberately separates **data quality validation** from business analysis so that downstream insights are based on documented and reproducible assumptions.

---

## 🚧 Project Status

**Current Phase:** 🟡 Project Setup & Data Profiling

| Phase                          | Status         |
| ------------------------------ | -------------- |
| Repository Setup               | ✅ Complete     |
| Dataset Acquisition            | 🔄 In Progress |
| Data Profiling                 | ⏳ Pending      |
| Data Quality Validation        | ⏳ Pending      |
| SQL / DuckDB Modeling          | ⏳ Pending      |
| KPI Development                | ⏳ Pending      |
| Risk Analytics                 | ⏳ Pending      |
| Power BI Dashboard             | ⏳ Pending      |
| Final Business Recommendations | ⏳ Pending      |

---

## 📌 Portfolio Objective

This project demonstrates the ability to move from:

**Raw Data → Data Quality → Analytical Modeling → Business KPIs → Risk Insights → Decision Support**

rather than simply producing charts from a raw dataset.

---

## 👤 Author

**Damaris Waithera**

Analytics Engineer · Data Analyst · Business Analytics

[GitHub](https://github.com/DWaithera)
