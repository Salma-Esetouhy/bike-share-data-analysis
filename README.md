# Bike Share Data Analysis – SQL Project

## Project Overview

This project analyzes bike-sharing data using SQL and Google BigQuery to identify usage patterns, customer behavior, station performance, and business growth opportunities.

The analysis focuses on more than 15,000 rides and aims to translate raw data into actionable business insights and operational recommendations.

## Tools & Technologies

- SQL
- Google BigQuery
- Common Table Expressions (CTEs)
- Window Functions
- Data Aggregation
- Business Analysis

## Business Analysis & Key Findings

### 1. Operational Pulse: The Double-Hump Trend

Our analysis of 15,000+ rides confirms that UrbanRoll is primarily a commuting tool.

**Key Finding: Peak Demand**

Usage spikes at:
- 7:00 AM
- 3:00 PM

**Business Recommendation:**

Ensure rebalancing crews (the trucks that move bikes between stations) are active between 10:00 AM and 2:00 PM to prepare for the evening rush.

### 2. The Subscriber vs. Casual Split

The data revealed two distinct user personas:

**The Commuter (Subscriber)**
- Short, predictable trips.
- Average trip duration: 15 minutes.
- They are the backbone of daily ride volume.

**The Explorer (Casual)**
- Longer, less predictable trips.
- Average trip duration: 35 minutes.
- They represent lower ride volume but higher bike-time usage.

**Business Recommendation:**

Launch a "Weekend Explorer" pass targeted at Casual users to increase their ride frequency during off-peak hours.

### 3. The Rebalancing Crisis (Advanced Insight)

Using our Net Flow CTE, we identified significant differences between stations. Some stations are "Sinks" (they receive more bikes than they send out), while others are "Sources" (more bikes leave than arrive).

**Key Findings:**

- **Top Source: Jennifer Land St** – Recorded 648 departures and 582 arrivals, resulting in a net flow of -66. This indicates that more bikes leave this station than return.
- **Top Sink:** To be confirmed from the station with the highest positive net flow.

**Business Recommendation:**

Implement "Dynamic Incentives" by offering users small discounts if they end their rides at Source stations. This can encourage better bike distribution and reduce the risk of bike shortages.

Additionally, rebalancing crews can transfer bikes from stations with excess supply to stations experiencing shortages.

### 4. Growth & Retention

Our Month-over-Month (MoM) analysis shows a steady growth rate. However, we identified a small group of "Power Users" (the top 1%) who account for a disproportionate amount of revenue.

**Key Observation:**

Our 7-day moving average smooths out daily fluctuations and helps reveal the underlying growth trend.

The estimated month-over-month growth rate remains to be calculated and confirmed from the query results.

**Business Implications:**

- Monitor monthly user growth to understand customer acquisition trends.
- Identify and retain high-value Power Users.
- Use moving averages to monitor underlying business performance.
- Develop strategies to encourage continued customer engagement.

## SQL Analysis Performed

| Analysis | SQL Techniques |
|---|---|
| Peak Hours Analysis | EXTRACT, COUNT, GROUP BY |
| Popular Stations | JOIN, COUNT, ORDER BY |
| Ride Duration Categories | CASE WHEN, TIMESTAMP_DIFF |
| Net Flow Analysis | CTEs, JOIN, COUNT |
| Monthly Signups | DATE_TRUNC, COUNT, GROUP BY |
| Monthly Growth | LAG, OVER, NULLIF |

## Final Business Recommendations

Based on the analysis, the following actions are recommended:

1. **Optimize Operations:** Prepare bike redistribution teams before peak demand periods.
2. **Improve Customer Segmentation:** Develop targeted offers for Subscribers and Casual users.
3. **Balance Bike Distribution:** Introduce incentives to encourage users to return bikes to stations experiencing shortages.
4. **Monitor Growth:** Track monthly signups and month-over-month growth.
5. **Retain High-Value Users:** Identify Power Users and develop strategies to maintain their engagement.




