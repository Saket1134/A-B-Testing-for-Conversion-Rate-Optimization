# A/B Testing for Conversion Rate Optimization

## Project Overview
This project analyzes an A/B test to compare two website versions and assess whether a change in conversion rate is statistically significant. It uses Python for data preparation, metric calculation, hypothesis testing, and visualization.

The dataset is synthetic and contains 1,000 user records split between:
- **Group A (Control):** The original website version
- **Group B (Treatment):** The modified website version

## Objectives
- Load and inspect user-level experiment data
- Check and clean missing, duplicate, and invalid records
- Calculate visitors, conversions, and conversion rates for each group
- Measure absolute lift and relative uplift
- Run a two-proportion z-test to compare conversion rates
- Visualize the results and provide a data-informed recommendation

## Tech Stack
- Python
- Pandas
- NumPy
- Statsmodels
- Matplotlib
- Seaborn
- Jupyter Notebook

## Dataset
File: `ab_test_data_small.csv`

| Column | Description |
|---|---|
| `user_id` | Unique identifier for each user |
| `group` | Experiment group: `A` (control) or `B` (treatment) |
| `converted` | Conversion outcome: `1` = converted, `0` = did not convert |

The CSV is synthetic practice data, not real customer data. The observed metrics are calculated by the notebook and may differ if the dataset changes.

## Key Metrics
- **Conversion rate:** Conversions divided by visitors, multiplied by 100
- **Absolute lift:** Treatment conversion rate minus control conversion rate, expressed in percentage points
- **Relative uplift:** The absolute difference divided by the control conversion rate, multiplied by 100
- **P-value:** Used to assess evidence against the null hypothesis

## Hypothesis Test
- **Null hypothesis (H₀):** The conversion rates of A and B are equal.
- **Alternative hypothesis (H₁):** The conversion rates of A and B are different.
- **Significance level:** 0.05
- **Test:** Two-proportion z-test

If the p-value is below 0.05, the result is considered statistically significant at the 5% level. Otherwise, the analysis fails to reject the null hypothesis; this does not prove that the conversion rates are equal.

## Project Workflow
1. Import libraries and load the CSV.
2. Inspect and validate the data.
3. Calculate group-level visitors, conversions, and conversion rates.
4. Calculate absolute lift and relative uplift.
5. Perform the two-proportion z-test.
6. Plot the conversion-rate comparison.
7. Interpret the findings and make a cautious recommendation.

## Setup and Run
1. Download or clone this project and place `ab_test_data_small.csv` in the same folder as your notebook.
2. Install dependencies:

   ```bash
   pip install pandas numpy matplotlib seaborn statsmodels jupyter
   ```

3. Start Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

4. Open the project notebook and run the cells from top to bottom.

## Business Value
A/B testing helps teams evaluate product or website changes using evidence instead of assumptions. The analysis can support decisions about which version to test further or roll out, while considering statistical uncertainty and business impact.

## Limitations
- The dataset is synthetic and intended for learning.
- A statistically significant result does not automatically imply a meaningful business impact.
- Valid conclusions depend on sound random assignment, independent observations, adequate sample size, and a correctly conducted experiment.
- Avoid repeatedly checking significance and stopping an experiment as soon as a favorable result appears.

## Author
Saket Tejpal
