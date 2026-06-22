hypothesis_notes = """# Hypothesis Test Notes

## Metric Being Tested

The primary metric selected for the experiment is **Paid Conversion Rate**, defined as the proportion of users who converted to a paid subscription.

---

## Null Hypothesis (H0)

There is no difference in paid conversion rates between the Control and Treatment groups.

H0: p_control = p_treatment

---

## Alternative Hypothesis (H1)

The Treatment group has a higher paid conversion rate than the Control group.

H1: p_treatment > p_control

---

## Type of Test

A **one-tailed hypothesis test** is used because the business objective is to determine whether the new onboarding experience improves paid conversion.

---

## Significance Level

α = 0.05

---

## Decision Rule

- If p-value < 0.05, reject the null hypothesis.
- If p-value ≥ 0.05, fail to reject the null hypothesis.

---

## Reason for Choosing the Metric

Paid Conversion Rate was selected as the North Star Metric because it directly measures the ability of the onboarding experience to convert users into paying customers and is closely linked to business growth and revenue generation.

---

## Interpretation Logic

If the Treatment group shows a statistically significant improvement in paid conversion rate and guardrail metrics remain acceptable, the new onboarding experience can be recommended for launch. Otherwise, further testing or segment-specific rollout should be considered.
"""

with open("hypothesis_test_notes.md", "w", encoding="utf-8") as f:
    f.write(hypothesis_notes)

print("hypothesis_test_notes.md created successfully.")

## Test Inputs

- Treatment group size: 710
- Treatment conversions: 50
- Control group size: 690
- Control conversions: 22

---

## Statistical Test

A one-tailed two-proportion z-test was performed to determine whether the treatment group achieved a higher paid conversion rate than the control group.

---

## Test Output

- Z-statistic = 3.264
- P-value = 0.000549

---

## Decision Rule

Reject the null hypothesis if p-value < 0.05.

Since the p-value (0.000549) is less than 0.05, the null hypothesis is rejected.

---

## Business Interpretation

The treatment group achieved a statistically significant improvement in paid conversion rate compared with the control group. Therefore, the new onboarding experience appears to increase user conversion. However, guardrail metrics must be evaluated before making a final rollout recommendation.