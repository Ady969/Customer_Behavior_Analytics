# Customer Shopping Behavior Analysis (Python + SQL + Power BI)

![Customer Behavior Dashboard](https://github.com/user-attachments/assets/6b4f571f-6639-4bde-a662-fd216f4a4c58)

## 📌 Business Problem

A retail company wants to understand shifting customer purchasing patterns across demographics, categories, and channels — and identify which factors (discounts, reviews, seasons, payment method) drive repeat purchases and loyalty.

**Question answered:** How can the company use shopping data to identify trends, improve engagement, and optimize marketing and product strategy?

## 🧩 Dataset

- **Rows:** 3,900 transactions
- **Columns:** 18 (demographics, purchase details, shopping behavior)
- **Data quality:** 37 missing values in Review Rating, imputed using category-level median

## 🛠️ Workflow

1. **Python (Pandas)** — data cleaning, snake_case column standardization, missing value imputation, feature engineering (`age_group`, `purchase_frequency_days`), redundancy check (dropped `promo_code_used` after confirming overlap with `discount_applied`)
2. **PostgreSQL** — loaded cleaned data and ran 10 structured business queries
3. **Power BI** — built an interactive dashboard with slicers for subscription status, gender, category, and shipping type

## 📊 Verified Key Insights (independently re-run against raw data)

| Business Question | Result |
|---|---|
| Revenue by gender | Male customers generate **$157,890** vs. Female **$75,191** — more than double |
| High-spending discount users | **839 customers** used a discount yet still spent above the $59.76 average |
| Top-rated products | Gloves (3.86★), Sandals, Boots, Hat, Skirt |
| Shipping type impact | Express shipping customers spend slightly more on average ($60.48 vs. $58.46 for Standard) |
| Subscriber vs. non-subscriber revenue | Non-subscribers drive **73% of total revenue** ($170,436 vs. $62,645) despite subscribers spending a similar average ($59.49 vs $59.87) |
| Most discount-dependent products | Hat (50% of purchases discounted), Sneakers, Coat, Sweater, Pants |
| Customer segmentation (by previous purchases) | Loyal: 3,116 · Returning: 701 · New: 83 |
| Top products per category | Jewelry (Accessories), Pants/Blouse (Clothing), Sandals (Footwear), Jacket (Outerwear) |
| Repeat buyers (>5 purchases) & subscription | Only **958 of 3,476** repeat buyers are subscribers — a clear conversion gap |
| Revenue by age group | Young Adults (≤31) lead at **$62,143**, followed closely by Adult, Middle-Aged, and Senior groups (all within $6K of each other) |

## 🔎 Notable Observation
The customer segmentation query (New / Returning / Loyal) puts **80% of customers into "Loyal"** because the dataset's average previous-purchase count (25) is high relative to a >10 threshold. This highlights the importance of calibrating segmentation thresholds to a dataset's actual distribution rather than using fixed generic cutoffs.

## 📈 Business Recommendations
- **Convert non-subscribers:** they drive 73% of revenue but get none of the loyalty benefits — a clear upsell opportunity
- **Re-tier the loyalty segmentation** using purchase-count percentiles instead of fixed thresholds, so "Loyal" reflects genuinely top-tier customers
- **Promote Express shipping** as a small but real revenue lever
- **Address high discount-dependency items** (Hat, Sneakers, Coat) — margin risk if discounting becomes the default expectation

## 🖼️ Dashboard
Built in Power BI with interactive filters for Subscription Status, Gender, Category, and Shipping Type — showing revenue/sales by category and by age group, plus subscriber mix.

## 🛠️ Tools & Skills Used
Python (Pandas) · PostgreSQL · SQL (CTEs, window functions, CASE logic) · Power BI · Data Modeling · Data Visualization

## 👤 About Me
**Mohmadadil Shaikh** — Data Analyst | Power BI | SQL | Excel
🔗 [LinkedIn](https://www.linkedin.com/in/mohmadadil-shaikh)
