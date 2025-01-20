# Nonlinear Regression: Exponential Growth and SIS Model Analysis

## Project Description

This project investigates the application of nonlinear regression to two epidemiological models:  
1. **Exponential Growth Model**:  
   dI/dt = (β - γ)I,\
   where I(t) is the number of infected individuals, β is the average number of contacts per person per unit time, and γ is the average recovery rate per person per unit time.  

2. **SIS Model**:  
   dI/dt = (β - γ)I - (β/N)I^2,\
   where N is the total population size.  

The project explores how well these models describe the early spread of an epidemic in a chosen country, using nonlinear regression to estimate key parameters.

---

## Objectives

### 1. Analytical Solutions
- Derive the solution for the Exponential Growth Model:
  I(t) = I_0 * exp((β - γ)t),\
  where I_0 is the initial number of infected individuals. Reformulate this as:
  I(t) = I_0 * exp(χ * t),\
  where χ = β - γ.
- Derive the solution for the SIS Model:
  I(t) = I_∞ / (1 + ((I_∞ / I_0) - 1) * exp(-χ * t)),\
  where I_∞ is the limiting number of infected individuals as t -> ∞:
  I_∞ = lim(t -> ∞) I(t).\

### 2. Data Collection
- Collect data on the number of infected individuals over time for a chosen country, based on the first letter of your surname.

### 3. Exponential Growth Model Regression
- Assume the first weeks of the outbreak are described by the exponential growth model.
- Use nonlinear regression to estimate χ by fitting:
  I(t) = I_0 * exp(χ * t)\
- Plot the results in a logarithmic scale, overlaying the predicted curve with the observed data.

### 4. SIS Model Regression
- Using the estimated χ, fit the SIS model to the data using nonlinear regression.
- Plot the predicted SIS model curve alongside the observed data.

### 5. Error Analysis and Predictions
- Evaluate the error of the SIS model approximation:
  - Using L1-norm (sum of absolute errors)
  - Using L∞-norm (maximum absolute error)
- Determine the maximum time period for which the exponential growth model is valid based on a chosen criterion.
- Predict:
  - The total number of infected individuals in the population.
  - The time required for the epidemic to end.

---

## Technologies Used

- **Programming Language**: Python  
- **Libraries**:
  - `numpy` — for numerical computations.
  - `scipy` — for optimization and integration.
  - `matplotlib` — for visualizations.
  - `pandas` — for data manipulation.

---

## Results

1. **Parameter Estimation**:
   - The growth rate χ was estimated using nonlinear regression on the early outbreak data.
   - The SIS model parameter I_∞ was estimated based on the limiting behavior of the data.

2. **Model Comparison**:
   - The exponential growth model is effective only for the early stages of the epidemic.
   - The SIS model provides a more accurate approximation for later stages, especially as the epidemic approaches its peak.

3. **Error Analysis**:
   - Errors were computed using L1-norm (sum of absolute errors) and L∞-norm (maximum absolute error) to assess the accuracy of the models.

4. **Epidemic Predictions**:
   - Predicted the maximum number of infected individuals and the time required for the epidemic to end in the chosen country.

---

## Project Files
- nonlinear_regression.ipynb — Main script that handles all tasks related to nonlinear regression. This Jupyter notebook includes the necessary code for data processing, model fitting, evaluation, and other related steps.
- README.md — Project documentation.
- data/ — Folder containing the dataset used for the nonlinear regression tasks.
- plots/ — Folder where the generated plots and visualizations are stored.
- report.pdf - A detailed report summarizing the entire project. It includes all necessary calculations, analysis of the results, and a comprehensive discussion of the work completed according to the project requirements.

