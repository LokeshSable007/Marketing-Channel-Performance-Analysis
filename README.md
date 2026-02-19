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

<table style="width:100%; font-family: sans-serif; border-collapse: collapse;">
  <tr style="background-color: #2E5A88; color: white;">
    <th style="padding: 10px;">Table Type</th>
    <th style="padding: 10px;">Table Name</th>
    <th style="padding: 10px;">Primary Columns</th>
  </tr>
  <tr>
    <td style="border: 1px solid #ddd; padding: 8px;"><b>Fact Table</b></td>
    <td style="border: 1px solid #ddd; padding: 8px;">Fact_Performance</td>
    <td style="border: 1px solid #ddd; padding: 8px;">Sessions, Revenue, Cost, Conversions, Page_Views</td>
  </tr>
  <tr style="background-color: #f2f2f2;">
    <td style="border: 1px solid #ddd; padding: 8px;"><b>Dimension</b></td>
    <td style="border: 1px solid #ddd; padding: 8px;">Dim_Marketing</td>
    <td style="border: 1px solid #ddd; padding: 8px;">Channel, Campaign_Name, Traffic_Source</td>
  </tr>
  <tr>
    <td style="border: 1px solid #ddd; padding: 8px;"><b>Dimension</b></td>
    <td style="border: 1px solid #ddd; padding: 8px;">Dim_Context</td>
    <td style="border: 1px solid #ddd; padding: 8px;">Geography, Device_Type, User_Type</td>
  </tr>
  <tr style="background-color: #f2f2f2;">
    <td style="border: 1px solid #ddd; padding: 8px;"><b>Dimension</b></td>
    <td style="border: 1px solid #ddd; padding: 8px;">Dim_Time</td>
    <td style="border: 1px solid #ddd; padding: 8px;">Date, Month, Quarter, Year</td>
  </tr>
</table>

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

<img width="1600" height="1280" alt="image" src="https://github.com/user-attachments/assets/ccc4267d-374f-4af6-a913-46b70c0ba3c9" />

> Social Media's 55%+ bounce rate across all devices — **16+ points above the next-highest channel** — suggests a serious disconnect between social ad creative and landing page content.

---

<h1 align="center">Campaign Performance</h1>

 <h3 align="left">Best & Worst Campaigns</h3>

All six named campaigns performed within a narrow **$45K revenue band**, suggesting the campaign calendar is well-balanced. Holiday Special led revenue while Spring Collection delivered the highest efficiency.

<img width="1600" height="933" alt="image" src="https://github.com/user-attachments/assets/c28d3927-b6f4-49d1-8c31-95c9cfbb42dd" />


 <h3 align="left">Campaign × Device Revenue</h3>

<img width="1600" height="914" alt="image" src="https://github.com/user-attachments/assets/696e3f62-969c-48bc-8a78-753c5618e23d" />


> Spring Collection skews heavily **Mobile (+$57K vs. Desktop)** — a strong signal to prioritize mobile-first creative for this campaign. Holiday Special and Remarketing lean toward Tablet, suggesting those audiences favor larger-screen browsing.

---

<h1 align="center">Device & User Type Analysis</h1>

<h3 align="left">Device Performance</h3>

Revenue is **remarkably balanced** across all three device types — a strong signal that DataPulse's funnel is well-optimized across form factors.

<img width="1600" height="567" alt="image" src="https://github.com/user-attachments/assets/84e9f687-87a5-4789-b237-a203a382ba4a" />


 <h1 align="left">New vs. Returning Visitors</h1>

<img width="1600" height="700" alt="image" src="https://github.com/user-attachments/assets/9f085004-59f3-4115-91b0-fd85b0f68c8e" />


Key takeaways:
- Returning Visitors generate a **3% revenue premium** over New Visitors despite comparable session volumes.
- Conversion rates are nearly **identical** (3.71% vs. 3.76%), suggesting the onboarding funnel converts new users as efficiently as retained ones.
- The near-parity across both groups signals a **mature, balanced audience** — neither acquisition nor retention is clearly bottlenecked.

<h3 align="left">Conversion Rate Heatmap — Channel × Device</h3>

<img width="1600" height="1280" alt="image" src="https://github.com/user-attachments/assets/b920a7f9-2472-4e45-9be9-76a46c8bce55" />


---

<h1 align="center">Regional Results</h1>

<h3 align="left">Revenue by Geography</h3>

Revenue distribution across eight markets is fairly uniform — spanning from **Canada at $788K (12.8%)** down to **France at $738K (12.0%)**. All regions show consistent conversion rates (3.6%–3.9%), suggesting broad product-market fit internationally.

<img width="1600" height="1067" alt="image" src="https://github.com/user-attachments/assets/793c22ec-a641-4ee9-8958-b20b860eafa3" />

<h3 align="left">Channel × Geography Heatmap Findings</h3>

