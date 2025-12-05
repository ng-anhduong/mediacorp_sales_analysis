# Mediacorp Sales Analysis

Mediacorp is Singapore’s national media network and largest content creator, engaging 99% of the population weekly across four languages on digital, TV, radio, and social platforms. In this repository, I created an Excel-based dashboard that consolidates monthly sales reports and turns them into actionable insights for brands and merchandisers.

The dashboard is built with Power Query and PivotTables/PivotCharts. It automatically ingests new monthly files from a folder, computes key metrics (e.g., Net GMV after refunds, Net Margin Value, Net Qty), and provides custom date-range filtering via slicers. It also includes a simple sales channel tracker for a focused understanding of different channels and their campaigns' performance.

The data is sourced from a data challenge from Mediacorp's Commerce Team, which is anonymized and used solely for demonstration.

Before we go into more details, here is a quick look at the dashboard:
<img width="1201" height="672" alt="image" src="https://github.com/user-attachments/assets/5e5baa2c-c7b9-475e-a74f-3e9ccdf8ea74" />

You can find the data [here](https://github.com/ng-anhduong/mediacorp_sales_analysis/blob/main/Monthly_reports.zip), and the dashboard file [here](https://github.com/ng-anhduong/mediacorp_sales_analysis/blob/main/Mediacorp_dashboard.xlsm).

## A. INSTRUCTIONS ON USING THE DASHBOARD

1. Download files:
- An .xlsm file "Mediacorp_dashboard" which contains the merged data, pivot tables, and the dashboard
- A folder "Monthly_reports" containing datasets used by the dashboard

2. Add future reports:
Future reports must:
- Be in .xlsx format. You can try this out by generating similar datasets to the given ones inside "Monthly_reports" folder
- Have the same columns/headers & sheet structure as the provided reports

3. Open the excel file "Mediacorp_dashboard" 
- Data will auto update upon opening the file, and every 30 minutes while the file is opened
- Users can go to DASHBOARD Sheet, click the top right Refresh button (3 circular arrows) to update the pivots

## B. INSIGHTS FROM DATA

After some data handling, analysis, and dashboard making, here are some insights for sales trends from Nov to Dec 2024:

1. GMV: $820,508 → $849,000 (+3.47% MoM)

2. Margin value: $114,982 → $118,172 (≈+2.8% MoM)

3. Top Products (GMV / Qty / Margin Share)
- The leaders list is not identical across the three metrics
- Some items drive revenue (GMV) but not volume, suggesting higher price points
- Others are workhorse SKUs (Qty leaders) that can be featured for traffic/customer retention
- Products with high margin share are profit engines even if their GMV are not top 1–2

4. Category: mix shifted slightly. Based on %GMV by category,
- Home & Living remains #1 category (~47% → ~45%)
- Health & Beauty shifted up a bit (~24%→ ~25%)
- Food & Beverage rose 2% (~6% → ~8%)
- Consumer Electronics decreased slightly (~23% → ~22%)

5. By channel: performance is very similar across CCTR and ONLE; ONLE edges ahead on net qty (2516 vs 2488)

## C. RECOMMENDATIONS

1. Act on the three “Top 5” lists
- GMV leaders: run cross-sell bundles and cart-value boosters (e.g., “Complete the set” accessory bundles)
- Qty leaders: use for traffic campaigns; high number of purchases likely attracts customer visits
- Margin leaders: feature in prominent placements with lighter discounting and loyalty point multipliers instead of price cuts. This is to preserve profits

2. Category strategy
- Home & Living: keep always-on exposure
- Food & Beverage: Dec uplift suggests seasonality; we can capture this with limited-time deals

3. Channel optimization
- Given similar channel performance, run an A/B split of the same campaign across CCTR vs ONLE to measure: Cost to sell, refund rate, net margin per order
- Once we have validated this, we can shift budget toward the better net margin channel
