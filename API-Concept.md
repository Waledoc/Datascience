# API Concept – Data Acquisition Strategy

This document defines the API and data-source strategy for each research topic.  
It specifies data providers, variable scope, spatial/temporal resolution, and integration logic.

---

# Topic 1: Weather Conditions vs. Road Accidents in Germany

## 1. Research Objective

To analyze how weather conditions influence accident frequency and severity across Germany, controlling for time and regional characteristics.

---

## 2. Required Data Components

The analysis requires three core data blocks:

1. Accident Data  
2. Weather Data  
3. Regional Classification Data  

---

## 3. Accident Data

### Source: 
Statistisches Bundesamt (Destatis) – Verkehrsunfälle  
Unfallatlas (Open Data)

### Coverage:
- Germany-wide
- Regional level (state / district)
- Historical time series
- Accident type & severity classification

### Key Variables:
- Date (day / month / year)
- Region (Bundesland / Landkreis)
- Number of accidents
- Severity (injury / fatality / property damage)
- Road type (if available)

### Purpose in Model:
- Dependent variable (accident frequency / severity)
- Regional aggregation unit

---

## 4. Weather Data

### Primary API Recommendation:
Open-Meteo (Historical Weather API)

### Why:
- Free
- No API key required
- Hourly historical data
- Germany-wide coverage via coordinates

### Key Variables:
- temperature_2m
- precipitation
- snowfall
- windspeed
- windgusts
- visibility
- weathercode

### Temporal Resolution:
- Hourly (for lag-effect testing)
- Aggregated to daily level for robustness checks

---

### Optional Scientific Alternative:
Deutscher Wetterdienst (DWD Open Data)

- Station-based official German weather data
- Higher scientific credibility
- Requires manual parsing

---

## 5. Regional Classification

### Data Sources:
- Destatis regional statistics
- Population density datasets
- Urban vs. rural proxy classification

### Variables:
- Population density
- Settlement structure
- Federal state
- District classification

---

## 6. Data Integration Strategy

Weather data will be matched to accident data by:

1. Geographic mapping (district centroid coordinates → nearest weather grid)
2. Temporal alignment (hourly or daily aggregation)
3. Lag construction (0–3 hour windows after weather changes)

Example:
- Rain onset at 14:00  
- Accident frequency measured 14:00–17:00  
- Compare to dry baseline days

---

## 7. Extreme Weather Definition

Extreme weather will be operationalized via thresholds:

- Heavy rain: precipitation above 90th percentile
- Storm: wind gusts above threshold
- Snowfall days
- Temperature near 0°C (−2°C to +2°C window)

---

## 8. Analytical Readiness

This API combination enables:

- Multivariate regression models
- Time-series lag models
- Regional heterogeneity analysis
- Severity classification models

---
