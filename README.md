# Mobile Game Player Analytics: Monetization, Engagement & LTV

**Product Analytics | Gaming | AdTech | Monetization | User Acquisition | Experimentation | LTV**

> **How can a mobile game acquire high-quality players, optimize advertising and IAP monetization, and maximize long-term player value without compromising engagement and retention?**

This project analyzes anonymized mobile game event data to understand the relationship between **user acquisition, player engagement, retention, advertising behavior, IAP conversion, monetization, and long-term LTV.**

Rather than treating acquisition, engagement, advertising, and IAP as isolated KPIs, the analysis builds an end-to-end view of the player and monetization lifecycle:

User Acquisition → Gameplay & Engagement → Retention → Ad Exposure → Ad Monetization → IAP Conversion → Long-Term LTV

The project combines **product analytics, AdTech, user acquisition, monetization analytics, and experimentation** to answer practical questions faced by gaming and consumer-product teams.

Key areas include:

- **IAP Monetization:** How do payer conversion and IAP revenue contribute to overall player economics alongside advertising revenue?
- **AdTech & Advertising Monetization:** Which ad networks and placements generate the strongest combination of impression volume, eCPM, ad revenue, and player value?
- **User Acquisition:** Which acquisition channels and player segments generate high-quality users relative to acquisition cost?
- **Product Engagement:** How do player engagement, session behavior, and retention relate to downstream monetization?
---

# Executive Summary

## 1. Ad Monetization Funnel & Diagnostic Analysis

**Business question**

> **Where do players drop out of the advertising monetization funnel, and where are the biggest opportunities to improve ad monetization efficiency across formats, placements, networks, platforms, and player cohorts?**

The analysis first maps the end-to-end advertising funnel:

**Installed Players → Active Players → Ad-Exposed Players → Format/Placement Exposure → Monetized Impressions → Ad Revenue**

This distinguishes **reach, engagement, ad exposure, and monetization** rather than treating impressions or revenue as standalone metrics.

**Hypotheses**

> **H1:** Significant player drop-off occurs at different stages of the advertising funnel, limiting the number of players who ultimately contribute to ad revenue.

> **H2:** Advertising monetization efficiency varies meaningfully by **ad format, placement, network, platform, country, and player lifecycle stage**.

> **H3:** High impression volume does not necessarily translate into high revenue efficiency; some lower-volume inventory may generate disproportionately higher **eCPM and revenue/user**.

**Analysis**

Built the advertising funnel at the player/event level:

1. **Installed Players** — unique users in the dataset
2. **Active Players** — users with ≥1 `session_start`
3. **Ad-Exposed Players** — users with ≥1 ad impression
4. **Format/Placement Exposure** — users exposed to specific ad formats or placements
5. **Monetized Impressions** — ad impressions generating revenue
6. **Ad Revenue** — total advertising revenue

The funnel is then decomposed across **network × placement × format × platform × country × player lifecycle** to identify where scale and monetization efficiency diverge.

**Result**

> **[INSERT ACTUAL FUNNEL FINDING]** — The funnel showed **[X%] of installed players reached ad exposure and [X%] of exposed players generated monetized impressions**, identifying **[specific funnel stage]** as the largest opportunity/drop-off point.

> **[INSERT ACTUAL MONETIZATION FINDING]** — **[Placement/network/format]** generated **[X% higher eCPM / revenue per user]** despite **[lower/similar]** impression volume, highlighting a potential inventory optimization opportunity.

**Product implication**

> Improve monetization by optimizing the **entire funnel**, not simply maximizing impressions: increase valuable player exposure, identify high-efficiency inventory, and shift monetization toward formats/placements that generate stronger revenue while monitoring **retention, engagement, and IAP** as guardrails.

**Key skills:** Ad monetization funnel analysis · KPI development · AdTech analytics · dimensional/root-cause analysis · monetization optimization


---

## 2. Engagement → Ad Monetization → LTV

**Business question**

> How does early player engagement relate to advertising monetization and long-term player value?

**Hypothesis**

> More engaged players generate greater advertising revenue and higher long-term LTV, but the relationship between ad exposure and player value may be nonlinear.

**Result**

> **[INSERT ACTUAL FINDING]**
> Players in the **[high-engagement segment/tier]** generated **[X%] higher ad revenue/user** and **[X%] higher LTV** than **[comparison group]**. Ad exposure showed **[linear/nonlinear/diminishing-return]** patterns across LTV and retention.

