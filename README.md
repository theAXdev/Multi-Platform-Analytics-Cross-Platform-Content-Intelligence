# 📱 Social Media Analytics — Cross-Platform Content Intelligence

> A Power BI analytics project investigating cross-platform social media performance across 5,600 posts on YouTube, TikTok, Instagram, X.com, LinkedIn, and Facebook. Covers engagement patterns, content category effectiveness, post type analysis, regional reach, and organic vs sponsored content performance across 8 global regions in 2024.

---



---

## 📌 Project Background

Social media has become the primary battleground for brand visibility, audience engagement, and digital marketing ROI. For a global brand operating across eight regions with content published to six distinct platform ecosystems, the ability to analyse post-level performance data and translate it into strategic content decisions is a core commercial competency.

This project analyses 5,600 FedEx social media posts from 2024 — examining how platform choice, content category, post type, content format, and posting timing interact to drive impressions, engagements, views, clicks, and click-through rates across YouTube, TikTok, X.com, Instagram, LinkedIn, and Facebook.

The analysis is structured to answer the questions that content strategists, digital marketing managers, and social media analytics teams face daily — and presents findings in a format directly usable for budget allocation, content calendar planning, and platform investment decisions.

---

## 🎯 Project Objectives

- Identify which platforms generate the highest impressions, engagements, views, and clicks — and whether platform leadership is consistent across all metrics
- Determine which post types (Video, Image, Live Stream, Text, Article, Carousel, PDF) drive the most engagement and reach
- Identify which content categories achieve the highest engagement rates across platforms
- Analyse day-of-week engagement patterns to identify the optimal publishing schedule
- Quantify the relationship between content type (Organic vs Sponsored) and engagement outcomes
- Profile regional performance across eight global regions — USA, UK, Canada, Japan, India, Australia, Brazil, Germany
- Identify which content-platform combinations generate the strongest performance

---

## ⚙️ Tools & Technologies

| Tool | Role in This Project |
|---|---|
| **Microsoft Power BI Desktop** | Six-page interactive dashboard, data modelling, geographic map visual, KPI cards with MoM indicators |
| **DAX (Data Analysis Expressions)** | MoM percentage calculations, aggregated metric measures, organic vs sponsored impression share |
| **Power Query** | Data type validation, datetime field extraction (hour, day, month), engagement level classification |

### DAX Measures Built

| Measure | Logic | Purpose |
|---|---|---|
| Total Impressions | `SUM(Impressions)` | Aggregate reach across all posts and platforms |
| Total Engagements | `SUM(Engagement)` | Aggregate interaction volume — likes, shares, comments |
| Total Views | `SUM(Views)` | Total content view count across all post types |
| Avg Engagement Rate | `AVERAGE(Engagement_Rate)` | Mean engagement rate for normalised platform comparison |
| MoM % Change | `DIVIDE([Current Month]-[Prior Month],[Prior Month])` | Month-over-month trend indicator powering KPI card arrows |
| Total Video Views | `SUM(Video_Views)` | Video-specific view metric |
| Total Live Stream Views | `SUM(Live_Stream_Views)` | Live stream-specific view metric |
| Organic Impression Share | `CALCULATE([Total Impressions], Content_Type="Organic") / [Total Impressions]` | Organic vs Sponsored reach distribution |

---

## 📊 Key Metrics at a Glance

| Metric | Value |
|---|---|
| Total Posts Analysed | 5,600 |
| Total Impressions | 5.77 Billion |
| Total Engagements | 646 Million |
| Total Views | 4.81 Billion |
| Total Video Views | 3.59 Billion |
| Total Live Stream Views | 549 Million |
| Average Engagement Rate | 15.28% |
| Total Clicks (trackable platforms) | 35.4 Million |
| Platforms Covered | 6 |
| Regions Covered | 8 |

---

## 🗄️ Dataset

| Field | Detail |
|---|---|
| Source | FedEx Social Media Post-Level Performance Data |
| Coverage | 5,600 posts, 6 platforms, 8 regions, 2024 |
| Format | Excel (.xlsx) |

### Variable Categories

**Post Identity**
- Post ID, Platform, Content Type (Organic / Sponsored), Content Category, Post Type

