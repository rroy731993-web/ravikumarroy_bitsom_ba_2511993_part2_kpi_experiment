# ravikumarroy_bitsom_ba_2511993_part2_kpi_experiment
Part 2: KPI Framework, Business Experiment Analysis &amp; Decision Recommendation

## Task 1: Understand the Business Problem

## Business Problem Statement

The company recently introduced a new onboarding and activation campaign with the goal of helping more users successfully move from signup to paid subscription.

### What decision needs to be made?

Before rolling out this new experience to all users, leadership wants to determine whether the new onboarding campaign delivers meaningful business value compared to the current onboarding process and whether it should be launched company-wide.

### Who does this decision impact?

This decision impacts several teams, including Product, Marketing, Customer Success, Revenue Operations, and Executive Leadership. A full rollout could influence customer acquisition, user experience, operational workload, and overall revenue growth.

### What metric should improve?

The primary metric expected to improve is the **Paid Conversion Rate**, which measures the percentage of users who become paying customers. In addition, improvements in user engagement and onboarding completion are considered positive indicators of campaign success.

### What risks must be monitored?

While increasing conversion is important, the company must ensure that the new onboarding experience does not create unintended negative consequences such as:

* Increased support ticket volume
* Higher refund rates
* Longer conversion times
* Reduced user satisfaction
* Poor performance within specific customer segments

### What evidence is required before making a recommendation?

To make an informed recommendation, the experiment must provide statistically significant evidence that the Treatment group performs better than the Control group on the primary success metric while maintaining acceptable performance across key guardrail metrics such as refund rate, support ticket rate, engagement score, and days to convert.





## Task 2: Define the North Star Metric



### Selected North Star Metric: Paid Conversion Rate

**Definition**

Paid Conversion Rate = Number of Users Converted to Paid Subscribers / Total Number of Users

### Why this metric is the main success metric

Paid Conversion Rate is the most important metric for this experiment because the primary goal of the new onboarding campaign is to help more users become paying customers. Since the company operates on a subscription-based business model, increasing the percentage of users who convert to paid plans directly contributes to revenue growth.

## Why other metrics are supporting metrics instead of the North Star

While several other metrics provide valuable insights, they do not directly represent business success. For example:

* Landing Page Visit Rate measures initial interest.
* Trial Start Rate measures activation.
* Onboarding Completion Rate measures onboarding effectiveness.
* Engagement Score measures user interaction.

These metrics help explain user behavior throughout the journey, but Paid Conversion Rate ultimately determines whether the campaign achieves its business objective.

### How this metric connects to business growth

An increase in Paid Conversion Rate means more users become paying customers, leading to higher subscription revenue and improved return on customer acquisition efforts. Therefore, improving this metric directly supports sustainable business growth.

### What could go wrong if this metric is optimized blindly

Focusing only on Paid Conversion Rate could lead to unintended consequences. Users might convert initially but experience confusion or dissatisfaction later, resulting in higher refund requests, increased support tickets, or poor long-term retention. Therefore, guardrail metrics such as Refund Rate, Support Ticket Rate, Engagement Score, and Days to Convert must also be monitored.



## Task 4: Clean and Prepare Experiment Data



## Data Preparation and Quality Checks

Before performing the experiment analysis, the dataset was reviewed to ensure data quality and suitability for A/B test evaluation.

### Missing Values Check

A missing value assessment was performed across all variables. Most fields contained complete data. Minor missing values were identified in the `device_type`, `traffic_source`, and `engagement_score` columns. A large number of missing values were observed in `days_to_convert`; however, this was expected because users who did not convert to a paid subscription do not have a conversion date. Therefore, no corrective action was required.
| Column Name          | Missing Values |
| -------------------- | -------------: |
| user_id              |              0 |
| signup_date          |              0 |
| experiment_group     |              0 |
| region               |              0 |
| device_type          |             18 |
| traffic_source       |             24 |
| plan_type            |              0 |
| visited_landing_page |              0 |
| started_trial        |              0 |
| completed_onboarding |              0 |
| converted_to_paid    |              0 |
| revenue_30d          |              0 |
| support_tickets_30d  |              0 |
| refund_requested     |              0 |
| days_to_convert      |           1335 |
| engagement_score     |             14 |


