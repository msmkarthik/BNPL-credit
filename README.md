# BNPL Credit Risk

Exploratory data analysis (EDA) for a Buy Now Pay Later (BNPL) credit score project. The goal is to understand which customer characteristics predict default, before building a credit scoring model.

## Notebook

[`BNPL_CreditRisk_EDA.ipynb`](BNPL_CreditRisk_EDA.ipynb) is written for beginners. It explains every concept and every line of code, and covers:

- Data quality checks (missing values, duplicates, capped values)
- Target analysis (overall default rate)
- Distributions of each feature
- Default rate by credit score, employment, income, debt-to-income, repayment history and more
- Detection of derived and potentially leaky columns
- Correlation and interaction analysis
- Feature ranking with Weight of Evidence and Information Value

## Data

The notebook uses `Buy_Now_Pay_Later_BNPL_CreditRisk_Dataset.csv` (10,345 customers × 17 columns). The dataset is not included in this repository. Place it in the same folder as the notebook to run it.

## Running it

```bash
pip install "pandas>=2.3" matplotlib jupyter
jupyter notebook BNPL_CreditRisk_EDA.ipynb
```

pandas 2.3 or newer is required on Python 3.14.