**Timing Variables**
- Post Published At (datetime), Post Date, Post Hour — enabling hour-of-day, day-of-week, and monthly trend analysis

**Geographic Variables**
- Region, Longitude, Latitude — enabling regional performance comparison and geographic map visualisation

**Reach Metrics**
- Impressions, Views, Video Views, Live Stream Views

**Engagement Metrics**
- Engagement (total), Likes, Shares, Comments, Engagement Rate

**Conversion Metrics**
- Clicks, Click-Through Rate (CTR)

**Content Signals**
- Main Hashtag, Engagement Level (Low / Medium / High)

---

## 📈 Platform Performance Breakdown

| Platform | Impressions | Engagements | Views | Clicks | Best Format | Best Category |
|---|---|---|---|---|---|---|
| **YouTube** | **1.35B** | 151M | 1.13B | — | Video | Educational, Customer Story |
| TikTok | 1.31B | 147M | 1.09B | **22.97M** | Video | Educational, Promotional |
| X.com | 1.20B | 133M | 1.00B | — | Text / Short Video | News, Announcements |
| Instagram | 1.18B | 135M | 985M | — | Video (Reels) | Product Promotion, Customer Story |
| LinkedIn | 408M | 45M | 341M | 5.85M | Article, Video | Educational |
| Facebook | 319M | 36M | 265M | 6.59M | Video | Customer Story |

YouTube leads in impression volume (23.45% of total). TikTok leads in click volume (22.97M) — the strongest conversion signal in the dataset. These are complementary strengths: YouTube for awareness, TikTok for action.

---

## 🎯 Content Category Analysis

| Content Category | Impressions | Engagements | Avg Engagement Rate | Post Count |
|---|---|---|---|---|
| **Educational** | **1.43B** | **238M** | **19.89%** | 2,026 |
| Customer Story | 439M | 73M | 19.88% | 735 |
| Event / Webinar | 262M | 31M | 13.94% | 577 |
| Product Promotion | **2.31B** | 223M | 11.59% | 1,385 |
| Entertainment | 1.32B | 82M | 7.51% | 877 |

**The most commercially significant finding:** Product Promotion generates the highest impressions (2.31B; 40.1% of total) but achieves the second-lowest engagement rate (11.59%). Educational and Customer Story content both achieve nearly 20% engagement rates — far above Product Promotion — yet receive significantly less impression investment.

---

## 🎬 Post Type Performance

| Post Type | Engagements | Impressions | Share % | Post Count |
|---|---|---|---|---|
| **Video** | **472M** | **4.37B** | **52.6%** | 2,948 |
| Image | 59M | 429M | 7.4% | 996 |
| Live Stream | 52M | 421M | 7.3% | 924 |
| Text | 31M | 256M | 4.4% | 458 |
| Article | 25M | 227M | 3.9% | 207 |
| Carousel | 6M | 51M | 0.9% | 51 |
| PDF | 2M | 14M | 0.3% | 16 |

Video accounts for **73.2% of all engagements** from 52.6% of posts. It is not one format among many — it is the primary engagement driver across every platform in the dataset.

---

## 📅 Day-of-Week Engagement

| Day | Total Engagements | Rank |
|---|---|---|
| **Wednesday** | **100,405,596** | 🥇 Peak |
| Saturday | 97,835,985 | 🥈 2nd |
| Sunday | 90,775,992 | 🥉 3rd |
| Friday | 90,286,025 | 4th |
| Thursday | 89,961,582 | 5th |
| Monday | 89,769,636 | 6th |
| Tuesday | 87,456,626 | Lowest |

Wednesday peaks 14.8% above Tuesday. The strong weekend performance (Saturday 2nd, Sunday 3rd) challenges the assumption that business content underperforms at weekends.

---

## ⚖️ Organic vs Sponsored

| Metric | Organic | Sponsored |
|---|---|---|
| Post Count | 4,646 (83.0%) | 954 (17.0%) |
| Total Impressions | 4.65B (80.63%) | 1.12B (19.37%) |
| Total Engagements | 523.6M | 122.9M |
| **Avg Engagement Rate** | **15.26%** | **15.40%** |

