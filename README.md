# WGU-BSDA-Capstone

This project is my Capstone for the Bachelor of Science Data Analytics (BSDA) program at Western Governors University (WGU). Within this project are:

- This summary (`README.md`)
- Source and Compiled Data (`data/`)
- Exploratory Analysis (`eda/`)
- Proposal Documents (`proposal/`)
- Final Report (`report/`)

## Optimistic Analysis: Evaluating S&P 500 Analyst Accuracy

Analysis by Dustin Keate<br>
BSDA Program, WGU<br>
15 August 2026

### Project Description

Analysis of stock analyst sentiment bias against target revision directional accuracy.

By analyzing analyst revisions across the S&P 500 index, this project will seek to provide investors with a data-driven context to evaluate analyst performance based on historical analyst optimism.

### Research Question

Do financial analyst firms that exhibit a higher proportion of positive stock ratings (hereon “optimistic”) have better accuracy and success over different time horizons?

## Methodology

### Data Collection

My primary data, the S&P 500 analyst set, was obtained from a publically available Kaggle data set, cited below (Urad, 2026).

### Data Cleaning

In order to make the data set more usable and accurate, the following actions were performed:

1. Convert ```event_date``` from a ```str``` object to a ```datetime``` object.
2. Remove entries with a missing ```firm``` entry.
3. Remove rows missing accurate ```forward_return``` entries. Specifically, rows with an ```event_date``` on or before ```2014-12-03```

### Data Created

Using the FMP API @ https://site.financialmodelingprep.com/developer/docs, analyze closing prices to identify market downturns, including corrections and bear markets.

### Exploratory Data Analysis

My core analysis is focused around calculating 2 derivative metrics, ```firm_optimism``` and ```firm_accuracy```, and comparing them visually using a scatterplot. From this exploratory analysis, there appeared to be a direct link between analyst performance and optimism.

### Analyst Correlation and p-value

I performed a Pearson Correlation test. The results show that analyst optimism is *moderately* correlated to accuracy and this correlation is *very* likely accurate.

Time Period |Pearson Correlation (r) |p-value
------------|------------------------|--------
30 Days     |0.319                   |0.00137
90 Days     |0.352                   |3.77e-04
180 Days    |0.546                   |6.04e-09
365 Days    |0.594                   |1.84e-10

### Time Period Correlation and p-value

I also perform Pearson Correlation tests for predictions during periods of market downturns. The results of this were inconclusive.

Time Period |Pearson Correlation (r) |p-value
------------|------------------------|--------
30 Days     |-0.272                  |0.0161
90 Days     |-0.247                  |0.0294
180 Days    |-0.0283                 |0.806
365 Days    |0.0505                  |0.661

## Findings

Analyst firms classified as optimistic show a higher rate of directional accuracy compared to the remaining analyst population.

## Tools

- WSL w/ Ubuntu
- Conda
- Python
  - pandas
  - matplotlib
  - scipy
  - seaborn
  - requests
  - json
- VS Code
- JupyterLab
- GitHub

## Data Source

Urad. (2026). S&P 500 Analyst Rating and Price Target Accuracy [Data set]. Kaggle. https://www.kaggle.com/datasets/uradkr/s-and-p-500-analyst-rating-and-price-target-accuracy

## License

CC BY-NC-SA 4.0

https://creativecommons.org/licenses/by-nc-sa/4.0/
