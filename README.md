# PART 2: KPI FRAMEWORK, BUSINESS EXPERIMENT ANALYSIS & DECISION RECOMMENDATION

## Business Context

A subscription-based digital product company launched a new onboarding and activation campaign to improve user conversion and early engagement. Users were randomly divided into control and treatment groups. The objective of the experiment was to evaluate how the new onboarding experience affected conversion and customer quality, and whether it should be rolled out to all users.

## Business Problem

The leadership team needs to determine whether the existing onboarding process should be replaced with the new experience. This decision impacts customers, growth teams, and product teams. The company aims to improve conversion and engagement while maintaining customer quality. Potential risks such as higher support ticket volume, refund requests, slower conversion, and lower revenue quality need to be monitored before making a decision. Any recommendation should be supported by statistical evidence and guardrail metrics.

## Dataset Description

The dataset contains information for 1,408 users who participated in the experiment. It includes user attributes, experiment group assignment, region, device type, traffic source, subscription plan, landing page visits, trial starts, onboarding completion status, paid conversion, revenue generated, support tickets, refund requests, days to conversion, and engagement scores.

## North Star Metric

Paid Conversion Rate was selected as the North Star metric because the onboarding experience directly influences the conversion of users into paying customers. This metric is closely related to revenue growth and overall business performance. Supporting metrics such as trial start rate, onboarding completion rate, engagement score, and revenue metrics help explain the behavior behind conversion but are not the primary success metric.

## KPI Framework

The KPI framework was built around Paid Conversion Rate. Three major drivers were identified:

- User Acquisition Quality
- User Activation and Engagement
- Revenue Generation

User acquisition quality was represented by landing page visit rate and trial start rate. User activation and engagement included onboarding completion rate and engagement score. Revenue generation was measured using Average Revenue per User (ARPU) and Average Revenue per Converted User (ARPCU).

### Guardrail Metrics

- Refund Rate
- Support Ticket Rate
- Average Days to Convert

## Data Preparation and Cleaning

The experiment dataset was checked for missing values, duplicate user IDs, invalid binary values, revenue outliers, and segment distribution.

- Missing values in device type and traffic source were replaced with **"Unknown"**.
- Missing engagement scores were filled using the median value.
- Missing values in days to convert were left unchanged because they corresponded to users who did not convert.
- Duplicate user IDs were removed.
- Revenue outliers were retained because they may represent legitimate high-value customers.

## Experiment Analysis Approach

The experiment compared the performance of the control and treatment groups across multiple metrics, including:

- Landing page visit rate
- Trial start rate
- Onboarding completion rate
- Paid conversion rate
- Revenue metrics
- Support ticket rate
- Refund rate
- Engagement score
- Average days to convert

Additional segment-level analysis was performed based on region, device type, and traffic source.

## Hypothesis Testing

Paid Conversion Rate was selected as the primary metric for statistical testing.

### Null Hypothesis (H0)

There is no difference in paid conversion rates between the control and treatment groups.

### Alternative Hypothesis (H1)

The treatment group achieves a higher paid conversion rate than the control group.

### Statistical Test

A one-tailed two-proportion z-test was performed with a significance level of 0.05.

### Results

- Z-statistic = 3.264
- P-value = 0.000549

Since the p-value is less than 0.05, the null hypothesis was rejected. This indicates that the treatment group achieved a statistically significant improvement in paid conversion rate.

## Guardrail Analysis

Guardrail metrics were analyzed to ensure that improvements in conversion did not negatively affect customer quality.

### Positive Findings

- Higher engagement scores in the treatment group.
- Faster conversion times.
- Improved conversion rates across all regions.

### Risks Identified

- Support ticket rates increased significantly.
- Refund requests increased slightly.
- Average revenue per converted user decreased considerably.

These findings suggest that although the treatment improves conversion, there are concerns regarding customer quality and support burden.

## Final Recommendation

The treatment group demonstrated a statistically significant improvement in paid conversion rate. However, the increase in support ticket rates and the decline in revenue per converted user suggest that a full rollout may be premature.

Continuing experimentation or gradually introducing the treatment to selected segments would be a safer approach. Further investigation into customer quality, retention, and support issues is recommended before deploying the new onboarding experience to all users.

## Assumptions and Limitations

- The analysis is based on a single experiment period.
- Long-term retention and customer lifetime value were not evaluated.
- Revenue outliers were retained because they may represent legitimate high-value customers.
- Missing values in days to convert correspond to users who did not convert and were therefore left unchanged.
- Additional experiments may be required to validate the findings over longer periods.

## Screenshots Included

The repository contains the following screenshots:

- `summary_metrics.png`
- `hypothesis_test_output.png`
- `kpi_tree_preview.png`

These screenshots provide supporting evidence for the analysis and conclusions.

## Repository Contents

- `campaign_experiment_data.xlsx`
- `experiment_analysis.xlsx`
- `hypothesis_test_notes.md`
- `experiment_summary.xlsx`
- `recommendation_memo.md`
- `kpi_tree.png`
- `summary_metrics.png`
- `hypothesis_test_output.png`
- `kpi_tree_preview.png`
- `README.md`