**Product implication**

> The objective should not be simply to maximize ad impressions. The stronger strategy is to identify the **level and type of monetization that supports sustainable player value**.

**Skills:** Product analytics · behavioral analysis · cohort analysis · LTV · regression · statistical modeling

---

## 3. Player Segmentation & Monetization Personas

**Business question**

> Are there distinct player segments with materially different engagement, monetization, retention, and LTV profiles?

**Hypothesis**

> Players exhibit distinct behavioral and monetization profiles, making a one-size-fits-all monetization strategy suboptimal.

**Result**

> **[INSERT ACTUAL FINDING]**
> Identified **[X] behavioral segments** with materially different **D7 retention, ad revenue/user, IAP revenue/user, and LTV**. The highest-value segment represented **[X%] of players but [Y%] of total value**.

**Product implication**

> Monetization and engagement strategies should be **segment-specific**, with different interventions for high-value, ad-dependent, casual, and potentially at-risk players.

**Skills:** Behavioral segmentation · K-Means/GMM · player personas · personalization · monetization strategy

---

## 4. Acquisition Channel → Retention & LTV

**Business question**

> Which acquisition channels bring players who remain engaged and generate long-term value?

**Hypothesis**

> Acquisition channels differ meaningfully in downstream player quality; high install volume does not necessarily indicate high-quality acquisition.

**Result**

> **[INSERT ACTUAL FINDING]**
> **[Channel A]** produced **[X%] higher/lower LTV** than **[Channel B]**, while **[channel]** showed **[strong/weak] retention and monetization performance** relative to its acquisition volume.

**Product implication**

> Evaluate acquisition sources based on **downstream player quality and LTV**, rather than installs alone.

**Important limitation:** The dataset does not contain acquisition spend, so this analysis evaluates **player quality**, not true CPI, CAC, ROAS, or ROI.

**Skills:** UA analytics · cohort analysis · channel evaluation · LTV · acquisition quality

---

## 5. Rewarded vs. Other Ad Formats

**Business question**

> How does rewarded advertising compare with other ad formats in monetization efficiency and downstream player value?

**Hypothesis**

> Rewarded ads may provide stronger monetization efficiency and player value, but excessive exposure could produce diminishing returns or negative engagement effects.

**Result**

> **[INSERT ACTUAL FINDING]**
> Rewarded exposure was associated with **[X% higher/lower] eCPM**, **[X% higher/lower] ad revenue/user**, and **[X% higher/lower] LTV** versus **[comparison group]**. Rewarded-ad exposure showed **[describe exposure/LTV or retention pattern]**.

**Product implication**

> Optimize rewarded advertising around the **balance between monetization efficiency and player experience**, rather than maximizing exposure.

**Skills:** AdTech analytics · rewarded advertising · monetization trade-offs · retention · observational modeling

---

# The Product Story

These analyses are designed to answer one overarching product question:

> **How can a mobile game maximize sustainable player value across acquisition, engagement, advertising, and IAP monetization?**

```text
                     ACQUISITION
                         │
                         ▼
                ┌─────────────────┐
                │ Channel Quality │
                │ Country         │
                │ Platform        │
                └────────┬────────┘
                         │
                         ▼
                    ENGAGEMENT
                         │
                ┌────────┴────────┐
                │                 │
                ▼                 ▼
             RETENTION       AD EXPOSURE
                                  │
                                  ▼
                           AD MONETIZATION
                                  │
                    ┌─────────────┴─────────────┐
                    │                           │
                    ▼                           ▼
                   IAP                       AD REVENUE
                    │                           │
                    └─────────────┬─────────────┘
                                  ▼
                             PLAYER LTV
                                  │
                                  ▼
                         PRODUCT DECISIONS
```

**Player segmentation cuts across the entire system**, allowing the same lifecycle to be evaluated for different behavioral and monetization personas.

---

# Key Business Questions

| Analysis                   | Business Question                                                | Primary Outcome        |
| -------------------------- | ---------------------------------------------------------------- | ---------------------- |
| **Ad Monetization Funnel** | Where is monetization efficiency highest/lowest?                 | eCPM & Ad Revenue/User |
| **Engagement → LTV**       | Which early behaviors are associated with future value?          | D8–D180 LTV            |
| **Player Segmentation**    | Which player types behave and monetize differently?              | Segment LTV            |
| **Acquisition → LTV**      | Which channels acquire higher-quality players?                   | Channel LTV            |
| **Rewarded vs. Other Ads** | Which ad experience best balances monetization and player value? | LTV + Retention        |

