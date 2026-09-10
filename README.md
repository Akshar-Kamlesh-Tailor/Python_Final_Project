# 📈 Stock Market Analyzer

A comprehensive Jupyter Notebook project for **downloading, exploring, analyzing, and visualizing** stock-market data using **yfinance**, **Pandas**, **NumPy**, **Matplotlib**, and **Seaborn**.

The analysis is divided into two clear parts:

1. **Part 1 — Single Company Analysis** — deep dive into one selected ticker  
2. **Part 2 — Multiple Company Analysis** — side-by-side comparison of several companies on price performance, returns, volatility, volume, and risk

> **Note:** An internet connection is required when the data-download cells are executed.  
> All charts are displayed in the notebook **and** saved as high-quality PNG files in the `charts/` folder.

---

## ✨ Features

### Part 1 — Single Company Analysis
- Select any ticker from a curated company list (AAPL, NVDA, MSFT, TSLA, AMZN, GOOGL)
- Download historical OHLCV data for a custom date range
- Explore dataset shape, head, dtypes, missing values, and descriptive statistics
- Engineer useful columns (Year, Month, Day, Daily Return, Price Change)
- Compute key metrics (average open/close, max/min prices, volume, daily return & volatility)
- Year-wise performance summary (start/end close, average volume, yearly return %)
- Visualizations:
  - Closing price over time
  - Trading volume over time
  - Daily return distribution (with KDE)
  - Closing price with 20-day & 50-day moving averages
  - Yearly returns bar chart

### Part 2 — Multiple Company Analysis
- Select multiple tickers for comparison
- Download aligned Close prices for all selected companies
- Normalized price performance (start = 100)
- Total return, average daily return, volatility, and average volume comparison
- Correlation heatmap of daily returns
- Risk–return scatter plot

---

## 🛠️ Tech Stack

- **Python 3**
- **yfinance** — live market data download
- **Pandas** — data manipulation, cleaning, and aggregation
- **NumPy** — numerical calculations
- **Matplotlib** + **Seaborn** — professional charts
- **Jupyter Notebook** — interactive analysis environment

---

## 🧠 Skills Demonstrated

| Concept                        | Implementation                                      |
|--------------------------------|-----------------------------------------------------|
| **API Data Fetching**          | `yfinance` for historical OHLCV data                |
| **Data Cleaning & Preparation**| MultiIndex flattening, datetime handling, feature engineering |
| **Exploratory Data Analysis**  | Shape, head, dtypes, missing values, describe       |
| **Financial Metrics**          | Daily returns, volatility, total return, yearly returns |
| **Time-Series Visualization**  | Price trends, volume, moving averages               |
| **Comparative Analysis**       | Normalized performance, correlation, risk-return    |
| **Reproducible Workflow**      | Hard-coded defaults, clear sectioning, saved charts |

---

## 📊 Workflow

```mermaid
flowchart TD
    A([Start]) --> B[Import Libraries]
    B --> C[Company List]
    
    C --> D[PART 1 — Single Company]
    D --> D1[Select Ticker & Date Range]
    D1 --> D2[Download OHLCV Data]
    D2 --> D3[Explore & Prepare]
    D3 --> D4[Descriptive Stats & Metrics]
    D4 --> D5[Year-wise Performance]
    D5 --> D6[Visualizations]
    
    C --> E[PART 2 — Multiple Companies]
    E --> E1[Select Tickers]
    E1 --> E2[Download Aligned Data]
    E2 --> E3[Normalized Performance]
    E3 --> E4[Return / Volatility / Volume]
    E4 --> E5[Correlation Heatmap]
    E5 --> E6[Risk–Return Scatter]
    
    D6 --> F[Final Summary]
    E6 --> F
    F --> G([End — Charts Saved])
```

---

## 📸 Screenshots

### 1️⃣ Libraries & Setup

![Libraries](Screenshots/Screenshot-1.png)

### 2️⃣ Company Reference Table

![Company List](Screenshots/Screenshot-2.png)

### 3️⃣ Selected Company & Date Range

![Selection](Screenshots/Screenshot-3.png)

### 4️⃣ Downloaded Single-Company Data

![Download](Screenshots/Screenshot-4.png)

### 5️⃣ Dataset Exploration

![Explore](Screenshots/Screenshot-5.png)

### 6️⃣ Missing Values & Descriptive Statistics

![Stats](Screenshots/Screenshot-6.png)

### 7️⃣ Prepared Data with New Columns

![Prepared](Screenshots/Screenshot-7.png)

### 8️⃣ Key Numerical Metrics

![Metrics](Screenshots/Screenshot-8.png)

