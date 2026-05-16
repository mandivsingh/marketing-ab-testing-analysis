# Marketing A/B Testing Analysis

> Does replacing a public service announcement with a real marketing ad lift conversion? The data gives a clear answer.

## Overview

A rigorous end-to-end statistical analysis of a marketing experiment — covering hypothesis design, two-proportion z-test, confidence intervals, power analysis, and logistic regression to control for temporal confounds.

**Dataset:** Kaggle Marketing A/B Testing · 588,101 users · 2 groups

## Key Results

| Metric | Value |
|---|---|
| Ad Group Conversion Rate | 2.55% |
| PSA Group Conversion Rate | 1.78% |
| Absolute Lift | +0.77 percentage points |
| 95% Confidence Interval | +0.60% to +0.94% |
| p-value | << 0.05 (highly significant) |
| Statistical Power | ~1.0 (very high) |
| Odds Ratio (PSA vs Ad) | 0.69 — PSA users 31% less likely to convert |
| Conclusion | Reject H₀ — Ad wins |

## Experiment Design

| Group | Allocation | Description |
|---|---|---|
| Ad | 96% | Sees marketing advertisement |
| PSA | 4% | Sees public service announcement (control) |

⚠️ **Limitation:** The 96/4 split is atypical for a standard A/B test — flagged as a potential sample ratio mismatch. Analysis proceeds transparently with this constraint noted.

## Analysis Steps

1. **Hypothesis formulation** — one-sided test (does ad > PSA?)
2. **Two-proportion z-test** — p << 0.05, statistically significant
3. **Confidence interval estimation** — +0.60% to +0.94%, excludes zero
4. **Power analysis** — experiment is well-powered (~1.0)
5. **Logistic regression** — controls for day of week and hour of day
6. **Temporal heatmap** — identifies peak conversion windows

## Peak Ad Scheduling

- **Saturday 5–6 AM** and **weekend evenings (7–9 PM)** show highest conversion
- **Late night 2–4 AM** consistently weakest across all days
- Reallocating budget from dead zones to peak windows improves ROI without additional spend

## Tech Stack

- **Python** — Pandas, NumPy, Scipy, Statsmodels, Plotly
- **Logistic Regression** — controlling for temporal confounds
- Statistical testing: two-proportion z-test, odds ratio, confidence intervals

## Project Structure# Marketing A/B Testing Analysis

> Does replacing a public service announcement with a real marketing ad lift conversion? The data gives a clear answer.

## Overview

A rigorous end-to-end statistical analysis of a marketing experiment — covering hypothesis design, two-proportion z-test, confidence intervals, power analysis, and logistic regression to control for temporal confounds.

**Dataset:** Kaggle Marketing A/B Testing · 588,101 users · 2 groups

## Key Results

| Metric | Value |
|---|---|
| Ad Group Conversion Rate | 2.55% |
| PSA Group Conversion Rate | 1.78% |
| Absolute Lift | +0.77 percentage points |
| 95% Confidence Interval | +0.60% to +0.94% |
| p-value | << 0.05 (highly significant) |
| Statistical Power | ~1.0 (very high) |
| Odds Ratio (PSA vs Ad) | 0.69 — PSA users 31% less likely to convert |
| Conclusion | Reject H₀ — Ad wins |

## Experiment Design

| Group | Allocation | Description |
|---|---|---|
| Ad | 96% | Sees marketing advertisement |
| PSA | 4% | Sees public service announcement (control) |

⚠️ **Limitation:** The 96/4 split is atypical for a standard A/B test — flagged as a potential sample ratio mismatch. Analysis proceeds transparently with this constraint noted.

## Analysis Steps

1. **Hypothesis formulation** — one-sided test (does ad > PSA?)
2. **Two-proportion z-test** — p << 0.05, statistically significant
3. **Confidence interval estimation** — +0.60% to +0.94%, excludes zero
4. **Power analysis** — experiment is well-powered (~1.0)
5. **Logistic regression** — controls for day of week and hour of day
6. **Temporal heatmap** — identifies peak conversion windows

## Peak Ad Scheduling

- **Saturday 5–6 AM** and **weekend evenings (7–9 PM)** show highest conversion
- **Late night 2–4 AM** consistently weakest across all days
- Reallocating budget from dead zones to peak windows improves ROI without additional spend

## Tech Stack

- **Python** — Pandas, NumPy, Scipy, Statsmodels, Plotly
- **Logistic Regression** — controlling for temporal confounds
- Statistical testing: two-proportion z-test, odds ratio, confidence intervals

## Project Structure
- Marketing_AB.ipynb    # Main notebook
- marketing_AB.csv    # Dataset
- README.md

## Key Recommendations

1. **Deploy the ad at full scale** — evidence is robust across three independent analyses
2. **Concentrate spend on weekend peak slots** — Saturday morning and weekend evenings
3. **Eliminate 2–4 AM budget** — consistently the lowest performing window
4. **Rebalance allocation in future tests** — 50/50 or 80/20 split for cleaner comparison

## Live Portfolio

View the full interactive case study: [mandiv-analytics.netlify.app/project-ab.html](https://mandiv-analytics.netlify.app/project-ab.html)
