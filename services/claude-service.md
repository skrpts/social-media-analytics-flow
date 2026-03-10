---
type: service
id: claude-service
title: Claude Service
description: "How this skrpt uses Anthropic Claude for social media data analysis, audience profiling, and strategy recommendations"
tags: [Production, Tested]
connections: []
metadata:
  provider: "anthropic"
  model: "claude-sonnet"
  estimated_duration: "N/A"
---

## Claude Service — Social Media Analytics Flow

This skrpt uses Anthropic Claude as its primary AI service for analysing social media performance data, building audience profiles, and generating content strategy recommendations.

### Usage Pattern

Claude is invoked at each stage of the analytics pipeline:

1. **Engagement Analysis** — Claude processes raw social media metrics to identify performance patterns, trends, and anomalies. This requires statistical reasoning, the ability to normalise metrics across different periods, and pattern recognition to distinguish signal from noise.

2. **Performance Reporting** — Claude compiles analytics data into structured, executive-ready reports with key insights and actionable recommendations. This requires data synthesis, clear communication of statistical concepts, and the ability to translate numbers into strategic insights.

3. **Audience Profiling** — Claude builds audience profiles from engagement data, demographics, and behavioural signals. This requires inference from incomplete data, segmentation logic, and understanding of social media user behaviour patterns.

4. **Content Performance Modelling** — Claude analyses historical content data to identify variables that correlate with high performance. This requires multivariate analysis reasoning, the ability to identify confounding variables, and honest assessment of model limitations.

5. **Platform Comparison** — Claude evaluates cross-platform performance to recommend resource allocation. This requires comparative analysis, understanding of platform-specific metrics and algorithms, and strategic reasoning about ROI.

6. **Strategy Recommendations** — Claude generates content strategy, hashtag strategy, and engagement tactics based on data analysis. This requires creative strategy development grounded in data, understanding of social media best practices, and practical recommendations within resource constraints.

### Configuration

- **Temperature:** 0.3 for data analysis (engagement analysis, performance modelling), 0.5 for strategic recommendations (content strategy, hashtag strategy)
- **Max tokens:** 3000 per invocation, 3500 for comprehensive strategy recommendations
- **Context window:** Pipeline stages are sequential. Performance data feeds into audience insights, which feed into strategy recommendations.

### Data Handling

This skrpt processes social media metrics and audience data. Claude:
- Analyses aggregate metrics only — no individual user data processing
- Does not store or retain social media data between sessions
- Treats all input data as confidential to the user's organisation
- Provides analysis based on the data provided — does not access platform APIs directly

### Requirements

- An active Anthropic API key or Claude CLI access
- Sufficient token quota for the full pipeline (approximately 15,000-20,000 tokens per complete analysis)
- Social media analytics data exported from platform native analytics or third-party tools