### 9️⃣ Year-wise Performance Summary

![Yearly](Screenshots/Screenshot-9.png)

### 🔟 Highlights Summary

![Highlights](Screenshots/Screenshot-10.png)

### 1️⃣1️⃣ Multi-Company Selection

![Multi Select](Screenshots/Screenshot-11.png)

### 1️⃣2️⃣ Multi-Company Close Prices

![Multi Data](Screenshots/Screenshot-12.png)

### 1️⃣3️⃣ Comparison Summary Table

![Comparison](Screenshots/Screenshot-13.png)

---

## 📈 Generated Charts

### Single Company (NVDA example)

| Chart | Description |
|-------|-------------|
| **Closing Price** | Price trend over the selected period |
| **Trading Volume** | Daily volume time series |
| **Daily Return Distribution** | Histogram + KDE of daily returns |
| **Moving Averages** | Close price with 20-day & 50-day MAs |
| **Yearly Returns** | Bar chart of annual performance |

![NVDA Closing Price](charts/NVDA_closing_price.png)
![NVDA Volume](charts/NVDA_volume.png)
![NVDA Daily Returns](charts/NVDA_daily_return_dist.png)
![NVDA Moving Averages](charts/NVDA_moving_averages.png)
![NVDA Yearly Returns](charts/NVDA_yearly_returns.png)

### Multiple Companies

| Chart | Description |
|-------|-------------|
| **Normalized Performance** | All tickers rebased to 100 |
| **Total Return Comparison** | Bar chart of cumulative returns |
| **Volatility Comparison** | Daily return volatility by company |
| **Average Volume Comparison** | Trading activity ranking |
| **Correlation Heatmap** | Daily-return correlations |
| **Risk–Return Scatter** | Volatility vs Total Return |

![Normalized Performance](charts/multi_normalized_performance.png)
![Total Returns](charts/multi_total_returns.png)
![Volatility](charts/multi_volatility.png)
![Volume](charts/multi_volume.png)
![Correlation Heatmap](charts/multi_correlation_heatmap.png)
![Risk-Return](charts/multi_risk_return.png)

---

## 📁 Project Structure

```text
.
├── Stock_Market_Analyzer_Fixed.ipynb   # Main notebook
├── README.md
├── charts/                             # All generated PNG charts
│   ├── NVDA_closing_price.png
│   ├── NVDA_volume.png
│   ├── NVDA_daily_return_dist.png
│   ├── NVDA_moving_averages.png
│   ├── NVDA_yearly_returns.png
│   ├── multi_normalized_performance.png
│   ├── multi_total_returns.png
│   ├── multi_volatility.png
│   ├── multi_volume.png
│   ├── multi_correlation_heatmap.png
│   └── multi_risk_return.png
└── Screenshots/
    ├── Screenshot-1.png
    ├── Screenshot-2.png
    ├── ...
    └── Screenshot-13.png
```

---

## ▶️ How to Run

1. Open the notebook in Jupyter / VS Code / Google Colab:

```bash
jupyter notebook Stock_Market_Analyzer_Fixed.ipynb
```

2. Install dependencies if needed:

```bash
pip install yfinance pandas numpy matplotlib seaborn
```

3. Run all cells in order.  
   - Edit the `ticker`, `start_date`, and `end_date` cells to analyze different companies or periods.  
   - Charts are automatically saved to the `charts/` folder.

> **Internet required** for the `yfinance` download cells.

---

## 📋 Available Companies

| Name                     | Ticker |
|--------------------------|--------|
| Apple Inc.               | AAPL   |
| NVIDIA Corporation       | NVDA   |
| Microsoft Corporation    | MSFT   |
| Tesla, Inc.              | TSLA   |
| Amazon.com, Inc.         | AMZN   |
| Alphabet Inc. (Google)   | GOOGL  |

You can easily add more tickers to the company list.

---

## 💼 Why Recruiters Should Care

This project demonstrates practical skills that map directly to quantitative analysis and data science roles in finance:

- ✅ End-to-end **financial data pipeline** (download → clean → analyze → visualize)
- ✅ Real-world use of **yfinance** for live market data
- ✅ Calculation of core **risk & return metrics** (volatility, total return, correlation)
- ✅ Clean **time-series visualization** (price, volume, moving averages, distributions)
- ✅ Side-by-side **multi-asset comparison** with normalized performance and risk-return plots
- ✅ Fully reproducible notebook with saved charts and clear documentation

Ideal for showcasing applied data analysis skills in a finance context.

---

⭐ If you found this project useful, consider giving it a star!

## 👨‍💻 Author

**Akshar Tailor**
