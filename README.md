# Beyond-the-Threshold-Re-examining-the-Intelligence-Creativity-Relationship
Beyond the Threshold? Re-examining the Intelligence–Creativity Relationship Across Creativity Dimensions Using Classical, Nonlinear, and Explainable Analytical Approaches 
IQ3 (4)(3).ipynb — CRJ revision / final confirmatory analyses



Data preparation and reliability
Cleans and validates the CTONI-2 item data.
Identifies the six CTONI-2 subtest blocks: PA, GA, PC, GC, PS, GS.
Calculates KR-20/internal consistency for each subtest, PCI constituent items, GCI constituent items, and overall CTONI-2.
Calculates grade-specific CTONI reliability.
Constructs the eight PCA Drawing tasks and calculates Drawing Creativity α = .813.
Inspects the remaining PCA raw variables rather than forcing an unsupported Category reliability estimate.
Grade/developmental analyses
Produces M (SD) by Grade 1–10 for Age, IQ, PCI, GCI, Drawing, Category, Total Creativity, Parent Rating, and Teacher Rating.
Runs one-way ANOVAs with η² for grade effects.
Tests whether grade changes the IQ–creativity relationship.
Performs the separate age-sensitivity analysis.
Primary threshold/nonlinear analyses
Fits grade-adjusted linear, GAM, and segmented regression models.
Searches IQ breakpoints over the prespecified range.
Performs 300 bootstrap resamples to evaluate breakpoint stability.
Performs 10-fold cross-validation, with breakpoint selection occurring within the training folds.
Generates the publication-quality Drawing, Category, and Total GAM/segmented figures.
Machine learning / interpretability
Fits Random Forest models.
Generates PDP/ICE plots for IQ.
Performs SHAP analysis, including numerical mean absolute SHAP importance and SHAP figures.


IQProject2 (1)(2).ipynb — original/exploratory project analyses

This is the much larger exploratory notebook. It contains many analyses tried during development, including:

initial data cleaning and descriptives;
correlations;
original linear regressions;
different IQ grouping/threshold analyses;
quadratic models;
early segmented/piecewise regression;
AIC/BIC comparisons;
multiple regression with IQ, PCI, GCI, grade, gender, ratings, etc.;
LASSO;
Random Forest;
XGBoost;
early SHAP analyses;
various GAM/nonlinear analyses;
NCA;
K-means clustering;
several different Gaussian-mixture/LPA specifications;
entropy/profile diagnostics;
ANOVAs comparing profiles;
earlier cross-validated breakpoint analyses;
centered quadratic and interaction analyses.


