# Business Analytics Project: User Activity & Retention Analysis

## 🧠 Project Overview

The company has hired you to analyze raw transaction logs from its website. Each row in the dataset represents a user's interaction—such as viewing a product, opening a shopping cart, or completing a purchase. Your job is to help the company understand user behavior, conversion, and retention using spreadsheet analysis techniques.

---

## 📊 Dataset Description

Data is stored in the `raw_user_activity` tab and contains the following columns:

- `user_id`: Unique customer identifier
- `event_type`: Type of user activity (e.g. view, cart, purchase)
- `category_code`: Product category
- `brand`: Product brand
- `price`: Price of the product in USD
- `event_date`: Date of activity (YYYY-MM-DD)

---

## 🧩 Part 1: Build a Conversion Funnel

Create a funnel to understand how users move through the site:

1. Insert a pivot table in a new sheet named `conversion_funnel`.
2. Count **unique users** at each funnel stage: 
   - Product View
   - Cart Open
   - Purchase
3. Add two columns:
   - **Total conversion rate** (from product view to purchase)
   - **Step-by-step conversion rate** (e.g., view → cart → purchase)

---

## 📅 Part 2: Cohort Analysis Preparation

### Step 1: Filter Purchase Events
- Create a new tab `purchase_activity`.
- Filter `raw_user_activity` for `event_type = purchase` and copy data to the new tab (should contain 4,845 rows).

### Step 2: First Purchase Dates
- Insert a pivot table in a new tab `first_purchase` to find the earliest `event_date` per `user_id`.
- In `purchase_activity`, add a `first_purchase_date` column using `VLOOKUP()` from the `first_purchase` tab.

### Step 3: Create Monthly Tracking Columns
In `purchase_activity`, add:

- `event_month` (format: YYYY-MM)
- `first_purchase_month` (format: YYYY-MM)
- `cohort_age` using `DATEDIF()` to calculate months between `first_purchase_date` and `event_date`

---

## 📈 Part 3: Calculate Retention Rates

### Step 1: Build Cohorts
- Create a pivot table in a new sheet `cohort_analysis`
- Rows: `first_purchase_month` (cohort)
- Columns: `cohort_age` (0 to 4 months)
- Values: count of **unique users**

### Step 2: Calculate Retention Rates
- Create a new tab `retention_rates`
- Rebuild the layout similar to `cohort_analysis` but with **percentage retention**
- In cell `B3`, use a formula to divide each month’s users by the cohort's starting size

---

## 📋 Part 4: Organize & Document the Spreadsheet

### Executive Summary
Fill out the `Executive Summary` sheet:
- **Results**:
  - Summary of funnel findings and retention trends
- **Analysis**:
  - Data sources and assumptions
  - Methodology for funnel conversion rates
  - Decisions made during cohort analysis

### Table of Contents
Update the `Table of Contents` tab:
- List each tab in logical order:
  1. `Table of Contents`
  2. `Executive Summary`
  3. `conversion_funnel`
  4. `retention_rates`
  5. `cohort_analysis`
  6. `purchase_activity`
  7. `first_purchase`
  8. `raw_user_activity`
- Add a brief one-line description for each tab

### Formatting & Presentation
- Format dates and numbers for clarity
- Freeze headers, use bold fonts, borders, and highlight calculated cells
- Use consistent colors and spacing

---

## ✅ Outcome

You will deliver a polished and professional spreadsheet that includes:
- A clear conversion funnel
- Cohort-based retention analysis
- Executive-friendly summaries and formatting

This project will help guide decisions around customer retention and website performance.

