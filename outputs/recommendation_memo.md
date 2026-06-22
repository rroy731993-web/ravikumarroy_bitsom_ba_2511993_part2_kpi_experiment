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
