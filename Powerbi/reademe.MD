# 📊 Shopify App Store Analysis

## 🎯 Project Overview

You have been hired to analyze the landscape of apps in the Shopify App Store using publicly scraped data. Your goal is to identify key factors that drive app success. Using Power BI, this project involves building a visual report with insightful analytics for each of the three main areas:

- App Landscape
- Reviews
- App Reviews

Each part corresponds to a dedicated page in the Power BI report. Screenshots are taken at each step to show your process and final visualizations.

---

## 🗂️ Dataset Overview

The project uses `shopify.xlsx`, which contains the following tables:

- **apps**: Main table with details about Shopify apps
- **apps_categories**: Join table between apps and categories
- **categories**: App category names
- **reviews**: User reviews, ratings, and developer responses

---

## 📁 Power BI Report Pages

### 📌 Part 1: App Landscape

> **Power BI Page:** `App Landscape`

**Goals:** Explore general statistics about apps and how they are performing in terms of visibility and reviews.

#### Tasks:

1. **KPI Card:**
   - Metric: Count of unique apps.
   - Visual Type: KPI Card.

2. **Line Chart:**
   - Y-Axis: Sum of `reviews_count`
   - X-Axis: `lastmod` date (not in hierarchy format)
   - Purpose: Understand review trends over time.

3. **Scatterplot:**
   - X-Axis: `reviews_count`
   - Y-Axis: Average `rating`
   - Add a Text Box with interpretation: Examine if apps with more reviews tend to be rated higher or lower.

---

### 📌 Part 2: Reviews

> **Power BI Page:** `Reviews`

**Goals:** Derive new metrics from review data to assess helpfulness and developer responsiveness.

#### Tasks:

1. **Create DAX Column - `helpful_reviews`:**
   ```DAX
   helpful_reviews = reviews[rating] * (1 + reviews[helpful_count])
