# theLook eCommerce: Full-Funnel Commercial & Customer Analytics

Portfolio case study built on the public **theLook eCommerce** dataset (BigQuery). The goal: turn raw orders, customers, products and web events into an interactive Tableau "Sales Cockpit" that answers *how are we trending, who buys, what sells, and what leaks*.

## What is in this repo

| Path | What it is |
|---|---|
| `data/theLook_orders_flat.csv.gz` | Order-item level analytical table (181,397 rows, 38 columns) built from orders, order_items, users, products and distribution centers |
| `docs/metric_definitions.md` | How every KPI is calculated (net revenue, repeat rate, return rate, targets, period logic) |
| `images/` | Dashboard screenshots |
| `Thelooks new.twbx` | Tableau workbook (168 MB, too large for a normal commit: attach it under GitHub Releases or use Git LFS) |

## Dashboard pages

- **Cockpit**: Sales, Margin, Margin %, Cost, Total Orders, Repeat Rate, Return Rate, Avg Order Value, with a Period selector (This Year / This Month / Total Period) and YoY or MoM change.
- **Customer Insight**: top customers and spend.
- **Product Insight**: category, brand and product-line performance.

![Cockpit](images/cockpit.png)

## Key facts (data to 2 Aug 2026)

- 181,397 order lines, 93,887 valid orders, 66,135 buying customers
- Net revenue **$8.14M** and gross margin **~52%** (Complete, Shipped and Processing orders only)
- Return rate **~28%** of delivered-or-returned items

## How it was built

1. Joined the BigQuery source tables into one order-item grain table (one row per item) with customer, product, cost and location attributes.
2. Defined *net* revenue by excluding Cancelled and Returned items.
3. Built period-aware measures in Tableau (a Period parameter drives current vs. previous comparison for every KPI).
4. Added a growth-based sales target (prior-year sales x 1.45) with margin and cost targets scaled at the same ratio.

## Data note

The dataset is the public, synthetic theLook eCommerce data. No real customers.

## Author

Sween | MSc Business Analytics
