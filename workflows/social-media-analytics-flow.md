---
type: workflow
id: social-media-analytics-flow
title: Social Media Analytics Flow
description: "Social media performance analysis, content strategy optimisation, and audience insight extraction"
tags: [Production, Tested, Audience, Metrics]
connections:
  - target: engagement-analysis
    type: uses
  - target: audience-profiling
    type: uses
  - target: content-performance-modelling
    type: uses
  - target: audience-segmentation
    type: uses
  - target: llm-service
    type: runs_on
  - target: social-media-metrics-reference
    type: references
  - target: social-media-analytics-guide
    type: references
  - target: campaign-performance-benchmarks
    type: references
  - target: visual-spec-generation
    type: uses
metadata:
  estimated_duration: "20-35 minutes"
  trigger: manual
execution:
  - skill: "engagement-analysis"
    step_type: "synthesis"
  - skill: "audience-profiling"
    step_type: "synthesis"
    input_from: "engagement-analysis"
  - skill: "content-performance-modelling"
    step_type: "synthesis"
    input_from: "audience-profiling"
  - skill: "audience-segmentation"
    step_type: "synthesis"
    input_from: "content-performance-modelling"
  - skill: "visual-spec-generation"
    step_type: "synthesis"
    input_from: "audience-segmentation"
---

## Overview

This workflow analyses social media performance data to produce actionable insights, content strategy recommendations, and audience intelligence. It moves from raw metrics analysis through audience profiling, content performance modelling, and strategic recommendations. Designed to run on a regular cadence (weekly or monthly) to track trends and optimise social media strategy.

## Pipeline Stages

### Stage 1: Performance Data Analysis

**Input:** Raw social media metrics exported from platform analytics (impressions, reach, engagement, followers, clicks) across the reporting period

Invoke the **engagement-analysis** skill to process raw metrics and identify performance patterns, trends, and anomalies. Then run the **performance-report-generator** prompt to produce a structured performance report.

**Output:** Performance report with key metrics, trend analysis, top-performing content identification, and underperforming content flags.

**Gate:** Minimum one full week of data required for meaningful analysis. Monthly reporting requires at least 4 weeks.

### Stage 2: Audience Insight Extraction

**Input:** Engagement data by content type, demographic data (if available), follower growth patterns, audience activity patterns

Invoke the **audience-profiling** skill to build audience profiles from engagement patterns. Then run the **audience-insight-extractor** prompt to produce detailed audience intelligence.

**Output:** Audience profiles including content preferences, peak activity times, demographic indicators, and engagement behaviour patterns.

### Stage 3: Content Performance Modelling

**Input:** Performance data from Stage 1, audience insights from Stage 2, content calendar and posting history

Invoke the **content-performance-modelling** skill to identify what drives high performance. Analyse content by format, topic, posting time, length, visual style, and tone to build a performance model.

**Output:** Content performance model showing which variables correlate with high engagement, reach, and conversion.

### Stage 4: Platform Comparison & Resource Allocation

**Input:** Performance data across all active platforms, current resource allocation (time and budget per platform)

Invoke the **platform-comparison-prompt** to compare performance across platforms and recommend resource reallocation based on ROI.

**Output:** Platform comparison matrix with resource allocation recommendations.

**Note:** This stage is optional for single-platform strategies. Most valuable for teams managing 3+ platforms.

### Stage 5: Strategy Recommendations

**Input:** All outputs from Stages 1-4, current content strategy and goals

Invoke the **content-strategy-advisor** prompt to produce strategic recommendations based on the performance data, audience insights, and content model. Then run the **hashtag-strategy-prompt** to develop hashtag and topic strategies.

**Output:** Content strategy adjustment recommendations, updated posting schedule, content mix recommendations, hashtag strategy, and topic calendar suggestions.

## Error Handling

- If data is insufficient for statistical confidence, note the limitation and provide directional insights rather than definitive conclusions
- If audience demographic data is unavailable, infer audience characteristics from engagement patterns and content preferences, flagging these as inferences
- If a platform's API changes or data format shifts, adapt the analysis approach and note any comparability issues with previous periods
- If engagement drops across all content, investigate external factors (algorithm changes, seasonal patterns, audience fatigue) before recommending content changes
- If metrics appear anomalous (sudden spikes or drops), investigate the cause (viral content, paid promotion, bot activity) before including in trend analysis

## Reporting Cadence

| Report Type | Frequency | Depth | Audience |
|-------------|-----------|-------|----------|
| Quick metrics check | Weekly | KPI dashboard only | Social media manager |
| Performance report | Fortnightly/Monthly | Full analysis with recommendations | Marketing team |
| Strategic review | Quarterly | Full review with audience insights and strategy shifts | Marketing leadership |

## Inputs

| Name | Required | Description | Example |
|------|----------|-------------|---------|
| `{{input.platforms}}` | Yes | Social media platforms being analysed | `Instagram, LinkedIn, X, TikTok` |
| `{{input.account_name}}` | Yes | Account or brand name | `Acme Corp` |
| `{{input.industry}}` | Yes | Industry or niche | `B2B SaaS marketing` |
| `{{input.raw_social_media_metrics}}` | Yes | Raw social media metrics exported from platform analytics across the reporting period | `Paste the latest metrics, exported data, or summary notes relevant to the workflow.` |
| `{{input.engagement_data_by_content}}` | Yes | Engagement data by content type | `Paste the latest metrics, exported data, or summary notes relevant to the workflow.` |
| `{{input.demographic_data}}` | Yes | Demographic data | `Paste the latest metrics, exported data, or summary notes relevant to the workflow.` |
| `{{input.follower_growth_patterns}}` | No | Follower growth patterns | `Paste the relevant brief, notes, source material, or dataset here.` |

## Outputs

| Name | Description |
|------|-------------|
| Performance report | Performance report with key metrics, trend analysis, top-performing content identification, and underperforming content flags |
| Audience profiles including content preferences, peak activity times, demographic indicators, and engagement behaviour patterns | Audience profiles including content preferences, peak activity times, demographic indicators, and engagement behaviour patterns |
| Content performance model showing which variables correlate | Content performance model showing which variables correlate with high engagement, reach, and conversion |
| Platform comparison matrix | Platform comparison matrix with resource allocation recommendations |
| Content strategy adjustment recommendations, updated posting schedule, content mix recommendations, hashtag strategy, and topic calendar suggestions | Content strategy adjustment recommendations, updated posting schedule, content mix recommendations, hashtag strategy, and topic calendar suggestions |

## Setup

Before running this workflow:

1. No external services required — paste your content directly and provide any supporting context as inputs or source nodes.
2. Review the included documents, assets, or source nodes and customise them to match your team, brand, or domain conventions where needed.
3. No specific AI provider or API key is required beyond your configured skrptiq LLM provider.

## Provider Notes

- Most stages work with any capable model; stronger models usually improve synthesis, judgement, and writing quality.
- Extraction, classification, and formatting steps generally run well on smaller or faster models.
- Because there are no vendor-specific integrations here, provider choice is mostly a trade-off between speed, quality, and cost.

## Example Input

To test this workflow immediately after import:

```
Platforms: "Instagram, LinkedIn, X, TikTok"
Account Name: "Acme Corp"
Industry: "B2B SaaS marketing"
Raw Social Media Metrics: "Paste the latest metrics, exported data, or summary notes relevant to the workflow."
Engagement Data By Content: "Paste the latest metrics, exported data, or summary notes relevant to the workflow."
Demographic Data: "Paste the latest metrics, exported data, or summary notes relevant to the workflow."
Follower Growth Patterns: "Paste the relevant brief, notes, source material, or dataset here."
```

