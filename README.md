# Movie Budget & Revenue Prediction using Linear Regression

Welcome to the **Movie Budget & Financial Performance Records** analysis project, conducted at **DataPulse Data Science Lab**. This project explores how film industry budgets have evolved over time and uses Machine Learning to predict worldwide box office revenue based on production costs.

---

## Project Overview & Domain
* **Domain:** Exploratory Data Analysis (EDA), Data Cleaning, Business Analytics, and Predictive Modeling.
* **Core Goal:** To clean dirty financial records and find the relationship between movie budgets and their worldwide gross revenue.
* **Tech Stack:** Python, Pandas, NumPy, Seaborn, Matplotlib, and Scikit-Learn.

---

## Key Steps Completed

1. **Data Cleaning & Type Conversion:**
   * Removed unwanted characters (like `$`, `,`) from financial columns.
   * Converted data types from generic `object` (text) to precise numeric `int64` format.
   * Dropped invalid data points (such as unreleased future films) using dataframe index filtering.

2. **Statistical Analysis:**
   * Investigated dataset metrics (`mean`, `median`, and `std`).
   * Analyzed high **Standard Deviation (std)** values which revealed extreme variation between low-budget indie films and mega-blockbuster outliers.
   * Isolated and calculated the exact proportion of money-losing films.

3. **Predictive Modeling (Linear Regression):**
   * Separated the dataset into two distinct eras (Old Films $\le$ 1960 vs. New Films $>$ 1960).
   * Developed a **Linear Regression** model using Scikit-Learn to estimate revenues.

---

## Core Insights & Model Parameters

### New Era Films Model (Post-1960)
* **Slope (Coefficient):** `~3.12`
  * *Insight:* For every **$1** invested in a movie's production budget, it generates an estimated **$3.12** in worldwide revenue.
* **Intercept:** `-$8,650,768`
  * *Insight:* Reflects the high-risk nature of the modern movie business where a zero-budget scenario theoretical forces a baseline loss.

### Old Era Films Model (Pre-1960)
* **Slope (Coefficient):** `~1.65`
  * *Insight:* Older films had significantly lower earning multiplication power compared to modern blockbusters.
* **Intercept:** `+$22,821,539`

---

## Visualizations Generated
The project features several key statistical plots that have been saved directly to the workspace:
* `results/budget_vs_revenue_scatter.png` — General distribution of production costs vs. worldwide gross.
* `results/movie_trends_over_years.png` — A detailed bubble plot scaling dots by revenue across different release decades.
* `results/old_films_regression.png` — Linear trend line for classic cinema data.
* `results/new_films_regression.png` — High-resolution regression plot showing modern box office trajectory.

---

## How to Run
1. Open the uploaded `.ipynb` notebook file directly in Google Colab.
2. Ensure you have the `cost_revenue_dirty.csv` file inside your runtime directory.
3. Run all cells sequentially to reproduce the metrics and regression slopes!
