# Business Memo

## Subject

Key Drivers of Customer Churn Identified Through Exploratory Data Analysis

---

# Executive Summary

Analysis of 2,400 customers revealed an overall churn rate of 47%.

Across customer demographics, purchasing behaviour, product experience, support interactions, digital engagement, and campaign activity, the strongest churn signals consistently point toward customer inactivity and declining engagement.

---

# Finding 1: Customer Inactivity Is the Strongest Churn Signal

### Evidence

* Customers inactive for more than 180 days exhibit a churn rate of 91.4%.
* Customers inactive for 91–180 days exhibit a churn rate of 78.7%.
* Customers purchasing within the last 30 days exhibit a churn rate of only 11.7%.

### Business Impact

Recency is the strongest positive correlate of churn and should be monitored continuously.

---

# Finding 2: One-Time Buyers Are Extremely High Risk

### Evidence

* Customers with only 1 order exhibit 100.0% churn.
* Customers with 10+ orders exhibit only 8.8% churn.
* Churn decreases consistently as order frequency increases.

### Business Impact

Moving customers from their first purchase to a second purchase represents a major retention opportunity.

---

# Finding 3: Recent Purchase Frequency Strongly Predicts Retention

### Evidence

| Frequency (180 Days) | Churn Rate |
| -------------------- | ---------: |
| 0 Purchases          |      91.4% |
| 1 Purchase           |      53.1% |
| 2 Purchases          |      35.9% |
| 3+ Purchases         |      16.2% |

### Business Impact

Repeat purchasing behaviour is strongly associated with customer retention.

---

# Finding 4: Higher Spending Customers Churn Less

### Evidence

| Spend Segment | Churn Rate |
| ------------- | ---------: |
| Low Spend     |      75.7% |
| Medium-Low    |      50.7% |
| Medium-High   |      40.8% |
| High Spend    |      20.7% |

### Business Impact

Customer value and retention show a strong inverse relationship.

---

# Finding 5: Category Diversity Improves Retention

### Evidence

Churn declines consistently as category diversity increases:

* 0 categories → 91.4%
* 1 category → 50.5%
* 2 categories → 31.5%
* 3 categories → 16.9%
* 4 categories → 10.0%

### Business Impact

Customers purchasing across multiple categories are significantly more likely to remain active.

---

# Finding 6: Product Satisfaction Supports Retention

### Evidence

* Excellent ratings (4–5) churn at 38.8%.
* Good ratings (3–4) churn at 52.9%.

### Business Impact

Customers reporting stronger product experiences demonstrate better retention outcomes.

---

# Finding 7: Support Engagement Appears Protective

### Evidence

| Ticket Activity | Churn Rate |
| --------------- | ---------: |
| 0 Tickets       |      50.6% |
| 1 Ticket        |      35.2% |
| 2+ Tickets      |      15.2% |

### Additional Observation

79% of customers never raised a ticket and represent the highest-churn segment.

### Business Impact

Support interactions may provide opportunities to strengthen customer relationships.

---

# Finding 8: Digital Inactivity Precedes Churn

### Evidence

* 0 sessions → 66.3% churn
* 10+ sessions → 20.9% churn
* Retained customers: median last visit = 7 days
* Churned customers: median last visit = 26 days

### Business Impact

Web and app inactivity provide early warning signals of churn risk.

---

# Finding 9: Campaign Performance Varies Despite Similar Reach

### Evidence

Campaign distribution was relatively balanced across customers.

Observed churn rates:

| Campaign        | Churn Rate |
| --------------- | ---------: |
| None            |      45.2% |
| Welcome Offer   |      45.3% |
| Free Shipping   |      46.3% |
| Bundle Discount |      46.9% |
| New Launch      |      51.0% |

### Business Impact

Campaign effectiveness appears to differ even when campaign reach is similar.

---

# Operational Insight: Major Support Pain Points

Among 1,921 support tickets:

* Late Delivery ≈ 375 tickets
* Refund Delay ≈ 345 tickets

Together these account for approximately 37% of all support issues.

### Business Impact

Post-purchase fulfilment and refund processes represent major sources of customer friction.

---

# Conclusion

The strongest churn indicators identified in the analysis are:

1. High recency (customer inactivity)
2. Low order frequency
3. Low purchase frequency in the last 180 days
4. Low monetary spend
5. Limited category diversity
6. Low digital engagement

These findings provide a strong foundation for churn prediction modelling and future retention strategies.
