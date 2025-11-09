# README — Trader Behavior Insights

## 📘 Project Overview

This project explores the relationship between **Bitcoin market sentiment (Fear & Greed Index)** and **trader performance (Hyperliquid Historical Data)**. The analysis uncovers behavioral patterns and performance trends across market regimes, helping to derive smarter trading strategies.

---

## 🧩 Datasets Used

1. **Historical Trader Data (Hyperliquid)**

   * File: `historical_data.csv`
   * Columns: `account`, `symbol`, `execution_price`, `size`, `side`, `time`, `start_position`, `event`, `closedPnL`, `leverage`, etc.

2. **Bitcoin Market Sentiment Data (Fear & Greed Index)**

   * File: `fear_greed_index.csv`
   * Columns: `Date`, `Classification` (Fear/Greed) or `Value` (0–100 index)

---

## 🧠 Objectives

* Explore the relationship between **market sentiment** and **trader profitability**.
* Identify behavioral patterns in trader actions under different sentiment regimes.
* Visualize and quantify performance differences between *fear* and *greed* markets.
* Build a simple model predicting daily trader success based on sentiment.

---

## ⚙️ Project Structure

```
Trader_Behavior_Insights/
│
├── historical_data.csv
├── fear_greed_index.csv
├── Trader_Behavior_Insights_Notebook.ipynb
├── merged_trader_sentiment_daily.csv
├── Untitled5.html (exported report)
└── README.md
```

---

## 🚀 How to Run the Notebook in Google Colab

1. Open Google Colab → New Notebook.
2. Upload the following files into the Colab environment:

   * `historical_data.csv`
   * `fear_greed_index.csv`
3. Copy and paste all code from `Trader_Behavior_Insights_Notebook.ipynb` into the Colab cells.
4. Run cells sequentially.

After completing, export the notebook as an **HTML report**:

```python
from google.colab import files
from nbconvert import HTMLExporter
import nbformat

notebook_filename = '/content/Untitled5.ipynb'  # replace with your filename
notebook_node = nbformat.read(open(notebook_filename, encoding='utf-8'), as_version=4)
html_exporter = HTMLExporter()
html_data, _ = html_exporter.from_notebook_node(notebook_node)

output_filename = '/content/Trader_Behavior_Insights.html'
with open(output_filename, 'w', encoding='utf-8') as f:
    f.write(html_data)

files.download(output_filename)
```

---

## 📊 Key Analyses Performed

* Data cleaning and feature engineering for timestamps and PnL metrics.
* Aggregation of per-account daily trading performance.
* Merging with market sentiment index.
* Exploratory visualizations: boxplots, histograms, time trends.
* Statistical testing (T-test, Mann–Whitney U) for differences in PnL distributions.
* Simple logistic regression model predicting daily win probability.

---

## 💡 Example Insights (replace with your real results)

* Traders tend to take higher leverage and larger trade sizes durin