---

# 1. Ad Monetization Funnel & Diagnostic Analysis

## Business Question

> **Where are the biggest opportunities to improve advertising monetization across ad formats, placements, networks, platforms, and player cohorts?**

Instead of measuring impressions alone, this analysis decomposes advertising revenue into:

**Players × Impressions/Player × Revenue/Impression**

This makes it possible to distinguish between:

* high-volume / low-efficiency inventory
* low-volume / high-efficiency inventory
* high-value networks
* underperforming placements
* lifecycle changes in monetization efficiency

## Metrics

### Primary

* Ad revenue/user
* Ad revenue/DAU
* eCPM

### Secondary

* Ad impressions
* Impressions/user
* Unique users exposed
* Revenue/impression
* Rewarded-ad share
* Ad revenue by day since install

### Dimensions

* Ad format
* Placement
* Network
* Platform
* Country
* Day since install
* Install week
* Event hour

### Guardrails

* D1 retention
* D7 retention
* Sessions/user
* IAP revenue/user
* Total revenue/user

## Key Analysis

### Network × Placement Performance

Evaluate each network-placement combination on:

* impression volume
* eCPM
* revenue/user
* total revenue

This identifies inventory that is both **material and actionable**.

### Volume vs. Efficiency

**X:** Impressions
**Y:** eCPM
**Bubble:** Revenue

This separates scale from monetization efficiency.

### Monetization Over Player Lifecycle

Track eCPM and ad revenue/user from:

**Day 0 → Day 7**

to understand how monetization evolves as players progress through the game.

---

# 2. Player Engagement → Ad Monetization → LTV

## Business Question

> **How does early player behavior relate to advertising monetization and long-term player value?**

This analysis connects product behavior to business outcomes.

## User-Level Feature Engineering

A D0–D7 player feature table is constructed for each `user_id`.

### Engagement

* Session count
* Active days
* Sessions/day
* Sessions/active day
* First/last active day
* D1 retention
* D3 retention
* D7 retention

### Advertising

* Ad impressions
* Rewarded impressions
* Interstitial impressions
* Ad revenue
* Ad revenue/user
* Impressions/session
* Rewarded ads/session
* Unique placements
* Unique networks

### IAP

* Purchase count
* IAP revenue
* Payer flag
* Average order value

## Analysis Framework

```text
Early Engagement
       │
       ▼
Ad Exposure ───────► Ad Monetization
       │                    │
       │                    ▼
       └──────────────► Long-Term LTV
                              ▲
                              │
                             IAP
```

Regression is used to evaluate associations between early behavior and future LTV while controlling for observable player characteristics.

Example:

```text
log(LTV) ~
    engagement
    + ad_exposure
    + IAP_behavior
    + platform
    + country
    + acquisition_channel
```

**Important:** This is observational analysis. Regression coefficients are interpreted as **associations, not causal effects**.

---

# 3. Player Segmentation & Monetization Personas

## Business Question

> **Are there distinct player segments with meaningfully different engagement, advertising, IAP, retention, and LTV profiles?**

A user-level behavioral feature table is transformed using `log1p` where appropriate and standardized before clustering.

### Candidate Features

**Engagement**

* Sessions
* Active days
* Sessions/active day
* D1
* D7

**Advertising**

* Ad impressions
* Rewarded ads
* Interstitials
* Ad revenue
* Ad revenue/user
* Exposure intensity

**IAP**

* Purchase count
* IAP revenue
* Payer flag
* AOV

### Modeling

* K-Means
* Optional Gaussian Mixture Models
* Silhouette score
* Cluster size
* Business interpretability

Cluster selection is based not only on statistical separation but also on whether the resulting segments support **meaningful product decisions**.

## Example Persona Framework

Actual labels are assigned after examining the data.

**Highly Engaged Monetizers**

* High engagement
* High retention
* Strong ad + IAP monetization
* High LTV

**Ad-Dependent Players**

* High ad engagement
* Lower IAP contribution
* Strong ad monetization

**Casual Players**

* Low engagement
* Low ad exposure
* Lower LTV

**High-Value / Declining Players**

* Historically valuable
* Declining engagement
* Potential re-engagement opportunity

---

# 4. Acquisition Channel → Retention/LTV

