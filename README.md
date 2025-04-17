#  📉 Stock Market Crash Analysis with Python

This project is a comprehensive stock market crash analysis tool that uses historical Sensex data and synthetic data to identify, visualize, and understand major market downturns. It combines data processing, drawdown analysis, crash clustering, and synthetic forecasting to give insights into past and potential future crashes.

## 📊 Project Workflow & Code Explanation

### 1. **Importing Libraries**
Used `pandas`, `numpy`, and `plotly` for data manipulation, calculation, and interactive visualizations.

### 2. **Loading the Data**
The CSV file is loaded using `pandas.read_csv()`, sorted by date, and indexed by the `Date` column for time-series analysis.

### 3. **Data Cleaning**
- Converts `Date` to datetime.
- Checks for and handles missing values.

### 4. **Daily Returns and Crash Detection**
- Calculates daily percentage return using `.pct_change()`.
- Flags a crash if the daily return is less than or equal to -5%.
- Plots closing prices and highlights crash days with red dots.

### 5. **Drawdown Analysis**
- Calculates drawdown as the percentage decline from the all-time high using `.cummax()`.
- A drawdown greater than 20% is considered a major crash.
- Interactive plot shows drawdown over time with a threshold line.

### 6. **Crash Clustering**
- Groups crash days into clusters if they occur within 3 days of each other.
- Displays the start and end dates of each cluster.
- Plots zoomed-in analysis of the first detected crash cluster.

### 7. **Historical Crash Case Studies**
Three major crashes are explored in detail:
- 1997 Crash
- 2008 Financial Crisis
- 2020 COVID-19 Crash

Each crash is visualized through:
- Closing price with crash period shaded
- Daily returns during the crash

### 8. **Synthetic Crash Forecasting (2025 Simulation)**
- Simulates 250 trading days in 2025 using `numpy`.
- Introduces artificial stable, crash, and recovery periods.
- Calculates 10-day rolling mean and volatility.
- Flags early warnings when:
  - Rolling mean return < -0.5%
  - Volatility > 2%
- Visualizes price with early warnings marked.

## 🛍️ Summary of Insights

- **Daily Crashes**: Several points in history showed -5% or more daily declines.
- **Drawdowns**: Major drawdowns beyond -20% identified big market events.
- **Clustering**: Many crashes grouped into clusters, highlighting multi-day panic events.
- **Case Studies**: Visual analysis of the 1997, 2008, and 2020 crashes shows steep and prolonged declines.
- **2025 Simulation**: Showed how early warning indicators can signal upcoming crashes using volatility and return drops.

---
