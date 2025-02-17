What is A/B Testing?
A/B Testing is a controlled experiment comparing two versions (A and B) of a variable (webpage, feature, ad, etc.) to determine which performs better in terms of a given metric (e.g., conversion rate, click-through rate).

Version A: The control or original version.
Version B: The variant, or the version with changes.

Key Terminology
Control Group: The group exposed to the original version (A).
Treatment/Variant Group: The group exposed to the new version (B).
Hypothesis: A prediction about the outcome of the test, often that the variant will outperform the control.
Conversion: The desired user action (e.g., purchase, signup, click).
Lift: The percentage increase/decrease in performance from the control to the variant.
P-value: Probability of obtaining a result as extreme as the observed one, assuming the null hypothesis is true.
Statistical Power: Probability that the test correctly rejects the null hypothesis when it is false.

A/B Testing Process
Identify the Objective: Define the key metric to improve (e.g., click-through rate, conversion rate).
Formulate Hypothesis: Propose changes in Version B and predict how it will impact the metric.
Split the Audience: Randomly assign users into control (A) and variant (B) groups.
Run the Test: Expose each group to their respective versions simultaneously for a set duration.
Measure the Results: Analyse the data using statistical methods.
Draw Conclusions: Determine whether the variant performed better or worse than the control.
Implement Changes: If the variant performs significantly better, deploy it as the new version.
Hypothesis Testing
A/B testing is built on hypothesis testing, which involves:

Null Hypothesis (H₀): Assumes no difference between the control and the variant (e.g., H₀: Conversion rate A = Conversion rate B).
Alternative Hypothesis (H₁): Assumes a difference between the control and the variant (e.g., H₁: Conversion rate A ≠ Conversion rate B).
Statistical Significance
Statistical significance ensures that observed differences in metrics are not due to chance.

P-value:
P-value < α (commonly 0.05): Reject the null hypothesis (significant result).
P-value > α: Fail to reject the null hypothesis (no significant result).
Confidence Level:
The confidence level is typically 95%, meaning there's a 5% chance of a Type I error (false positive).
Confidence Interval (CI):
A range in which the true difference between the control and variant lies with the specified confidence level (e.g., 95% CI).
Types of A/B Tests
Simple A/B Test: Compares two versions (A and B) to determine which performs better.
Multivariate Test: Tests multiple variables at once to see which combination performs best.
Split URL Test: Tests different web pages (URLs) against each other.
Bandit Testing: Dynamically allocates traffic to better-performing versions based on real-time results.
Metrics
The choice of metrics depends on the business goal. Common A/B testing metrics include:

Conversion Metrics
Conversion Rate: 
CR
=
Conversions
Total Visitors
CR= 
Total Visitors
Conversions
​
 
Click-Through Rate (CTR): 
CTR
=
Clicks
Impressions
CTR= 
Impressions
Clicks
​
 
Bounce Rate: Percentage of visitors who leave without interacting.
Statistical Metrics
P-value: Tests statistical significance.
Confidence Interval (CI): Range that estimates the true difference in performance between versions.
Lift: \text{Lift} = \frac{\text{CR_B} - \text{CR_A}}{\text{CR_A}} \times 100 \%
Standard Error (SE): Measures the variability in the metric being analysed.
Business Metrics
Revenue per Visitor (RPV): Measures average revenue generated per user.
Customer Lifetime Value (CLV): Predicts the total revenue from a user over their entire interaction period.
Common Mistakes
Running Tests Without Sufficient Sample Size: If the sample size is too small, results may not be statistically significant.
Stopping the Test Too Early: Stopping a test before reaching statistical significance may lead to incorrect conclusions.
Multiple Comparisons Problem: Testing too many variations at once increases the risk of false positives.
Not Accounting for Seasonality: Differences in traffic patterns (e.g., weekends vs. weekdays) may skew results.
Ignoring Statistical Power: Low statistical power increases the risk of Type II errors (false negatives).

Tools for A/B Testing
A/B Testing Platforms:
Google Optimise: Free A/B testing tool integrated with Google Analytics.
Optimizely: Advanced testing platform with features for multivariate and personalisation testing.
VWO (Visual Website Optimiser): A visual editor for creating A/B tests without coding.
Unbounce: Primarily used for landing page A/B testing.
Statistical Calculators:
Evan Miller’s AB Test Calculator: To calculate significance and sample size.
AB Test Guide: Online tool for evaluating A/B tests.
Useful Python Libraries
Pandas: For handling and analysing test data.
nginx
Copy
Edit
pip install pandas
SciPy: Statistical functions for hypothesis testing (e.g., t-tests).
nginx
Copy
Edit
pip install scipy
Statsmodels: Statistical models for hypothesis testing, including t-tests and regression analysis.
nginx
Copy
Edit
pip install statsmodels
Seaborn & Matplotlib: For visualising test results.
nginx
Copy
Edit
pip install seaborn matplotlib
A/B Testing Py: Dedicated library for A/B testing.
nginx
Copy
Edit
pip install ab-testing-py
Example: Conducting a t-test with SciPy
python
Copy
Edit
from scipy import stats

# Conversion data
control = [100, 105, 110, 95, 90]  # Conversion rates for control group
variant = [110, 115, 120, 108, 102]  # Conversion rates for variant group

# Perform an independent t-test
t_stat, p_value = stats.ttest_ind(control, variant)

print(f"T-statistic: {t_stat}")
print(f"P-value: {p_value}")

