# Sydney Retail Customer Behaviour Analysis

## Overview
An exploratory statistical analysis of retail customer behaviour across 
17 store locations in Sydney, Australia. This project investigates 
purchasing patterns, payment preferences, and customer satisfaction 
using hypothesis testing, confidence intervals, and regression modelling 
in R.

The dataset contains 633 customer transactions with variables including 
demographics, store location, purchase amount, payment method, and 
satisfaction score.

---

## Key Questions Explored

- Is store location choice independent of customer gender?
- Do purchase amounts differ significantly between store locations?
- Does payment method influence how much customers spend?
- Can customer satisfaction scores predict the number of items purchased?

---

## Statistical Methods Used

| Method | Purpose |
|---|---|
| Chi-square test (built-in + manual simulation) | Independence of gender and store location |
| Welch Two-Sample T-test | Comparing mean purchase amounts between locations |
| One-way ANOVA + Permutation test | Purchase amount variation across payment methods |
| Tukey HSD Post-hoc Test | Identifying specific payment method pairs with significant differences |
| Bootstrap Regression | Predicting number of items from satisfaction score |
| Residual Analysis | Evaluating model fit and assumptions |

---

## Key Findings

1. **Gender and store location are independent** (p = 0.168) — shopping 
   location preference does not differ significantly by gender, suggesting 
   stores should design inclusive marketing campaigns rather than 
   gender-targeted ones.

2. **Manly customers spend significantly more than Parramatta customers** 
   (mean difference: $34.37, 95% CI: [$14.20, $54.54], p = 0.001) — 
   suggesting Manly stores would benefit from stocking more premium products.

3. **Payment method significantly affects purchase amount** (F = 8.08, p < 0.001) 
   — Mobile Payment users spend significantly more than Cash, Debit Card 
   and Gift Card users, suggesting targeted mobile payment promotions 
   could increase revenue.

4. **Satisfaction score is a statistically significant but weak predictor 
   of items purchased** (slope = 4.46, p < 0.001, R² = 10.57%) — 
   while the relationship is real, satisfaction score alone explains 
   only ~10% of variation in items purchased, indicating other variables 
   are needed for a stronger model.

---

## Tools and Techniques

- **Language:** R
- **Libraries:** ggplot2, base R stats
- **Techniques:** Hypothesis testing, simulation, bootstrapping, 
  permutation testing, linear regression, post-hoc analysis

---

## Files

| File | Description |
|---|---|
| `analysis.R` | Full R script with all analysis and visualisations |
| `Retail.csv` | Dataset — 633 retail customer transactions across Sydney |
| `README.md` | Project overview and findings |

---

## How to Run

1. Clone this repository
2. Open `analysis.R` in RStudio
3. Make sure `Retail.csv` is in the same directory
4. Run the script — all visualisations and results will be generated

```r
# Install required packages if needed
install.packages("ggplot2")

# Load data
retail = read.csv("Retail.csv")
```

---

## Author
**Austin Darian Pratama**
Master of Data Science — Western Sydney University
[LinkedIn](https://linkedin.com/in/austin-darian-pratama) · 
[GitHub](https://github.com/austindarian)
