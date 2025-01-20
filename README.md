# The-Elements-Of-Statistical-Learning
This repository contains self projects of the book "The Elements Of Statistical Learning"

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# South African Heart Disease Analysis Project

## Overview
This project analyzes data from the Coronary Risk-Factor Study (CORIS) baseline survey conducted in three rural areas of the Western Cape, South Africa. The study focuses on identifying and analyzing risk factors for ischemic heart disease in a high-incidence region.

## Dataset
- **Population**: White males between 15 and 64 years old
- **Sample Size**: 462 subjects (160 cases, 302 controls)
- **Collection Method**: Case-control study with retrospective sampling
- **Source**: Rousseauw et al., 1983, South African Medical Journal

### Features
- Systolic blood pressure (sbp)
- Cumulative tobacco consumption (kg)
- Low-density lipoprotein cholesterol (ldl)
- Family history of heart disease (famhist)
- Type-A behavior
- Obesity measures
- Alcohol consumption
- Age
- Coronary Heart Disease status (target variable)

## Methods & Techniques

### 1. Logistic Regression Analysis
- Initial model with all variables
- Stepwise feature selection based on statistical significance
- L1 regularization for coefficient analysis

### 2. Advanced Statistical Modeling
- Natural Cubic Splines for non-linear relationships
- Thin-Plate Spline modeling for 2D visualization
- Local Logistic Regression with tri-cube kernel
- Kernel Density Estimation
- Gaussian Mixture Models for density estimation and classification

### 3. Visualization Techniques
- Scatter plot matrices
- Contour plots
- Density plots
- Confidence interval visualizations

## Key Findings

1. **Risk Factor Significance**
   - Strong associations: Age, LDL cholesterol, Family history, Tobacco use
   - Weaker associations: Systolic blood pressure, Obesity (when controlling for other factors)

2. **Model Performance**
   - Logistic Regression achieved 68% accuracy
   - Gaussian Mixture Model reached 69% accuracy using age alone

3. **Non-linear Relationships**
   - Identified complex non-linear relationships between risk factors
   - Age and tobacco use showed particularly strong non-linear effects

## Technical Implementation
- Programming Language: Python
- Key Libraries: 
  - scikit-learn for machine learning models
  - statsmodels for statistical analysis
  - scipy for specialized statistical functions
  - matplotlib and seaborn for visualization

## Notes
- The study accounts for the case-control sampling bias (5.1% actual prevalence vs 35% in sample)
- Some measurements were taken after treatment interventions, potentially affecting certain variables

## Conclusions
The analysis successfully identified key risk factors for heart disease in the study population while demonstrating the importance of using multiple modeling approaches to understand complex relationships between variables. The combination of traditional statistical methods with modern machine learning techniques provided robust and interpretable results.
