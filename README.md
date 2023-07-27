This is the boilerplate for the Medical Data Visualizer project. Instructions for building your project can be found at https://www.freecodecamp.org/learn/data-analysis-with-python/data-analysis-with-python-projects/medical-data-visualizer


# Medical Examination Data Visualizer

## Introduction

In this project, you will be working with medical examination data using Python's pandas, matplotlib, and seaborn libraries. The dataset contains information about patients, including body measurements, blood test results, and lifestyle choices. Your goal is to explore the relationship between cardiac disease and various factors.

## Data Description

The dataset has the following features:

- Age (Objective Feature): age in days (int)
- Height (Objective Feature): height in centimeters (int)
- Weight (Objective Feature): weight in kilograms (float)
- Gender (Objective Feature): categorical code for gender (binary)
- Systolic blood pressure (Examination Feature): ap_hi (int)
- Diastolic blood pressure (Examination Feature): ap_lo (int)
- Cholesterol (Examination Feature): 1 - normal, 2 - above normal, 3 - well above normal
- Glucose (Examination Feature): 1 - normal, 2 - above normal, 3 - well above normal
- Smoking (Subjective Feature): smoke (binary)
- Alcohol intake (Subjective Feature): alco (binary)
- Physical activity (Subjective Feature): active (binary)
- Presence or absence of cardiovascular disease (Target Variable): cardio (binary)

## Tasks

1. **Create a Chart:** Generate a chart similar to `examples/Figure_1.png`, showing the counts of good and bad outcomes for the cholesterol, gluc, alco, active, and smoke variables in different panels, grouped by `cardio=1` and `cardio=0`.

2. **Add Overweight Column:** Calculate the Body Mass Index (BMI) for each patient and add an "overweight" column to the data. If BMI > 25, set the value to 1 (overweight), otherwise 0 (not overweight).

3. **Normalize Data:** Convert the cholesterol and gluc values to binary, where 0 means "good" and 1 means "bad." If cholesterol or gluc is greater than 1, set the value to 1.

4. **Create Categorical Features Chart:** Convert the data into long format and create a chart that displays the value counts of the categorical features using seaborn's `catplot()`. The dataset should be split by `Cardio` so that there is one chart for each cardio value.

5. **Clean the Data:** Filter out incorrect data segments by keeping only the correct data where diastolic pressure is less than or equal to systolic pressure (`df['ap_lo'] <= df['ap_hi']`), height is greater than or equal to the 2.5th percentile (`df['height'] >= df['height'].quantile(0.025)`), height is less than or equal to the 97.5th percentile, weight is greater than or equal to the 2.5th percentile, and weight is less than or equal to the 97.5th percentile.

6. **Create Correlation Matrix Chart:** Generate a correlation matrix using the dataset and plot it using seaborn's `heatmap()`. Mask the upper triangle of the matrix.

## Development and Testing

For development, use `main.py` to test your functions. Click the "run" button, and `main.py` will execute.

Testing is already set up for you in `test_module.py`. The tests will run automatically whenever you click the "run" button. Make sure to set all variables to the correct code (`None` when not implemented) before submitting.