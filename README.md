## Data Source: Women, Peace and Security (WPS) Index 2025/26

The dataset used in this analysis comes from the **Women, Peace and Security (WPS) Index 2025/26**, produced by the **Georgetown Institute for Women, Peace and Security (GIWPS)** in collaboration with the **Peace Research Institute Oslo (PRIO)**, with support from the Government of Norway.

The WPS Index evaluates and ranks **181 countries** based on women’s overall wellbeing. Scores range from **0 (worst)** to **1 (best)** and are calculated using **13 indicators** that span three core dimensions:

Each row in the dataset represents a single country, and each column represents either an overall index score, a rank, or one of the component indicators used to compute the final score.

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
The analysis explores:
- Distribution of the WPS Index across countries
- Relationships between conflict exposure and women’s safety
- Links between education, employment, and political representation

## Files
- `analysis.ipynb` – exploratory data analysis and visualizations
- `analysis.html` – rendered notebook (best viewing experience)
- `analysis.md` – markdown export for GitHub preview

## Notes
Raw data files are excluded from the repository via `.gitignore`.

## Reflection: .ipynb, .html, and .md Files on GitHub
## What do your three files look like online?

The three exported formats of the analysis serve different purposes when viewed on GitHub:

Jupyter Notebook (.ipynb)
The notebook displays all code cells, markdown explanations, and outputs together. However, on GitHub it can feel slightly cluttered, as the code and visualizations compete for attention. While it is excellent for reproducibility and transparency, it is not the most reader-friendly format for a general audience.

HTML Export (.html)
The HTML version provides the best viewing experience. All charts are rendered at full resolution, formatting is preserved, and the narrative flows smoothly without requiring the reader to interpret code. This format is ideal for presenting findings to non-technical audiences or stakeholders.

Markdown Export (.md)
The markdown file integrates well with GitHub’s interface and is easy to skim. Text renders cleanly, but images are stored in a separate folder and referenced externally. This can sometimes make the visuals feel less seamless compared to the HTML version.

## Which one looks best?

The HTML file looks the best overall. It balances clarity, visual quality, and readability, making it the strongest option for presenting insights. The markdown file is a close second for GitHub-native viewing, while the notebook is best suited for development and reproducibility rather than presentation.

## Where are the images?

In the .ipynb, images are embedded directly within the notebook outputs.

In the .html, images are fully embedded in the document itself.

In the .md, images are stored in a separate directory (e.g., wps_index_2025_analysis_files/) and linked within the markdown file.

This highlights how different export formats handle visual assets differently, even when generated from the same notebook.

