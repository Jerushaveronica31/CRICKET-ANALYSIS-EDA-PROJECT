# CRICKET-ANALYSIS-EDA-PROJECT
# Cricket Batting Statistics — Exploratory Data Analysis (EDA)

An exploratory data analysis (EDA) workflow in Python built to clean, inspect, treat outliers, aggregate, and visualize cricket batting performance data from `batting_stats.csv`.

## Overview

This notebook walks through a structured EDA pipeline on a batting dataset (`batting_stats.csv`), covering data quality checks, missing value handling, duplicate removal, IQR-based outlier capping, team-wise aggregations, and multi-dimensional visualizations[cite: 1].

## Key Steps & Features

- **Initial Data Inspection:** Checks row/column dimensions, column names, data types, `.info()`, and summary statistics (`describe`)[cite: 1].
- **Missing Value Analysis & Imputation:** Calculates missing counts and percentages per column, visualizes missingness, and creates a cleaned dataset (`df_clean`) using median imputation for numeric columns and mode imputation for categorical columns[cite: 1].
- **Duplicate Detection:** Checks for exact duplicate rows and creates a deduplicated copy (`df_no_duplicates`)[cite: 1].
- **Outlier Detection & IQR Capping:** Computes Q1, Q3, IQR, and lower/upper fences (`1.5 × IQR`) for `runs`, clips extreme values across key batting columns (`runs`, `average`, `strike_rate`, `balls_faced`, `fours`, `sixes`), and compares **Before vs. After** box plots[cite: 1].
- **Team & Position Aggregations:** Summarizes `runs` (count, mean, median, min, max), `strike_rate`, `average`, and boundaries (`fours`, `sixes`) by `team`, as well as performance trends across batting `position`[cite: 1].
- **Data Visualizations:**
  - Histograms and density curves (`runs`, `strike_rate`)[cite: 1]
  - Bar and count plots by `team`[cite: 1]
  - Box plots and violin plots (`runs` distribution by `team`, before/after outlier capping)[cite: 1]
  - Scatter and bubble plots (`average` vs. `strike_rate`, `runs` vs. `strike_rate` sized/colored by `impact`, and `fours` vs. `sixes` sized by `runs`)[cite: 1]
  - Dual-axis line chart of average `runs` and `strike_rate` by batting `position`[cite: 1]
  - Pairplot across key numeric batting features[cite: 1]

## Tech Stack & Libraries

- **Python**
- **Pandas & NumPy** — Data loading, cleaning, imputation, grouping, and aggregations[cite: 1]
- **Matplotlib & Seaborn** — Statistical plots and visual comparisons[cite: 1]
- **SciPy** — Statistical utilities (`scipy.stats.mstats`)[cite: 1]
- **Google Colab** — Notebook environment[cite: 1]

## Project Structure

- `JERUSHA_VERONICA_EDA PROJECT.ipynb` (exported as `jerusha_veronica_eda_project.py`) — Complete EDA code and visualizations[cite: 1]
- `batting_stats.csv` — Input dataset (expected at `/content/batting_stats.csv` in Colab)[cite: 1]

## How to Run

1. Open the notebook in **Google Colab** or **Jupyter / VS Code**[cite: 1].
2. Ensure `batting_stats.csv` is available at `/content/batting_stats.csv` (or update the file path in `pd.read_csv(...)`)[cite: 1].
3. Run all cells sequentially from top to bottom to generate summary tables and charts[cite: 1].