## Business Question

> **Which acquisition channels bring players who remain engaged and generate long-term value?**

The analysis evaluates:

```text
Channel
   ↓
Engagement
   ↓
Retention
   ↓
Monetization
   ↓
LTV
```

## Channel-Level Metrics

* Users acquired
* D1 retention
* D7 retention
* Sessions/user
* Active days
* Ad revenue/user
* IAP revenue/user
* IAP conversion
* Total revenue/user
* D8–D180 LTV

## Key Comparisons

### Channel Quality

Compare channels on:

**Volume × Retention × Monetization × LTV**

### Volume vs. Quality

**X:** Acquired users
**Y:** LTV
**Bubble:** Total revenue

This highlights:

* High volume / high value
* High volume / low value
* Low volume / high value
* Low volume / low value

### Channel × Platform

Compare channel performance across:

* Android
* iOS

to identify channel/platform interaction effects.

## Limitation

Because acquisition spend is not included in the dataset, the analysis does **not** estimate:

* CPI
* CAC
* ROAS
* ROI

Instead, it answers:

> **Which channels appear to acquire higher-quality players?**

---

# 5. Rewarded vs. Other Ad Formats

## Business Question

> **Which advertising format provides the best balance between monetization efficiency, engagement, retention, and long-term player value?**

The key trade-off is:

```text
                 MONETIZATION
                      ▲
                      │
                      │
                      │
PLAYER EXPERIENCE ────┼────►
                      │
                      │
                      ▼
                 PLAYER VALUE
```

The goal is **not** simply to maximize ad revenue.

It is to identify whether an advertising format is associated with **sustainable player value**.

## Exposure Cohorts

Where supported by the data, players are grouped into:

* No ad exposure
* Rewarded only
* Non-rewarded only
* Rewarded + non-rewarded

## Metrics

### Monetization

* eCPM
* Ad revenue/user
* Impressions/user
* Revenue/impression

### Engagement

* Sessions/user
* Active days

### Retention

* D1
* D3
* D7

### IAP

* Payer conversion
* IAP revenue/user
* Purchase frequency
* AOV

### Long-Term Value

* `ltv_d8_d180`

## Rewarded Exposure Intensity

Exposure is bucketed into ranges such as:

```text
0
1–2
3–5
6–10
11+
```

Then compare:

**Rewarded ads/player → LTV**

and

**Rewarded ads/player → D7 retention**

This tests for potential **diminishing returns or ad fatigue**.

---

# Target: Long-Term Player LTV

The central prediction target is:

### `ltv_d8_d180`

Total revenue generated by a player between **day 8 and day 180** after installation.

It includes:

* In-app purchase revenue
* Advertising revenue

Non-paying players have an LTV of `0`.

The portfolio therefore focuses on the fundamental UA/product problem:

> **Can early behavioral signals tell us which players will generate long-term value?**

---

# Dataset

The dataset contains event-level records from approximately:

* **41,300 training users**
* **10,300 test users**

Each player can have multiple event records.

### Event Types

* `session`
* `iap`
* `ad_impression`

### Key User Attributes

* `platform`
* `country_tier`
* `channel_tier`
* `install_day`
* `install_week`

### Key Event Attributes

* `day_since_install`
* `event_hour`
* `event_type`
* `event_name`
* `product_id`
* `network`
* `ad_placement`
* `revenue_usd`

### Prediction Target

`ltv_d8_d180`

The target represents revenue generated between **days 8–180** after install.

---

# Analytical Approach

The project follows a product analytics workflow:

### 1. Event-Level Data

Raw session, IAP, and ad-impression events.

↓

### 2. Feature Engineering

Aggregate behavioral signals to the player level.

↓

### 3. Diagnostic Analysis

Identify monetization, engagement, retention, and acquisition patterns.

↓

### 4. Statistical Analysis

Use confidence intervals, hypothesis tests, regression, and clustering where appropriate.

↓

### 5. Segmentation

Identify distinct behavioral and monetization profiles.

↓

### 6. Business Interpretation

Translate analytical findings into product and monetization decisions.

---

# Key Product Metrics

| Area                   | Metrics                                         |
| ---------------------- | ----------------------------------------------- |
| **Engagement**         | Sessions/user, active days, sessions/active day |
| **Retention**          | D1, D3, D7                                      |
| **Advertising**        | Impressions/user, eCPM, ad revenue/user         |
| **IAP**                | Payer conversion, IAP revenue/user, AOV         |
| **Total Monetization** | Total revenue/user                              |
| **Long-Term Value**    | D8–D180 LTV                                     |
| **Acquisition**        | Users acquired, channel share, channel LTV      |

