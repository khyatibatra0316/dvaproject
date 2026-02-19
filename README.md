# Blinkit Data Analytics Dashboard

## Project Overview

This project analyzes operational and business performance of **Blinkit** using cleaned datasets.
The objective is to derive actionable insights from inventory, delivery, and order data and present them through key performance indicators (KPIs) and interactive dashboards.

The analysis focuses on:

* Inventory quality and damage trends
* Delivery efficiency and service performance
* Order revenue and product performance

## Datasets Used

The following cleaned datasets were used:

1. **blinkit_inventoryNew**

   * product_id
   * date
   * stock_received
   * damaged_stock
   * Month

2. **blinkit_delivery_performance**

   * order_id
   * delivery_partner
   * promised_time
   * actual_time
   * delivery_time_minutes
   * distance_km
   * delivery_status
   * reasons_if_delayed
   * Negative_flag
   * Future_flag

3. **blinkit_order_items**

   * order_id
   * product_id
   * quantity
   * unit_price
   * total_price


## Data Cleaning Steps

### General

* Header rows frozen
* Filters applied for quick inspection
* Datatypes standardized (numeric, datetime)
* Duplicates removed where applicable
* Whitespaces trimmed

### Inventory

* Verified damage calculations
* Created damage rate metric
* Checked for extreme or missing values

### Delivery

* Validated datetime formats
* Recalculated delivery time logic
* Flagged negative delivery times
* Checked for future dates
* Standardized delivery status

### Order Items

* Verified:
  `total_price = quantity × unit_price`
* Checked for negative or extreme quantities
* Validated unit price values
* Confirmed revenue consistency


## Key Performance Indicators (KPIs)

### Inventory

* **Total Stock Received:** 14,275
* **Total Damaged Stock:** 995
* **Damage Rate:** 6.97%
* **Total Products:** 269

### Delivery Performance

* **Total Orders:** 5,001
* **On-Time Delivery Rate:** 69.39%
* **Average Delivery Distance:** 2.72 km


### Order Performance

* **Total Orders:** 5,001
* **Total Revenue:** ₹4,972,415
* **Total Items Sold:** 10,034
* **Average Order Value:** ₹994

## Pivot Analysis

### Inventory

* Monthly stock received vs damaged stock
* Monthly damage rate trends

### Delivery

* Order count by delivery status

### Orders

* Revenue by product
* Quantity sold by product


## Dashboard Visualizations

### Inventory

* Monthly Damage Rate (Line Chart)
* Stock vs Damaged Comparison (Column Chart)

### Delivery

* Delivery Status Distribution (Pie Chart)

### Orders

* Revenue Distribution by Product
* Quantity Distribution (Histogram)


## Key Insights

* Overall inventory damage rate is **6.97%**, with certain months showing higher loss.
* Approximately **69% of deliveries are completed on time**, indicating scope for service improvement.
* Average delivery distance is low (≈2.7 km), supporting quick-commerce operations.
* Revenue is concentrated among a small set of high-performing products.
* Average order value is around **₹994**, indicating strong basket value.

## Tools Used

* Google Sheets
* Pivot Tables
* Charts & Dashboards
* Data Cleaning Functions

## Project Outcome

This dashboard provides a consolidated view of Blinkit's operational efficiency across inventory, delivery, and sales, enabling data-driven decision-making and performance monitoring.