**The counter-intuitive finding:** Organic and Sponsored content achieve near-identical engagement rates (15.26% vs 15.40%). Sponsored investment buys 4x more reach — but no meaningful improvement in engagement quality. Paid amplification is a reach strategy, not an engagement quality strategy.

---

## 📊 Dashboard Structure — Six Pages

### Page 1: Overview
> Answers: *What is the headline performance picture across all platforms?*

| Visual | Chart Type | Key Finding |
|---|---|---|
| Total Views & Engagements by Platform | Grouped Bar Chart | YouTube and TikTok dominate — Facebook and LinkedIn trail significantly |
| Total Impressions by Platform & Content Type | Donut Chart | YouTube (23.45%), TikTok (22.68%), X.com (20.77%), Instagram (20.50%), LinkedIn (7.08%), Facebook (5.53%) |
| Total Engagements by Post Type | Horizontal Bar | Video leads at 472M (73.2%); PDF last at 1.88M |
| Total Impressions by Content Category per Platform | 100% Stacked Bar | Cross-platform content category mix by platform |
| Total Engagements by Day of the Week | Dual-Axis Line Chart | Wednesday peak (100.4M); Tuesday trough (87.5M) |

### Page 2: Platforms
> Answers: *How does each platform perform across content quality and regional reach?*

| Visual | Chart Type | Key Finding |
|---|---|---|
| Total Impressions by Region | Geographic Map | USA largest regional bubble; Japan and Australia visible |
| Avg Engagement Rate & CTR by Content Category | Grouped Bar | Educational leads both CTR and engagement rate |
| Content Quality & Efficiency Metrics | Matrix Heatmap | 6-platform × 6-metric matrix with conditional formatting |
| Impressions Distribution by Content Type | Pie Chart | Organic (80.63%) vs Sponsored (19.37%) |

### Pages 3–6: Pre-Analysis, In-Analysis, Observations & Recommendations
Structured analytical narrative pages covering pre-analysis hypotheses, in-process findings, structured observations across platform performance and content effectiveness, and 10 targeted recommendations across content strategy, scheduling, platform focus, and regional localisation.

---

## 🔍 Key Findings

### 1. YouTube Leads in Reach; TikTok Leads in Action
YouTube generates the highest impressions (1.35B; 23.45%) but TikTok drives the highest trackable click volume (22.97M). These are complementary strengths suggesting a dual-platform strategy — YouTube for awareness, TikTok for conversion.

### 2. Video Is Non-Negotiable
Video accounts for 73.2% of all engagements (472M) from 52.6% of posts. Any content strategy that does not prioritise video production is structurally disadvantaged across every platform in this dataset.

### 3. Educational Content Is the Most Commercially Efficient Category
Educational content achieves the highest engagement rate (19.89%) AND the second-highest impression volume (1.43B) — making it simultaneously highly visible and highly engaging. It is significantly underweighted relative to Product Promotion.

### 4. Product Promotion Has an Engagement Quality Problem
Product Promotion generates the most impressions (2.31B; 40.1%) but achieves only 11.59% engagement rate. The content is reaching audiences but not resonating — signalling a creative strategy review is required.

### 5. Customer Story Is the Highest-ROI Underinvested Format
Customer Story achieves a 19.88% engagement rate from only 735 posts (13.1% of total). Its per-post engagement quality matches Educational content. Increasing its post volume is the highest-confidence content investment identified in this analysis.

### 6. Wednesday and Saturday Are Priority Posting Days
Wednesday (100.4M) and Saturday (97.8M) are the two peak engagement days — a confirmed 14.8% advantage over Tuesday (87.5M). High-priority content should be consistently scheduled on these two days.

### 7. Sponsored Content Buys Reach — Not Engagement Quality
Organic (15.26%) and Sponsored (15.40%) engagement rates are effectively identical. Paid amplification budget is buying 4x more reach — but not improving audience engagement depth.

### 8. Event/Webinar Content Is Structurally Underperforming
Event/Webinar achieves the lowest CTR and third-lowest engagement rate (13.94%) across all platforms. Its 577-post volume represents a significant content investment consistently underperforming all other categories.

---

## ✅ Recommendations

