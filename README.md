# 🔍 Crime Forecasting — Vancouver Neighbourhood Crime Analysis & Prediction

> **Section C | Group 18**
> A data-driven analysis and forecasting project that examines crime patterns across Vancouver neighbourhoods from 1999 to 2011 and predicts future crime trends through 2015.

---

## 📌 Project Overview

This project presents a comprehensive crime forecasting study based on publicly available crime data from the **City of Vancouver**. The analysis covers **9,050+ crime records** spanning **13 years (1999–2011)** across **24 neighbourhoods** and **8 crime categories**.

Using **pivot table analysis, year-over-year (YoY) growth calculations, and trend-based forecasting**, the project identifies crime hotspots, peak crime hours, seasonal patterns, and neighbourhood-level risk profiles. Forecasted values for **2012–2015** are generated using growth-rate extrapolation methods to support proactive resource allocation and urban safety planning.

---

## 📊 Dataset Description

### Raw Dataset
- **Source:** City of Vancouver Open Data
- **Records:** 9,050+ crime incidents
- **Time Span:** 1999 – 2011
- **File:** `RawDataset/crimeForecasting.csv` (~57 MB)

### Features (Columns)

| Column | Description |
|---|---|
| `TYPE` | Crime category (e.g., Theft from Vehicle, Mischief) |
| `HUNDRED_BLOCK` | Approximate location (street block) |
| `NEIGHBOURHOOD` | Vancouver neighbourhood name |
| `X`, `Y` | UTM coordinates |
| `Latitude`, `Longitude` | Geographic coordinates |
| `HOUR`, `MINUTE` | Time of incident |
| `YEAR`, `MONTH`, `DAY` | Date of incident |

### Crime Categories Covered
1. Theft from Vehicle
2. Mischief
3. Break and Enter Residential/Other
4. Other Theft
5. Theft of Vehicle
6. Break and Enter Commercial
7. Theft of Bicycle
8. Vehicle Collision or Pedestrian Struck (with Injury)

---

## ⚙️ Methodology

The project follows a structured analytical pipeline:

1. **Data Cleaning** — Raw data was processed to remove inconsistencies, handle missing values, and standardize formats. The cleaned dataset is stored in `CleanedDataset/`.

2. **Pivot Table Analysis** — Six pivot tables were created to dissect crime data from multiple dimensions:
   - **Pivot Table 1:** Year-over-Year crime trend with growth % and directional indicators
   - **Pivot Table 2:** Crime distribution by hour of day and crime type
   - **Pivot Table 3:** Crime cases by time of day (Night, Evening, Day, Afternoon)
   - **Pivot Table 4:** Crime type distribution with percentage breakdown
   - **Pivot Table 5:** Neighbourhood-wise crime ranking across all crime types
   - **Pivot Table 6:** Monthly crime distribution across all categories

3. **Forecasting** — Trend extrapolation using YoY growth rates to predict crime counts for 2012–2015, applied at both city-wide and neighbourhood levels (e.g., Central Business District, Arbutus Ridge).

---

## 🔑 Key Findings

### 🏙️ Neighbourhood Insights
- **Central Business District (CBD)** is the highest crime zone with **2,035 cases** — nearly **2.5× higher** than the second-ranked West End (803 cases).
- Low-crime areas like Shaughnessy and South Cambie still show proportionally high residential break-ins.

### 🕐 Temporal Patterns
- **Peak crime hour:** 6 PM (691 cases) — a sharp jump from 448 cases at 3 PM.
- **Lowest crime hour:** 5 AM (126 cases).
- **Night-time dominates:** 4,294 cases (47.4%) occur at night, followed by evening (3,950 cases).

### 📈 Yearly Trends
- Crime **declined consistently from 2000–2006** (steepest drop: -17.22% in 2003).
- A **reversal began in 2007** (+2.93%), with the **strongest rebound in 2010** (+14.15%).

### 🚗 Crime Type Breakdown
- **Theft from Vehicle** is overwhelmingly dominant at **36.7%** of all incidents.
- **Mischief** (14.2%) and **Break & Enter Residential** (13.1%) are the next most common.
- **Vehicle Collision with Injury** (4.4%) is rare but high-severity.

---

## 📁 Repository Structure

```
SectionC_Group18_CrimeForcasting/
│
├── RawDataset/
│   └── crimeForecasting.csv              # Original raw crime dataset (~57 MB)
│
├── CleanedDataset/
│   └── crimeForecastingFinal - cleanedData.csv   # Processed & cleaned data
│
├── Calculation&PivotTable/
│   ├── crimeForecastingFinal - Pivot_Table1.csv  # YoY crime trend analysis
│   ├── crimeForecastingFinal - Pivot_Table2.csv  # Hourly crime distribution
│   ├── crimeForecastingFinal - Pivot_Table3.csv  # Time-of-day breakdown
│   ├── crimeForecastingFinal - Pivot_Table4.csv  # Crime type percentages
│   ├── crimeForecastingFinal - Pivot_Table5.csv  # Neighbourhood ranking
│   ├── crimeForecastingFinal - Pivot_Table6.csv  # Monthly distribution
│   ├── crimeForecastingFinal - FORECASTING.csv   # Neighbourhood-level forecasts
│   └── crimeForecastingFinal - Advanced_Forecast.csv  # CBD advanced forecast
│
├── Dashboard/                            # Visualisation dashboards
│
├── Documentation/
│   └── CrimeForecastingReport.pdf        # Detailed project report
│
├── Presentation/
│   └── Presentation.pdf                  # Project presentation slides
│
└── README.md                             # Project overview (this file)
```

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| **Microsoft Excel / Google Sheets** | Data cleaning, pivot tables, and forecasting calculations |
| **PDF Documentation** | Project report and presentation |
| **Git & GitHub** | Version control and collaboration |

---

## 👥 Team

**Section C — Group 18**

---

## 📄 License

This project is developed for academic purposes. The dataset is sourced from publicly available City of Vancouver open data.
