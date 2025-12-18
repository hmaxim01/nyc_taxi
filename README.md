# NYC Yellow Taxi — Exploratory Data Analysis (EDA)

## Overview
Analyzed **New York City Yellow Taxi trip data** (January 2025) to explore patterns in trip distances, fares, tips, and temporal trends.  

This project demonstrates **data ingestion, cleaning, feature engineering, and visualization** on a large dataset using **R**.

---

## Key Insights

### Trip Distance
![Trip Distance Histogram](https://raw.githubusercontent.com/hmaxim01/nyc_taxi/figures/trip_distance_hist.png)
- Most trips are **short (0–10 miles)**.  
- Extremely long trips are rare and were filtered for clarity.

### Total Fare Distribution
![Total Fare Histogram](https://raw.githubusercontent.com/hmaxim01/nyc_taxi/figures/total_fare_hist.png)  
- Majority of fares are **under $50**, with outliers for long or airport trips.  
- Log scale plots reveal rare high-fare trips clearly.

### Tip Amount Distribution
![Tip Amount Histogram](https://raw.githubusercontent.com/hmaxim01/nyc_taxi/figures/tip_amount_hist.png)  
- Tips cluster around **$0–$5**, with few larger tips.  

### Average Fare by Hour
[![Average Fare by Hour](https://raw.githubusercontent.com/hmaxim01/nyc_taxi/figures/avg_fare_hour.png) 
- Fares **peak during commuting hours** (8–9 AM, 5–6 PM).

### Trips by Weekday
![Trips by Weekday](https://raw.githubusercontent.com/hmaxim01/nyc_taxi/figures/trips_weekday.png)  
- Trip counts are relatively consistent across the week.

---

## Methodology

1. **Data Loading**  
   - Used `arrow` for efficient Parquet ingestion.

2. **Sampling**  
   - Random 50% sample with fixed seed for reproducibility.

3. **Cleaning & Feature Engineering**  
   - Lowercased column names  
   - Converted pickup/dropoff times to POSIXct  
   - Derived features: `hour`, `weekday`, `trip_duration_min`, `tip_amount`

4. **EDA & Visualization**  
   - Histograms, boxplots, line plots  
   - Filtering out zero or extreme values for clear visualization

5. **Data Quality Checks**  
   - Summary statistics  
   - Missing value counts  
   - Initial row inspection

---

## Tools & Packages
- **R**  
- `arrow` — Parquet ingestion  
- `dplyr` — Data wrangling  
- `ggplot2` — Visualization  
- `lubridate` — Date-time manipulation  

---
