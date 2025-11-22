# Formula 1 Race Outcome Analysis (2014–2024)

## Project Overview

This project analyzes Formula 1 race results from 2014 to 2024 to understand how factors like **grid position**, **pit stops**, and **team performance** influence race outcomes. We also build predictive models to estimate the likelihood of finishing in top positions and identify key predictors.
![Formula 1 Logo](visuals/formula-1-logo-racing-free-vector.png)


## Features & Analyses

### 1. Exploratory Data Analysis (EDA)

* Investigated distributions of **grid positions**, **finish positions**, and **positions gained/lost**.
* Examined relationships between **starting position and race outcome**, confirming that drivers starting near the front generally finish higher.
* Created visualizations like scatterplots, heatmaps, and bar charts to summarize race trends.

### 2. Grid Position Analysis

* Analyzed correlation between **grid position** and **finish position**.
* Pearson correlation: 0.77, indicating a strong positive relationship.
* Linear regression showed that starting position explains ~59% of the variance in finish position.
* Calculated **win percentages by grid position (P1–P10)**, highlighting that front-row starters win most races.

### 3. Pit Stop Analysis

* Merged race results with **pit stop data** to analyze total pit stop times per driver.
* Computed **positions gained/lost** and measured the effect of pit stop efficiency on race outcomes.
* Visualized the relationship between **total pit time and positions gained/lost**, showing shorter pit stops generally correlate with better positions.
* Calculated team-wise average pit stop effectiveness (`pitEffect`) for comparison.

### 4. Predictive Modeling

* **Top 3 Finishes:** Built a logistic regression model using **grid position**, **pitEffect**, and **constructor/team** as features.
* **Position Groups:** Classified drivers as **Top5**, **Midfield**, or **Backmarker** using a Random Forest model.
* Model performance:

  * Logistic Regression Accuracy: 92%
  * Random Forest Accuracy: 88%
* Tested models on individual driver race data to verify predictions.

### 5. Key Findings

* Major predictors of race outcome: **grid position**, **pit stop efficiency**, and **team constructor**.
* Efficient pit stops can significantly influence positions gained.
* Starting near the front greatly increases the likelihood of winning or finishing in top positions.
* Random Forest feature importance highlights which variables contribute most to race outcomes.

## Data Sources

* Formula 1 official datasets (2014–2024):

  * `races.csv`
  * `qualifying.csv`
  * `results.csv`
  * `drivers.csv`
  * `pit_stops.csv`
* Cleaned & merged dataset: `merged_f1_data_clean.csv`

## Tools & Libraries

* Python: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`, `statsmodels`

## Future Work

* Include **weather**, **tire wear**, **safety car effects**, or **track conditions** to improve predictive models.
* Explore **driver-specific trends** and **team strategy impacts** over multiple seasons.

