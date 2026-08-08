# 🌦️ Telangana Weather Insights Dashboard (2021–2024)

## 📘 Overview
The **Telangana Weather Insights Dashboard** is a Power BI–based analytical project designed to visualize and analyze 4 years (2021–2024) of district-wise weather data across Telangana, India.  
It provides a comprehensive look at **rainfall, temperature, humidity, and wind speed**, helping identify trends, anomalies, and climate patterns across regions.

The dataset was compiled from **36+ monthly CSV files (≈705K records)** and cleaned, merged, and transformed using Power Query before creating dynamic, interactive dashboards in Power BI.

---

## 🧰 Tools & Technologies
- **Power BI Desktop**
- **Power Query Editor**
- **DAX (Data Analysis Expressions)**
- **Excel / CSV**
- **Data Modeling and Relationships**

---

## 🗂️ Data Description
Each CSV file includes the following columns:

| Column | Description |
|--------|--------------|
| District | District name of Telangana |
| Mandal | Subdivision/region within district |
| Date | Recorded date |
| Rain (mm) | Daily rainfall in millimeters |
| Min Temp (°C) | Minimum daily temperature |
| Max Temp (°C) | Maximum daily temperature |
| Min Humidity (%) | Minimum humidity level |
| Max Humidity (%) | Maximum humidity level |
| Min Wind Speed (Kmph) | Minimum wind speed |
| Max Wind Speed (Kmph) | Maximum wind speed |

---

## 📊 Dashboards Overview

### 🌧️ 1. Rainfall Analysis
- Highest and lowest rainfall districts
- Seasonal rainfall variations
- Yearly trend lines
- Rainfall anomalies using Z-score and percentile detection
- Monthly rainfall distribution and top 5 rainfall zones

### 🌡️ 2. Temperature Insights
- Min/Max/Average temperature distribution
- Seasonal temperature fluctuations
- Heatwave identification using percentile thresholds
- Correlation between Min & Max temperature
- Daily temperature range (Max–Min)

### 💧 3. Humidity Patterns
- Avg/Min/Max humidity levels per district
- Seasonal variation in humidity
- Extreme humidity day detection
- Year-over-year humidity comparison
- Humidity anomalies using standard deviation

### 💨 4. Wind Speed Analysis
- District-wise wind speed trends
- Outlier detection using violin & box plots
- Min/Max/Average wind range
- Seasonal and yearly speed patterns
- Extreme wind events and distribution

### 💻 5. Comprehensive Weather Insights
- Unified dashboard comparing all key metrics (Rainfall, Temp, Humidity, Wind)
- Year and District slicers for dynamic insights
- Correlation matrix between weather parameters
- Anomaly detection and seasonal summaries

---

## 🧮 Key DAX Measures

```DAX
-- Total Rainfall
Total Rainfall (mm) = SUM('Weather'[Rain (mm)])

-- Average Temperature
Avg Temperature (°C) = AVERAGE( ('Weather'[Max Temp (°C)] + 'Weather'[Min Temp (°C)]) / 2 )

-- Daily Temperature Range
Daily Temp Range (°C) = AVERAGE('Weather'[Max Temp (°C)] - 'Weather'[Min Temp (°C)])

-- Average Humidity
Avg Humidity (%) = AVERAGE(('Weather'[Max Humidity (%)] + 'Weather'[Min Humidity (%)]) / 2)

-- Average Wind Speed
Avg Wind Speed (Kmph) = AVERAGE(('Weather'[Max Wind Speed (Kmph)] + 'Weather'[Min Wind S
