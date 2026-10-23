# BNPL Credit Risk

A Buy Now Pay Later (BNPL) credit scoring project: explore the data, then build and compare models that predict whether a customer will default. The notebooks are written for beginners: they explain every concept and every line of code.

## Notebooks

| Notebook | What it does | Open |
|---|---|---|
| [`BNPL_CreditRisk_EDA.ipynb`](BNPL_CreditRisk_EDA.ipynb) | Exploratory data analysis. Runs in Colab or locally. | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/msmkarthik/BNPL-credit/blob/main/BNPL_CreditRisk_EDA.ipynb) |
| [`BNPL_CreditRisk_Modeling_Local.ipynb`](BNPL_CreditRisk_Modeling_Local.ipynb) | Modelling, local version, saved with all outputs | View on GitHub |
| [`BNPL_CreditRisk_Modeling_Colab.ipynb`](BNPL_CreditRisk_Modeling_Colab.ipynb) | Modelling, Google Colab version (reads the data from Google Drive) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/msmkarthik/BNPL-credit/blob/main/BNPL_CreditRisk_Modeling_Colab.ipynb) |

The two modelling notebooks are identical except for how they find the data file.

**EDA** covers data quality checks, the default rate, feature distributions, default rate by each feature, detection of derived and leaky columns, correlation and interaction analysis, and feature ranking with Weight of Evidence and Information Value.

**Modelling** covers:
- Feature selection based on the EDA, and feature engineering (log income, threshold flags)
- A multicollinearity check (VIF) and a stratified train/test split
- Logistic regression, a decision tree and a random forest, tuned with 5-fold cross-validation
- Every common metric: accuracy, precision, recall, specificity, F1, ROC AUC, Gini, KS, PR AUC, log loss and Brier score
- Confusion matrices, ROC, precision-recall and calibration curves
- Cut-off analysis, a gains (decile) table and permutation feature importance

**Headline result:** all three models reach a test AUC of about 0.77 (Gini about 0.53), beating the dataset's existing `risk_score` (AUC 0.73). Logistic regression is recommended because it performs as well as the others and is the easiest to explain.

## Data

The notebooks use `Buy_Now_Pay_Later_BNPL_CreditRisk_Dataset.csv` (10,345 customers × 17 columns). The dataset is not included in this repository.

## Running in Google Colab

1. In Google Drive, create a folder called `bnpl` directly inside **My Drive**.
2. Upload `Buy_Now_Pay_Later_BNPL_CreditRisk_Dataset.csv` into it.
3. Click an **Open in Colab** badge above.
4. Run the cells from the top. The first code cell asks for permission to access your Google Drive; click **Allow**.

To keep your own edits, use **File → Save a copy in Drive** in Colab.

## Running locally

Place the CSV in the same folder as the notebooks, then:

```bash
pip install "pandas>=2.3" matplotlib scikit-learn jupyter
jupyter notebook
```

pandas 2.3 or newer is required on Python 3.14. The modelling notebook was run with scikit-learn 1.7.2.
