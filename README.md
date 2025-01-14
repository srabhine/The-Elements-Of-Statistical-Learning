# The-Elements-Of-Statistical-Learning
This repository contains self projects of the book "The Elements Of Statistical Learning"

## South African Heart Disease

### Study Overview
This project presents an analysis of the Coronary Risk-Factor Study (CORIS) dataset, examining heart disease risk factors in rural Western Cape, South Africa.

Study population: White males aged 15-64 years
Sample size: 462 subjects (160 cases, 302 controls)
Regional MI prevalence: 5.1%
Case-control study design with 2:1 control-to-case ratio

Key Variables Analyzed

Systolic blood pressure (sbp)
Cumulative tobacco consumption (kg)
LDL cholesterol levels
Family history (binary: present/absent)
Obesity
Alcohol consumption
Age at onset

Technical Methodology

Statistical Analysis:

Logistic regression with LASSO regularization
Natural cubic splines for non-linear relationships
Local regression techniques
Kernel density estimation
Gaussian mixture models


Visualization Techniques:

Correlation matrices
Coefficient path plots
Natural spline function plots
Kernel density plots
Mixture model visualizations

### Key Findings

* Risk Factor Importance (LASSO Analysis):

Age emerged as the strongest predictor
Family history showed significant impact
Tobacco use and LDL cholesterol demonstrated moderate effects
Blood pressure showed complex relationships
Obesity displayed unexpected negative correlations in multivariate analysis


* Non-linear Relationships:

Complex U-shaped relationship for blood pressure
Age shows increasing risk until 40, then stabilization
Tobacco use shows accelerating risk at higher consumption levels



* Limitations

Some measurements taken post-treatment
Sample bias requiring statistical correction
Retrospective study design limitations

Technical Implementation
The analysis was implemented using Python, utilizing:

Pandas for data manipulation
Scikit-learn for statistical modeling
Matplotlib and Seaborn for visualization
Custom implementations for specialized statistical methods

This project demonstrates advanced statistical modeling techniques while providing valuable insights into heart disease risk factors in this specific population.
