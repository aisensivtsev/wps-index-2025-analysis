# Women, Peace & Security Index 2025 — Project Writeup

**Repository:** [aisensivtsev/wps-index-2025-analysis](https://github.com/aisensivtsev/wps-index-2025-analysis)  
**Author:** Aisen Sivtsev  
**Date:** February 2026

---

## Project Overview

This project analyzes the **Women, Peace and Security (WPS) Index 2025** dataset to explore global patterns related to women's wellbeing, security, and inclusion across countries.

The goal is to transform structured data into meaningful insights using Python data analysis tools. The analysis focuses on identifying patterns across regions, highlighting high- and low-performing countries, and visualizing the key components of the WPS Index.

The project demonstrates the full data analysis workflow:

- loading and cleaning a dataset
- exploring variables and distributions
- performing exploratory data analysis (EDA)
- visualizing patterns across countries
- communicating insights clearly

---

## Dataset

**Source:** Women, Peace and Security Index 2025 (Georgetown Institute for Women, Peace and Security / PRIO)

The dataset covers 181 countries scored on 13 indicators grouped into three dimensions:

| Dimension | Indicators |
|---|---|
| **Inclusion** | Education, employment participation, political participation |
| **Justice** | Legal discrimination, access to justice, equality under the law |
| **Security** | Personal safety, organized violence, intimate partner violence |

Each country receives a composite WPS score (0–1) combining all three dimensions.

---

## Tools Used

| Library | Purpose |
|---|---|
| `pandas` | Data loading, cleaning, and manipulation |
| `matplotlib` | Core data visualization |
| `seaborn` | Statistical charts and heatmaps |
| `Jupyter Notebook` | Interactive analysis workflow |

---

## Data Processing Workflow

### 1. Data Loading
The dataset used in this project comes from the **Women, Peace and Security (WPS) Index 2025**.

The original dataset was provided in **Excel (.xlsx) format** and was converted to **CSV format** for easier processing in Python using the pandas library.

Working with CSV files simplifies data loading and allows the dataset to be easily imported into analysis tools such as pandas and Jupyter Notebook.

### 2. Data Cleaning
- Removed or handled missing values
- Verified and corrected data types
- Standardized country name formatting
- Prepared all indicator variables for analysis

### 3. Exploratory Analysis
Basic statistics and distributions were examined to understand:
- average WPS scores globally and by region
- score variability across countries
- correlations between indicators and the composite score

### 4. Visualization
Charts were created to surface patterns in the data, including:
- distribution of WPS scores across all countries
- country-level comparisons (top and bottom performers)
- regional differences in scores
- relationships between the Inclusion, Justice, and Security dimensions

---

## Key Findings

**Security is the most volatile dimension.** Security indicators — particularly organized conflict and proximity to conflict — show the widest spread across countries and have a strong pull on overall scores. Countries affected by active conflict almost universally rank in the lower half of the index.

**Legal protections matter.** Countries with stronger legal frameworks for women (fewer discriminatory laws, stronger access to justice) tend to score higher overall — and this relationship holds even when controlling for income level.

**Regional inequality is significant.** Sub-Saharan Africa and South Asia show the widest within-region variation, meaning regional averages can be misleading. Europe and Central Asia cluster most tightly at the top.

**A small group of countries leads across all three dimensions.** Nordic countries consistently rank in the top tier across Inclusion, Justice, and Security simultaneously — suggesting that no single dimension drives their performance alone.

**Political participation diverges from economic inclusion.** High female employment and education do not reliably predict high parliamentary representation. Several high-income countries score poorly on political participation, indicating that economic and political empowerment follow different trajectories.

---

## Repository Structure

```
wps-index-2025-analysis/
│
├── data/                          # dataset files (gitignored)
├── wps_index_2025_analysis.ipynb  # Jupyter analysis notebook
├── wps_index_2025_analysis.html   # rendered HTML (best for reading)
├── wps_index_2025_analysis.md     # Markdown export for GitHub preview
├── wps_index_2025_analysis_files/ # images linked from Markdown export
├── WRITEUP.md                     # this document
├── REFLECTION.md                  # personal course reflection
├── README.md                      # project overview
└── .gitignore
```

**Recommended viewing:** Open `wps_index_2025_analysis.html` in a browser for the best experience — visualizations are fully rendered and the narrative flows without interruption from code cells.

---

## AI Use Statement

AI tools were used during this project as coding and writing assistants. AI helped with debugging Python code, suggesting visualization approaches, and explaining errors in pandas operations. All analysis decisions, interpretation of results, and final outputs were reviewed and edited manually.

---

## Limitations

- The composite score aggregates complex factors into a single number, which can mask within-country inequality and regional variation.
- Findings describe associations, not causal relationships.
- For countries in active conflict, some indicators may rely on older survey data or estimates.
- Cultural and institutional context that shapes women's outcomes is difficult to quantify and is not directly captured in the index.

---

## Future Improvements

- **Time-series analysis:** Merge the 2019, 2021, 2023, and 2025 editions to track which countries are improving fastest
- **Regional deep-dives:** Disaggregate findings within regions that show high variability
- **Interactive dashboard:** Convert key charts into a Plotly Dash or Streamlit app
- **Additional datasets:** Integrate GDP, conflict event data, or education spending to explore predictors of WPS score change over time

---

*Data sourced from the Georgetown Institute for Women, Peace and Security (GIWPS).*
