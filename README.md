# 🚚 Supply Chain Route Optimizer (SAP HANA Cloud)

This project simulates optimal delivery routes from warehouses to demand zones based on:
- Stock availability
- Fuel cost per km
- Geo-coordinates (Haversine distance)

## 💻 Tech Stack
- SAP HANA Cloud
- SQLScript
- BTP Cockpit

## 🗃️ Tables Used
- Warehouses.csv
- DemandZones.csv
- VehicleAvailability.csv

## ⚙️ What It Does
- Computes all possible warehouse → zone routes
- Calculates fuel cost and adds penalties if stock is insufficient
- Ranks routes by lowest cost and best supply match

## 📂 Files
- `CalculateRoutes.sql`: Procedure to compute routes
- `*.csv`: Sample data to import
- `sample_query.sql`: Shows top 10 optimal routes

## 🧪 Run Example
```sql
CALL CalculateRoutes();
SELECT * FROM Routes ORDER BY RouteScore ASC LIMIT 10;
