---
type: skill
id: engagement-analysis
title: Engagement Analysis
description: "Analyses social media engagement metrics to identify performance patterns, trends, and actionable insights"
tags: [Production, Tested]
connections:
  - target: llm-service
    type: runs_on
  - target: social-media-metrics-reference
    type: references
metadata:
  estimated_duration: "4-6 minutes"
  avg_tokens: 2500
---

## Capability

Processes raw social media engagement data to identify meaningful patterns, trends, and anomalies. Moves beyond surface-level vanity metrics to extract insights about what is driving engagement, what is underperforming, and where opportunities exist.

## When to Use

- Producing regular social media performance reports
- Diagnosing sudden changes in engagement (drops or spikes)
- Evaluating the impact of a content strategy change
- Benchmarking current performance against historical data
- Preparing data for content strategy planning sessions

## Process

1. **Metric Normalisation** — Standardise metrics across the reporting period. Calculate engagement rate (engagements / impressions or reach), click-through rate, amplification rate (shares per post), and conversation rate (comments per post). Normalise for follower count changes during the period.

2. **Trend Identification** — Compare current period metrics against:
   - Previous period (week-over-week or month-over-month)
   - Same period last year (if data available)
   - Rolling averages (4-week, 12-week)

   Identify statistically meaningful trends versus normal variation. A 5% engagement fluctuation is noise; a 25% sustained change is a trend.

3. **Content Performance Ranking** — Rank all content published during the period by:
   - Engagement rate (primary metric)
   - Reach (awareness metric)
   - Click-through rate (action metric)
   - Shares/saves (value metric)

   Identify the top 10% and bottom 10% of content. Analyse what distinguishes high performers from low performers.

4. **Engagement Pattern Analysis** — Identify patterns in when and how the audience engages:
   - Day-of-week engagement patterns
   - Time-of-day engagement patterns
   - Response time to posts (how quickly engagement accrues)
   - Engagement decay curves (how long posts continue generating engagement)

5. **Anomaly Detection** — Flag unusual patterns:
   - Posts with significantly above or below average performance
   - Sudden follower count changes (gains or losses)
   - Engagement rate shifts not explained by content changes
   - Algorithm-driven reach changes (reach drops with stable engagement rate)

6. **Competitive Context** — If competitor data is available, contextualise performance against industry benchmarks and competitor metrics.

## Inputs

- Raw platform analytics data (impressions, reach, engagement by type, follower count, click-throughs)
- Content log (what was posted, when, content type, topic)
- Previous period data for comparison
- Industry benchmarks (optional)
- Competitor metrics (optional)

## Outputs

- Engagement summary dashboard (key metrics with period-over-period comparison)
- Content performance ranking with top and bottom performers
- Engagement pattern analysis (optimal posting times, content types, formats)
- Anomaly report with likely explanations
- Trend assessment (improving, stable, declining) with confidence level

## Constraints

- Never treat vanity metrics (likes, follower count) as the primary measure of success without context
- Always normalise metrics for follower count and posting frequency changes
- Distinguish between organic and paid performance when data allows
- Avoid drawing conclusions from insufficient data — state minimum sample sizes needed
- Account for platform algorithm changes when interpreting reach and engagement trends
