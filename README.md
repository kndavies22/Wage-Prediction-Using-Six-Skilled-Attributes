# Wage Prediction Using Six Skill Attributes

This project applies a full data analysis pipeline to the FIFA 21 player dataset to explore whether a player's weekly wage can be predicted from their six skill attributes and player type. The analysis also uses Principal Component Analysis (PCA) to uncover underlying skill dimensions that separate player archetypes.

## Analytical Question

**Can we predict a player's weekly wage from their six skill attributes and player type, and what underlying skill dimensions separate player archetypes?**

## Project Structure

```
Wage-Prediction-Using-Six-Skilled-Attributes/
├── README.md
├── LICENSE
├── .gitignore
│
├── report/
│   └── wage_prediction.Rmd
│
├── output/
└── R/
```

## Dataset

The data used in this project is the **FIFA 21 Complete Player Dataset**, sourced from a publicly available Google Sheets URL. No local data file is required — the dataset is loaded automatically when the `.Rmd` file is run.

**Direct data URL:**
```
https://docs.google.com/spreadsheets/d/e/2PACX-1vRWpw5hL7DUtcb9k7NsVNsE4BPV9QPZ-w1uBTovoE6TbHDur3a0dwSCmiRjcZlyX-lQ3_PhfnkFfBhl/pub?gid=0&single=true&output=csv
```

The raw dataset contains 18,944 players across 106 columns covering identity information, skill scores, sub-attributes, and market data.

## How to Reproduce

1. Clone this repository
2. Open RStudio
3. Install the required libraries (see below)
4. Open `report/wage_prediction.Rmd`
5. Click **Run All** (or knit the document)

All data is loaded directly from the public URL above — no manual data download is needed. A fixed random seed (`set.seed(123)`) is used in the PCA step to ensure identical results on every run.

## Required Libraries

Install the following R packages before running the analysis:

```r
install.packages(c("tidyverse", "corrplot", "broom"))
```

| Package | Purpose |
|------------|--------------------------------------|
| tidyverse | Data wrangling and visualisation |
| corrplot | Correlation matrix visualisation |
| broom | Tidying regression model output |

## Analysis Pipeline

1. **Data Acquisition** — loading the FIFA 21 dataset from a public URL
2. **Data Understanding** — exploring how player scores are constructed
3. **Data Cleaning** — systematic 8-step framework
4. **Exploratory Data Analysis** — visualising distributions and relationships
5. **Statistical Modelling** — multiple linear regression to predict player wage
6. **Dimension Reduction** — PCA to identify underlying skill dimensions

## Key Findings

- Dribbling is the strongest predictor of wage among the six skill scores
- Defenders and Forwards earn ~50-52% more than Midfielders with identical skill scores
- The regression model explains 44.2% of wage variation (R² = 0.442)
- PCA reveals two fundamental skill dimensions: technical attacking ability (PC1) and defensive/physical ability (PC2)

## Author

Kevin Davies

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.
