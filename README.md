# Beyond the Threshold? Re-examining the Intelligence–Creativity Relationship

## Re-examining the Intelligence–Creativity Relationship Across Creativity Dimensions Using Classical, Nonlinear, and Explainable Analytical Approaches

This repository contains the analysis notebooks associated with the revised manuscript **“Beyond the Threshold? Re-examining the Intelligence–Creativity Relationship Across Creativity Dimensions Using Classical, Nonlinear, and Explainable Analytical Approaches.”**

Two notebooks are included. They serve different purposes and should be interpreted accordingly.

---

## 1. `IQ3 (4)(3).ipynb` — CRJ Revision / Final Confirmatory Analyses

This notebook contains the revised and streamlined analyses conducted primarily in response to the statistical and reporting recommendations provided by the *Creativity Research Journal* editor.

The revised manuscript primarily relies on the analyses reported in this notebook.

### Data Preparation and Reliability

The notebook:

- Cleans and validates the analysis data.
- Examines the CTONI-2 item-level structure.
- Identifies the six CTONI-2 subtest blocks:
  - Pictorial Analogies (PA)
  - Geometric Analogies (GA)
  - Pictorial Categories (PC)
  - Geometric Categories (GC)
  - Pictorial Sequences (PS)
  - Geometric Sequences (GS)
- Calculates KR-20/internal consistency reliability for:
  - PA
  - GA
  - PC
  - GC
  - PS
  - GS
  - Pictorial Composite Index (PCI) constituent items
  - Geometric Composite Index (GCI) constituent items
  - Overall CTONI-2 constituent items
- Calculates grade-specific CTONI-2 reliability coefficients.
- Constructs the eight PCA Drawing Creativity tasks.
- Calculates sample-specific internal consistency for PCA Drawing Creativity (`α = .813`).
- Examines the available PCA raw scoring structure without forcing an unsupported internal-consistency estimate for Category Creativity.

### Grade and Developmental Analyses

The notebook:

- Produces grade-specific descriptive statistics for Grades 1–10.
- Reports `M (SD)` for:
  - Age
  - IQ
  - PCI
  - GCI
  - Drawing Creativity
  - Category Creativity
  - Total Creativity
  - Parent Rating
  - Teacher Rating
- Conducts one-way ANOVAs examining grade differences.
- Calculates η² effect sizes for grade effects.
- Examines whether grade contributes to variation in the IQ–creativity relationship.
- Conducts a separate age-sensitivity analysis.

### Primary Threshold and Nonlinear Analyses

The notebook compares complementary approaches to modeling the intelligence–creativity relationship.

It:

- Fits grade-adjusted linear regression models.
- Fits generalized additive models (GAMs).
- Fits segmented regression models.
- Searches for IQ breakpoints across a prespecified candidate range.
- Compares linear, GAM, and segmented model fit.
- Evaluates whether apparent threshold effects differ across:
  - Drawing Creativity
  - Category Creativity
  - Total Creativity

### Bootstrap Breakpoint Stability

To assess whether estimated IQ breakpoints are stable rather than sample-specific, the notebook:

- Performs **300 bootstrap resamples**.
- Re-estimates the segmented-regression breakpoint within each bootstrap sample.
- Summarizes:
  - Median breakpoint
  - Mean breakpoint
  - Breakpoint SD
  - 95% bootstrap percentile interval
  - Minimum and maximum breakpoint
  - Concentration around the full-sample breakpoint
  - Frequency of lower- and upper-boundary solutions

### 10-Fold Cross-Validation

The notebook evaluates out-of-sample model performance using **10-fold cross-validation**.

It:

- Compares linear, GAM, and segmented models.
- Selects segmented-model breakpoints using the training portion of each fold only.
- Evaluates predictions on held-out observations.
- Reports cross-validated:
  - R²
  - RMSE
  - MAE
- Records fold-specific breakpoint estimates.

This procedure helps distinguish reproducible nonlinear patterns from potentially sample-specific breakpoint estimates.

### Publication Figures

The notebook generates publication-oriented figures illustrating the grade-adjusted relationship between IQ and:

- Drawing Creativity
- Category Creativity
- Total Creativity

The figures compare GAM and segmented-regression relationships and are used to visualize the degree and form of nonlinearity across creativity dimensions.

### Machine Learning and Model Interpretability

The notebook fits Random Forest regression models for:

- Drawing Creativity
- Category Creativity
- Total Creativity

