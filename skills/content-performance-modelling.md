---
type: skill
id: content-performance-modelling
title: Content Performance Modelling
description: "Identifies the variables that drive social media content performance and builds predictive models for optimisation"
tags: [Production, Tested]
connections:
  - target: claude-service
    type: runs_on
  - target: social-media-metrics-reference
    type: references
metadata:
  estimated_duration: "5-7 minutes"
  avg_tokens: 3000
---

## Capability

Analyses historical content performance data to identify which variables correlate with high engagement, reach, and conversion. Builds a content performance model that predicts what types of content are likely to perform well, enabling data-driven content planning.

## When to Use

- Planning a content calendar based on performance data rather than intuition
- Diagnosing why recent content is underperforming
- Justifying content strategy changes with data to stakeholders
- Optimising content mix allocation across formats and topics
- Testing hypotheses about what drives performance on specific platforms

## Process

1. **Variable Identification** — Catalogue the variables that might influence content performance:
   - **Content variables:** Format (image, video, carousel, text, link), topic/theme, length (caption length, video duration), visual style, tone (humorous, educational, inspirational, provocative)
   - **Timing variables:** Day of week, time of day, proximity to events or trends, posting frequency
   - **Engagement variables:** Use of questions, calls to action, hashtag strategy, tagging strategy
   - **Platform variables:** Algorithm preferences (reels vs. static, long-form vs. short-form), feature usage (stories, polls, threads)

2. **Performance Attribution** — For each piece of content in the analysis period, map performance metrics against the content variables. Look for:
   - Which formats consistently outperform others?
   - Which topics drive the highest engagement rate?
   - Does caption length correlate with engagement?
   - Do specific visual styles or templates perform better?
   - Is there a posting frequency sweet spot (diminishing returns)?

3. **Pattern Extraction** — Identify the strongest performance patterns:
   - **High-performance recipe:** The combination of variables that most reliably produces strong results
   - **Underperformance triggers:** Variables or combinations that consistently underperform
   - **Diminishing returns:** Where more effort produces less incremental result
   - **Surprise performers:** Content that broke the model — what was different?

4. **Content Mix Optimisation** — Based on the model, recommend:
   - Optimal content mix by format (e.g., 40% video, 30% carousel, 20% static image, 10% text)
   - Topic allocation (which themes deserve more or less airtime)
   - Posting frequency and cadence recommendations
   - Experimentation budget (proportion of content to dedicate to testing new approaches)

5. **Predictive Indicators** — Identify early signals that predict content success:
   - First-hour engagement as a predictor of total performance
   - Save-to-like ratio as an indicator of content value
   - Share rate as a predictor of reach amplification
   - Comment depth (replies to comments) as an indicator of community building

6. **Model Limitations** — Explicitly state the limitations:
   - Sample size adequacy
   - Variables not captured in the data
   - Platform algorithm influence (confounding variable)
   - Temporal factors (what worked last quarter may not work next quarter)

## Inputs

- Historical content performance data (minimum 30 posts, ideally 100+)
- Content metadata (format, topic, length, visual style, posting time)
- Platform analytics (reach, impressions, engagement by type, click-throughs)
- Follower count over time (to normalise for audience growth)

## Outputs

- Content performance model summary (key drivers of high and low performance)
- Optimal content mix recommendation with rationale
- Posting schedule recommendation based on performance data
- Content experimentation plan (what to test next)
- Performance prediction framework (early indicators to track)

## Constraints

- Correlation is not causation — note when patterns are correlational and when they have been experimentally validated (A/B tested)
- Do not overfit to small data sets — models built on 20 posts are unreliable
- Account for algorithmic influence — platform algorithm changes can invalidate historical patterns
- Include confidence ranges, not just point estimates
- Recommend ongoing testing rather than treating the model as fixed truth
