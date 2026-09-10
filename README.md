<p align="center">
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTR0zA1OR5KYBnBRZtxjn8du9EJxseMzpBsIfxor6qm7A&s=10" alt="Seasonal Agriculture Performance Analysis Banner" width="100%">
</p>

<h1 align="center">🌾 Seasonal Agriculture Performance Analysis</h1>

<p align="center">
  Exploratory data analysis of seasonal farming performance — environment, resources, yield, and economics — across Kharif, Rabi, and Zaid seasons in India.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10+-blue.svg" alt="Python">
  <img src="https://img.shields.io/badge/Platform-Google%20Colab-orange.svg" alt="Colab">
  <img src="https://img.shields.io/badge/Status-Complete-brightgreen.svg" alt="Status">
  <img src="https://img.shields.io/badge/License-MIT-lightgrey.svg" alt="License">
</p>

---

## 📌 Overview

This project analyzes farm-level agricultural data across **4,000 records** spanning **8 Indian states** and **3 growing seasons** (Kharif, Rabi, Zaid) to understand how environmental conditions, resource usage, and crop economics vary seasonally — and to surface actionable insights for improving yield and profitability.

The analysis was built and run as a Jupyter/Google Colab notebook, and covers the full pipeline: data cleaning, exploratory analysis, visualization, and findings.

---

## 📂 Repository Structure

```
├── Seasonal_Agriculture_Performance_Analysis.ipynb   # Full Colab notebook (code + outputs)
├── seasonal_agriculture_performance_dataset.csv      # Source dataset
├── graphs/                                           # Exported plots + captions
│   ├── 01_farm_records_by_season.png
│   ├── 01_farm_records_by_season.txt
│   ├── 02_environmental_conditions_by_season.png
│   ├── 02_environmental_conditions_by_season.txt
│   ├── ...
│   ├── 12_avg_yield_by_state_and_season_heatmap.png
│   └── 12_avg_yield_by_state_and_season_heatmap.txt
└── README.md
```

Each graph in `graphs/` has a matching `.txt` file with the same name containing a **title** and a **data-grounded caption**, ready to drop under the image in a report or slide deck.

---

## 📊 Dataset

| | |
|---|---|
| **Rows** | 4,000 farm records |
| **States covered** | Andhra Pradesh, Maharashtra, Telangana, Karnataka, Gujarat, Tamil Nadu, Punjab, Madhya Pradesh |
| **Crops covered** | Rice, Wheat, Maize, Cotton, Pulses, Groundnut, Chilli, Sugarcane |
| **Seasons** | Kharif, Rabi, Zaid |
| **Key fields** | Rainfall, Temperature, Humidity, Sunlight, Soil pH/Moisture, NPK levels, Irrigation Method, Fertilizer & Pesticide use, Seed Quality, Yield, Production, Market Price, Cost/Revenue/Profit, Water Used, Water Efficiency, Disease/Pest Risk |

---

## 🛠️ Tech Stack

- **Python 3**
- **pandas** / **numpy** — data cleaning & aggregation
- **matplotlib** / **seaborn** — visualization
- **Google Colab / Jupyter** — notebook environment

---

## 🚀 How to Run

1. Open [`Seasonal_Agriculture_Performance_Analysis.ipynb`](./Seasonal_Agriculture_Performance_Analysis.ipynb) in [Google Colab](https://colab.research.google.com/).
2. Upload `seasonal_agriculture_performance_dataset.csv` to the Colab session (or uncomment the `files.upload()` cell in the notebook).
3. Run all cells — plots and summary tables will generate inline.

```python
# Quick start (in Colab)
from google.colab import files
uploaded = files.upload()   # select the dataset CSV

import pandas as pd
df = pd.read_csv('seasonal_agriculture_performance_dataset.csv')
```

---

## 🔍 Analysis Pipeline

1. **Data Loading & Exploration** — shape, dtypes, missing values, duplicates, category breakdowns
2. **Data Cleaning** — season/crop-aware median imputation for missing values; outlier-capped yield column for cleaner plots
3. **Seasonal Overview** — record counts and key averages per season
4. **Environmental Conditions** — rainfall, temperature, humidity, sunlight by season
5. **Resource Usage** — fertilizer, water usage, water efficiency, irrigation method mix
6. **Crop Production & Yield** — yield distributions and crop × season performance heatmap
7. **Economic Performance** — cost, revenue, profit, and share of loss-making farms
8. **Correlation Analysis** — relationships between environmental/resource inputs and yield/profit
9. **Disease & Pest Risk** — seasonal risk patterns
10. **State-Level Consistency** — whether seasonal trends hold across all states

---

## 📈 Key Findings

- **Kharif** is the wettest, most humid season (avg. 852 mm rainfall, 72% humidity) and carries the highest disease/pest risk (54.5%), consistent with monsoon conditions.
- **Zaid** is the hottest and driest season (avg. 31°C, 299 mm rainfall) but also the least profitable — **64.5% of Zaid farms report a loss**, compared to 51.1% in Rabi and 42.2% in Kharif.
- **Water efficiency correlates positively with profit** (r = 0.49) — a stronger driver of profitability than rainfall, fertilizer use, or seed quality, none of which show a meaningful linear relationship with yield in this dataset.
- **Yield is highly crop-specific**: Sugarcane in Kharif is the best-performing crop-season combination (51.6 t/ha avg.), while Pulses in Zaid is the weakest (0.65 t/ha avg.).
- **Seasonal patterns are not uniform across states** — e.g., Rabi is the strongest season for Maharashtra and Punjab, while Zaid is strongest for Karnataka, showing regional agro-climatic differences moderate national trends.

---

## ✅ Recommendations

- Prioritize water-efficient irrigation (drip/sprinkler) in **Kharif**, where both pest risk and water usage are elevated.
- Direct cost-efficiency support toward **Zaid**-season farms, where losses are most widespread.
- Align crop selection with each state's strongest-performing season using the state × season yield heatmap.
- Investigate high-yield and high-loss outlier farms as best/worst practice case studies.

---

## 📝 License

This project is released under the [MIT License](https://opensource.org/licenses/MIT). Feel free to use, modify, and share.

---

<p align="center">Made with 🌱 and pandas</p>
