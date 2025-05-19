# 📈 A/B Testing Analysis – Marketing Campaign Performance

Welcome to a data-driven deep dive into a marketing experiment designed to answer one deceptively simple question:

> **Will this new marketing strategy drive more action — or just cost more?**

---

##  Project Overview

This A/B testing project evaluates the performance of a new marketing campaign (*Test Campaign*) compared to the existing one (*Control Campaign*). The goal: determine whether the new campaign strategy drives better ROI and more purchases per impression.

With business budgets and buyer behavior on the line, we leaned into the numbers to find out if the new approach is worth the investment.

➡️ See Colab [HERE](https://colab.research.google.com/drive/1GZ1eCE6W_9Wvd9TmOwp63pOEuiKeI1j-?usp=sharing)

---

##  Hypotheses

1. **H1 (ROI)**: The Test Campaign will deliver at least a **5% increase in Return on Investment (ROI)** compared to the Control Campaign.
2. **H2 (PR)**: The Test Campaign will increase **Purchase Rate (PR)** by at least **8%** over the Control Campaign.

---

##  Dataset Summary

Data was segmented into:

- **Control Campaigns**: 29 entries  
- **Test Campaigns**: 30 entries

Newly engineered features:

- `ROI = spend_[usd] / #_of_purchase`
- `CTR = #_of_website_clicks / #_of_impressions`
- `PR = #_of_purchase / #_of_impressions`

Columns available:  
`['campaign_name', 'date', 'spend_[usd]', '#_of_impressions', 'reach', '#_of_website_clicks', '#_of_searches', '#_of_view_content', '#_of_add_to_cart', '#_of_purchase', 'ROI', 'CTR', 'PR']`

---

## 📈 Key Metrics

| Metric               | Control Campaign | Test Campaign |
|----------------------|------------------|----------------|
| **Mean ROI**         | 5.05             | 5.90           |
| **Spend [USD]**      | $66,818          | $76,892        |
| **% of Total Spend** | 46.5%            | 53.5%          |
| **# of Purchases**   | 15,161           | 15,637         |

---

## Statistical Testing

### ✅ PR (Purchase Rate) – **Significant Result**

- **Test Used**: Mann-Whitney U (non-parametric)
- **U = 245.0**, **p = 0.0041**
- **Interpretation**: We reject the null hypothesis. The Test Campaign significantly outperformed the Control Campaign in **Purchase Rate**.

📈 This means the new campaign drove more purchases per impression — a powerful sign of stronger engagement and better message-market fit.

---

### ❌ ROI – **Not Statistically Significant**

- **Test Used**: Mann-Whitney U
- **U = 362.0**, **p = 0.2717**
- **Interpretation**: We fail to reject the null hypothesis. The observed **+9.5% lift in mean ROI** is encouraging, but **not statistically significant** in this sample.

📉 Possible reasons:
- Sample size (59 total campaigns)
- Skewed ROI distributions with high variance

---

## Insights & Recommendations

- The **Test Campaign improved PR significantly**, suggesting it’s better at converting attention into action.
- Although **ROI saw a +9.5% increase**, the variance means we can’t yet say the improvement is definitive — but it's **a promising trend worth monitoring**.
- With the Test Campaign already achieving **greater purchase volume and reach**, scaling it gradually with continued ROI tracking is advisable.

