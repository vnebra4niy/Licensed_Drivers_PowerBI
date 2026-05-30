# US Licensed Drivers Analysis (2010–2023)

This project provides an interactive business intelligence report analyzing licensed driver data across all 50 US states and the District of Columbia. Using **Microsoft Power BI**, the report explores spatial trends, gender distribution, and driver density relative to population.

## 📁 Project Structure
```
├── BAD - raport_48860.docx # Project documentation (Polish)
├── Licensed_Drivers_By_Sex_And_Ratio_To_Population__2010-2023__DL-1C_data.gov.csv # Main dataset
├── states.csv # State coordinates for mapping
└── README.md # This file
```
## 🎯 Objective

Analyze licensed driver statistics in the United States from 2010 to 2023 to answer the following business questions:

- Did the total number of licensed drivers grow systematically between 2010 and 2023?
- Are there significant differences between states in the number of drivers per 1,000 residents?
- How has the gender structure of drivers evolved over time?
- Which states have the highest and lowest driver density?

## 📊 Data Sources

### Main Dataset (`Licensed_Drivers_By_Sex_And_Ratio_To_Population__2010-2023__DL-1C_data.gov.csv`)

Contains annual records for each state (2010–2023) with the following key columns:

- `Year` – Calendar year
- `State` – US state name
- `Drivers_Male` – Number of male licensed drivers
- `Drivers_Male%` – Percentage of male drivers
- `Drivers_Female` – Number of female licensed drivers
- `Drivers_Female%` – Percentage of female drivers
- `Drivers_Total` – Total licensed drivers
- `Residents` – Total state population
- `Residents_16+` – Population aged 16 and over
- `Drivers_per_1000Residents` – Drivers per 1,000 total residents
- `Drivers_per_1000Residents16+` – Drivers per 1,000 residents aged 16+

### Auxiliary Table (`states.csv`)

Provides geographic coordinates for each state, used to display states correctly on Power BI maps:

- `State` – State abbreviation (e.g., AK, AL)
- `Latitude` / `Longitude` – Center coordinates
- `Name` – Full state name

## 🧠 Methodology

1. **Data Import** – Load both CSV files into Power BI Desktop.
2. **Data Transformation** – Change data types, create calculated columns if needed (Power Query).
3. **Relational Model** – Create a relationship between the main table and `states.csv` via the `State` field.
4. **Visualizations** – Build three report pages:
   - **Page 1: Regional Comparison** – US map with geographic clustering (driver density by state).
   - **Page 2: Gender Analysis** – Pie chart of male/female driver distribution and bar chart of top states by female driver percentage.
   - **Page 3: Driver Density Analysis** – Additional charts exploring drivers per 1,000 residents over time and across states.

## 📈 Key Findings (from the report)

- Total number of licensed drivers in the US increased steadily from 2010 to 2023.
- Significant differences exist between states – larger, more urbanized states tend to have higher numbers of drivers.
- The gender structure of drivers remained relatively stable, though some states showed a notable increase in female driver share.
- The `Drivers_per_1000Residents` metric provides a better comparison across states, independent of population size.
- Interactive Power BI visualizations enable quick comparisons and data exploration.

> **Note:** The analysis uses state‑level aggregated data, which may mask variations within individual regions.

## 🚀 How to Use

1. Open **Power BI Desktop**.
2. Load the two CSV files (`Licensed_Drivers_By_Sex_And_Ratio_To_Population__2010-2023__DL-1C_data.gov.csv` and `states.csv`).
3. Create a relationship between the tables using the `State` column (match full names with abbreviations).
4. Build the visualizations as described in the methodology or explore the provided `.pbix` file if available.
5. Use slicers to filter by year, state, or gender.

## 🔧 Requirements

- **Power BI Desktop** (free) – [Download](https://powerbi.microsoft.com/en-us/desktop/)
- No additional Python or R libraries required.

## 📸 Sample Visualizations (from the report)

- US map with geographic clusters (driver density)
- Pie chart: male vs. female drivers (national or per state)
- Bar chart: top states by percentage of female drivers
- Line chart: driver density trends over time

## 📝 Notes

- Data covers all 50 states + District of Columbia.
- Time period: 2010–2023 inclusive.
- The auxiliary `states.csv` ensures correct map rendering in Power BI.

## 📚 References

- Data source: [data.gov](https://www.data.gov/) – Licensed Drivers by Sex and Ratio to Population.
- Report documentation (Polish): `BAD - raport_48860.docx`

## 👤 Author

**Mikita Kutsayeu**  
Student ID: 48860  
Warsaw, Akademia Vizja – Business Data Analysis course