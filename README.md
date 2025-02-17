# 📊 A/B Testing Cheatsheet

A/B testing is a controlled experiment comparing two versions (A and B) of a variable (webpage, feature, ad, etc.) to determine which performs better in terms of a given metric (e.g., conversion rate, click-through rate).

---

## 🔹 Key Terminology

| Term                  | Definition |
|----------------------|------------|
| **Control Group**     | Group exposed to the original version (A). |
| **Variant Group**     | Group exposed to the new version (B). |
| **Hypothesis**        | Prediction about the outcome of the test. |
| **Conversion**        | Desired user action (purchase, signup, click). |
| **Lift**             | Percentage increase/decrease in performance. |
| **P-value**          | Probability of obtaining observed results under null hypothesis. |
| **Statistical Power** | Probability of correctly rejecting the null hypothesis. |

---

## 🔹 A/B Testing Process

1. **Identify the Objective** – Define the key metric to improve (e.g., conversion rate).
2. **Formulate Hypothesis** – Predict how changes in Version B will impact the metric.
3. **Split the Audience** – Randomly assign users into control (A) and variant (B) groups.
4. **Run the Test** – Expose each group to their respective versions simultaneously.
5. **Measure the Results** – Analyse data using statistical methods.
6. **Draw Conclusions** – Determine if the variant outperforms the control.
7. **Implement Changes** – Deploy Version B if statistically significant.

---

## 🔹 Statistical Significance

- **P-value Interpretation:**
  - `P-value < 0.05` → Reject the null hypothesis (significant result ✅).
  - `P-value > 0.05` → Fail to reject the null hypothesis (no significant result ❌).
- **Confidence Level:**
  - Typically **95%**, meaning a **5% chance of a Type I error (false positive).**
- **Confidence Interval (CI):**
  - Range in which the true difference between A and B lies with **95% confidence**.

---

## 🔹 Types of A/B Tests

| Test Type         | Description |
|------------------|-------------|
| **Simple A/B Test** | Compares two versions (A and B). |
| **Multivariate Test** | Tests multiple elements at once. |
| **Split URL Test** | Tests different web pages (URLs). |
| **Bandit Testing** | Dynamically allocates traffic based on performance. |

---

## 🔹 Common A/B Testing Metrics

**📌 Conversion Metrics**
- **Conversion Rate (CR):** `CR = (Conversions / Total Visitors) * 100%`
- **Click-Through Rate (CTR):** `CTR = (Clicks / Impressions) * 100%`
- **Bounce Rate:** Percentage of visitors who leave without interacting.

**📌 Statistical Metrics**
- **P-value:** Tests statistical significance.
- **Confidence Interval (CI):** Estimates the true performance difference.
- **Lift:** `Lift = ((CR_B - CR_A) / CR_A) * 100%`

**📌 Business Metrics**
- **Revenue per Visitor (RPV):** Measures average revenue per user.
- **Customer Lifetime Value (CLV):** Predicts total revenue from a user.

---

## 🔹 Common Mistakes

❌ **Insufficient Sample Size** – Small samples may lead to unreliable results.  
❌ **Stopping Tests Too Early** – Wait for statistical significance before concluding.  
❌ **Multiple Comparisons Problem** – Testing too many variations increases false positives.  
❌ **Ignoring Seasonality** – Account for traffic patterns (e.g., weekends vs. weekdays).  
❌ **Low Statistical Power** – Increases the risk of Type II errors (false negatives).  

---

## 🔹 A/B Testing Tools

### **📊 A/B Testing Platforms**
- **Google Optimise** – Free tool integrated with Google Analytics.
- **Optimizely** – Advanced multivariate testing & personalisation.
- **VWO (Visual Website Optimiser)** – No-code A/B test creation.
- **Unbounce** – Focused on landing page A/B testing.

### **📈 Statistical Calculators**
- [Evan Miller’s AB Test Calculator](https://www.evanmiller.org/ab-testing/sample-size.html) – Sample size & significance testing.
- [AB Test Guide](https://www.abtestguide.com/) – Online tool for evaluating A/B tests.

---

## 🔹 Useful Python Libraries for A/B Testing

```bash
pip install pandas scipy statsmodels seaborn matplotlib ab-testing-py
```

### **Example: Conducting a t-test with SciPy**
```python
from scipy import stats

# Conversion data
control = [100, 105, 110, 95, 90]  # Control group conversion rates
variant = [110, 115, 120, 108, 102]  # Variant group conversion rates

# Perform an independent t-test
t_stat, p_value = stats.ttest_ind(control, variant)

print(f"T-statistic: {t_stat}")
print(f"P-value: {p_value}")
```

---

📌 **Author:** [@sarahsufi](https://github.com/sarahsufi)  
 


