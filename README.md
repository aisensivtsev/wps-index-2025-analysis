# Women, Peace and Security Index (2025/26): Project Overview
## Data Source

This analysis uses data from the Women, Peace and Security (WPS) Index 2025/26, produced by the Georgetown Institute for Women, Peace and Security (GIWPS) in collaboration with the Peace Research Institute Oslo (PRIO), with support from the Government of Norway.

The WPS Index evaluates 181 countries based on women’s overall wellbeing, inclusion, justice, and security. Scores range from 0 (lowest performance) to 1 (highest performance) and are calculated using 13 indicators grouped into three core dimensions.

In the dataset, each row represents a single country, while each column represents either the overall index score, the country’s rank, or one of the component indicators used to calculate the final score.

According to the 2025/26 Index, Denmark ranks highest globally, while Afghanistan ranks lowest, highlighting persistent global inequalities in women’s status. The report also notes that while global progress on women’s rights has largely stalled, some conflict-affected countries have experienced limited improvements.

The WPS Index is designed to support evidence-based policymaking, track trends over time, and hold governments accountable for commitments to advance women’s rights and security.

## Project Purpose

The goal of this project is to explore cross-country patterns in women’s wellbeing using exploratory data analysis (EDA). Rather than making causal claims or predictions, the analysis focuses on identifying broad relationships between social, political, legal, and conflict-related factors.

## Key Insights from the Analysis

Several clear patterns emerge from the data:

Countries with lower exposure to armed conflict generally achieve higher overall WPS Index scores.

Education and employment are often associated with greater parliamentary representation of women, though the relationship is not perfectly linear.

Indicators related to safety, legal protections, and justice vary widely across regions, underscoring persistent global inequalities in women’s security and rights.

These findings reinforce the idea that women’s wellbeing is shaped by multiple, interconnected dimensions rather than a single factor.

## Files Included in This Repository

This repository contains three versions of the same analysis, each serving a different purpose:

analysis.ipynb — The original Jupyter Notebook, including all code, explanations, and outputs.

analysis.html — A rendered version of the notebook optimized for reading and presentation.

analysis.md — A Markdown export designed for GitHub preview and quick skimming.

## Limitations of the Analysis

While the WPS Index provides a valuable comparative framework, it has important limitations:

The index aggregates complex social, legal, and security factors into a single score, which can mask within-country inequalities and regional variation.

Cultural, historical, and institutional influences on women’s status are difficult to quantify and are not directly measured in the dataset.

As an exploratory analysis, the findings should be interpreted as associations rather than causal relationships.

# Reflection on File Formats: .ipynb, .html, and .md
## How the Files Appear on GitHub

Each file format offers a different viewing experience:

Jupyter Notebook (.ipynb)

The notebook displays code cells, narrative text, and visual outputs together. While this format is excellent for transparency and reproducibility, it can feel cluttered on GitHub because readers must navigate both code and results simultaneously.

HTML Export (.html)

The HTML version provides the best overall viewing experience. Visualizations are fully rendered, formatting is preserved, and the narrative flows without interruption from code. This format is ideal for presenting findings to non-technical audiences or stakeholders.

Markdown Export (.md)

The Markdown file integrates well with GitHub’s interface and is easy to skim. However, images are stored in a separate directory and linked externally, which can make the visual experience feel less seamless compared to the HTML version.

## Best Format for Presentation

Overall, the HTML file is the strongest choice for presenting insights. It balances clarity, visual quality, and readability, making it well suited for audiences who want to focus on results rather than code.

## Where the Images Are Stored

In the .ipynb, images are embedded directly within the notebook outputs.

In the .html, images are fully embedded in the document itself.

In the .md, images are saved in a separate directory (for example, wps_index_2025_analysis_files/) and linked within the Markdown file.

This highlights how the same analysis can be displayed differently depending on the export format.

## How to View This Project

For the best viewing experience, open the analysis.html file directly in a web browser.
The Jupyter Notebook (analysis.ipynb) is included to support transparency and reproducibility for readers who wish to examine the underlying code.