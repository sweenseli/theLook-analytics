# Metric definitions

| Metric | Definition |
|---|---|
| Valid order / net revenue | Items with status Complete, Shipped or Processing. Cancelled and Returned are excluded. |
| Sales Margin | Sales Amount minus product cost |
| Margin % | Sales Margin / Sales Amount (about 52%, flat across years) |
| Total Orders | Distinct Order Id on valid items |
| Unique Buyers | Distinct User Id |
| Repeat Rate | Customers with more than 1 valid order / customers in the selected period |
| Return Rate | Returned items / (Returned + Complete) items |
| Avg Order Value | Net sales / distinct valid orders |
| Session to Purchase | Sessions with a purchase event / total sessions (events table) |

## Period logic

A Period parameter has 3 options: This Year, This Month, Total Period. Each KPI has a current value (CY/CM), a prior value (PY/PM, same period a year or month earlier) and a delta. For Total Period the delta is hidden.

## Targets

Sales target for a year = previous year's sales x 1.45 (the 2019 target equals 2019 sales). Margin target uses the same ratio, because margin % is flat in this dataset.