---

# Key Product Trade-offs

A central principle throughout the project is:

> **Optimizing a single monetization KPI can produce the wrong product decision.**

For example:

### More ads

→ Higher ad revenue

but potentially:

→ Lower engagement
→ Lower retention
→ Lower IAP
→ Lower long-term LTV

Similarly:

### Higher acquisition volume

does not necessarily mean:

→ Higher-quality players
→ Higher retention
→ Higher LTV

The analysis therefore evaluates monetization decisions against **player-value guardrails**.

---

# Limitations & Causal Considerations

Several analyses use observational event data.

Therefore:

> **Correlation between player behavior and LTV should not be interpreted as causal impact.**

For example, if rewarded-ad users have higher LTV, this does not necessarily mean rewarded ads caused the higher LTV.

Highly engaged players may simply be:

* more likely to watch rewarded ads
* more likely to make IAP purchases
* more likely to remain active
* more likely to generate long-term revenue

To address this, the analysis uses observable controls and regression where appropriate, while explicitly distinguishing **association from causation**.

For stronger causal decisions, the next step would be controlled experimentation or quasi-experimental measurement.

---

# Business Recommendations Framework

The analyses ultimately support four types of decisions:

### 1. Monetization Optimization

Identify:

* high-value placements
* high-performing networks
* efficient ad formats
* lifecycle opportunities

### 2. Player Experience

Monitor:

* retention
* engagement
* ad exposure intensity
* potential ad fatigue

### 3. Player-Level Strategy

Use behavioral segments to inform:

* monetization strategies
* rewarded-ad experiences
* re-engagement
* personalization

### 4. User Acquisition

Prioritize acquisition sources based on:

**Player Quality → Retention → Monetization → LTV**

rather than install volume alone.

---

# Why This Project Matters

This project demonstrates the ability to connect **product behavior to commercial outcomes** rather than analyzing individual metrics in isolation.

It combines:

**Product Analytics**

* Funnel analysis
* Cohort analysis
* Retention
* Behavioral analytics
* KPI development

**Gaming & AdTech**

* Ad formats
* Rewarded advertising
* Ad placements
* Ad networks
* eCPM
* Ad monetization

**Monetization**

* IAP
* Advertising revenue
* LTV
* Monetization trade-offs

**Data Science**

* Feature engineering
* Regression
* Clustering
* Hypothesis testing
* Confidence intervals

**Business Decision-Making**

* Acquisition quality
* Monetization optimization
* Player segmentation
* Product trade-offs
* Root-cause analysis

---

# Project Structure

```text
mobile-game-player-analytics/
│
├── data/
│   ├── train.csv
│   ├── test.csv
│   └── sample_submission.csv
│
├── notebooks/
│   ├── 01_ad_monetization_funnel.ipynb
│   ├── 02_engagement_ad_ltv.ipynb
│   ├── 03_player_segmentation.ipynb
│   ├── 04_acquisition_ltv.ipynb
│   └── 05_rewarded_vs_other_ads.ipynb
│
├── src/
│   ├── feature_engineering.py
│   ├── metrics.py
│   └── modeling.py
│
├── visualizations/
│
├── README.md
└── requirements.txt
```

---

# Tools & Technologies

**Python**

* Pandas
* NumPy
* Scikit-learn
* SciPy
* Statsmodels
* Matplotlib

**Analytics**

* Cohort analysis
* Funnel analysis
* Behavioral segmentation
* Regression
* Hypothesis testing
* Confidence intervals

**Domain**

* Mobile gaming
* AdTech
* User acquisition
* Player monetization
* LTV
* Retention

---

# Final Takeaway

The portfolio is built around a simple product principle:

> ### **The goal is not to maximize installs, impressions, or ad revenue in isolation. The goal is to acquire and monetize players in a way that maximizes sustainable long-term player value.**

The analysis connects:

**Acquisition**

→ **Engagement**

→ **Retention**

→ **Advertising**

→ **IAP**

→ **LTV**

and uses player segmentation to identify **where different strategies may create the most value**.

This provides a framework for making practical decisions around **UA allocation, ad placement, rewarded advertising, player experience, and long-term monetization.**
