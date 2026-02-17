<h1 align="center"> Web Traffic Analytics — Performance Analysis Report</h1>

> **Dataset:** `web_traffic_data.csv` &nbsp;|&nbsp; **Records:** 10,000 &nbsp;|&nbsp; **Period:** Jan 18, 2024 – Jan 16, 2025 &nbsp;|&nbsp; **Markets:** 8 Countries

---

## Table of Contents

1. [Client Background](#1-client-background)
2. [Northstar Metrics](#2-northstar-metrics)
3. [Executive Summary](#3-executive-summary)
4. [Data Structure](#4-data-structure)
5. [Insight Deep-Dive](#5-insight-deep-dive)
   - [5.1 Traffic Trends](#51-traffic-trends)
   - [5.2 Channel Performance](#52-channel-performance)
   - [5.3 Campaign Performance](#53-campaign-performance)
   - [5.4 Device & User Type Analysis](#54-device--user-type-analysis)
   - [5.5 Regional Results](#55-regional-results)
   - [5.6 Traffic Source Analysis](#56-traffic-source-analysis)

---

 <h1 align="center"> Client Background</h1>

**DataPulse** is a global digital marketing intelligence platform serving brands across eight key international markets: the United States, United Kingdom, Canada, Australia, Germany, France, Brazil, and Japan. Founded to help organizations understand and optimize their online presence, DataPulse tracks multi-channel web traffic, campaign performance, and audience behavior across the full digital funnel.

DataPulse operates across **six distinct marketing channels** — Paid Ads, Organic Search, Direct, Email Campaigns, Social Media, and Referral — and leverages **eight traffic sources** including Google, Instagram, LinkedIn, Facebook, Twitter, Bing, Direct, and Email Newsletter. Campaigns span seasonal and lifecycle-driven initiatives such as Holiday Special, Black Friday, Summer Sale, Spring Collection, Welcome Series, and Remarketing.

Reporting to the Head of Digital Strategy, a comprehensive analysis was conducted to evaluate DataPulse's web traffic performance across the full calendar year. This review surfaces actionable insights that cross-functional teams in marketing, growth, and product will use to optimize spend allocation, improve audience targeting, and strengthen overall digital performance.

---

<h1 align="center"> Northstar Metrics</h1>

The analysis is anchored around seven core performance areas:

-  **Traffic Performance** — Tracking core volume metrics including total sessions, unique visitors, page views, and session quality indicators such as bounce rate and average session duration.

-  **Conversion & Revenue Trends** — Analyzing conversion rates, total conversions, revenue generated, and cost-efficiency across time periods, channels, and campaigns.

-  **Channel Effectiveness** — Evaluating the six marketing channels (Paid Ads, Organic Search, Direct, Email Campaigns, Social Media, and Referral) to identify top performers and areas requiring budget reallocation.

-  **Campaign Performance** — Assessing campaign-level impact across seven campaigns to understand which drives the greatest revenue, conversions, and return on investment.

-  **Device & Audience Segmentation** — Examining performance across Tablet, Mobile, and Desktop devices, as well as New vs. Returning visitor behavior, to inform UX and targeting strategies.

-  **Geographic Results** — Evaluating demand, revenue contribution, and conversion performance across eight international markets to identify regional strengths and gaps.

-  **Traffic Source Analysis** — Understanding which referring platforms (Google, Instagram, LinkedIn, Facebook, Twitter, Bing, Direct, Email Newsletter) deliver the highest quality traffic and ROI.

---

<h1 align="center">Executive Summary</h1>

<img width="1600" height="700" alt="image" src="https://github.com/user-attachments/assets/4c51998a-4354-441c-a832-2254c3881fe5" />


<table>
  <tr>
    <td valign="top" width="50%">

###  1. Strong Full-Year Performance
- Total revenue reached **$6.14M** from **60,552 conversions** across **2.14M sessions** over the 12-month period.
- The overall average ROI was **15.84x**, with an average conversion rate of **3.73%** and bounce rate of **38.91%**.
- **Q2 2024** was the top-performing quarter with **$1.57M** in revenue and **15,458 conversions**, closely followed by Q4 2024 at $1.57M.

</td>
    <td valign="top" width="50%">

###  2. Channel Performance Disparity
- **Paid Ads** generated the highest absolute revenue ($1.88M) but delivered the **lowest actual ROI at just 0.72x** — meaning costs nearly matched returns.
- **Direct channel** was the most cost-efficient, generating $1.04M in revenue at a remarkable **68.12x ROI** due to near-zero acquisition costs.
- **Organic Search** produced $1.47M in revenue at **7.62x ROI**, making it the best balance of scale and efficiency.
- **Social Media** underperformed with only **0.44x ROI**, suggesting significant budget waste that requires strategic reallocation.

</td>
  </tr>
  <tr>
    <td valign="top" width="50%">

###  3. Campaign Insights & Seasonal Patterns
- **Holiday Special** was the top-revenue campaign at **$889K**, followed closely by Welcome Series ($888K) and Remarketing ($878K).
- **Spring Collection** achieved the highest ROI **(17.0x)**, suggesting it delivers disproportionate value relative to cost.
- All campaigns showed remarkably consistent revenue performance, indicating a well-distributed content calendar with no single campaign dominating.

</td>
    <td valign="top" width="50%">

###  4. Device & Geography Are Balanced
- Revenue is nearly perfectly split across **Tablet ($2.06M)**, **Mobile ($2.06M)**, and **Desktop ($2.03M)** — signaling a mature, multi-device audience.
- **Canada ($788K)** and **Japan ($779K)** lead revenue by geography, while **France ($738K)** lags and represents an optimization opportunity.

</td>
  </tr>
</table>

### . Key Recommendations
>  **Reallocate** budget away from Social Media (0.44x ROI) toward Direct and Email Campaigns, both of which deliver 7x+ returns.

>  **Scale** Spring Collection campaigns — the highest ROI campaign — especially in high-performing geos like Canada and Japan.

>  **Prioritize** Organic Search content investment to compound its 7.62x return without proportionally increasing cost.

>  **Investigate** the Social Media bounce rate anomaly (55.1%) — nearly 16 points above the next-highest channel — to identify UX or targeting mismatches.

---

 <h1 align="center">Data Structure</h1>

The dataset is a **single flat-file CSV** containing 10,000 rows and 18 columns. There is no relational ERD as data is stored in a denormalized format. Each row represents a unique combination of date, channel, campaign, device, geography, traffic source, and user type.

###  Data Dictionary

| # | Column | Data Type | Description |
|---|--------|-----------|-------------|
| 1 | `Date` | Date | Daily date of the traffic record (DD-MM-YYYY, Jan 2024 – Jan 2025) |
| 2 | `Channel` | Categorical | Marketing channel: Direct, Email Campaigns, Organic Search, Paid Ads, Referral, Social Media |
| 3 | `Campaign_Name` | Categorical | Campaign driving traffic: Remarketing, Black_Friday, Holiday_Special, Summer_Sale, Spring_Collection, Welcome_Series, or None |
| 4 | `Device_Type` | Categorical | User device: Desktop, Mobile, or Tablet |
| 5 | `Geography` | Categorical | Country of the visitor: USA, UK, Canada, Australia, Germany, France, Brazil, Japan |
| 6 | `Traffic_Source` | Categorical | Referring platform: Google, Instagram, LinkedIn, Facebook, Twitter, Bing, Direct, Email Newsletter |
| 7 | `User_Type` | Categorical | Visitor classification: New Visitor or Returning Visitor |
| 8 | `Sessions` | Integer | Total number of sessions for this row's dimension combination |
| 9 | `Unique_Visitors` | Integer | Count of unique individual visitors |
| 10 | `Page_Views` | Integer | Total pages viewed across all sessions in this record |
| 11 | `Bounce_Rate` | Float (0–1) | Proportion of sessions that left without further interaction |
| 12 | `Average_Session_Duration` | Float (min) | Mean time spent per session in minutes |
| 13 | `Conversion_Rate` | Float (0–1) | Proportion of sessions resulting in a conversion |
| 14 | `Conversions` | Integer | Absolute number of goal completions (purchases, sign-ups, etc.) |
| 15 | `Cost` | Float (USD) | Total marketing spend attributed to this record |
| 16 | `Revenue` | Float (USD) | Total revenue generated from the sessions in this record |
| 17 | `ROI` | Float | Return on investment ratio (Revenue / Cost) |
| 18 | `Exit_Rate` | Float (0–1) | Proportion of page views that were the last in their session |

> **Note:** No primary/foreign key relationships exist — this is a single flat table structure optimized for slice-and-dice analysis across all dimension combinations.

---

 <h1 align="center">Insight Deep-Dive</h1>

---

 <h2 align="center">Traffic Trends</h2>

<h3 align="left"> Sessions & Visitor Volume</h3>

Total sessions for the year reached **2,138,211** with **1,647,074 unique visitors**, yielding a repeat-visit ratio that indicates a healthy returning audience. Q2 2024 saw the highest session volume at 533,921, while Q3 2024 peaked at 190,262 sessions in September alone.

<h3 align="left"> Quarterly Performance Summary</h3>

<img width="1600" height="700" alt="image" src="https://github.com/user-attachments/assets/5e6f25a7-8cf6-478d-8fd4-94f122b770c7" />

The business achieved a powerful scale-up in 2024, surging 30.3% in revenue by Q2 and maintaining a high-performance floor above 1.5M for the remainder of the year. Remarkably, this growth was achieved without sacrificing profitability, as the ROI remained consistent between 15x and 16x, signaling a highly scalable and stable operational model

<h3 align="left"> Bounce Rate & Session Quality</h3>

The platform-wide average bounce rate was **38.91%** with an average session duration of **3.05 minutes** — both indicating moderate but consistent engagement. Bounce rates showed stability across all quarters (38.5%–39.3%), suggesting engagement quality is stable but not improving over time.

<h3 align="left"> Peak & Low Traffic Days</h3>

<img width="1600" height="700" alt="image" src="https://github.com/user-attachments/assets/806d8b43-2cd1-4a9c-a507-020bdc1362dd" />

Three of the top 10 revenue days fell in Q2 (April–June), while the lowest-performing day — September 28 — was a notable valley in an otherwise strong Q3.

---

 <h2 align="center">Channel Performance</h2>

 <h3 align="left">Revenue by Channel</h3>

Paid Ads dominated revenue contribution at **$1.88M (30.6%)**, followed by Organic Search at **$1.47M (24.0%)** and Direct at **$1.04M (17.0%)**. Social Media was the weakest performer at $528K (8.6%) despite representing **14.9% of total sessions** — highlighting poor conversion efficiency relative to traffic volume.

<img width="1600" height="700" alt="image" src="https://github.com/user-attachments/assets/b91f0bfb-9214-4ba0-9bde-ea70e0999e07" />


 <h3 align="left">ROI Deep-Dive</h3>

The ROI gap between channels is extreme:

- **Direct (68.12x):** Near-zero acquisition cost ($15,100 total) makes every conversion extraordinarily profitable.
- **Email Campaigns & Organic Search (7–8x):** Solid returns at meaningful scale — the sweet spot of the channel mix.
- **Paid Ads (0.72x):** $1.09M spent to generate $1.88M in revenue. Barely covers costs before operational overhead.
- **Social Media (0.44x):** $367K spent to generate $529K — the channel is actively losing value relative to investment. 🚨

 <h3 align="left">Bounce Rate Heatmap — Channel × Device</h3>

| Channel | Desktop | Mobile | Tablet |
|---------|---------|--------|--------|
| Email Campaigns | 27.5% ✅ | 27.3% ✅ | 27.3% ✅ |
| Direct | 30.4% | 29.7% | 30.1% |
| Organic Search | 35.3% | 35.2% | 34.8% |
| Referral | 39.8% | 41.0% | 39.3% |
| Paid Ads | 45.2% | 44.9% | 45.0% |
| Social Media | 54.9% 🚨 | 55.4% 🚨 | 55.2% 🚨 |

> Social Media's 55%+ bounce rate across all devices — **16+ points above the next-highest channel** — suggests a serious disconnect between social ad creative and landing page content.

---

### 5.3 Campaign Performance

#### Best & Worst Campaigns

All six named campaigns performed within a narrow **$45K revenue band**, suggesting the campaign calendar is well-balanced. Holiday Special led revenue while Spring Collection delivered the highest efficiency.

| Campaign | Sessions | Revenue | Conversions | Avg ROI | AOV Proxy |
|----------|----------|---------|-------------|---------|-----------|
| Holiday Special | 309,568 | **$889,422** | 8,760 | 14.47x | $102 |
| Welcome Series | 312,951 | $887,858 | 8,774 | 15.97x | $101 |
| Remarketing | 308,665 | $878,486 | 8,666 | 15.68x | $101 |
| Black Friday | 303,263 | $875,831 | 8,643 | 15.48x | $101 |
| Summer Sale | 305,917 | $871,281 | 8,706 | 14.86x | $100 |
| Spring Collection | 287,086 | $844,166 | 8,229 | **17.01x** 🏆 | $103 |

#### Campaign × Device Revenue

| Campaign | Desktop | Mobile | Tablet | Top Device |
|----------|---------|--------|--------|------------|
| Black Friday | $268,191 | **$305,967** | $301,673 | 📱 Mobile |
| Holiday Special | **$309,115** | $270,473 | **$309,834** | 📱💊 Tie |
| Remarketing | $288,853 | $280,771 | **$308,862** | 💊 Tablet |
| Spring Collection | $266,486 | **$317,480** | $260,200 | 📱 Mobile |
| Summer Sale | $285,300 | $290,255 | **$295,727** | 💊 Tablet |
| Welcome Series | $291,164 | **$302,493** | $294,201 | 📱 Mobile |

> Spring Collection skews heavily **Mobile (+$57K vs. Desktop)** — a strong signal to prioritize mobile-first creative for this campaign. Holiday Special and Remarketing lean toward Tablet, suggesting those audiences favor larger-screen browsing.

---

### 5.4 Device & User Type Analysis

#### Device Performance

Revenue is **remarkably balanced** across all three device types — a strong signal that DataPulse's funnel is well-optimized across form factors.

| Device | Sessions | Revenue | Conversions | Conv Rate | Bounce Rate |
|--------|----------|---------|-------------|-----------|-------------|
| Tablet | 724,845 | $2,062,552 | 20,258 | 3.70% | 38.65% |
| Mobile | 718,510 | $2,055,993 | 20,371 | 3.73% | 39.22% |
| Desktop | 694,856 | $2,027,136 | 19,923 | 3.77% | 38.87% |

#### New vs. Returning Visitors

| User Type | Sessions | Revenue | Conversions | Conv Rate | Bounce Rate |
|-----------|----------|---------|-------------|-----------|-------------|
| New Visitor | 1,044,472 | $3,025,562 | 29,795 | 3.76% | 38.86% |
| Returning Visitor | 1,093,739 | $3,120,119 | 30,757 | 3.71% | 38.96% |

Key takeaways:
- Returning Visitors generate a **3% revenue premium** over New Visitors despite comparable session volumes.
- Conversion rates are nearly **identical** (3.71% vs. 3.76%), suggesting the onboarding funnel converts new users as efficiently as retained ones.
- The near-parity across both groups signals a **mature, balanced audience** — neither acquisition nor retention is clearly bottlenecked.

#### Conversion Rate Heatmap — Channel × Device

| Channel | Desktop | Mobile | Tablet |
|---------|---------|--------|--------|
| Direct | **6.00%** | **6.15%** | **6.02%** |
| Email Campaigns | 4.98% | 5.07% | 4.98% |
| Referral | 3.57% | 3.51% | 3.53% |
| Paid Ads | 3.58% | 3.48% | 3.48% |
| Social Media | 2.45% | 2.47% | 2.52% |
| Organic Search | 2.01% | 2.03% | 1.98% |

---

### 5.5 Regional Results

#### Revenue by Geography

Revenue distribution across eight markets is fairly uniform — spanning from **Canada at $788K (12.8%)** down to **France at $738K (12.0%)**. All regions show consistent conversion rates (3.6%–3.9%), suggesting broad product-market fit internationally.

| Geography | Sessions | Revenue | Conversions | Avg ROI | Rev Share |
|-----------|----------|---------|-------------|---------|-----------|
| 🇨🇦 Canada | 270,895 | **$788,229** | 7,638 | 16.79x | 12.8% |
| 🇯🇵 Japan | 271,052 | $778,938 | 7,730 | 16.82x | 12.7% |
| 🇺🇸 USA | 269,832 | $778,660 | 7,658 | 16.22x | 12.7% |
| 🇩🇪 Germany | 269,067 | $778,071 | 7,607 | 15.16x | 12.7% |
| 🇧🇷 Brazil | 263,148 | $768,885 | 7,572 | 16.04x | 12.5% |
| 🇦🇺 Australia | 268,366 | $760,889 | 7,546 | 15.65x | 12.4% |
| 🇬🇧 UK | 264,572 | $753,670 | 7,420 | 15.04x | 12.3% |
| 🇫🇷 France | 261,279 | $738,339 | 7,381 | 14.96x | 12.0% |

#### Channel × Geography Heatmap Findings

- **Paid Ads** dominates every geography, generating $232K–$247K per market. Canada ($247K) and Germany ($235K) lead; USA trails at $232K.
- **Organic Search** is the second-largest channel in every market. USA generates the most Organic revenue ($195K), suggesting stronger SEO authority in English-language markets.
- **Direct channel** is highest in Japan ($147K) and Canada ($146K), signaling stronger brand recognition and direct intent in those markets.
- **France consistently underperforms** across Organic Search and Direct — implying weaker brand awareness or SEO presence that warrants targeted investment.

---

### 5.6 Traffic Source Analysis

#### Source Performance Overview

All eight traffic sources performed within a narrow **$66K revenue range** — from Twitter at $795K down to Direct at $730K. ROI varies more meaningfully: **Facebook leads at 17.56x** while **Google lags at 14.19x**.

| Traffic Source | Sessions | Revenue | Conversions | Mean ROI |
|----------------|----------|---------|-------------|----------|
| Twitter | 277,685 | **$795,943** | 7,822 | 15.95x |
| Instagram | 279,664 | $795,476 | 7,868 | 15.12x |
| LinkedIn | 279,183 | $786,103 | 7,789 | 16.77x |
| Bing | 262,506 | $773,285 | 7,600 | 15.94x |
| Google | 267,148 | $756,712 | 7,521 | 14.19x |
| Facebook | 261,259 | $754,088 | 7,399 | **17.56x** 🏆 |
| Email Newsletter | 255,212 | $753,746 | 7,390 | 15.58x |
| Direct | 255,554 | $730,328 | 7,163 | 15.69x |

#### Best-Performing Channel × Source Combinations

| Rank | Channel | Source | Revenue | ROI |
|------|---------|--------|---------|-----|
| 🥇 | Paid Ads | Instagram | $259,836 | 0.77x |
| 🥈 | Paid Ads | Email Newsletter | $249,292 | 0.79x |
| 🥉 | Paid Ads | LinkedIn | $240,472 | 0.78x |
| — | Organic Search | LinkedIn | $201,197 | **8.89x** ✅ |
| — | Organic Search | Twitter | $205,279 | **8.55x** ✅ |

> While Paid Ads × Instagram wins on **absolute revenue**, Organic Search × LinkedIn wins on **ROI (8.89x vs. 0.77x)**. This underscores the strategic opportunity: investing in LinkedIn-targeted organic content could compound returns without proportionally increasing cost — particularly valuable for DataPulse's likely B2B audience segments.

---

## 📌 Summary of Key Recommendations

| Priority | Area | Action | Expected Impact |
|----------|------|--------|-----------------|
| 🔴 High | Social Media | Reduce spend or redesign landing pages to fix 55% bounce rate | Improve 0.44x ROI |
| 🔴 High | Paid Ads | Audit cost structure; shift budget toward Email & Organic | Improve 0.72x ROI |
| 🟡 Medium | Spring Collection | Scale this campaign — highest ROI (17.0x) across all campaigns | Revenue uplift |
| 🟡 Medium | Organic Search | Invest in SEO content, especially LinkedIn-distributed content | Compound 7.62x ROI |
| 🟢 Low | France | Target geo-specific campaigns to close $50K gap vs. top markets | Geo parity |
| 🟢 Low | Mobile UX | Spring Collection & Black Friday skew mobile — optimize creatives | Conversion lift |

---

*Report generated from `web_traffic_data.csv` | Analysis period: Jan 18, 2024 – Jan 16, 2025 | 10,000 records across 18 dimensions*
