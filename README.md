Customer Shopping Behavior Analysis

An end-to-end analysis of a 3,900-row retail dataset, from raw data to business insight. The project covers data cleaning and feature engineering in Python, analytical querying in SQL, and dashboard visualization in Power BI.

Project Overview

This project explores customer shopping behavior to understand purchasing patterns, segment customers by loyalty, and evaluate the impact of discounts and subscriptions on revenue. The goal was to move from a raw transactional dataset to insights that could support merchandising and pricing decisions.

Data Preparation (Python / Pandas)
Cleaned a 3,900-row dataset with 18 original columns
Handled missing review ratings (37 nulls) using category-level median imputation, rather than dropping rows or using a single global median, to preserve category-specific rating patterns
Identified and removed a redundant column (promo_code_used duplicated discount_applied) after validating the two columns were identical
Engineered an age_group feature (Young Adult, Adult, Middle Age, Senior) using quartile-based binning
Engineered a purchase_frequency_days feature, mapping categorical purchase frequency (e.g. "Weekly," "Fortnightly," "Annually") to numeric day counts to support cohort and forecasting analysis
Loaded the cleaned dataset into PostgreSQL via SQLAlchemy for the analysis stage
Analysis (SQL / PostgreSQL)

Wrote analytical SQL queries to answer specific business questions, and here's what the data showed:

Revenue by gender: Male customers generated $157,890 in total revenue versus $75,191 for female customers — driven largely by a higher share of male customers in the dataset (2,652 of 3,900) rather than higher per-customer spend
Discount users who still spend above average: 839 customers applied a discount and still spent above the $59.76 average purchase amount, suggesting discounting doesn't always signal price-sensitivity
Top-rated products: Gloves (3.86), Sandals (3.84), Boots (3.82), Hat (3.80), and Skirt (3.78) had the highest average review ratings
Shipping type: Express shipping customers spent slightly more on average ($60.48) than Standard shipping customers ($58.46)
Subscribers vs. non-subscribers: Subscribed customers did not spend more on average ($59.49 vs. $59.87 for non-subscribers) — subscription status has little bearing on order value in this dataset
Most discount-dependent products: Hats (50% of purchases discounted), Sneakers (49.7%), Coats (49.1%), Sweaters (48.2%), and Pants (47.4%)
Customer segmentation: Using previous-purchase-count thresholds (New = 1, Returning = 2–10, Loyal = 10+), 3,116 customers classified as Loyal, 701 as Returning, and only 83 as New — the heavy skew toward "Loyal" suggests the segmentation thresholds could be recalibrated for a more evenly distributed view in a follow-up iteration
Top 3 products per category: e.g. Jewelry, Sunglasses, and Belt led Accessories; Blouse, Pants, and Shirt led Clothing; Sandals, Shoes, and Sneakers led Footwear
Repeat buyers and subscriptions: Customers with 5+ previous purchases subscribed at roughly the same rate (27.6%) as the overall customer base (27%) — repeat buying doesn't predict subscription likelihood here
Revenue by age group: Fairly even across segments, with Young Adults contributing the most ($62,143) and Seniors the least ($55,763)
Visualization (Power BI)

Findings from the SQL analysis were brought into an interactive Power BI dashboard with KPI cards (customer count, average purchase amount, average review rating), a subscription-status breakdown, and revenue/sales views by category and age group — filterable by subscription status, gender, category, and shipping type.

Business Recommendations
Promote subscription benefits more strongly, since subscribers currently spend no more than non-subscribers — there's room to make the subscription tier more compelling
Build loyalty incentives that reward repeat purchases specifically, since high purchase frequency alone isn't converting into subscriptions
Revisit discount policy for high-discount-dependency items (Hats, Sneakers, Coats) to protect margin
Feature top-rated products (Gloves, Sandals, Boots) more prominently in marketing

Tools & Technologies
Python (Pandas)
SQL (PostgreSQL)
Power BI

Skills: Python (Pandas) • SQL (PostgreSQL) • Power BI • Data Cleaning • Feature Engineering • Data Visualization
Jupyter Notebook

This is a portfolio project created for learning and demonstration purposes, based on a publicly available sample retail dataset. It showcases data cleaning, feature engineering, SQL analysis, and dashboard design skills.