### Platform & Content Strategy

1. **Double Down on TikTok and YouTube** — Both generate 1B+ impressions and 130M+ engagements. TikTok leads in click volume — the strongest conversion signal. Prioritise both for high-investment campaigns.

2. **Scale Customer Story Volume** — From 735 to 1,500 posts. Specifically target TikTok, Instagram, and LinkedIn where Customer Story formats perform strongest.

3. **Rebalance Product Promotion Creative** — Conduct a creative audit of Product Promotion posts. Redesign toward story-driven, problem-solution formats to improve engagement from 11.59% toward the 15% dataset average.

4. **Invest Heavily in Video Production** — Allocate a minimum of 60% of content production budget to video. Short-form for TikTok and Instagram; long-form educational video for YouTube.

5. **Reformat Event/Webinar Content** — Replace static event announcements with behind-the-scenes clips, speaker highlights, and post-event recap videos.

### Timing, Scheduling & Paid Strategy

6. **Prioritise Wednesday and Saturday Publishing** — Schedule all high-priority launches and campaign activations on these two peak engagement days.

7. **Test Weekend Storytelling Formats** — Saturday and Sunday both outperform the weekday average (excluding Wednesday). Test storytelling-led content formats for weekend scheduling.

8. **Use Sponsored Budget for Reach Extension** — Since Organic and Sponsored engagement rates are near-identical, use paid budget to amplify proven organic performers rather than creating separate sponsored-only content.

9. **A/B Test Sponsored CTAs on Facebook and LinkedIn** — Both platforms have trackable click volumes. Systematically test CTA placements, creative formats, and messaging on sponsored posts.

10. **Localise Content for USA, Japan, and UK** — These three regions account for over 2.2B combined impressions. Develop region-specific variants — short educational videos for India, entertainment shorts for Germany.

---

## ⚠️ Limitations

- **Platform post count imbalance** — YouTube's 1,320 posts vs Facebook's 299 posts means absolute metric comparisons overstate YouTube's per-post efficiency
- **Missing click data for YouTube and X.com** — click-based analysis is incomplete across two of the six platforms
- **No advertising spend data** — CPM, CPC, and ROAS calculations are not possible without cost figures
- **Single year** — 2024 data only; seasonality and year-over-year trend direction cannot be validated
- **Hashtag analysis limited** — single hashtag capture does not support multi-hashtag performance or hashtag-to-conversion attribution

---

## 🔭 Future Extensions

- Integrate advertising spend data to calculate CPM, CPC, ROAS, and engagement cost efficiency by platform and content category
- Build a predictive engagement model using post type, category, platform, region, and posting hour as features
- Add competitor social media performance data to contextualise results against industry benchmarks
- Extend to multi-year data to identify seasonal content patterns and campaign impact on platform performance
- Develop a live Power BI dashboard connected to social media API feeds for real-time performance monitoring

---

## 📁 Repository Structure
📦 Social-Media-Analytics-Cross-Platform-Content-Intelligence
┣ 📊 Multi-Platform_Engagement_Intelligence.pbix              ← Power BI dashboard file
┣ 📋 Raw_Data.xlsx                                            ← Source dataset — 5,600 posts across 6 platforms
┣ 📄 Multi_Platform_Engagement_Intelligence_Technical_Report.docx  ← Full technical report
┣ 🖼️ Social_Media_Analytics_Dashboard.jpg                     ← Dashboard preview image (displayed in README)
┗ 📝 README.md                                                ← Project documentation (you are here)


### How to Use This Repository

1. **To explore the dashboard** — download `Multi-Platform_Engagement_Intelligence.pbix` and open in [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free to download)
2. **To read the full analysis** — open `Multi_Platform_Engagement_Intelligence_Technical_Report.docx` in Microsoft Word or Google Docs
3. **To work with the raw data** — open `Raw_Data.xlsx` in Excel, Python, or R for further analysis

---

## 🏷️ Tags

`power-bi` `dax` `social-media-analytics` `digital-marketing` `content-strategy` `cross-platform` `engagement-analytics` `portfolio` `fedex` `marketing-analytics`

---

* Analytics Portfolio — Digital Marketing & Social Media Analytics Project*

