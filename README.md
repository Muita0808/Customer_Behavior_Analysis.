# Customer Shopping Behavior Analysis

An end-to-end retail analytics project analyzing **3,900 customer transactions** to uncover purchasing patterns, customer segments, subscription behavior, and the relationship between discounts and revenue.

The project demonstrates a complete analytics workflow — from **data cleaning and feature engineering in Python**, through **SQL-based business analysis in PostgreSQL**, to **interactive dashboard development in Power BI**.

## 📌 Project Overview

Understanding customer purchasing behavior can help retailers improve pricing, customer retention, merchandising, and loyalty strategies.

This project analyzes customer shopping data to answer questions such as:

* How does customer spending vary across different customer segments?
* Do subscribers spend more than non-subscribers?
* Which product categories generate the most sales?
* How does discount usage relate to purchasing behavior?
* Which customer groups and products present opportunities for stronger retention and marketing?
* Does frequent purchasing translate into subscription adoption?

The analysis transforms raw transactional data into business-focused insights that can support **customer segmentation, pricing, merchandising, and loyalty decisions**.

## 🗂️ Dataset

The dataset contains **3,900 customer transaction records** and **18 original columns**, covering customer demographics, purchasing behavior, product information, discounts, subscriptions, shipping preferences, and review ratings.

Key fields include:

* Customer demographics
* Product category
* Purchase amount
* Review rating
* Discount usage
* Subscription status
* Purchase frequency
* Shipping type
* Previous purchases

> **Note:** This is a portfolio project created for learning and demonstration purposes using a publicly available sample retail dataset.


# 1. Data Preparation — Python / Pandas

The raw dataset was cleaned and prepared using **Python and Pandas**.

### Data Cleaning

Key cleaning activities included:

* Cleaned a **3,900-row dataset containing 18 original columns**
* Investigated missing values and data quality issues
* Identified **37 missing review ratings**
* Imputed missing ratings using the **median review rating within each product category**
* Removed a redundant `promo_code_used` column after validating that it duplicated `discount_applied`
* Checked the dataset for consistency before loading it into the database

### Why category-level median imputation?

Instead of replacing all missing ratings with one global median, the analysis used the median rating within each product category.

This approach preserves potential differences in customer rating behavior between categories while avoiding unnecessary loss of records.

---

## ⚙️ Feature Engineering

Additional analytical features were created to make the dataset more useful for segmentation and analysis.

### `age_group`

Customers were grouped into four age segments:

* Young Adult
* Adult
* Middle Age
* Senior

The segmentation was created using **quartile-based binning** to support demographic comparisons.

### `purchase_frequency_days`

The categorical purchase frequency variable was converted into an approximate numerical representation of purchase intervals.

For example:

This enabled purchase frequency to be analyzed as a numerical variable for comparisons and further analytical work.

# 2. SQL Analysis — PostgreSQL

The cleaned dataset was loaded into **PostgreSQL using SQLAlchemy**.

SQL was then used to answer business questions and identify patterns in customer behavior.

The analysis focused on areas including:

### Customer Behavior

* Customer purchasing patterns
* Average purchase amount
* Purchase frequency
* Previous purchase behavior
* Customer segmentation

### Subscription Analysis

* Subscriber vs. non-subscriber behavior
* Spending differences between subscription groups
* Relationship between purchase frequency and subscription adoption

### Product & Category Analysis

* Revenue and sales performance by category
* Product/category rating patterns
* High-performing and high-discount categories

### Discount Analysis

* Discount usage across products
* Categories with greater dependence on discounts
* Potential implications for pricing and profitability

---

# 3. Power BI Dashboard

The results from the SQL analysis were transformed into an interactive **Power BI dashboard**.

### Dashboard KPIs

The dashboard provides high-level metrics including:

* **Customer Count**
* **Average Purchase Amount**
* **Average Review Rating**

### Dashboard Analysis

Users can explore:

* Revenue and sales by product category
* Customer distribution by age group
* Subscription vs. non-subscription customers
* Purchasing behavior
* Product/category performance

### Interactive Filters

The dashboard can be filtered by:

* Subscription Status
* Gender
* Product Category
* Shipping Type

This allows users to move from high-level KPIs into more specific customer and product segments.

---

# Key Business Insights

The analysis generated several insights with potential implications for retail strategy.

### 1. Subscription adoption presents an opportunity

Subscribers did **not demonstrate a clear spending advantage over non-subscribers** in the analyzed dataset.

This suggests that the current subscription proposition may not be sufficiently compelling to drive higher customer value.

**Opportunity:** Strengthen subscription benefits around tangible customer value such as exclusive offers, early access, loyalty rewards, or shipping benefits.

---

### 2. Frequent purchasing does not automatically translate into subscriptions

Customers with relatively frequent purchasing behavior are not necessarily converting into subscribers.

This indicates a potential gap between **customer engagement and loyalty program adoption**.

**Opportunity:** Introduce targeted loyalty incentives that encourage frequent purchasers to move into subscription or membership programs.

---

### 3. Some categories show stronger discount dependency

Categories such as **Hats, Sneakers, and Coats** showed relatively high discount usage.

Heavy discounting can support sales volume but may also create pressure on margins or condition customers to wait for promotions.

**Opportunity:** Review discount strategies for these categories and evaluate whether targeted promotions can replace broad discounting.

---

### 4. Highly rated products provide marketing opportunities

Products/categories including **Gloves, Sandals, and Boots** recorded strong customer ratings.

High customer satisfaction can provide an opportunity for stronger merchandising and marketing visibility.

**Opportunity:** Feature highly rated products more prominently in campaigns, recommendations, and promotional placements.

---

# Business Recommendations

Based on the analysis, the following actions could be considered:

| Insight                                             | Recommendation                                                     |
| --------------------------------------------------- | ------------------------------------------------------------------ |
| Subscribers do not clearly outspend non-subscribers | Strengthen subscription benefits and value proposition             |
| Frequent purchasers are not necessarily subscribers | Target frequent buyers with loyalty/subscription incentives        |
| Some categories rely heavily on discounts           | Review discount depth and frequency to protect margins             |
| Highly rated products have marketing potential      | Increase visibility of highly rated products                       |
| Customer behavior varies across segments            | Use demographic and behavioral segmentation for targeted campaigns |

---

# Tools

### Programming & Analysis

* **Python**
* **Pandas**
* **Jupyter Notebook**

### Database & SQL

* **PostgreSQL**
* **SQLAlchemy**

### Visualization

* **Microsoft Power BI**

# Project Objective

The objective of this project was not simply to visualize the dataset, but to demonstrate an **end-to-end analytics workflow**:

> **Raw data → Clean data → Engineered features → SQL analysis → Business insights → Interactive dashboard**

The project demonstrates the ability to combine **Python, SQL, and Power BI** to transform transactional data into insights that can support business decision-making.

---

## About the Project

This project was developed as part of my continued development in **data analytics**, with a focus on building practical skills across data preparation, SQL analysis, visualization, and business interpretation.

It is intended as a portfolio project to demonstrate practical application of:

**Python • SQL • Power BI • Data Cleaning • Feature Engineering • Business Analytics**
