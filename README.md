# Economic Freedom Index 2019: Exploratory Data Analysis

An R-based exploratory analysis of economic freedom across 186 countries. This project examines how overall economic freedom varies across regions and relates to institutional and macroeconomic indicators, including property rights, judicial effectiveness, government integrity, trade freedom, GDP per capita, GDP growth, and population.

## Project Overview

The analysis uses the Heritage Foundation's 2019 Index of Economic Freedom dataset, which contains 34 country-level variables. After cleaning and converting the relevant fields, I used descriptive statistics and visual analysis to explore three central questions:

- Which institutional and economic factors are most closely associated with economic freedom?

- How do economic freedom and GDP per capita differ across regions?

- What distinguishes the countries at the highest and lowest ends of the index?

## Key Findings

- Institutional measures had the strongest relationships with the overall score. In the complete-case correlation matrix, economic freedom was strongly correlated with property rights (r = 0.86), judicial effectiveness (r = 0.81), and government integrity (r = 0.80).

- Economic freedom and prosperity were positively related. GDP per capita had a moderate positive correlation with economic freedom (r = 0.64).

- Short-term growth and country size explained comparatively little. Annual GDP growth had a weak correlation with economic freedom (r = 0.18), while population had almost no linear relationship (r = -0.04).

- Regional differences were substantial. Europe had the highest mean economic freedom score (68.6), while Sub-Saharan Africa had the lowest (54.2).

- The extremes of the index showed wide institutional gaps. The five highest-scoring countries consistently outperformed the five lowest-scoring countries across property rights, government integrity, business freedom, trade freedom, investment freedom, and financial freedom.

These findings describe associations within the 2019 data and should not be interpreted as evidence of causation.

## Analysis Workflow

1. Cleaned currency-formatted and character fields and converted selected variables to numeric values.

2. Summarized the distributions of economic freedom and property rights using descriptive statistics, histograms, and density plots.

3. Log-transformed GDP per capita to improve regional comparisons.

4. Calculated a complete-case Pearson correlation matrix for selected institutional and economic indicators.

5. Compared countries across regions and quantile-based categories using scatterplots, boxplots, and grouped summaries.

6. Profiled the five highest- and lowest-scoring countries across key index components.

7. Compiled the code, visualizations, results, and interpretation into a reproducible PDF report with R Markdown.

## Tools and Skills

- R: data cleaning, transformation, aggregation, and statistical analysis

- tidyverse / dplyr: data wrangling and grouped summaries

- ggplot2 / ggpubr: exploratory visualizations

- corrplot / reshape2: correlation and comparative analysis

- R Markdown: reproducible reporting and PDF generation

## Repository Structure

| File | Description |
| --- | --- |
| [`Economic_Freedom_Index_Case_Study.Rmd`](./Economic_Freedom_Index_Case_Study.Rmd) | R Markdown source containing the full analysis |
| [`Economic_Freedom_Index_Case_Study.pdf`](./Economic_Freedom_Index_Case_Study.pdf) | Rendered 37-page report with code, visualizations, and conclusions |
| [`economic_freedom_index2019_data.csv`](./economic_freedom_index2019_data.csv) | Country-level source data used in the analysis |

## Data Source

The dataset is based on the Heritage Foundation's 2019 Index of Economic Freedom, which evaluates policies and economic conditions across 186 countries. The copy used for this analysis is included in the repository for reproducibility.

## Limitations

- This is a cross-sectional analysis of a single year, so it cannot establish causal or time-series relationships.

- Several institutional variables analyzed here are inputs to the overall Economic Freedom score. Their correlations with the total partly reflect how the index is constructed.

- Six countries do not have a reported overall score, and selected variables contain additional missing values.

- Pearson correlations summarize linear relationships and may not capture nonlinear patterns or confounding factors.
