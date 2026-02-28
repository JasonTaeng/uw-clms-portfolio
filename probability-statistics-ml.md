---
title: Probability & Statistics for ML
source: Coursera — DeepLearning.AI
---

# Probability & Statistics for ML — Notes

## What this is
A compact set of notes on probability/statistics ideas that frequently appear in ML:
uncertainty, distributions, estimation, confidence intervals, hypothesis testing, and A/B testing mindset.

---

## 1) Probability basics
- Conditional probability: P(A|B) = P(A ∩ B) / P(B)
- Independence: P(A ∩ B) = P(A)P(B)
- Bayes’ rule: P(A|B) = P(B|A)P(A) / P(B)

Pitfall: mixing up P(A|B) and P(B|A).

---

## 2) Random variables and distributions
- Discrete vs continuous random variables
- PMF (discrete), PDF (continuous), CDF (both)
- Expectation E[X], variance Var(X)
- Covariance and correlation

Pitfall: for continuous X, P(X = x) = 0 (interval probabilities matter).

---

## 3) Common distributions (intuition)
Discrete:
- Bernoulli(p), Binomial(n,p), Geometric(p), Poisson(λ)

Continuous:
- Uniform(a,b), Normal(μ, σ²), Exponential(λ)

Habit: attach a story to X (what does it measure/count?).

---

## 4) Sampling and averages
- LLN (informal): sample mean → true mean as n grows
- CLT (informal): sample mean distribution → approximately normal as n grows
- Standard error: how much an estimate would vary across repeated samples

---

## 5) Estimation
- Point estimation: choose a single best θ from data

MLE:
- θ_MLE = argmax_θ P(data | θ)

MAP:
- θ_MAP = argmax_θ P(data | θ)P(θ)

Connection: regularization often behaves like a prior.

---

## 6) Confidence intervals (CI)
A 95% CI procedure means:
Across repeated samples, ~95% of intervals contain the true value.

It does NOT mean:
“There is a 95% probability the true value lies in this specific interval.”
(that would be Bayesian phrasing).

---

## 7) Hypothesis testing
- H0 vs H1, test statistic
- p-value: probability of observing data at least as extreme as the sample, assuming H0 is true
- Type I / II error, power

Reminder:
statistical significance ≠ practical significance.

---

## 8) A/B testing mindset (conceptual)
Design:
- clear metrics (primary + guardrails)
- randomization assumptions
- avoid peeking/optional stopping
- be careful with multiple comparisons

Interpretation:
- effect size + uncertainty (CI), not just p-values
- check confounds (seasonality, selection effects, non-stationarity)

---

## Key terms (10)
- random variable
- PMF / PDF / CDF
- expectation
- variance
- covariance / correlation
- LLN
- CLT
- MLE
- confidence interval
- p-value

## Common confusions (4)
- **PDF is not “probability at a point”**: for continuous variables, probabilities are over intervals
- **p-value is not P(H0 is true)**: it is computed assuming H0 is true
- **CI interpretation**: long-run coverage of a procedure, not probability of a single interval (in frequentist framing)
- **statistical vs practical significance**: small effects can be “significant” with enough data