- **Paid Ads** dominates every geography, generating $232K–$247K per market. Canada ($247K) and Germany ($235K) lead; USA trails at $232K.
- **Organic Search** is the second-largest channel in every market. USA generates the most Organic revenue ($195K), suggesting stronger SEO authority in English-language markets.
- **Direct channel** is highest in Japan ($147K) and Canada ($146K), signaling stronger brand recognition and direct intent in those markets.
- **France consistently underperforms** across Organic Search and Direct — implying weaker brand awareness or SEO presence that warrants targeted investment.

---

<h1 align="center">Traffic Source Analysis</h1>

<h3 align="left">Source Performance Overview</h3>

All eight traffic sources performed within a narrow **$66K revenue range** — from Twitter at $795K down to Direct at $730K. ROI varies more meaningfully: **Facebook leads at 17.56x** while **Google lags at 14.19x**.

<img width="1600" height="1067" alt="image" src="https://github.com/user-attachments/assets/ef93817d-1c20-4ee5-9eea-566b61c72a06" />


<h3 align="left">Best-Performing Channel × Source Combinations</h3>

<img width="1600" height="933" alt="image" src="https://github.com/user-attachments/assets/4b223268-8393-46c1-bc87-632b5c6afc62" />


> While Paid Ads × Instagram wins on **absolute revenue**, Organic Search × LinkedIn wins on **ROI (8.89x vs. 0.77x)**. This underscores the strategic opportunity: investing in LinkedIn-targeted organic content could compound returns without proportionally increasing cost — particularly valuable for DataPulse's likely B2B audience segments.

---

<h1 align="center">Summary of Key Recommendations</h1>

<!DOCTYPE html>
<html>
<head>
<style>
  table {
    font-family: Arial, sans-serif;
    border-collapse: collapse;
    width: 100%;
    margin-bottom: 25px;
  }
  th {
    background-color: #2E5A88;
    color: white;
    text-align: left;
    padding: 12px;
  }
  td {
    border: 1px solid #dddddd;
    padding: 10px;
    text-align: left;
  }
  tr:nth-child(even) {
    background-color: #f9f9f9;
  }
  .status-high { color: #2ca02c; font-weight: bold; }
  .status-med { color: #ff7f0e; font-weight: bold; }
  .status-low { color: #d62728; font-weight: bold; }
  .header-row { background-color: #e9eff5; font-weight: bold; }
</style>
</head>
<body>

<h2>Strategic Performance Overview</h2>

<table>
  <tr>
    <th>Category</th>
    <th>Segment</th>
    <th>Revenue</th>
    <th>ROI / Rate</th>
    <th>Performance Status</th>
  </tr>
  
  <tr class="header-row"><td colspan="5">Channel Efficiency</td></tr>
  <tr>
    <td>Primary Driver</td>
    <td>Paid Ads</td>
    <td>$1,877,701</td>
    <td>0.72x</td>
    <td class="status-low"> Audit Required</td>
  </tr>
  <tr>
    <td>Profit Leader</td>
    <td>Direct</td>
    <td>$1,043,732</td>
    <td>68.12x</td>
    <td class="status-high"> Top Performer</td>
  </tr>
  <tr>
    <td>Balanced Growth</td>
    <td>Organic Search</td>
    <td>$1,473,115</td>
    <td>7.62x</td>
    <td class="status-high"> Healthy</td>
  </tr>
  <tr>
    <td>Risk Area</td>
    <td>Social Media</td>
    <td>$528,668</td>
    <td>0.44x</td>
    <td class="status-low">High Bounce Rate</td>
  </tr>

  <tr class="header-row"><td colspan="5">Device Maturity</td></tr>
  <tr>
    <td>Tablet</td>
    <td>Global Users</td>
    <td>$2,062,552</td>
    <td>3.70% Conv.</td>
    <td class="status-high"> Fully Optimized</td>
  </tr>
  <tr>
    <td>Mobile</td>
    <td>Global Users</td>
    <td>$2,055,993</td>
    <td>3.73% Conv.</td>
    <td class="status-high"> Fully Optimized</td>
  </tr>
  <tr>
    <td>Desktop</td>
    <td>Global Users</td>
    <td>$2,027,136</td>
    <td>3.77% Conv.</td>
    <td class="status-high"> Fully Optimized</td>
  </tr>

  <tr class="header-row"><td colspan="5">Campaign Insights</td></tr>
  <tr>
    <td>Top Revenue</td>
    <td>Holiday Special</td>
    <td>$889,422</td>
    <td>14.47x</td>
    <td class="status-high"> Revenue Peak</td>
  </tr>
  <tr>
    <td>Top Efficiency</td>
    <td>Spring Collection</td>
    <td>$844,166</td>
    <td>17.01x</td>
    <td class="status-high"> ROI Winner</td>
  </tr>
</table>

</body>
</html>
---

*Report generated from `web_traffic_data.csv` | Analysis period: Jan 18, 2024 – Jan 16, 2025 | 10,000 records across 18 dimensions*
