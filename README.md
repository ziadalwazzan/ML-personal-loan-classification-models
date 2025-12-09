# Personal Loan Approval Classification

A machine learning project that predicts personal loan approval outcomes using demographic, financial, and credit-related features. This repository implements and compares three classification approaches: Logistic Regression, Random Forest, and Artificial Neural Networks.

---

## 🎯 Project Goal

Develop and evaluate predictive models to accurately classify loan approval decisions based on applicant characteristics. The project explores feature engineering, model optimization, and practical deployment considerations for financial decision-making systems.

---

## 📊 Dataset

- **Size:** ~45,000 loan applications
- **Features:** 16 variables including age, income, employment history, credit score, and loan characteristics
- **Target Variable:** Binary loan approval status (0 = rejected, 1 = approved)

### Key Features
- Demographic information (age, gender, education)
- Financial indicators (income, employment experience)
- Loan details (amount, interest rate, purpose)
- Credit history (credit score, length, previous defaults)
- Household characteristics (home ownership, household size)

---

## 📁 File Structure

```
.
├── data/
│   └── Dataset - 2526.csv              # Original dataset
│
├── notebooks/
│   ├── 01_data_exploration.ipynb       # EDA and initial analysis
│   ├── 02_feature_engineering.ipynb    # Feature transformation and engineering
│   ├── 03_model_training.ipynb         # Model training and validation
│   ├── 04_model_optimization.ipynb     # Hyperparameter tuning
│   └── final_submission.ipynb          # Complete workflow for submission
│
├── models/
│   ├── logistic_regression.pkl         # Trained Logistic Regression model
│   ├── random_forest.pkl               # Trained Random Forest model
│   └── ann_model.h5                    # Trained ANN model
│
├── results/
│   ├── figures/                        # Plots and visualizations
│   └── metrics.csv                     # Performance metrics and comparisons
│
├── docs/
│   └── report.md                       # Detailed project report and analysis
│
├── requirements.txt                    # Python dependencies
├── .gitignore                          # Git ignore file
└── README.md                           # This file
```

---

## 🚀 Getting Started

### Prerequisites
- Python 3.8+
- Jupyter Notebook/Lab

### Installation

1. Clone the repository:
```bash
git clone https://github.com/ziadalwazzan/ML-personal-loan-classification-models.git
cd ml-personal-loan-classification-models
```

2. Create a virtual environment (recommended):
```bash
python -m venv venv
source venv/bin/activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

### Running the Analysis

1. Start with data exploration:
```bash
jupyter notebook notebooks/01_data_exploration.ipynb
```

2. Follow the numbered notebooks sequentially for the complete workflow

3. For the complete analysis:
```bash
jupyter notebook notebooks/final_submission.ipynb
```

---

## 📊 Dataset Variables

| Variable | Type | Description |
|----------|------|-------------|
| `person_age` | Float | Age of applicant in years |
| `person_gender` | Categorical | Gender (male/female) |
| `person_education` | Categorical | Education level (5 unique values) |
| `person_income` | Float | Annual income |
| `person_emp_exp` | Integer | Professional experience in years |
| `empl_len` | Integer | Length of employment |
| `person_home_ownership` | Categorical | Home ownership status (4 unique values) |
| `loan_amnt` | Float | Requested loan amount |
| `loan_intent` | Categorical | Purpose of loan (6 unique values) |
| `loan_int_rate` | Float | Interest rate |
| `loan_percent_income` | Float | Loan to income ratio |
| `cb_person_cred_hist_length` | Float | Credit history length in years |
| `ppl_household` | Integer | Number of people in household |
| `credit_score` | Integer | Credit score |
| `previous_loan_defaults_on_file` | Boolean | Previous loan defaults |
| **`loan_status`** | **Binary** | **Target: 0=rejected, 1=approved** |

---

## 📝 Documentation

For detailed analysis, methodology, and results, see the [project report](docs/report.md).

The report covers:
- Problem analysis and business context
- Data exploration and feature engineering
- Model training and evaluation
- Hyperparameter optimization
- Model comparison and recommendations
- Deployment considerations

---

## 📚 Dependencies

Core packages:
- `numpy` - Numerical computing
- `pandas` - Data manipulation and analysis
- `scikit-learn` - Machine learning algorithms and tools

Additional packages may be required for visualization and deep learning (see `requirements.txt`).
