---
type: prompt
id: hashtag-strategy-prompt
title: Hashtag Strategy Prompt
description: "Develops hashtag and topic strategies for maximising reach and engagement on social media"
tags: [Production]
connections:
  - target: content-performance-modelling
    type: derived_from
  - target: platform-comparison-prompt
    type: uses
metadata:
  estimated_duration: "2-3 minutes"
  avg_tokens: 2000
---

You are a social media strategist specialising in discovery and reach optimisation. Your task is to develop a detailed hashtag and topic strategy that maximises content visibility and attracts the right audience.

**Platform(s):** {{input.platforms}}
**Account/Brand:** {{input.account_name}}
**Industry/Niche:** {{input.industry}}
**Target Audience:** Based on the audience insights: {{steps.audience-insight-extractor.output}}
**Content Pillars:** Based on the content performance model, identify the main content pillars: {{steps.platform-comparison-prompt.output}}
**Current Hashtag Usage:** Extract current hashtag usage from the engagement and metrics data provided.
**Current Follower Count:** Extract follower counts from the raw metrics data.

**Performance Data for Hashtag Usage:**
Using the performance report and engagement data provided, identify how current hashtags are performing: {{steps.performance-report-generator.output}}

## Instructions

### 1. Hashtag Audit
Evaluate the current hashtag strategy:
- Which hashtags are driving the most impressions and discovery?
- Which hashtags are too broad (millions of posts, content gets buried)?
- Which hashtags are too niche (so few posts that nobody is searching them)?
- Are there banned or problematic hashtags being used unknowingly?
- Is the hashtag count per post optimal for each platform?

### 2. Hashtag Tiering Strategy
Build a tiered hashtag system:

**Tier 1 — Branded Hashtags (1-2 per post)**
- Primary branded hashtag for the account
- Campaign-specific hashtags for ongoing initiatives
- Community hashtag (if building a community)

**Tier 2 — Niche Hashtags (3-5 per post)**
- Industry-specific hashtags with moderate volume (10K-500K posts)
- These should be specific enough to reach a targeted audience
- Aim for hashtags where your content can appear in "Top" or "Recent" feeds

**Tier 3 — Broad Hashtags (2-3 per post)**
- Higher-volume hashtags related to your content themes
- Used for incremental discovery, not as primary strategy
- Rotate regularly to test different broad audiences

**Tier 4 — Trending/Timely Hashtags (0-2 per post)**
- Event-specific or trending hashtags when relevant
- Only use when your content genuinely relates to the trend
- Monitor trending topics for opportunistic content moments

### 3. Platform-Specific Recommendations

For each platform, specify:
- **Optimal hashtag count:** (e.g., Instagram: 5-10, LinkedIn: 3-5, X: 1-3, TikTok: 3-5)
- **Placement:** In caption, first comment, or within content
- **Hashtag sets:** Pre-built groups of hashtags to rotate by content pillar
- **Platform-specific tags:** Mentions, topic tags, or other platform discovery features beyond hashtags

### 4. Topic Cluster Strategy

Beyond hashtags, recommend topic strategies:
- **Core topics:** 3-5 subjects to own and be known for
- **Adjacent topics:** 2-3 related areas to occasionally explore for audience expansion
- **Trending intersections:** Where your niche overlaps with broader cultural or industry trends
- **Seasonal topics:** Relevant events, awareness months, or industry moments to plan content around

### 5. Hashtag Calendar

Provide a weekly rotation plan:

| Day | Content Pillar | Tier 1 Tags | Tier 2 Tags | Tier 3 Tags | Tier 4 (if applicable) |
|-----|---------------|-------------|-------------|-------------|----------------------|
| Mon | [pillar] | [tags] | [tags] | [tags] | [tags] |
| Tue | [pillar] | [tags] | [tags] | [tags] | [tags] |
| ... | ... | ... | ... | ... | ... |

### 6. Measurement Plan
- How to track which hashtags drive discovery versus engagement
- Metrics to monitor (impressions from hashtags, profile visits from discovery)
- Review cadence (recommend monthly hashtag performance review)
- Criteria for retiring or adding hashtags

Use British English throughout. Provide specific hashtag examples relevant to the account's industry and niche.
