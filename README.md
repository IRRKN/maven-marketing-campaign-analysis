# Maven Marketing Campaign Analysis

### Customer Segmentation & Campaign Performance | Python · pandas · seaborn

---

## Executive Summary

When Maven Marketing's Marketing Director needs to plan the next campaign
budget, the existing customer data offers more answers than expected. Through
quartile-based segmentation of 2,231 customers and analysis of 6 historical
campaigns, this project reveals that the company's top 25% of customers
(VIPs) drive disproportionate value, spending $1,490 annually versus $40
for the bottom segment, a 37x gap.

The mechanism is counterintuitive: VIPs don't buy more frequently than
others. They buy bigger. Premium categories (Wines and Meat) account for
81% of their basket, and Number of Children at Home is a stronger negative
predictor of customer value than Age, Tenure, or Recency combined.

For campaigns, two of the six historical efforts (Cmp1, Cmp5) achieved
above 20% acceptance among VIPs but zero traction in lower segments,
suggesting significant budget waste from mass broadcasting.

The recommendation: shift campaign investment toward VIP-targeted premium
offerings and replicate the formula of Cmp6, the only campaign reaching
30%+ VIP acceptance.

---

## Business Context

### The Company

Maven Marketing is a retail company serving 2,231 active customers across
seven countries, with Spain as its primary market (49% of customers). The
business operates across three sales channels: physical stores, a product
catalog, and an online store, while running periodic marketing campaigns
across six product categories.

### The Problem

The Marketing Director faces a recurring challenge: planning the next
campaign budget without clear visibility into customer value, campaign ROI,
or channel performance. Currently, campaigns are broadly distributed
without segment-specific targeting.

### Research Questions

1. Who is the typical Maven Marketing customer?
2. Which customers generate the most value?
3. Which product categories drive revenue?
4. Which sales channels perform best?
5. Which marketing campaigns are most effective?
6. Which customers may need reactivation?

---

## Dataset

| Parameter | Value |
|-----------|--------|
| Source | Maven Analytics / Kaggle |
| Rows | 2,240 → 2,231 after cleaning |
| Columns | 28 original + engineered features |
| Type | Synthetic marketing dataset |

---

## Tools & Libraries

```python
Python
pandas
numpy
matplotlib
seaborn
```

## Methodology

1. Business understanding
2. Data cleaning
3. Feature engineering
4. Exploratory Data Analysis
5. Customer segmentation
6. Statistical analysis
7. Business recommendations

---

## Feature Engineering

| Feature | Purpose |
|----------|----------|
| Age | Customer age |
| Total_Spend | Total customer spending |
| Total_Children | Household composition |
| Customer_Tenure | Loyalty indicator |
| Total_Campaigns_Accepted | Marketing responsiveness |
| Total_Purchases | Overall purchasing activity |
| Avg_Order_Value | Basket size |

---

## Customer Segmentation

Customers were segmented into spending quartiles.

| Segment | Spend Range |
|----------|------------|
| Low | $8 – $69 |
| Below Average | $69 – $397 |
| Above Average | $397 – $1,046 |
| VIP | $1,046 – $2,525 |

---

## Key Findings

### 1. VIP Customers Are Defined by Basket Size, Not Frequency

- Average annual spend: $1,490 vs $40
- Income: $75,088 vs $30,945
- Average order value: $72 vs $7
- Fewer children in household

VIP customers do not purchase significantly more often. They simply spend much more per transaction.

### 2. Wines and Meat Drive Premium Revenue

| Category | VIP Average Spend |
|-----------|------------------|
| Wines | $741 |
| Meat | $455 |
| Fish | $89 |
| Gold | $78 |
| Sweet | $64 |
| Fruits | $62 |

Wines and Meat represent approximately 81% of total VIP spending.

### 3. Catalog Is a Premium Channel

Catalog purchases increase dramatically among higher-value customers.

| Segment | Catalog Purchases |
|----------|------------------|
| Low | 0.21 |
| Below Average | 1.02 |
| Above Average | 3.53 |
| VIP | 5.92 |

Web visits show a negative relationship with spending, suggesting that browsing activity does not necessarily translate into purchasing behavior.

### 4. Campaign Performance Differs by Segment

| Campaign Type | Campaigns |
|---------------|-----------|
| Premium-focused | Cmp1, Cmp5 |
| Universal winner | Cmp6 |
| Mass-market | Cmp3 |
| Poor performer | Cmp2 |

Cmp6 achieved the highest acceptance rate across all customer groups.

### 5. Income Is the Strongest Predictor

| Variable | Correlation with Total Spend |
|-----------|----------------------------|
| Income | 0.80 |
| Catalog Purchases | 0.78 |
| Total Purchases | 0.76 |
| Total Children | -0.50 |
| Web Visits | -0.50 |
| Recency | 0.02 |

Income is the strongest available predictor of future customer value.

---

## Business Recommendations

### Stop Mass Broadcasting Premium Campaigns

Premium campaigns should target VIP and Above Average segments only.

### Replicate the Cmp6 Formula

Analyze and reuse the campaign structure responsible for Cmp6's success.

### Use Catalog Activity as a VIP Signal

Customers engaging with catalog purchases should receive premium treatment and personalized offers.

### Reactivate Dormant High-Value Customers

Focus retention efforts on inactive VIP customers.

### Reduce Dependence on Recency

Recency alone is a weak predictor of customer value and should not drive segmentation decisions.

---

## Visualizations

- Customer Profile Dashboard
- Spending Segments Overview
- Product Basket by Segment
- Channel Performance Heatmap
- Campaign Effectiveness Analysis
- Correlation Matrix

---

## Repository Structure

```text
maven-marketing-analysis/
│
├── README.md
├── marketing_analysis2026.ipynb
│
├── data/
│   ├── marketing_data.csv
│   └── marketing_data_dictionary.csv
│
└── charts/
    ├── customer_profile_dashboard.png
    ├── spending_segments_overview.png
    ├── product_basket_by_segment.png
    ├── channel_performance_heatmap.png
    ├── campaign_effectiveness.png
    └── correlation_heatmap.png
```

---

## Skills Demonstrated

- Data Cleaning
- Exploratory Data Analysis
- Customer Segmentation
- Feature Engineering
- Statistical Analysis
- Data Visualization
- Business Intelligence
- Marketing Analytics

---

## Author

**Iryna Sukach**

Aspiring Data Analyst | Python | SQL | Data Visualization | Marketing Analytics
