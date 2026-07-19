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

Do financial analyst firms that exhibit a higher proportion of positive stock ratings (hereon “optimistic”) have better accuracy and success over 90-day and 365-day horizons?

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

TODO

### Null Hypothesis

TODO

### Correlation Testing

TODO

### p-value Calculation

TODO

### Model Training

TODO

### Model API

TODO

## Findings

TODO

### Statistical Significance

TODO

Return Horizon | p-value
---------------|--------
 30 days       | 
 90 days       | 
180 days       | 
365 days       | 

## Tools

- WSL w/ Ubuntu
- Conda
- Python
  - pandas
  - numpy
  - scikit-learn
  - matplotlib
  - scipy
  - seaborn
- VS Code
- JupyterLab
- GitHub

## Data Source

Urad. (2026). S&P 500 Analyst Rating and Price Target Accuracy [Data set]. Kaggle. https://www.kaggle.com/datasets/uradkr/s-and-p-500-analyst-rating-and-price-target-accuracy

## License

CC BY-NC-SA 4.0

https://creativecommons.org/licenses/by-nc-sa/4.0/
