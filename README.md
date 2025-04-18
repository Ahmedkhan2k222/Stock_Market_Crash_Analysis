# 📉 Stock Market Crash Analysis

This project performs an in-depth analysis of stock market crashes using historical Sensex data. It includes identification of daily crashes, drawdown-based crashes, visualization of major market declines, and synthetic modeling for early warning signals.

---

## 📁 Dataset
- File used: `cleaned_sensex.csv`
- Contains historical Sensex data with date and closing prices.

---

## 🔍 Key Features & Workflow

### 1. **Preprocessing**
- Read data with `pandas`.
- Convert `Date` column to datetime format.
- Sort by date and set as index.

### 2. **Daily Crash Detection**
- Calculate daily return %.
- Identify crash days where drop > 5%.
- Visualize with red markers.

### 3. **Drawdown Analysis**
- Calculate cumulative max.
- Compute % drawdown from peak.
- Mark drawdowns below -20%.
- Visualize drawdowns over time.

### 4. **Crash Cluster Detection**
- Group consecutive drawdown days within 3-day gaps.
- Print identified clusters with start-end dates.
- Visualize zoomed-in view for selected cluster.

### 5. **Major Historical Crashes**
Visualizations for:
- 📉 1997 Crash
- 📉 2008-09 Global Financial Crisis
- 📉 2020 COVID Crash

Each includes:
- Closing prices
- Daily returns

### 6. **Synthetic Early Warning System (2025)**
- Create synthetic Sensex data for 2025 with a simulated crash.
- Compute 10-day rolling mean and volatility.
- Flag early warnings where:
  - Mean return < -0.5%
  - Volatility > 2%

### 7. **📊 Monthly Visualization of 2025**
- Each of the 12 months from January to December 2025 is analyzed separately.
- For every month, a dedicated graph is created to visualize the closing price trends.
- Red dots are used to clearly mark early warning signals detected within that month.
- This approach gives a more detailed view of how market behavior evolves throughout the year and helps identify patterns specific to individual months.

---

## 📦 Libraries Used
- pandas
- numpy
- plotly
- calendar

---

## 📈 Summary
This project allows you to:
- Detect both short-term (daily) and long-term (drawdown) crashes.
- Analyze real market behavior across historical and simulated data.
- Generate early warning signals based on market behavior.
- Visualize everything using interactive Plotly charts, including monthly-level insights for 2025.

> Great for financial analysts, students, and data scientists interested in market behavior.

---

