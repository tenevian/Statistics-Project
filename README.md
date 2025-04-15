# Health and Income Level Analysis

## Overview
This project investigates the relationship between income levels (represented by GDP per capita) and various health indicators, including physical and mental health, across different countries in 2019. The analysis is performed using publicly available datasets and is implemented in Python using Pandas, Matplotlib, and other libraries.

## Research Question
What is the relationship between income level and health elements (physical and mental)?

## Hypothesis
Higher income levels are associated with better physical health but worse mental health. This is based on the assumption that:

- Wealthier countries have better access to healthcare infrastructure, thus improving physical health.
- Mental health disorders might be more frequently reported or diagnosed in wealthier societies, possibly due to lifestyle stressors and greater awareness.

## Variables

### Independent Variable
- GDP per capita (2019) — Represents the income level of each country. (Source: World Bank)

### Dependent Variables
- Mental Illness Share (%) — Share of population diagnosed with mental health disorders.
- Cardiovascular Disease Prevalence (%) — Prevalence rate in the population.
- Undernourishment Prevalence (%) — Share of population suffering from undernutrition.

## Data Sources
Data was collected from publicly available sources via Google Drive:

- `gdp2019.csv`: GDP per capita for each country.
- `mental.csv`: Share of mental health disorders in population.
- `cardio.csv`: Prevalence of cardiovascular disease.
- `undernurished.csv`: Prevalence of undernourishment.

Data for the year 2019 was extracted and merged for consistent analysis.

## Setup Instructions

### Install Required Packages
```bash
pip install matplotlib pandas gdown
```

### Download Datasets
Files are downloaded programmatically using gdown. Make sure you are connected to the internet and have access to Google Drive files.

### Run the Notebook
Use Jupyter Notebook or VSCode with a Python environment to run the analysis.

## Data Preprocessing
1. Removed non-country rows.
2. Standardized and renamed columns across datasets.
3. Filtered only 2019 data.
4. Removed rows with missing values.
5. Merged datasets on country code.
6. Handled outliers using the IQR method.

## Analysis Performed
- Scatter plots visualizing correlation between GDP and:
  - Mental illness share
  - Cardiovascular disease prevalence
  - Undernourishment prevalence
- Data inspection and cleaning routines.
- Basic exploratory data analysis (EDA).

## Visualizations
The project uses Matplotlib for creating scatter plots to visually represent:
- GDP vs Mental Illness
- GDP vs Cardiovascular Disease
- GDP vs Undernourishment

These plots help illustrate any observable correlations.

## Key Observations
- A general trend suggests that higher GDP is associated with lower rates of undernourishment and cardiovascular diseases.
- The relationship between GDP and mental illness is more complex and might suggest a U-shaped curve or noise due to cultural differences in reporting.

## File Structure
```
├── README.md
├── health_income_analysis.ipynb
├── gdp2019.csv
├── mental.csv
├── cardio.csv
├── undernurished.csv
```

## Future Work
1. Perform regression analysis to quantify the relationships.
2. Explore multivariate modeling to account for confounding variables.
3. Integrate regional or demographic breakdowns for finer insights.

