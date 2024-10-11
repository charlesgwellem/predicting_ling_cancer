# Predicting Lung Cancer

## Overview
This repository contains an R script for analyzing and predicting lung cancer risk using a dataset that includes demographic, lifestyle, and health-related factors. The script processes the data, performs various statistical analyses, and applies machine learning techniques like Lasso regression and logistic regression to identify key predictors of lung cancer.

## Dataset
The dataset consists of the following columns:

- **GENDER**: The individual's gender (Male/Female).
- **AGE**: The individual's age (numeric).
- **SMOKING**: Whether the individual is a smoker (Yes/No).
- **YELLOW_FINGERS**: Whether the individual has yellow fingers (Yes/No).
- **ANXIETY**: Whether the individual suffers from anxiety (Yes/No).
- **PEER_PRESSURE**: Whether the individual is influenced by peer pressure (Yes/No).
- **CHRONIC_DISEASE**: Whether the individual has chronic diseases (Yes/No).
- **FATIGUE**: Whether the individual experiences fatigue (Yes/No).
- **ALLERGY**: Whether the individual has allergies (Yes/No).
- **WHEEZING**: Whether the individual has wheezing symptoms (Yes/No).
- **ALCOHOL_CONSUMING**: Whether the individual consumes alcohol (Yes/No).
- **COUGHING**: Whether the individual has a coughing symptom (Yes/No).
- **SHORTNESS_OF_BREATH**: Whether the individual experiences shortness of breath (Yes/No).
- **SWALLOWING_DIFFICULTY**: Whether the individual has difficulty swallowing (Yes/No).
- **CHEST_PAIN**: Whether the individual experiences chest pain (Yes/No).
- **LUNG_CANCER**: Whether the individual has been diagnosed with lung cancer (Yes/No).

## Key Analyses
The script covers the following key analyses:

1. **Data Preprocessing**:
   - Conversion of binary columns (Yes/No) to numeric (1/0).
   - Recoding of the gender column (M/F) to numeric (1 for male, 0 for female).

2. **Correlation Analysis**:
   - A point-biserial correlation is computed between continuous variables (e.g., age) and binary variables to assess linear relationships.
   - Results show weak correlations, indicating minimal linear relationships between the variables.

3. **Chi-Square Test**:
   - Chi-square tests are performed to analyze relationships between categorical variables and lung cancer.
   - Wheezing shows a statistically significant association with lung cancer, while other variables do not.

4. **Lasso Regression**:
   - Lasso regression is used to select important predictors for lung cancer.
   - Wheezing emerges as the most important predictor of lung cancer based on Lasso regression.

5. **Logistic Regression**:
   - Logistic regression is performed with wheezing as the key predictor, with an Area Under the Curve (AUC) of 0.519, suggesting poor model performance.
   - Further feature engineering and more complex models are recommended for improvement.

## Installation
To run this script, make sure you have the following R packages installed:

- `ggplot2`
- `corrr`
- `tidyverse`
- `patchwork`
- `glmnet`
- `caret`
- `pROC`
- `vcd`

You can install these packages using the command:

```r
install.packages(c("ggplot2", "corrr", "tidyverse", "patchwork", "glmnet", "caret", "pROC", "vcd"))
```

## How to Run
1. Load the dataset from the `raw_data` directory.
2. Run the script from top to bottom for the analysis.
3. The results of statistical tests and regression models will be printed in the console, and key plots will be generated.

## Future Improvements
- **Feature Engineering**: Adding or transforming features could improve the model.
- **Model Complexity**: Exploring more complex models such as Random Forest or Gradient Boosting might yield better results.
- **Regularization**: Fine-tuning regularization parameters could improve performance.
- **Data Quality**: Ensuring high data quality and feature relevance is essential for accurate predictions.

## License
This project is open-source and can be modified to suit your needs.
