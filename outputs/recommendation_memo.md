## Recommendation Memo

## Business Problem Summary

The company introduced a new onboarding and activation campaign to help more users progress from signup to paid subscription. 
The key decision is whether this new onboarding experience should be rolled out to all users or if the existing onboarding process should remain in place.
This decision impacts teams across Product, Marketing, Customer Success, and Revenue Operations because it can affect user acquisition, customer experience,
support workload and revenue growth.
The primary goal of the experiment is to improve the Paid Conversion Rate while maintaining a positive user experience. Potential risks include increased 
refund requests, higher support ticket volumes and weaker performance among certain customer segments.
A final recommendation will be based on statistical evidence showing whether the Treatment group performs better than the Control group while maintaining 
acceptable guardrail metrics.


## North Star Metric

The North Star Metric selected for this experiment is **Paid Conversion Rate**.

Paid Conversion Rate was chosen because the primary objective of the onboarding campaign is to increase the number of users who become paying subscribers. Since the company operates on a subscription-based business model, improving this metric directly contributes to revenue growth and business success.

Supporting metrics such as Landing Page Visit Rate, Trial Start Rate, Onboarding Completion Rate, and Engagement Score help explain user behavior throughout the onboarding journey, but they do not directly measure the final business outcome.

While improving Paid Conversion Rate is important, optimizing it in isolation could create unintended consequences such as higher refund requests, increased support ticket volume, or reduced customer satisfaction. Therefore, guardrail metrics were also evaluated alongside the North Star Metric.




## Task 8: Evaluate Guardrail Metrics

## Guardrail Metrics Evaluation

The experiment was not evaluated solely on Paid Conversion Rate. Additional guardrail metrics were reviewed to ensure that the new onboarding experience did not negatively impact customer experience or business quality.

| Guardrail Metric | Control | Treatment | Assessment |
|----------|----------:|----------:|----------|
| Refund Rate | 0.00% | 0.42% | Increased |
| Support Ticket Rate | 14.72% | 24.76% | Increased |
| Average Engagement Score | 57.03 | 62.93 | Improved |
| Average Days to Convert | 8.86 | 6.40 | Improved |

### Refund Rate

The Refund Rate increased from 0.00% in the Control group to 0.42% in the Treatment group. Although the increase is relatively small, it indicates that a small number of users requested refunds after conversion. This metric should continue to be monitored after rollout.

### Support Ticket Rate

The Support Ticket Rate increased from 14.72% to 24.76%. This is the primary risk identified during the experiment. The increase suggests that users may require additional assistance while navigating the new onboarding experience.

### Average Engagement Score

The Average Engagement Score improved from 57.03 to 62.93. This indicates that users exposed to the new onboarding experience were more actively engaged with the product.

### Average Days to Convert

The average number of days required to convert decreased from 8.86 days to 6.40 days. This suggests that the new onboarding experience helps users understand product value faster and convert more quickly.

### Segment-Level Review

Paid Conversion Rate improved across all geographic regions and across most device and traffic source segments. The only notable decline was observed in the Social traffic segment, where conversion decreased slightly from 7.69% to 6.02%.

### Guardrail Risk Assessment

The increase in Support Ticket Rate represents the most significant guardrail risk identified during the experiment. The slight increase in Refund Rate should also be monitored. However, improvements in Engagement Score, Days to Convert, and Paid Conversion Rate suggest that the overall business impact remains positive.





## Executive Summary

This analysis evaluated the impact of a new onboarding and activation campaign designed to improve user conversion and engagement. Users were randomly assigned to either the Control group (existing onboarding experience) or the Treatment group (new onboarding experience).

The Treatment group demonstrated significantly stronger performance across key business metrics, including Paid Conversion Rate, Onboarding Completion Rate, Engagement Score, and Average Revenue Per User. Statistical testing confirmed that the improvement in Paid Conversion Rate was significant and unlikely to be due to random variation.

While the Treatment group also showed increases in Support Ticket Rate and Refund Rate, the overall business impact was positive. Based on the results of the experiment, a broader rollout of the new onboarding experience is recommended with continued monitoring of guardrail metrics.

---

## KPI Tree Explanation

The North Star Metric for this experiment is Paid Conversion Rate.

The KPI Tree was designed to identify the key drivers influencing conversion performance.

Primary KPI Drivers:

1. User Acquisition Quality

   * Traffic Source Quality
   * Landing Page Visit Rate

2. User Activation

   * Trial Start Rate
   * Onboarding Completion Rate

3. User Engagement

   * Engagement Score
   * Days to Convert

Guardrail Metrics:

* Refund Rate
* Support Ticket Rate
* Segment-Level Performance

These metrics help ensure that conversion improvements are achieved without negatively affecting customer experience or revenue quality.

---

## Experiment Result Summary

| Metric                     | Control | Treatment |
| -------------------------- | ------: | --------: |
| Paid Conversion Rate       |   3.17% |     6.99% |
| Onboarding Completion Rate |  15.58% |    21.26% |
| Average Revenue Per User   |   51.75 |     53.88 |
| Average Engagement Score   |   57.03 |     62.93 |
| Average Days to Convert    |    8.86 |      6.40 |

The Treatment group outperformed the Control group across most primary performance metrics, indicating that the new onboarding experience was more effective at guiding users toward conversion and engagement.

---

## Hypothesis Test Interpretation

A Two-Proportion Z-Test was conducted using Paid Conversion Rate as the primary success metric.

Test Results:

* Control Conversion Rate: 3.17%
* Treatment Conversion Rate: 6.99%
* Z Statistic: 3.25
* P-Value: 0.0006
* Significance Level: 0.05

Since the p-value was significantly lower than 0.05, the Null Hypothesis was rejected.

This provides strong statistical evidence that the Treatment group achieved a higher Paid Conversion Rate than the Control group.

---

## Segment-Level Insight

Paid Conversion Rate improved across all geographic regions and most device and traffic source segments.

Key observations:

* North Region showed the largest regional improvement.
* Mobile users demonstrated the strongest device-level improvement.
* Referral traffic produced the highest increase in conversion rate.
* Social traffic was the only major segment where Treatment performed slightly worse than Control.

Overall, the positive treatment effect was broadly consistent across customer segments.

---

## Final Recommendation

Recommendation: Launch

The Treatment group delivered a statistically significant improvement in Paid Conversion Rate while also increasing user engagement and reducing the average time required for users to convert.

Although Support Ticket Rate and Refund Rate increased, these risks appear manageable relative to the magnitude of conversion improvement observed during the experiment.

Therefore, the new onboarding experience should be launched to all users while maintaining ongoing monitoring of guardrail metrics.

---

## Risks and Limitations

* Support Ticket Rate increased significantly in the Treatment group.
* Refund Rate increased slightly compared to the Control group.
* Some fields contained missing values that were retained during analysis.
* The experiment reflects only the observed test period and may not capture long-term customer behavior.
* Segment-level performance should continue to be monitored after rollout.

---

## Next Steps

1. Roll out the new onboarding experience to all users.
2. Continue monitoring Support Ticket Rate and Refund Rate.
3. Investigate the weaker performance observed within the Social traffic segment.
4. Conduct follow-up experiments to optimize onboarding steps that generate support requests.
5. Review long-term retention and revenue outcomes after implementation.
