# Insurance-Claims-Analysis
Actuarial insurance claims analysis using Excel, including data cleaning, PivotTables, visualizations, and chi-square hypothesis testing of fraud indicators.

## Project Overview

The goal of this project was to analyze insurance claims dataset and identify factors associated with claim amount and reported fraud.
The analysis focuses on questions such as:
- How does claim severity affect average claim amounts?
- Which incident types have the highest reported fraud rates?
- Is fraud status statistically associated with incident type?
- Is fraud status statistically associated with damage severity?
- How do claim amounts vary by collision type?
- How have average claim amounts varied across claim years?

  ## Tools and Techniques

  - Microsoft Excel
  - XLOOKUP
  - COUNTIFS
  - PivotTables
  - PivotCharts
  - Data cleaning and catergorization
  - Descriptive analysis
  - Data visualization
  - Chi-square test of independence
  - Expected frequency calculations
  - Hypothesis testing
 
  ## Data Preperation

The original claims data was prepared for analysis by creating additional variables and categories.

Key preperation steps included:

- Using XLOOKUP to categorize vehicle age
- Creating vehicle age categories
- Organizing fraud-related variables
- Checking and structuring categorical claim variables
- Creating PivotTables to summarize claim characteristics
- Preparing data for statistical hypothesis testing

## Exploratory Analysis

PivotTables and charts were created to examine the relationships between:

- Incident severity and average claim amount
- Incident type and fraud rate
- Damage severity and fraud rate
- Collision type and claim amount
- Claim year and average claim amount
- Auto make and fraud rate

## Statistical Analysis

Two chi-square tests of independence were performed using a significant level of:

**a = 0.05**

###1. Incident Type vs. Fraud status

**Null Hypothesis (H₀):** Fraud status and incident type are independent.

**Alternative Hypothesis (H₁):** Fraud status and incident type are associated.

| Statistic | Result |
|---|---:|
| Chi-square (χ²) | 29.13 |
| Degrees of freedom | 3 |
| P-value | 2.10 × 10⁻⁶ |
| Significance level | 0.05 |
| Decision | Reject H₀ |

**Conclusion:** There is statistically significant evidence of an association between incident type and fraud status in the dataset.

### 2. Damage Severity vs. Fraud Status

**Null Hypothesis (H₀):** Fraud status and damage severity are independent.

**Alternative Hypothesis (H₁):** Fraud status and damage severity are associated.

| Statistic | Result |
|---|---:|
| Chi-square (χ²) | 264.24 |
| Degrees of freedom | 3 |
| P-value | < 0.0001 |
| Significance level | 0.05 |
| Decision | Reject H₀ |

**Conclusion:** There is statistically significant evidence of an association between damage severity and fraud status in the dataset.

> Statistical significance indicates an association between the variables; it does not establish a causal relationship.

## Key Findings

### Claim Severity

Major damage incidents had the highest average claim amount at approximately **$64,067**, while trivial damage incidents had the lowest average claim amount at approximately **$5,302**.

### Incident Type & Fraud

Single-vehicle collisions had the highest fraud rate among incident types at approximately **29%**, compared with an overall fraud rate of **25%**.

The chi-square test indicated that incident type and fraud status were statistically significantly associated.

### Damage Severity & Fraud

Major damage incidents had the highest fraud rate at approximately **61%**, compared with an overall fraud rate of **25%**.

The chi-square test found a statistically significant association between damage severity and fraud status (**χ² = 264.24, p < 0.0001**).

### Collision Type

Front collisions had the highest average claim amount among identified collision types at approximately **$64,658** across 254 claims.

Rear collisions had the largest number of classified collision claims, with **292 claims**.

### Claims Over Time

1995 had the highest average claim amount at approximately **$58,470**, while 2001 had the lowest at approximately **$45,468**.

Average claim amounts fluctuated across the years without a consistent long-term trend.

## Project Structure

```text
Insurance-Claims-Analysis/
│
├── README.md
└── Insurance_Claims_Analysis.xlsx
