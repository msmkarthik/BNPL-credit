# BNPL Credit Risk

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/msmkarthik/BNPL-credit/blob/main/BNPL_CreditRisk_EDA.ipynb)

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

The notebook uses `Buy_Now_Pay_Later_BNPL_CreditRisk_Dataset.csv` (10,345 customers × 17 columns). The dataset is not included in this repository.

## Running it in Google Colab

1. In Google Drive, create a folder called `bnpl` directly inside **My Drive**.
2. Upload `Buy_Now_Pay_Later_BNPL_CreditRisk_Dataset.csv` into it.
3. Click the **Open in Colab** badge above.
4. Run the cells from the top. The first code cell asks for permission to access your Google Drive; click **Allow**.

To keep your own edits, use **File → Save a copy in Drive** in Colab.

## Running it locally

Place the CSV in the same folder as the notebook, then:

```bash
pip install "pandas>=2.3" matplotlib jupyter
jupyter notebook BNPL_CreditRisk_EDA.ipynb
```

pandas 2.3 or newer is required on Python 3.14.
