# 🚗 US Licensed Drivers Analysis (2010–2023)

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://python.org)
[![Pandas](https://img.shields.io/badge/Pandas-2.0%2B-green)](https://pandas.pydata.org)
[![Power BI](https://img.shields.io/badge/Power%20BI-Desktop-yellow)](https://powerbi.microsoft.com)
[![License](https://img.shields.io/badge/License-MIT-lightgrey)](LICENSE)

## 📋 Project Overview

This project analyzes licensed driver statistics across all 50 US states and the District of Columbia from 2010 to 2023. The analysis explores **spatial trends**, **gender distribution**, and **driver density** relative to population using **Python (Pandas/Matplotlib)** for exploratory data analysis (EDA) and **Power BI** for an interactive dashboard.

## 🎯 Key Business Questions

| # | Question |
|---|----------|
| 1 | Did the total number of licensed drivers grow systematically between 2010 and 2023? |
| 2 | Are there significant differences between states in drivers per 1,000 residents? |
| 3 | How has the gender structure of drivers evolved over time? |
| 4 | Which states have the highest and lowest driver density? |

## 📁 Repository Structure

```
Licensed_Drivers_PowerBI/
│
├── README.md                    # Project documentation (this file)
├── Licensed_Drivers.ipynb       # Python EDA notebook (Pandas, Matplotlib)
├── Licensed_Drivers.pbix        # Power BI interactive dashboard
│
├── data/
│   ├── Licensed_Drivers_By_Sex_And_Ratio_To_Population__2010-2023__DL-1C_data.gov.csv
│   └── states.csv               # State coordinates for accurate map rendering
│
└── images/
    └── Licensed_Drivers.pdf     # PDF export of the Power BI dashboard (3 pages)
    └── driver_density.png
    └── gender_analysis.png
    └── national_trends.png
    └── population_vs_drivers.png
    └── top_states_trends.png
```

## 🔧 Tools & Methodologies

| Tool/Method | Purpose |
|-------------|---------|
| **Python (Pandas)** | Data cleaning, aggregation, and statistical analysis |
| **Matplotlib / Seaborn** | Static visualizations (trends, distributions, correlations) |
| **Power BI** | Interactive dashboard with maps, slicers, and drill-through |
| **Pearson Correlation** | Measure relationship between population and licensed drivers |
| **Stacked Area Chart** | Visualize gender distribution over time |
| **Geographic Clustering** | Power BI automatic clustering for regional patterns |

## 📊 Key Findings

| Metric | Result |
|--------|--------|
| **Total Growth (2010–2023)** | +8.2% increase in licensed drivers |
| **Highest Driver Density** | Delaware (859 drivers per 1,000 residents) |
| **Lowest Driver Density** | New York (629 drivers per 1,000 residents) |
| **National Gender Split (2023)** | 50.3% Male / 49.7% Female |
| **Highest Female % (2023)** | Georgia (53.95% female drivers) |
| **Population–Drivers Correlation** | r = 0.99 (strong positive linear relationship) |

### 🔍 Detailed Insights

1.  **Steady National Growth**  
    The total number of licensed drivers increased consistently year over year, with a notable acceleration observed post-2020. The Python notebook calculates a total growth of **8.2%** from 2010 to 2023.

2.  **Geographic Disparities**  
    States like Delaware, Maryland, and New Jersey show driver density above 850 per 1,000 residents, while New York, Texas, and California lag below 650. This suggests varying levels of car dependency and public transport availability.

3.  **Gender Trends**  
    Female driver representation has slowly increased over the decade. The analysis in the notebook identifies Southern states (Georgia, Mississippi, Louisiana) as having the highest proportions of female licensed drivers.

4.  **Population Impact**  
    As expected, population size strongly correlates with total licensed drivers (\( r = 0.99 \)). However, the `Drivers_per_1000Residents` metric reveals meaningful per-capita differences, making it a better tool for cross-state comparison.

## 🚀 How to Run / Reproduce

### 1. Python Notebook (`Licensed_Drivers.ipynb`)

```bash
# Clone the repository (if you haven't already)
git clone https://github.com/vnebra4niy/Licensed_Drivers_PowerBI.git
cd Licensed_Drivers_PowerBI

# (Optional) Create and activate a virtual environment
# python -m venv venv && source venv/bin/activate (Mac/Linux) or venv\Scripts\activate (Windows)

# Install required packages
pip install pandas matplotlib seaborn jupyter

# Launch the notebook
jupyter notebook Licensed_Drivers.ipynb
```

The notebook will automatically load the CSV files from the `data/` folder and generate all static charts.

### 2. Power BI Dashboard (`Licensed_Drivers.pbix`)

1.  **Download** the `Licensed_Drivers.pbix` file from the repository.
2.  Open it with **Power BI Desktop** (free version available from Microsoft).
3.  Use the **slicers** on each page to filter by **Year** and **State**.
4.  Explore the three prepared report pages:
    - **📍 Regional Comparison** (US map with geographic clusters of driver density).
    - **👥 Gender Analysis** (national pie chart + bar chart of top states by % female drivers).
    - **📈 Driver Density Analysis** (trends over time and rankings per state).

### 3. PDF Export

The `images/Licensed_Drivers.pdf` file contains a static export of all three dashboard pages for quick preview without Power BI.

## 📈 Sample Visualizations (from the notebook)

| Analysis | Visualization Type | Key Insight |
|----------|--------------------|--------------|
| National trends (2010–2023) | Line chart (total) + Stacked area (gender) | Steady growth, stable gender split |
| Driver density by state (2023) | Horizontal bar chart (top/bottom 10) | Wide variation from 629 to 859 per 1,000 |
| Population vs. drivers | Scatter plot with correlation line | Strong linear relationship (r=0.99) |
| Gender distribution by state | Horizontal bar chart (top 10 by % female) | Southern states lead in female driver percentage |

> **Full interactive dashboard** → `Licensed_Drivers.pbix`  
> **Static PDF export** → `images/Licensed_Drivers.pdf`

## 🗃️ Data Source

| Attribute | Details |
|-----------|---------|
| **Dataset** | Licensed Drivers by Sex and Ratio to Population |
| **Source** | data.gov (U.S. Department of Transportation) |
| **Time Period** | 2010–2023 (14 consecutive years) |
| **Geography** | 50 US states + District of Columbia |
| **Key Columns Used** | `Drivers_Male`, `Drivers_Female`, `Drivers_Total`, `Drivers_per_1000Residents` |
| **Auxiliary Data** | `states.csv` (custom coordinates for Power BI map accuracy) |
| **License** | Public Domain / U.S. Government Work |

## ⚠️ Limitations & Caveats

- **State‑level aggregation only** – The analysis uses state‑summarized data, which may mask significant intra‑state variations (e.g., urban vs. rural differences, county‑level trends).
- **Licensed drivers ≠ active drivers** – Holding a license does not guarantee active driving; this metric may overestimate driving activity in certain states.
- **Population denominator** – The primary metric `Drivers_per_1000Residents` includes residents under 16 (not eligible to drive). The dataset also provides `Drivers_per_1000Residents16+`, which may be more accurate for comparisons among the eligible population.
- **Gender binary** – The source data reports only male/female categories, which does not reflect current demographic understanding.
- **Data quality** – The Python notebook includes a data quality check, confirming no missing values or impossible entries (e.g., drivers exceeding population).

## 📚 Methodology References

- **Data aggregation** – Pandas `groupby()` for annual and state summaries.
- **Growth calculation** – `((2023 value - 2010 value) / 2010 value) × 100`.
- **Correlation** – Pearson’s r, calculated with Pandas `.corr()`.
- **Trend visualization** – Line plots, stacked area charts, and bar charts using Matplotlib.
- **Dashboard design** – Three‑page layout with bookmarks, slicers, and automatic geographic clustering in Power BI.

## 📝 SQL Equivalents

The Appendix of `Licensed_Drivers.ipynb` includes SQL versions of key analyses, such as:

- Top 10 states by driver density (2023)
- Year-over-year growth calculation using `LAG()`
- State ranking by percentage of female drivers

## 📧 Contact & Attribution

**Author:** Mikita Kutsayeu (GitHub: [vnebra4niy](https://github.com/vnebra4niy))  
**Course:** Business Data Analysis  

**Data provided by:** [data.gov](https://catalog.data.gov/dataset/licensed-drivers-by-sex-and-ratio-to-population-2010-2023-dl-1c?from_hint=eyJxIjoibGljZW5zZWQgZHJpdmVycyJ9) (U.S. Government open data initiative)