
# A/B Testing for Conversion Rate Optimization

## Project Overview
This project analyzes an A/B test to determine whether a new version of a website or application improves the conversion rate compared with the existing version.

Python is used for data cleaning, exploratory analysis, conversion rate calculations, statistical hypothesis testing, and visualization.

## Objectives
- Compare conversion rates between Control Group A and Treatment Group B.
- Calculate absolute lift and relative uplift.
- Perform a two-proportion z-test to check statistical significance.
- Visualize conversion rates.
- Provide a data-driven business recommendation.

## Technologies Used
- Python
- Pandas
- NumPy
- Statsmodels
- Matplotlib
- Seaborn
- Jupyter Notebook

## Dataset Description

The dataset contains the following columns:

| Column | Description |
|---|---|
| `user_id` | Unique identifier for each user |
| `group` | Experiment group: A or B |
| `converted` | 1 if the user converted, otherwise 0 |

## Project Workflow

1. Load the dataset.
2. Inspect and clean the data.
3. Calculate visitors, conversions, and conversion rates.
4. Calculate absolute lift and relative uplift.
5. Perform statistical hypothesis testing.
6. Visualize the conversion rates.
7. Make a business recommendation.

## Installation

Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn statsmodels jupyter
```

## How to Run

1. Download or clone this repository.
2. Place `ab_test_data_small.csv` in the project folder.
3. Open Jupyter Notebook or create a Python file.
4. Run the code below.

## Key Concepts

### Conversion Rate
The percentage of users who completed the desired action.

Conversion Rate = (Conversions / Visitors) × 100

### Absolute Lift
The difference between the treatment and control conversion rates, measured in percentage points.

### Relative Uplift
The percentage change in the conversion rate compared with the control group.

### Hypothesis Testing
- **Null Hypothesis (H0):** Both groups have equal conversion rates.
- **Alternative Hypothesis (H1):** The conversion rates are different.
- **Significance Level:** 0.05.
- If the p-value is below 0.05, reject the null hypothesis.

A p-value below 0.05 indicates statistically significant evidence of a difference under the test assumptions. It does not prove that the treatment caused the difference; experiment design and data quality also matter.

## Business Value

This project demonstrates how data analysis and statistical testing can help businesses evaluate website changes, optimize conversion rates, and make evidence-based product decisions.

## Limitations

- The included dataset is synthetic and intended for practice.
- Statistical significance does not necessarily imply business significance.
- Real experiments should check random assignment, sample size, data quality, and relevant external factors.

