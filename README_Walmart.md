# Walmart Black Friday Purchase Analysis

Statistical analysis of Walmart Black Friday transaction data to compare purchase amounts across gender, age, and marital-status segments. The project applies descriptive analysis, the Central Limit Theorem (CLT), confidence intervals, and one-tailed two-sample Z-tests to assess spending patterns.

## Business Question

Do women spend more per transaction than men during the Black Friday sale? The analysis also compares spending across age groups and marital status.

## Dataset

`walmart_data.csv` contains **550,068 transaction records** and 10 fields, including user and product IDs, customer demographics, product category, and purchase amount. The records represent **5,891 unique users**, so individual users may appear in multiple transactions.

The dataset contains no missing or duplicate rows. The notebook retains potential high-purchase outliers, noting that they may represent genuine transactions. Customer occupation and product category are masked numeric categories in the supplied data.

## Key Findings

- **Gender:** Average purchase amount was approximately **₹9,437.53 for male transactions** and **₹8,734.57 for female transactions**. The notebook's one-tailed Z-test reports a statistically significant difference, with male transactions higher.
- **Age:** The 51–55 group had the highest average purchase amount (about **₹9,534.81**), while the 0–17 group had the lowest (about **₹8,933.46**). The notebook reports statistically significant differences in its selected age-group comparisons, while noting that some differences are small in practical terms.
- **Marital status:** Average purchase amounts were nearly identical: approximately **₹9,265.91** for unmarried and **₹9,261.17** for married transactions. The reported test did not find sufficient evidence of a difference.
- **Distribution:** Purchase amounts are right-skewed. The notebook's IQR method flagged about **0.49%** of transactions as potential outliers; these were retained.
- **CLT and confidence intervals:** The notebook demonstrates how sample-mean distributions narrow as sample size increases and calculates 90%, 95%, and 99% confidence intervals for selected groups.

## Recommendations from the Analysis

- Explore gender and age as possible inputs for Black Friday promotions, while validating campaign outcomes with controlled measurement.
- Avoid prioritizing marital status for offer segmentation based on this dataset, since average spending is almost identical between the groups.
- Monitor high-value transactions separately rather than automatically removing them as outliers.
- Evaluate average transaction value alongside transaction counts when comparing segments.

## Methods and Tools

- Python with Pandas and NumPy for data handling and statistical calculations
- Matplotlib and Seaborn for visualizations
- SciPy and Statsmodels for normal-distribution calculations and Z-tests
- Descriptive statistics and exploratory data analysis
- Central Limit Theorem sampling demonstrations
- Confidence intervals at 90%, 95%, and 99%
- One-tailed two-sample Z-tests
- Segment comparisons by gender, age, and marital status

## Interpretation Note

The analysis is performed on transaction rows, and many users have multiple rows. The notebook's Z-tests treat transaction amounts as observations; repeated purchases by the same user may weaken the independence assumption. The available materials also do not establish a random sampling design. Therefore, the findings describe this dataset and its reported tests; population-level conclusions should be treated cautiously. Statistical significance does not by itself establish a large practical or causal effect.

## Repository Structure

```text
walmart-black-friday-purchase-analysis/
├── README.md
├── Walmart_Businesscase.ipynb
└── walmart_data.csv
```

The notebook contains the analysis and visualizations. The CSV is the dataset loaded by the notebook.

## How to Review

1. Read this README for the business question and headline findings.
2. Open `Walmart_Businesscase.ipynb` to review the EDA, CLT demonstration, confidence intervals, and hypothesis tests.
3. Use `walmart_data.csv` as the notebook's input data.

## Author

**Aravinth Baskar**
