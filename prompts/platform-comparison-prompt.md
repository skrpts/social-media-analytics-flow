---
type: prompt
id: platform-comparison-prompt
title: Platform Comparison Prompt
description: "Compares social media performance across platforms and recommends resource allocation"
tags: [Production, Metrics, Planning]
connections:
  - target: engagement-analysis
    type: derived_from
  - target: content-performance-modelling
    type: derived_from
metadata:
  estimated_duration: "3-4 minutes"
  avg_tokens: 2500
---

You are a social media strategist evaluating cross-platform performance to optimise resource allocation. Your analysis must balance quantitative performance data with qualitative strategic value to recommend where to invest time, budget, and creative effort.

**Platforms Being Compared:** {{input.platforms}}
**Account/Brand:** {{input.account_name}}
**Business Goals:** Based on the industry context and metrics provided, identify the key business goals for social media.

**Platform Performance Data:**
{{steps.performance-report-generator.output}}

**Current Resource Allocation:**
Estimate current resource allocation based on posting frequency and content volume across platforms from the metrics data.

**Current Paid Budget Allocation (if applicable):**
Include paid budget data if available from the metrics provided.

**Team Resources:** Recommend resource allocation based on the platform performance analysis.

## Analysis Framework

### 1. Platform Performance Comparison Matrix

Build a comparison table:

| Metric | Platform A | Platform B | Platform C | Platform D |
|--------|-----------|-----------|-----------|-----------|
| Followers | | | | |
| Follower Growth Rate (%) | | | | |
| Avg. Reach per Post | | | | |
| Avg. Engagement Rate | | | | |
| Avg. Link Clicks per Post | | | | |
| Avg. Shares per Post | | | | |
| Comments per Post | | | | |
| Profile/Page Visits | | | | |
| Posting Frequency | | | | |
| Content Production Effort | Low/Med/High | | | |

### 2. Efficiency Analysis

For each platform, calculate:
- **Reach efficiency:** Reach per hour of effort invested
- **Engagement efficiency:** Engagements per hour of effort invested
- **Conversion efficiency:** Clicks/conversions per hour of effort invested
- **Cost efficiency (paid):** Cost per engagement, cost per click, cost per conversion
- **Content repurpose potential:** How easily content created for this platform can be adapted for others

### 3. Strategic Value Assessment

Beyond metrics, assess each platform's strategic value:
- **Audience quality:** Does this platform reach decision-makers, buyers, or influencers?
- **Brand building:** Does presence on this platform enhance credibility and authority?
- **Competitive presence:** Are competitors active here? Is there an opportunity to own the space?
- **Platform trajectory:** Is the platform growing, stable, or declining for your audience?
- **Search and discovery:** Does content on this platform appear in search results or get indexed?

### 4. Content-Platform Fit Analysis

Evaluate how well your content pillars fit each platform:
- Which content pillars perform best on which platforms?
- Does the platform's native format (short video, long text, images, stories) match your content strengths?
- Is the audience on this platform aligned with the audience you want to reach?

### 5. Resource Reallocation Recommendation

Based on the analysis, recommend:

**Increase investment:**
- [Platform] — [rationale with data] — Recommended allocation: [X%]

**Maintain current investment:**
- [Platform] — [rationale with data] — Recommended allocation: [X%]

**Decrease investment:**
- [Platform] — [rationale with data] — Recommended allocation: [X%]

**Consider exiting:**
- [Platform] — [rationale with data] — Only if the platform delivers minimal value relative to effort

**Consider entering:**
- [Platform] — [rationale with data] — Only if there is a clear strategic opportunity

### 6. Implementation Plan

For each reallocation recommendation:
- What specifically changes (more posts, higher production value, paid promotion, reduced frequency)
- Timeline for the transition (avoid abrupt changes — test gradually)
- Success metrics to validate the reallocation was correct
- Review date to assess the impact

Use British English throughout. Be honest about platforms that are not working — recommend reducing investment where the data supports it, even if the platform is culturally popular.
