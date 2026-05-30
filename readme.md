# 🚗 US Licensed Drivers Analysis (2010–2023)

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://python.org)
[![Pandas](https://img.shields.io/badge/Pandas-2.0%2B-green)](https://pandas.pydata.org)
[![Power BI](https://img.shields.io/badge/Power%20BI-Desktop-yellow)](https://powerbi.microsoft.com)
[![License](https://img.shields.io/badge/License-Public%20Domain-lightgrey)](https://creativecommons.org/publicdomain/zero/1.0/)

## 📋 Project Overview

This project analyzes licensed driver statistics across all 50 US states and the District of Columbia from 2010 to 2023. The analysis explores **spatial trends**, **gender distribution**, and **driver density** relative to population using **Python (Pandas/Matplotlib)** and **Power BI**.

## 🎯 Key Business Questions

| # | Question |
|---|----------|
| 1 | Did the total number of licensed drivers grow systematically between 2010 and 2023? |
| 2 | Are there significant differences between states in drivers per 1,000 residents? |
| 3 | How has the gender structure of drivers evolved over time? |
| 4 | Which states have the highest and lowest driver density? |

## 📁 Repository Structure

```
US-Driver-Analysis/
│
├── README.md                                    # Project documentation
├── Licensed_Drivers.ipynb                       # Python EDA notebook
├── Licensed_Drivers.pbix                        # Power BI dashboard
│
├── data/
│   ├── Licensed_Drivers_By_Sex_And_Ratio_To_Population__2010-2023__DL-1C_data.gov.csv
│   └── states.csv                               # State coordinates for mapping
│
└── images/
    └── Licensed_Drivers.pdf                     # Dashboard export (3 pages)
```

## 🔧 Tools & Technologies

| Tool | Purpose |
|------|---------|
| **Python (Pandas)** | Data cleaning, aggregation, statistical analysis |
| **Matplotlib / Seaborn** | Static visualizations (trends, distributions, correlations) |
| **Power BI** | Interactive dashboard with maps, slicers, and drill-through |
| **GitHub** | Version control and portfolio hosting |

## 📊 Key Findings

| Metric | Result |
|--------|--------|
| **Total Growth (2010–2023)** | +8.2% increase in licensed drivers |
| **Highest Driver Density** | Delaware (859 drivers per 1,000 residents) |
| **Lowest Driver Density** | New York (629 drivers per 1,000 residents) |
| **National Gender Split** | 50.3% Male / 49.7% Female |
| **Highest Female %** | Georgia (53.95% female drivers) |
| **Population–Drivers Correlation** | r = 0.99 (strong positive) |

### 🔍 Detailed Insights

1. **Steady National Growth**  
   The total number of licensed drivers increased consistently year over year, with accelerated growth observed post-2020.

2. **Geographic Disparities**  
   States like Delaware, Maryland, and New Jersey show driver density above 850 per 1,000 residents, while New York, Texas, and California lag below 650.

3. **Gender Trends**  
   Female driver representation has slowly increased over the decade, with Southern states (GA, MS, LA) showing the highest proportions of female licensed drivers.

4. **Population Impact**  
   As expected, population strongly correlates with total licensed drivers (\( r = 0.99 \)), but density metrics reveal meaningful per-capita differences.

## 🚀 How to Run

### Python Notebook
```bash
# Clone the repository
git clone https://github.com/yourusername/US-Driver-Analysis.git
cd US-Driver-Analysis

# Install dependencies
pip install pandas matplotlib seaborn jupyter

# Launch Jupyter Notebook
jupyter notebook Licensed_Drivers.ipynb
```

### Power BI Dashboard
1. Download `Licensed_Drivers.pbix`
2. Open with **Power BI Desktop** (free)
3. Use slicers to filter by **Year** and **State**
4. Explore three dashboard pages:
   - 📍 **Regional Comparison** (map with clusters)
   - 👥 **Gender Analysis** (pie chart + top states)
   - 📈 **Driver Density Analysis** (trends and rankings)

## 📈 Sample Visualizations

| Analysis | Visualization |
|----------|---------------|
| National trends (2010–2023) | Line chart (total drivers + gender split) |
| Driver density by state (2023) | Horizontal bar chart (top/bottom 10) |
| Population vs. drivers | Scatter plot with correlation line |
| Gender distribution | Pie chart + state rankings |

> **Full interactive dashboard** → `Licensed_Drivers.pbix`  
> **PDF export** → `images/Licensed_Drivers.pdf`

## 🗃️ Data Source

| Attribute | Details |
|-----------|---------|
| **Dataset** | Licensed Drivers by Sex and Ratio to Population |
| **Source** | data.gov (U.S. Department of Transportation) |
| **Time Period** | 2010–2023 (14 years) |
| **Geography** | 50 states + District of Columbia |
| **Key Columns** | Drivers_Male, Drivers_Female, Drivers_Total, Drivers_per_1000Residents |
| **License** | Public Domain / U.S. Government Work |

## 📝 SQL Equivalents (Appendix in Notebook)

The notebook includes SQL versions of key analyses:
- Top 10 states by driver density (2023)
- Year-over-year growth calculation using `LAG()`
- State ranking by percentage of female drivers

## 📧 Contact

**Author:** Mikita Kutsayeu  
**Student ID:** 48860  
**Course:** Business Data Analysis  
**Institution:** Akademia Vizja, Warsaw  

---

## ⭐ Acknowledgments

- Data provided by **data.gov** (U.S. Government open data initiative)
- Built as part of academic coursework in Business Data Analysis