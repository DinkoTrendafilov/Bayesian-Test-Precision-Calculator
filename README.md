# Bayesian Analysis of Medical Test Accuracy

A clear implementation demonstrating Bayes' Theorem applied to medical test interpretation, showing how prior probability affects the actual meaning of a "positive" result.

## Purpose

This code answers the critical question: **"If I test positive, what's the actual probability I have the disease?"** 

It demonstrates that even with a 99% accurate test for a rare disease (0.1% prevalence), a positive result only gives you about 9% probability of actually having the disease.

## The Bayesian Formula

The calculation follows Bayes' Theorem:

P(Sick|Positive) = P(Positive|Sick) * P(Sick) / P(Positive)


Where:
- `P(Sick|Positive)` = Posterior probability (what we want)
- `P(Positive|Sick)` = 0.99 (test sensitivity)
- `P(Sick)` = 0.001 (disease prevalence)
- `P(Positive)` = P(Positive|Sick)*P(Sick) + P(Positive|Healthy)*P(Healthy)

## Key Insight

This demonstrates the **base rate fallacy** - people often ignore prior probabilities when interpreting test results. Even excellent tests can be misleading for rare conditions.

## Usage

```python
# Install requirements
pip install scipy

Output Interpretation

The program calculates:

    Likelihood: Probability of getting this test result if sick/healthy

    Posterior: Actual probability of being sick after a positive test

Example output shows:

    With 99% test accuracy and 0.1% disease prevalence

    A positive test means only ~9% probability of actually being sick

    That's approximately 1 in 11 positive tests being true positives

Parameters You Can Modify

    prior_sick: Disease prevalence in population (currently 0.1%)

    p_positive_if_sick: Test sensitivity/true positive rate (currently 99%)

    p_positive_if_healthy: False positive rate (currently 1%)

    observed_positive: Number of positive results (currently 1)

    total_tests: Total tests taken (currently 1)

Extending This Code

Potential extensions:

    Multiple sequential tests

    Different test characteristics

    Population screening simulations

    Visualization of probability relationships

Mathematical Context

This is a classic example used in:

    Medical decision making

    Statistical literacy education

    Bayesian statistics introduction

    Risk assessment training

Requirements

    Python 3.x

    SciPy library

License

MIT License - free for educational and practical use.

# Run the analysis
python bayesian_test_analysis.py

Author
Dinko Trendafilov
