# 📊 E-Challan Daily Data Analysis

This repository contains Python scripts for analyzing **daily e-challan data** using `pandas` and `numpy`. The goal is to explore traffic challan records, compute meaningful ratios, detect outliers, and summarize key insights such as revenue, disposal rates, and growth trends.

---
## COLAB --> [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/17yY_7bIJvFJpNVGXpI9CerrGvWx8JTgY?usp=sharing)

## 🚀 Features

- **Data Cleaning & Preprocessing**
  - Load CSV data (`echallan_daily_data.csv`)
  - Convert date column to `datetime`
  - Handle missing values and duplicates

- **Feature Engineering**
  - Extract `year` from date
  - Create custom flags (`Free Kardo`)
  - Compute ratios:
    - `disposed ratio` = disposedAmount / totalChallan
    - `Collection Rate` = disposedAmount / totalAmount
    - `pending_ratio` = pendingChallan / disposedChallan
    - `Court ratio` = (totalCourt / totalChallan) × 100
    - `court_disposal_rate` = disposedCourt / totalCourt
  - Calculate `avg_fine` per challan
  - Track cumulative challans (`Cumulative_challan`)
  - Compute growth rate of challans (`pct_change`)

- **Statistical Analysis**
  - Correlation matrix between key variables
  - Outlier detection using **3σ rule**
  - Cumulative sums and conditional counts

- **Summary Metrics**
  - Total challans issued
  - Total revenue collected
  - Average daily challans
  - Maximum revenue day

---

## 📂 Project Structure

```
├── echallan_daily_data.csv   # Input dataset
├── analysis.py               # Main analysis script
├── README.md                 # Documentation
```

---

## 🛠️ Requirements

- Python 3.8+
- Libraries:
  - `numpy`
  - `pandas`

Install dependencies:

```bash
pip install numpy pandas
```

---

## 📈 Example Outputs

- **Correlation Matrix** between challans, pending challans, amount, and court cases.
- **Growth Rate** of challans over time.
- **Outliers** detected in total challans.
- **Summary Report**:

```python
{
    "Total Challans": 1234567,
    "Total Revenue": 987654321,
    "Avg Daily Challan": 4567.89,
    "Max Revenue Day": 123456
}
```

---

## 🔍 Insights

- Disposal and collection rates help measure **efficiency of challan resolution**.
- Pending vs disposed ratios highlight **backlog trends**.
- Court-related metrics show **judicial involvement** in challan disposal.
- Growth rate analysis identifies **spikes or drops** in enforcement activity.
- Outlier detection flags **unusual challan counts** for deeper investigation.
