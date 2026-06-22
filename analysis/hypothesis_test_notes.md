## Task 6: Frame Hypotheses

# Hypothesis Test Notes

---

## 1.Null Hypothesis (H0)

There is no statistically significant difference in Paid Conversion Rate between the Control group and the Treatment group.

Control Paid Conversion Rate = Treatment Paid Conversion Rate

---

## 2.Alternative Hypothesis (H1)

The Treatment group has a higher Paid Conversion Rate than the Control group.

Treatment Paid Conversion Rate > Control Paid Conversion Rate

---

## 3.Whether the test is one-tailed or two-tailed

One-Tailed Test

A one-tailed test was selected because the business objective is specifically to determine whether the new onboarding 
experience improves Paid Conversion Rate compared to the existing onboarding process.

---

## 4.Significance level used

α = 0.05 (5%)

A significance level of 5% was used. If the p-value is less than 0.05, the null hypothesis will be rejected.

---

## 5.Metric Being Tested

Paid Conversion Rate

The Paid Conversion Rate was selected as the primary metric because the objective of the onboarding campaign is to increase 
the number of users who become paying subscribers. Improving paid conversion directly contributes to revenue growth and 
long-term business performance.

## 6.Reason for choosing that metric

Paid Conversion Rate is the North Star Metric for this experiment because it directly measures the percentage of users who
become paying customers after experiencing the onboarding process.

Unlike engagement or onboarding completion metrics, Paid Conversion Rate has a direct impact on business revenue and customer 
growth. Therefore, it is the most appropriate metric for evaluating whether the campaign 
should be launched to all users.

---

## Decision Rule

If p-value < 0.05:
- Reject the Null Hypothesis
- Conclude that the Treatment group significantly improves Paid Conversion Rate

If p-value ≥ 0.05:
- Fail to Reject the Null Hypothesis
- Conclude that there is insufficient evidence that the Treatment group improves Paid Conversion Rate

---

## Interpretation Logic

A statistically significant increase in Paid Conversion Rate would indicate that the new onboarding experience successfully 
encourages more users to become paying customers.

However, the final business recommendation should not be based solely on conversion improvement. Guardrail metrics such as 
Refund Rate, Support Ticket Rate, Engagement Score, and Days to Convert must also be evaluated to ensure that the conversion 
gains do not come at the expense of customer experience or revenue quality.

---

## Connection to Business Decision

The purpose of this hypothesis test is to support the leadership team's decision on whether the new onboarding experience 
should be rolled out to all users.

If the Treatment group demonstrates a statistically significant improvement in Paid Conversion Rate while maintaining 
acceptable guardrail metrics, a broader rollout can be recommended. Otherwise, the company should continue testing or limit 
deployment to specific user segments.


## Task 7: Perform Hypothesis or A/B Test Analysis


## Test Inputs

| Metric | Control | Treatment |
|----------|----------:|----------:|
| Users | 693 | 715 |
| Conversions | 22 | 50 |
| Conversion Rate | 3.17% | 6.99% |

## Test Results

- Test Type: Two-Proportion Z-Test
- Test Statistic (Z): 3.25
- P-Value: 0.0006
- Significance Level (α): 0.05

## Decision

Because the p-value (0.0006) is less than the significance level of 0.05, the Null Hypothesis is rejected.

## Business Interpretation

The Treatment group achieved a significantly higher Paid Conversion Rate than the Control group. Statistical evidence suggests that the observed improvement 
is unlikely to be due to random chance.

The new onboarding experience increased Paid Conversion Rate from 3.17% to 6.99%, representing a substantial improvement in user conversion performance.

Based on the hypothesis test results, the Treatment experience demonstrates a positive impact on the primary business metric and should be considered for rollout, 
subject to evaluation of guardrail metrics.




