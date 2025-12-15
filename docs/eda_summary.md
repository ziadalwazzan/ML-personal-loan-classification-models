## Data Exploration Summary

- **Dataset:** 45,000 rows, 16 columns; no missing values detected.
- **Target balance:** 0 (rejected) 77.8%, 1 (approved) 22.2% → imbalanced.
- **Numeric highlights:**
  - Age mean ~27.8 (min 20, max 144) with long high-age tail.
  - Income mean ~80k, max 7.2M; highly right-skewed.
  - Loan amount mean ~9.6k (range 500–35k); loan_percent_income mean 0.14 (max 0.66).
  - Interest rate mean ~11% (range 5.4–20); credit score mean ~633 (range 390–850).
- **Categorical frequencies:**
  - Gender: ~55% male, 45% female.
  - Education: Bachelor 13.4k, Associate 12.0k, High School 12.0k, Master 7.0k, Doctorate 0.6k.
  - Home ownership: Rent 23.4k, Mortgage 18.5k, Own 3.0k, Other ~0.1k.
  - Loan intent: Education 9.1k, Medical 8.5k, Venture 7.8k, Personal 7.6k, Debt Consolidation 7.1k, others minimal.
  - Previous defaults: Yes 22.9k, No 22.1k.
- **Outliers (IQR rule):** highest rates on loan_amnt (~5.2%), person_income (~4.9%), person_age (~4.9%), person_emp_exp (~3.8%). Notable extremes include age 144 and multi-million incomes.
- **Correlations with target:** negative for previous_loan_defaults_on_file_flag (-0.54) and income (-0.14); positive for loan_percent_income (0.38), loan_int_rate (0.33), loan_amnt (0.11); others weak.
- **Outputs:** plots saved to `results/figures/` and numeric/outlier/missing summaries in `results/`.


