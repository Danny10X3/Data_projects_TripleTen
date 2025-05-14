# Zuber Taxi Data Analysis

## 📊 Project Overview

This project analyzes taxi ride data in Chicago for Zuber, focusing on ride patterns, company performance, and potential effects of weather on ride duration. The analysis covers both exploratory data insights and a specific case study on rides between The Loop and O'Hare International Airport.

---

## 🗂️ Data Description

The dataset consists of four main tables:

### 1. `neighborhoods`
- `neighborhood_id`: Unique ID of the neighborhood
- `name`: Name of the neighborhood

### 2. `cabs`
- `cab_id`: Unique cab identifier
- `vehicle_id`: Technical vehicle ID
- `company_name`: Taxi company name

### 3. `trips`
- `trip_id`: Unique ride identifier
- `cab_id`: Linked cab ID
- `start_ts`: Ride start timestamp (rounded to the hour)
- `end_ts`: Ride end timestamp (rounded to the hour)
- `duration_seconds`: Ride duration in seconds
- `distance_miles`: Distance of the ride in miles
- `pickup_location_id`: Neighborhood ID for pickup
- `dropoff_location_id`: Neighborhood ID for dropoff

### 4. `weather_records`
- `record_id`: Unique weather record ID
- `ts`: Timestamp (rounded to the hour)
- `temperature`: Recorded temperature
- `description`: Weather condition (e.g., "light rain")

---

## 🔍 Tasks and Objectives

### 📈 Tasks 1-4: Exploratory Data Analysis
1. **Company Ride Counts (Nov 15–16, 2017)**  
   Count the number of trips per taxi company. Name the result `trips_amount` and sort in descending order.
   
2. **Yellow and Blue Taxis (Nov 1–7, 2017)**  
   Count rides for companies with names containing "Yellow" or "Blue". Group by `company_name`.

3. **Top Companies vs. Others (Nov 1–7, 2017)**  
   Aggregate rides for **Flash Cab** and **Taxi Affiliation Services**, group others under `"Other"`, and compare their trip counts (`trips_amount`).

4. **Get Neighborhood IDs**  
   Retrieve neighborhood identifiers for **The Loop** and **O'Hare International Airport** from the `neighborhoods` table.

---

### 🌧️ Tasks 5-7: Ride Duration Analysis During Rainy Saturdays
Investigate whether **ride durations from The Loop to O'Hare** change during **rainy Saturdays**:

- Merge ride data with weather conditions.
- Filter for Saturday rides from The Loop to O'Hare.
- Compare durations between rainy and non-rainy days.

---

## 🛠️ Tools & Technologies

- **Language**: SQL / Python (e.g., pandas)
- **Platform**: Jupyter Notebook / Data warehouse
- **Visualization**: Matplotlib / Seaborn / Power BI (optional)
- **Data Sources**: Internal Zuber database exports

---

## 📁 Project Structure

```
/data              # Raw CSV or database export files
/scripts           # SQL or Python scripts for analysis
/notebooks         # Jupyter notebooks with EDA and visualizations
/reports           # Summary of findings, charts, and presentation
README.md          # Project overview and instructions
```

---

## ✅ Outcome

- Understand ride distribution by company and time
- Identify how weather affects ride times
- Enable data-driven decisions for improving Zuber’s services and routing strategies

---

## 📬 Contact

For any questions or contributions, please contact the Zuber Analytics team.
