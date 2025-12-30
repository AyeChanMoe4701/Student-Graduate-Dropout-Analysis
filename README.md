# Student Graduate Dropout Analysis

## Overview

This notebook performs systematic data cleaning, exploratory analysis, and feature evaluation on a student graduation and dropout dataset. The analysis focuses on improving data quality, validating the feature space, and identifying the most influential variables associated with student outcomes. Emphasis is placed on redundancy reduction, fairness considerations, and robust feature selection rather than predictive performance.

## Techniques Used

The following data cleaning and analysis techniques were applied:

* Initial data inspection, including verification of the number of records, columns, and variable types
* Detection and removal of null values and duplicate records
* Column renaming to improve clarity, consistency, and usability
* Multicollinearity assessment using Variance Inflation Factor (VIF) to identify and remove invariant or redundant features
* Feature engineering (e.g., total units enrolled/approved), followed by correlation analysis and feature removal where redundancy was confirmed
* Exploratory data visualization to examine distributions of key variables
* Fairness analysis using true positive rates to assess outcome-related disparities
* Correlation analysis to examine linear relationships between features
* Principal Component Analysis (PCA) to validate the feature space and assess dimensionality; the first 15 components explained over 90% of the total variance
* Random Forest feature importance to rank variables based on their contribution within an ensemble classifier
* Shortlisting of 10 consistently high-ranking features based on Random Forest importance scores

## Key Insights

The analysis shows that the original feature set contains substantial redundancy, which can be effectively reduced through multicollinearity checks and dimensionality reduction. PCA results indicate that most of the dataset’s variance can be captured with a significantly smaller number of components, supporting feature space simplification. Random Forest feature importance further highlights a small subset of variables that consistently contribute most to outcome differentiation. Together, these results justify the selection of a reduced and more informative feature set while maintaining interpretability and supporting downstream modeling or fairness analysis.
