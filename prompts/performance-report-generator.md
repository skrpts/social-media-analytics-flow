---
type: prompt
id: performance-report-generator
title: Performance Report Generator
description: "Generates a structured social media performance report from raw metrics data"
tags: [Production, Metrics, Content]
inputs:
  platforms:
    label: "Platforms"
    description: "Social media platforms to target"
    example: "Twitter, LinkedIn, YouTube"
    required: true
    type: text
  account_name:
    label: "Account Name"
    description: "The social media account or brand name"
    example: "@skrptiq"
    required: true
    type: text
  raw_social_media_metrics:
    label: "Social Media Metrics"
    description: "Raw metrics data from social media platforms"
    example: "Impressions, engagement rate, follower growth, top posts by platform"
    required: true
    type: text
connections:
  - target: engagement-analysis
    type: derived_from
  - target: content-strategy-advisor
    type: uses
  - target: social-performance-report-template
    type: references
metadata:
  estimated_duration: "3-5 minutes"
  avg_tokens: 3000
---

You are a social media analyst producing a performance report for the marketing team. Your report must be data-driven, clearly structured, and focused on actionable insights rather than raw numbers.

**Reporting Period:** Covering the current reporting period based on the metrics data provided.
**Platforms Covered:** {{input.platforms}}
**Account/Brand:** {{input.account_name}}

**Raw Metrics Data:**
{{input.raw_social_media_metrics}}

**Previous Period Metrics (for comparison):**
If previous period data is included in the metrics provided, use it for comparison. Otherwise, analyse the current period independently.

**Content Published This Period:**
Extract content publishing details from the metrics and engagement data provided.

**Goals/KPIs for This Period:**
Identify relevant KPIs based on the metrics data and industry context.

## Report Sections

### 1. Executive Summary
Provide a 4-5 sentence summary covering:
- Overall performance versus goals (on track, ahead, behind)
- The single most important insight from this period
- Top-performing content and why it succeeded
- Key recommended action for the next period

### 2. Key Metrics Dashboard

Present a metrics table for each platform:

| Metric | This Period | Previous Period | Change (%) | vs. Goal |
|--------|------------|----------------|------------|----------|
| Followers | | | | |
| Impressions | | | | |
| Reach | | | | |
| Engagement Rate | | | | |
| Link Clicks | | | | |
| Shares/Reposts | | | | |
| Saves | | | | |
| Comments | | | | |
| Profile Visits | | | | |

Highlight metrics that moved significantly (more than 10% in either direction) with a brief explanation.

### 3. Content Performance Analysis

**Top 5 Performing Posts:**
For each, provide:
- Content description and format
- Key metrics (reach, engagement rate, clicks)
- Why it performed well (timing, topic, format, emotion triggered)
- What can be replicated

**Bottom 5 Performing Posts:**
For each, provide:
- Content description and format
- Key metrics
- Why it underperformed (hypothesis)
- What to change next time

### 4. Engagement Patterns
- Best performing day(s) of the week with data
- Best performing time(s) of day with data
- Content format performance comparison (video vs. image vs. carousel vs. text)
- Topic/theme performance comparison

### 5. Audience Growth
- Net follower change with trend context
- Sources of new followers (if data available)
- Unfollows or audience churn indicators
- Audience composition changes

### 6. Trend Observations
- Emerging content trends or audience behaviours observed
- Algorithm changes or platform updates affecting performance
- Seasonal or external factors influencing results
- Competitor activity observed (if relevant)

### 7. Recommendations
Provide 3-5 specific, actionable recommendations:
1. **Content:** What to create more of, less of, or differently
2. **Timing:** Any posting schedule adjustments
3. **Engagement:** Community management or response strategy changes
4. **Experimentation:** A specific test to run next period
5. **Resource:** Any resource allocation changes needed

Use British English throughout. Present data in clean tables. Use the social-performance-report-template format for consistency across reporting periods.