Predictors include IQ and relevant developmental, demographic, and educational variables.

The notebook evaluates held-out test-set performance using:

- R²
- RMSE
- MAE

### PDP and ICE Analyses

Partial Dependence Plots (PDPs) and Individual Conditional Expectation (ICE) plots are generated to examine:

- The average modeled relationship between IQ and creativity.
- Individual-level variation in the modeled IQ–creativity relationship.

These analyses are used for model interpretation rather than causal inference.

### SHAP Analyses

SHapley Additive Explanations (SHAP) are used to examine predictor contributions within the Random Forest models.

The notebook:

- Calculates mean absolute SHAP values.
- Ranks predictor importance separately for each creativity outcome.
- Generates SHAP summary figures.
- Examines the relative contribution of IQ across creativity dimensions.

Because Random Forest out-of-sample predictive performance is modest, SHAP results are interpreted as descriptive model-interpretability evidence rather than causal effects.

---

## 2. `IQProject2 (1)(2).ipynb` — Original / Exploratory Project Analyses

This notebook contains the broader set of analyses conducted during development of the project.

It documents the exploratory analytical process and includes methods and model specifications that were considered during earlier stages of the study but are not all retained in the revised manuscript.

Analyses explored in this notebook include:

- Initial data cleaning and descriptive analyses
- Correlation analyses
- Original linear regression models
- Multiple regression models
- Different IQ grouping and threshold analyses
- Quadratic regression models
- Early segmented/piecewise regression models
- AIC/BIC model comparisons
- Models incorporating IQ, PCI, GCI, grade, gender, teacher ratings, and parent ratings
- LASSO regression
- Random Forest models
- XGBoost models
- Early SHAP analyses
- Various GAM and nonlinear specifications
- Necessary Condition Analysis (NCA)
- K-means clustering
- Gaussian mixture models
- Latent/profile-oriented analyses
- Alternative profile specifications
- Entropy and profile diagnostics
- ANOVAs comparing profiles
- Earlier cross-validated breakpoint analyses
- Centered quadratic models
- Interaction analyses

### Person-Centered / Profile Analyses

The exploratory notebook also contains the person-centered analyses used to investigate heterogeneity in cognitive–creativity patterns.

A retained four-profile descriptive solution based on:

- IQ
- Drawing Creativity
- Category Creativity
- Teacher Rating

is used in the revised manuscript to provide a complementary illustration of heterogeneity in the intelligence–creativity relationship.

The exploratory notebook also contains alternative profile specifications. These alternative solutions document the analytical development process and should not be interpreted as additional confirmatory findings.

Accordingly, the profile analysis in the revised manuscript is treated primarily as a **descriptive person-centered analysis**, rather than as evidence that the sample contains four definitively established discrete student types.

---

## Relationship Between the Two Notebooks

The two notebooks serve different analytical purposes:

- **`IQ3 (4)(3).ipynb`** contains the streamlined revision and confirmatory analyses used to address the *Creativity Research Journal* editorial recommendations and forms the primary computational basis for the revised statistical results, tables, and figures.
- **`IQProject2 (1)(2).ipynb`** documents the broader exploratory and developmental analytical workflow, including alternative statistical, machine-learning, nonlinear, and person-centered approaches considered during the project.

Not every analysis contained in the exploratory notebook is reported in the revised manuscript.

For interpretation of the final statistical conclusions, the revised manuscript and the streamlined analyses in **`IQ3 (4)(3).ipynb`** should be treated as the primary reference.

---

## Main Analytical Framework of the Revised Manuscript

The revised analysis focuses on four complementary components:

1. **Measurement and developmental description**
   - Sample-specific reliability
   - Grade-specific reliability
   - Grade-specific descriptive statistics
   - Grade and age sensitivity analyses

2. **Intelligence–creativity functional relationships**
   - Linear regression
   - Generalized additive models
   - Segmented regression
   - Bootstrap breakpoint stability
   - Cross-validation

3. **Predictive model interpretation**
   - Random Forest
   - PDP
   - ICE
   - SHAP

4. **Person-centered description**
   - Gaussian mixture/profile analysis
   - Descriptive examination of cognitive–creativity heterogeneity

Together, these analyses are designed to evaluate whether the intelligence–creativity relationship is better characterized by a universal threshold or by **domain-specific, developmentally contextualized, and potentially nonlinear relationships across different dimensions of creativity**.
