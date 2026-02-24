# Data Science Project  
## Research Questions & Conceptual Framework

---

> This document defines the analytical research questions for the three proposed topics.  
> Each section can be expanded individually.

---

# Topic Overview

<details>
<summary><strong>Topic 1 ▸ Weather Conditions vs. Road Accidents in Germany</strong></summary>

<br>

### Objective
Investigate how weather conditions influence accident frequency and severity across time and region.

---

### Research Questions

**Weather & Frequency**
- How does accident frequency change on rainy vs. dry days, controlling for weekday and season?
- How is temperature around 0°C (frost/black ice risk) associated with accident rates in winter months?

**Severity Drivers**
- Which weather variables (precipitation intensity, wind gusts, visibility, snowfall) best explain accident severity?
- How do weather–accident relationships differ by time of day (daytime vs. nighttime)?

**Regional & Extreme Effects**
- Are there significant regional differences (states / urban vs. rural)?
- What is the impact of extreme weather events (heavy rain, storms, snow) compared to typical days?
- Are there lag effects after rain onset or sudden temperature drops?

---

### Analytical Dimensions
- Target variable: Accident frequency / severity
- Controls: Weekday, seasonality
- Methods: Regression, time-series models, lag analysis

</details>

---

<details>
<summary><strong>Topic 2 ▸ What Makes Movies / Netflix Series Successful?</strong></summary>

<br>

### Objective
Identify financial, structural, and audience-related determinants of media success.

---

### Research Questions

**Financial & Star Power**
- Which budget-related measures correlate most strongly with success?
- How does star power (cast popularity, awards history) influence success across genres?

**Release Strategy & Engagement**
- How does release strategy (weekly vs. binge) affect popularity trajectories?
- Which combination of critic vs. audience scores best predicts longer-term success?

**Structural Factors**
- Are there genre cycles over time?
- How do episode count and episode length relate to retention proxies?
- Does international availability increase success probability?

---

### Analytical Dimensions
- Target variable: Ratings / popularity proxies
- Features: Budget, cast metrics, release type, genre
- Methods: Correlation analysis, panel regression, time-series comparison

</details>

---

<details>
<summary><strong>Topic 3 ▸ Solar/Wind Potential vs. Deployment in Germany</strong></summary>

<br>

### Objective
Quantify the gap between renewable energy potential and actual installed capacity across regions.

---

### Research Questions

**Potential–Deployment Gap**
- How large is the gap between technical potential and installed capacity by district/state?
- Is deployment better explained by resource quality or non-resource factors?

**Infrastructure & Constraints**
- Does proximity to grid infrastructure predict deployment?
- Which land types contribute most to potential?
- Where do legal/environmental restrictions constrain deployment?

**Dynamics & Policy Effects**
- Where is installed capacity growing fastest?
- Are there structural breaks after regulatory changes?
- Can a predictive model classify high vs. low deployment regions reliably?

---

### Analytical Dimensions
- Target variable: Installed capacity (MW)
- Features: Irradiation, wind speed, land use, grid proximity, demographics
- Methods: Regression models, classification models, SHAP analysis

</details>