### Group Count Validation

The experiment dataset contained 1,408 users, with 693 users assigned to the Control group and 715 users assigned to the Treatment group. The distribution of users across groups was reasonably balanced, providing a reliable basis for comparison.
| Group     | User Count |
| --------- | ---------: |
| Control   |        693 |
| Treatment |        715 |
| Total     |       1408 |


### Duplicate User ID Check

A duplicate review was performed on the `user_id` field. The analysis identified 8 unique duplicate user IDs, representing 16 duplicate records. These records were reviewed and flagged before analysis. No records were removed because the duplicates did not materially affect the experiment evaluation.

| Check                    | Result                               |
| ------------------------ | ------------------------------------ |
| Duplicate User IDs Found | 8                                    |
| Action Taken             | Reviewed and flagged before analysis |


### Binary Value Validation

All binary variables were validated to ensure that only valid values (0 and 1) were present. The fields `visited_landing_page`, `started_trial`, `completed_onboarding`, `converted_to_paid`, and `refund_requested` contained only valid binary values. No invalid binary values were detected and no corrective action was required.

| Column               | Valid Values | Result |
| -------------------- | ------------ | ------ |
| visited_landing_page | 0,1          | Pass   |
| started_trial        | 0,1          | Pass   |
| completed_onboarding | 0,1          | Pass   |
| converted_to_paid    | 0,1          | Pass   |
| refund_requested     | 0,1          | Pass   |

### Revenue Outlier Review

Revenue values were reviewed for unusually high observations using the Interquartile Range (IQR) method.

| Metric | Value |
|----------|----------:|
| Minimum Revenue | 0.00 |
| Maximum Revenue | 8610.72 |
| Average Revenue | 52.83 |
| Revenue Records Above Upper Bound | 72 |

The revenue distribution was highly skewed because a large proportion of users generated no revenue during the observation period. As a result, both the first quartile (Q1) and third quartile (Q3) were equal to zero, resulting in an IQR value of zero. A total of 72 revenue records exceeded the calculated upper bound and were flagged as potential outliers.

These observations were retained in the dataset because they likely represent legitimate high-value customers and provide important information about business performance. Removing them could have understated the true revenue impact of the experiment.


### Segment Distribution Validation

Segment distribution was reviewed across Region, Device Type, Traffic Source, and Plan Type to ensure that the Control and Treatment groups were reasonably comparable before evaluating experiment outcomes.

#### Region Distribution

| Region | Control | Treatment |
|----------|----------:|----------:|
| East | 158 | 172 |
| North | 203 | 180 |
| South | 184 | 184 |
| West | 148 | 179 |

#### Device Type Distribution

| Device Type | Control | Treatment |
|-------------|----------:|----------:|
| Desktop | 200 | 214 |
| Mobile | 428 | 436 |
| Tablet | 56 | 56 |
| Missing | 9 | 9 |

#### Traffic Source Distribution

| Traffic Source | Control | Treatment |
|----------------|----------:|----------:|
| Email | 74 | 56 |
| Organic | 246 | 241 |
| Paid Search | 156 | 176 |
| Referral | 81 | 91 |
| Social | 130 | 133 |
| Missing | 6 | 18 |

#### Plan Type Distribution

| Plan Type | Control | Treatment |
|------------|----------:|----------:|
| Basic | 223 | 235 |
| Free | 361 | 368 |
| Premium | 109 | 112 |

#### Observation

The Control and Treatment groups showed reasonably balanced representation across Region, Device Type, Traffic Source, and Plan Type. While minor differences were observed, no major imbalance was identified that would invalidate the experiment comparison.

The Treatment group contained slightly more users from the West region and Paid Search traffic source. However, the overall distribution remained sufficiently similar across groups to support a fair evaluation of experiment performance.

Based on these checks, the dataset was considered suitable for A/B test analysis.
