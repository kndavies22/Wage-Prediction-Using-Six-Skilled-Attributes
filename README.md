# Wage Prediction Using Six Skill Attributes

This project applies a complete statistical analysis pipeline to the **FIFA 21 player dataset** to investigate whether a player's weekly wage can be predicted from their six skill attributes and player type. The analysis also uses **Principal Component Analysis (PCA)** to identify underlying skill dimensions that distinguish different player archetypes.

## Analytical Question

**Can a player's weekly wage be predicted from their six skill attributes and player type, and what underlying skill dimensions separate player archetypes?**

## Technologies & Methods

* **R**
* **R Markdown**
* **tidyverse** — Data wrangling and visualization
* **corrplot** — Correlation matrix visualization
* **broom** — Regression model output
* **Multiple Linear Regression**
* **Principal Component Analysis (PCA)**
* Exploratory Data Analysis
* Data Cleaning

## Project Structure

```text
Wage-Prediction-Using-Six-Skilled-Attributes/
├── README.md
├── LICENSE
├── .gitignore
│
├── report/
│   └── WAGE PREDICTION.Rmd
│
├── output/
└── R/
```

## Dataset

The analysis uses the **FIFA 21 Complete Player Dataset**, sourced from a publicly available Google Sheets dataset.

No local data file is required; the dataset is loaded automatically from the public URL when the `.Rmd` file is run.

**Direct data URL:**

```text
https://docs.google.com/spreadsheets/d/e/2PACX-1vRWpw5hL7DUtcb9k7NsVNsE4BPV9QPZ-w1uBTovoE6TbHDur3a0dwSCmiRjcZlyX-lQ3_PhfnkFfBhl/pub?gid=0&single=true&output=csv
```

The raw dataset contains **18,944 players across 106 columns**, covering player information, skill attributes, sub-attributes, and market data.

## How to Reproduce

1. Clone this repository.
2. Open the project in **RStudio**.
3. Install the required R packages listed below.
4. Open `report/WAGE PREDICTION.Rmd`.
5. Run all code or knit the document to reproduce the analysis.

All data is loaded directly from the public URL, so no manual data download is required.

A fixed random seed (`set.seed(123)`) is used during the PCA analysis to ensure reproducible results.

## Required Libraries

Install the required packages in R with:

```r
install.packages(c("tidyverse", "corrplot", "broom"))
```

| Package     | Purpose                          |
| ----------- | -------------------------------- |
| `tidyverse` | Data wrangling and visualization |
| `corrplot`  | Correlation matrix visualization |
| `broom`     | Tidying regression model output  |

## Analysis Pipeline

The project follows a structured statistical analysis workflow:

1. **Data Acquisition** — Loading the FIFA 21 dataset from a public URL.
2. **Data Understanding** — Examining the structure of the dataset and how player scores are constructed.
3. **Data Cleaning** — Applying a systematic eight-step data-cleaning framework.
4. **Exploratory Data Analysis** — Investigating distributions, relationships, and correlations among player attributes.
5. **Statistical Modelling** — Using multiple linear regression to investigate whether player wages can be predicted from skill attributes and player type.
6. **Dimension Reduction** — Applying PCA to identify underlying dimensions within the six skill attributes and examine player archetypes.

## Key Findings

* **Dribbling** was the strongest predictor of weekly wage among the six skill attributes.
* **Defenders and Forwards** earned approximately **50–52% more than Midfielders** with equivalent skill scores.
* The multiple linear regression model explained **44.2% of the variation in player wages** (`R² = 0.442`).
* PCA identified two major underlying skill dimensions: **technical attacking ability (PC1)** and **defensive/physical ability (PC2)**.

## Author

**Kevin Davies**

## License

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.
