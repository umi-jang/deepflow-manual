# Inventory Management

*Forecast inventory using item-level demand and automatically derive production and order quantities*

Item-level demand forecasts let you anticipate future inventory positions and automatically derive the production and order quantities — and timing — needed to prevent stockouts and overstock.

## [1] Walkthrough of the inventory screen

![Inventory screen layout](/images/inventory/01.png)

### Pick a time point

Choose the time point you want to inspect. The current month is shown by default.

### Search

Use the search field to find a specific item.

### Download

Export the data for the selected time point as a CSV.

### Inspect an item

Select an item to see expected shipments and ending inventory for the current month and the next six months. Hover any data point to see the underlying values.

## [2] Field reference and how to use it

### [2.1] Item info and basic fields

![Item info and basic fields](/images/inventory/02.png)

**Field description**

- **Safety stock**: Calculated from the forward demand forecast.

> **Note:** Traditional forecasting systems compute safety stock from historical indicators (such as the trailing 3-month average), which limits how well they adapt to future changes. DeepFlow computes safety stock from forward-looking demand forecasts instead.

**How to apply it**

DeepFlow supports two ways to compute safety stock from forecasts. Pick the one that fits your situation.

#### Add a buffer on top of the forecast

Example: To cover next month's shipments, treat `p%` of next month's forecast as safety stock. The target inventory becomes `next_month_forecast + (next_month_forecast × p%)`.

You need to define a `p%` that matches your target inventory range. If you know the acceptable inventory range, derive the optimal `p%` from that.

#### Hold several months of inventory

Example: To cover next month and additionally hold two months of inventory, set target inventory to `month+1_forecast + month+2_forecast`. The safety stock is `month+2_forecast`.

### [2.2] Shipment status

![Shipment status](/images/inventory/03.png)

**Field description**

- **Past avg. shipment (3M)**: Average shipment volume for the trailing 3 months (M-3 to M-1).
- **Past avg. shipment (6M)**: Average shipment volume for the trailing 6 months (M-6 to M-1).
- **Last month shipment (M-1)**: Last month's actual shipments.
- **Current shipment (M+0)**: This month's shipments.
- **Next shipment (M+1)**: Next month's predicted shipments.
- **Future avg. shipment (3M)**: Average predicted shipment over the next 3 months (M+1 to M+3).
- **Year-over-year shipment**: Shipment from the same period one year ago (for M+1).

**How to apply it**

- **Plan shipments for demand changes**: Combining past, current, and next-month volumes reveals demand volatility you can plan around.
- **Adjust shipments for cost optimization**: Compare past and future averages to handle uneven demand patterns.

### [2.3] Inventory status

![Inventory status](/images/inventory/04.png)

**Field description**

- **Safety stock**: The safety stock value implied by the configured safety stock level.

  Example: If the coverage period is one month (M+1) and the safety stock level is 0.42, safety stock is `M+1 shipment + 42% of M+1 shipment`.
- **Future avg. inventory**: Average ending inventory over the forecast horizon.
- **Future max. inventory**: Maximum ending inventory over the forecast horizon.
- **Future min. inventory**: Minimum ending inventory over the forecast horizon.

**How to apply it**

- **Manage safety stock to avoid stockouts**: Maintain required levels by referring to shipment and inventory forecasts, and tune safety stock during volatile periods.
- **Prevent overstock**: Use the max, min, and average forecasts to keep inventory from rising more than necessary.

### [2.4] Production plan

![Production plan](/images/inventory/05.png)

**Field description**

- **Recommended production quantity**: The proposed order quantity (production or purchase).

  ```
  Recommended = coverage_period_shipment_forecast + safety_stock − current_inventory
  ```
- **Confirmed production quantity**: The value you confirm after reviewing the recommendation.

**How to apply it**

- **Improve recommendation accuracy**: Add per-item minimum batch size and standard production units if useful. Production timing depends on lead time — DeepFlow accounts for the time from order placement to receipt. Entering the confirmed value back into DeepFlow further improves future inventory accuracy.

### [2.5] Shipments and ending inventory (time series)

![Time series view](/images/inventory/06.png)

**Field description**

- **Shipments (time series)**: Future shipments in chronological order.
- **Ending inventory (time series)**: Future ending inventory in chronological order.

**How to apply it**

- **Manage risk through long-range forecasts**: Use future shipment and ending-inventory series to spot unexpected demand swings or supply-chain risks early.
