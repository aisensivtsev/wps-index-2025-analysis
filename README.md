## Data Source: Women, Peace and Security (WPS) Index 2025/26

The dataset used in this analysis comes from the **Women, Peace and Security (WPS) Index 2025/26**, produced by the **Georgetown Institute for Women, Peace and Security (GIWPS)** in collaboration with the **Peace Research Institute Oslo (PRIO)**, with support from the Government of Norway.

The WPS Index evaluates and ranks **181 countries** based on women’s overall wellbeing. Scores range from **0 (worst)** to **1 (best)** and are calculated using **13 indicators** that span three core dimensions:

A single country is represented by each row in the dataset, and a rank, an overall index score, or one of the component indicators used to calculate the final score are represented by each column.

According to the 2025/26 Index, **Denmark ranks highest globally**, while **Afghanistan ranks lowest**, highlighting persistent global inequalities in women’s status. The report notes that global progress on women’s rights has stalled in recent years, though improvements have occurred in some conflict-affected countries.

The WPS Index is designed to support evidence-based policymaking, track trends over time, and hold governments accountable for commitments to advance women’s rights and security.

Source: Georgetown Institute for Women, Peace and Security (GIWPS), Women, Peace and Security Index 2025/26.
# Women, Peace and Security Index – Data Exploration

## Data Source
This project analyzes data from the 2025/26 Women, Peace and Security Index,
produced by the Georgetown Institute for Women, Peace and Security (GIWPS).

The dataset ranks 181 countries using indicators across inclusion, justice,
and security.

## Data Analysis
This project uses **exploratory data analysis (EDA)** to examine cross-country patterns
in women’s wellbeing, institutional inclusion, and security outcomes. The analysis
focuses on identifying broad relationships between social, political, and conflict-related
factors rather than making causal claims or predictions.

## Key Insights
- Countries with lower proximity to armed conflict generally achieve higher overall
  Women, Peace, and Security Index scores.
- Higher levels of education and employment tend to be associated with greater
  parliamentary representation of women.
- Indicators related to safety and legal protections vary widely across regions,
  highlighting persistent global inequalities in women’s security and access to justice.


## Files
- `analysis.ipynb` – exploratory data analysis and visualizations
- `analysis.html` – rendered notebook (best viewing experience)
- `analysis.md` – markdown export for GitHub preview

## Notes
Raw data files are excluded from the repository via `.gitignore`.

## Limitations
The WPS Index aggregates complex social, legal, and security indicators into a single
composite score, which may mask within-country inequalities and regional variation.
Additionally, cultural and historical influences on women’s status are difficult to
quantify and are not directly measured in the dataset.


# Reflection: .ipynb, .html, and .md Files on GitHub
## What do three files look like online?

The three exported formats of the analysis serve different purposes when viewed on GitHub:

Jupyter Notebook (.ipynb)
The notebook displays all code cells, markdown explanations, and outputs together. However, on GitHub it can feel slightly cluttered, as the code and visualizations compete for attention. While it is excellent for reproducibility and transparency, it is not the most reader-friendly format for a general audience.

HTML Export (.html)
The HTML version provides the best viewing experience. All charts are rendered at full resolution, formatting is preserved, and the narrative flows smoothly without requiring the reader to interpret code. This format is ideal for presenting findings to non-technical audiences or stakeholders.

Markdown Export (.md)
The markdown file integrates well with GitHub’s interface and is easy to skim. Text renders cleanly, but images are stored in a separate folder and referenced externally. This can sometimes make the visuals feel less seamless compared to the HTML version.

## Which one looks best?

Overall, the HTML file appears the best. It is the best choice for presenting insights because it strikes a balance between readability, clarity, and visual quality. The notebook is more appropriate for development and reproducibility than for presentation, but the markdown file is a close second for GitHub-native viewing.

## Where are the images?

In the .ipynb, images are embedded directly within the notebook outputs.

In the .html, images are fully embedded in the document itself.

In the .md, images are stored in a separate directory (e.g., wps_index_2025_analysis_files/) and linked within the markdown file.

This highlights how different export formats handle visual assets differently, even when generated from the same notebook.

## How to View
For the best viewing experience, open the `analysis.html` file directly in a web browser.
The Jupyter Notebook (`.ipynb`) is included for transparency and reproducibility.

