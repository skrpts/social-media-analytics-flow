---
type: skill
id: audience-profiling
title: Audience Profiling
description: "Builds audience profiles from social media engagement patterns, demographics, and behavioural signals"
tags: [Production, Tested, analysis:audience, data:metrics]
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

Constructs detailed audience profiles from social media data by analysing who engages with content, how they engage, what they engage with, and when they are most active. Produces actionable audience segments that inform content strategy, posting schedules, and messaging approaches.

## When to Use

- Developing or refreshing a social media content strategy
- Launching content aimed at a new audience segment
- Investigating why engagement patterns have shifted
- Preparing audience insights for advertising targeting
- Informing broader marketing persona development with social data

## Process

1. **Demographic Analysis** — Where platform analytics provide demographic data (age, gender, location, language), summarise the audience composition. Identify the core demographic segments and any underrepresented segments that might be growth opportunities.

2. **Behavioural Segmentation** — Segment the audience by engagement behaviour:
   - **Passive consumers:** Follow and view content but rarely engage
   - **Casual engagers:** Occasionally like or react to content
   - **Active participants:** Regularly comment, share, and save content
   - **Advocates:** Share content consistently, tag friends, create UGC
   - **Detractors:** Leave negative comments or unfollow

   Estimate the proportion in each segment based on engagement data.

3. **Content Preference Mapping** — Analyse which content types, topics, and formats resonate with different audience segments:
   - Which topics generate the most comments (indicating strong opinions)?
   - Which formats get the most saves (indicating high perceived value)?
   - Which content types drive the most shares (indicating audience alignment)?
   - Which topics generate negative engagement or unfollows?

4. **Activity Pattern Profiling** — Map when the audience is most active and responsive:
   - Peak activity hours by day of week
   - Seasonal engagement patterns
   - Response time expectations (how quickly they expect replies)
   - Content consumption patterns (scroll speed, video watch time)

5. **Interest and Affinity Mapping** — Where data allows, identify:
   - Related accounts the audience follows
   - Hashtags the audience uses or engages with
   - Topics outside your niche that resonate with your audience
   - Cultural references, language patterns, and communication style preferences

6. **Profile Synthesis** — Combine all signals into 2-4 distinct audience profiles with:
   - Descriptive name and summary
   - Demographic indicators
   - Content preferences
   - Engagement patterns
   - Best channels and times to reach them
   - Messaging tone that resonates

## Inputs

- Platform analytics demographic data (where available)
- Engagement data by content type, topic, and format
- Follower growth and churn data
- Comment and conversation analysis (themes, sentiment, language)
- Previous audience profiles for comparison (optional)

## Outputs

- 2-4 audience profiles with demographic, behavioural, and preference characteristics
- Content preference matrix by audience segment
- Optimal posting schedule by audience segment
- Audience growth opportunities (underserved segments)
- Messaging and tone recommendations per segment

## Constraints

- Distinguish between observed data and inferences — label assumptions clearly
- Do not overfit profiles to small data sets — note confidence levels
- Respect privacy — profiles should be based on aggregate patterns, not individual user tracking
- Acknowledge platform data limitations (many platforms provide limited demographic data)
- Update profiles regularly — audiences evolve and static profiles become misleading
