# Marketing Campaign Analysis

The google colab file can be found here - https://colab.research.google.com/drive/1z9Jttkm-kMWvWAqc1t0vlqsnjqy7dRfS?usp=sharing


## Project Overview

This project conducts a comprehensive analysis of an online subscription business's January 2018 marketing campaign. The aim is to evaluate campaign effectiveness, measure user conversion and retention rates, analyse marketing channels, conduct A/B testing, and uncover actionable insights using real-world data.

## Objectives

- Measure the performance of different marketing channels using conversion and retention rates.
- Attribute conversions to appropriate channels to inform marketing strategy.
- Conduct an A/B test to assess the effectiveness of personalised ads.
- Segment users by demographics (age, language) to understand behavior patterns.
- Investigate anomalies in campaign performance and assess their business impact.

<img width="350" alt="Screenshot 2025-03-28 at 10 48 44 PM" src="https://github.com/user-attachments/assets/cb7f4758-34ca-4708-8f9a-94cfbd342750" />

---

## Dataset

- **Source:** [DataCamp](https://assets.datacamp.com/production/repositories/3879/datasets/bdbbd97f839ef5cafebcc15363201d0e7b08881a/marketing.csv)
- The dataset contains 11 variables capturing ad views, subscription behavior, language preferences, channel exposure, and retention status for users in January 2018.

### Key Variables

- `user_id`, `date_served`, `marketing_channel`, `converted`, `subscribing_channel`, `variant`, `language_displayed`, `language_preferred`, `age_group`, `date_subscribed`, `is_retained`

<img width="450" alt="Screenshot 2025-03-28 at 10 50 58 PM" src="https://github.com/user-attachments/assets/fb9801b2-acd1-4e0a-8cf1-b1a75814b031" />


---

## Methodology

### 1. Data Cleaning & Feature Engineering

- Parsed dates, handled missing values, and engineered categorical mappings.
- Created additional variables such as `channel_code`, `DoW_served`, and language-match flags.

### 2. Exploratory Data Analysis

- Time-based trends in ad exposure, conversion, and retention.
- Key marketing KPIs:
  - **Overall Conversion Rate:** 14%
  - **Overall Retention Rate (1-month):** 67%

<img width="450" alt="Screenshot 2025-03-28 at 10 49 40 PM" src="https://github.com/user-attachments/assets/82a3ea91-be48-4869-89cb-d3b07fbb4475" />


### 3. Customer Segmentation

- Conversion and retention rates by:
  - **Subscribing Channel**
  - **Language Preference vs. Language Displayed**
  - **Age Group**
- Found Email and Instagram to perform best in conversions; Email also ranked high in retention.

  <img width="450" alt="Screenshot 2025-03-28 at 10 49 08 PM" src="https://github.com/user-attachments/assets/ffef9f6a-edec-4e73-a5d1-b0173160a397" />


### 4. A/B Testing for Personalisation

- Compared performance of generic vs personalised ads.
- Personalised emails yielded a 40% increase in conversions which proved to be highlt statistically significant — indicating value in targeting.

  <img width="500" alt="Screenshot 2025-03-28 at 10 50 38 PM" src="https://github.com/user-attachments/assets/9ddf286f-f7bc-4526-99c9-326505356c01" />


### 5. Conversion Attribution

- Developed a generalised function for conversion rate analysis across user segments.
- Used time-series visualisations to identify trends by marketing channel and demographic group.

---

## Key Insight: House Ads Language Bug and Subscription Loss

A sudden and sustained **drop in House Ads conversions after January 10, 2018** prompted further investigation. Key findings:

- The number of House Ads shown in **non-English languages (Spanish, Arabic, German)** drastically declined after Jan 10.
- Meanwhile, users with these languages as preferences continued to receive ads — now mostly in English.
- A clear **language mismatch** emerged, confirmed by analysing the percentage of ads shown in users' preferred languages.

### Quantifying the Impact

- Indexed pre-bug conversion rates for Spanish, Arabic, and German users against English.
- Estimated the number of lost subscriptions post-January 10 by applying expected conversion rates to the actual number of users.
- **Result:** The company may have lost over **16% of its potential subscriptions in January** due to the language delivery issue in House Ads.

This represents a major operational lapse with clear financial implications — and an opportunity for recovery if addressed. Therefore, correcting the language mismatch would have most likely **increased subscriptions by 20%** after 10th January 2018.

<img width="400" alt="Screenshot 2025-03-28 at 10 50 15 PM" src="https://github.com/user-attachments/assets/7aeae2a8-195e-4a7a-b941-9a51ea81263d" />  <img width="400" alt="Screenshot 2025-03-28 at 10 49 57 PM" src="https://github.com/user-attachments/assets/5bde71f1-d5fc-4c6d-85f0-ccf1c9698d64" />

---

## Real-World Relevance

This project replicates a real-world data science workflow for a marketing team. The analysis not only benchmarks campaign performance but also **uncovers a hidden technical error** with measurable business consequences.

### Business Applications:

- Better targeting using demographic segmentation.
- Data-driven decisions for channel-specific ad budgets.
- Automated anomaly detection in live campaigns.
- Preventing future losses from bugs in ad delivery systems.



