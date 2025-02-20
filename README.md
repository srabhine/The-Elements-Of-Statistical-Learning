# The-Elements-Of-Statistical-Learning
This repository contains self projects of the book "The Elements Of Statistical Learning"

## Content Description

- **Exercices/**: Contains organized practice exercises and their solutions from the book
- **south_afr_dataset/**: Heart disease analysis in South African population
- **vowel_dataset/**: Contains training and test data for vowel recognition problems
- **Code_Exercice_3_2.ipynb**: Implementation and solution of Exercise 3.2 from the book
- **prostate_cancer.ipynb**: Regression task for the prostate_cancer dataset
- **south_african_heart_disease.ipynb**: Comprehensive analysis of heart disease factors
- **vowel.ipynb**: Implementation of vowel recognition algorithms

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


----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Prostate Cancer Analysis Project

## Overview
This project analyzes data from a study by Stamey et al. (1989) examining the correlation between prostate specific antigen (PSA) levels and various clinical measurements in men scheduled for radical prostatectomy. The main goal is to predict the log of PSA (lpsa) using multiple clinical measurements.

## Dataset
- **Population**: Men scheduled for radical prostatectomy
- **Sample Size**: 97 subjects
- **Target Variable**: Log of prostate specific antigen (lpsa)
- **Study Type**: Supervised learning (regression)

### Features
- Log cancer volume (lcavol)
- Log prostate weight (lweight)
- Age
- Log of benign prostatic hyperplasia amount (lbph)
- Seminal vesicle invasion (svi)
- Log of capsular penetration (lcp)
- Gleason score
- Percent of Gleason scores 4 or 5 (pgg45)

## Methods & Techniques

### 1. Base Models
- Least Squares Regression
- Base Error Rate Analysis using DummyRegressor
- Cross-validation with one-standard-error rule

### 2. Advanced Regression Methods
- Ridge Regression
- Lasso Regression
- Principal Components Regression (PCR)
- Partial Least Squares (PLS)
- Best Subset Regression

### 3. Feature Selection and Regularization
- Standardization of predictors
- Cross-validated parameter selection
- Shrinkage methods comparison
- Forward Stagewise Regression

### 4. Visualization Techniques
- Scatterplot matrices
- Correlation matrices
- Coefficient profile plots
- Error rate comparisons

## Key Findings

1. **Model Performance**
   - Base Error Rate: 1.057
   - Least Squares Test Error: 0.521
   - PCR achieved best performance with test error of 0.449
   - Lasso showed strong feature selection capabilities

2. **Feature Importance**
   - Strong correlations between lcavol, lcp and the response lpsa
   - Significant relationships between svi and several predictors
   - Some predictors show high correlation (e.g., gleason and pgg45)

3. **Model Comparisons**
   - Ridge Regression effectively handled correlated predictors
   - Lasso provided sparse solutions
   - PCR showed advantage in handling multicollinearity
   - PLS performed similarly to other methods

## Technical Implementation
- Programming Language: Python
- Key Libraries:
  - scikit-learn for modeling
  - statsmodels for statistical analysis
  - seaborn for visualization
  - numpy and pandas for data manipulation
  - matplotlib for custom plotting

## Comparative Analysis of Methods
Results from different methods (coefficients):
- Least Squares captured all relationships but may overfit
- Best Subset selected fewer variables
- Ridge showed shrinkage while keeping all variables
- Lasso produced sparse solutions
- PCR and PLS provided alternative approaches to handling correlation

## Conclusions
The analysis demonstrates the effectiveness of various regression techniques in predicting PSA levels. PCR showed the best test performance, while different methods offered various trade-offs between interpretability, sparsity, and prediction accuracy. The study highlights the importance of considering multiple modeling approaches for medical prediction tasks.




----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Vowel Speech Recognition Analysis Project

## Overview
This project analyzes a speech recognition dataset focusing on vowel classification. The study aims to compare different classification methods for identifying 11 different vowel sounds from digitized speech data.

## Dataset
- **Population**: Speech samples from 15 speakers (8 for training, 7 for testing)
- **Sample Size**: 
  - Training set: 528 observations (8 speakers × 11 vowels × 6 repetitions)
  - Test set: 462 observations (7 speakers × 11 vowels × 6 repetitions)
- **Features**: 10 predictors derived from digitized speech
- **Classes**: 11 vowel sounds from different words (heed, hid, head, had, hard, hod, hoard, hood, who'd, heard, hud)

## Methods & Techniques

### 1. Linear Classification Methods
- Linear Regression with Indicator Matrix
- Linear Discriminant Analysis (LDA)
- Quadratic Discriminant Analysis (QDA)
- Regularized Discriminant Analysis (RDA)
- Logistic Regression

### 2. Advanced Techniques
- Reduced-Rank Linear Discriminant Analysis
- Flexible Discriminant Analysis (FDA)
- Multivariate Adaptive Regression Splines (MARS)

### 3. Visualization Techniques
- Canonical variate projections
- Decision boundary visualization
- Class centroid plotting
- Error rate curves

## Key Findings

1. **Model Performance Comparison**
   - Linear Regression: 67% test error
   - LDA: 56% test error
   - QDA: 53% test error
   - Logistic Regression: 51% test error
   - FDA/MARS: 43-44% test error (best performance)

2. **Dimensionality Reduction**
   - Best performance achieved with 2-dimensional LDA projection
   - Further dimensions did not improve classification accuracy

3. **Model Complexity Trade-offs**
   - Simple linear models showed high error rates
   - FDA/MARS with degree 2 achieved best balance of complexity and accuracy
   - QDA showed signs of overfitting (1% training error vs 53% test error)

## Technical Implementation
- Programming Language: Python
- Key Libraries:
  - scikit-learn for standard classification models
  - pyearth for MARS implementation
  - numpy for numerical computations
  - matplotlib for visualization
  - pandas for data handling

## Notes
- The classification problem is challenging due to significant class overlap
- FDA/MARS implementation required custom coding due to lack of standard library support
- Regularization techniques helped improve model generalization

## Conclusions
The analysis demonstrates the superiority of flexible discriminant analysis methods over traditional linear approaches for this vowel recognition task. While simple linear methods struggled with class separation, FDA/MARS achieved significantly better performance by capturing non-linear relationships in the data. The study also highlights the importance of dimensionality reduction, with optimal results achieved in a 2-dimensional projection space.
