# Mini Project 2: Predicting Used Car Prices

## Overview
This project develops a data-driven approach to predict the prices of used cars using linear regression. It includes model selection, validation, and prediction with interval estimates for newly acquired cars.

## Files Included
- **`Presentation.pptx`**: Final presentation summarizing the problem, analysis, and results.
- **`usedCars.csv`**: Dataset of 94 used cars used for model training and analysis.
- **`newCars.csv`**: Dataset of newly acquired cars for which prices were predicted.
- **`newCarResults.csv`**: Final predictions for new cars with interval estimates.
- **`resFigs.R`**: R script to generate diagnostic plots for model validation.
- **`miniproject2.Rmd`**: R Markdown file containing the analysis and code.
- **`miniproject2.html`**: HTML output of the R Markdown file.
- **`Mini Project 2.Rproj`**: R project file for this analysis.

## Key Features
- **Problem Statement**: Understand and predict the sale price of used cars.
- **Model Selection**: Identified key predictors using statistical tests (e.g., forward selection, AIC).
- **Final Model**: Selected predictors: `Power`, `Transmission`, `FuelType`, `KmDriven`, `Mileage`.
- **Validation**: Assumptions verified using diagnostic plots (residuals, Cook’s distance, leverage, etc.).
- **Predictions**: Predicted car prices and provided interval estimates for uncertainty analysis.

## Instructions
1. **Data Preparation**:
   - Processed data (`usedCars.csv`) to create indicators for categorical variables like `Transmission` and `FuelType`.
   - Removed weak predictors (`Engine`, `Seats`, `Age`) based on statistical significance and model tests.

2. **Modeling**:
   - Log-transformed the target variable (`Price`) for better model accuracy.
   - Used linear regression with selected predictors.

3. **Prediction**:
   - Applied the model to `newCars.csv` to predict prices.
   - Generated prediction intervals for each new car.

4. **Validation**:
   - Assessed model validity using diagnostic plots and statistical measures (e.g., RMSE, MAE).

## Results
- **Accuracy Metrics**:
  - **MAE**: 368,185.1
  - **RMSE**: 444,295.7
  - **MAPE**: 25.2%
- **Key Insights**:
  - `Power` strongly correlates with price.
  - Mileage and `KmDriven` show weaker negative relationships with price.

## How to Use
1. Clone the repository:
   ```bash
   git clone <repository_url>
