# Summer_Analytics
(Capstone Project)
# 🚗 Dynamic Pricing for Urban Parking Lots

A data-driven pricing engine built for optimizing parking lot occupancy and revenue using real-time demand features. This project was developed as part of the **Summer Analytics 2025 Capstone** hosted by **Consulting & Analytics Club × Pathway**.

---

## 📌 Problem Statement

Urban parking lots often use static pricing throughout the day, leading to:
- Underutilization during off-peak hours
- Overcrowding during peak hours

Our goal is to develop a **dynamic pricing model** that adjusts prices based on:
- Real-time demand signals
- Historical usage patterns
- External factors (traffic, special days, etc.)

---

## 📊 Dataset

The dataset includes **73 days** of usage data for **14 urban parking lots**, with:
- 18 time points per day (every 30 minutes from 8:00 AM to 4:30 PM)
- Features:
  - `Occupancy`, `Capacity`, `QueueLength`
  - `TrafficConditionNearby` (low/average/high)
  - `VehicleType` (car/bike/truck)
  - `IsSpecialDay` (0 or 1)
  - GPS coordinates for location (optional for Model 3)

---

## ⚙️ Models Implemented

### ✅ Model 1: Linear Occupancy-Based Pricing
- Formula:  
  \[
  Price_{t+1} = Price_t + \alpha \cdot \left(\frac{Occupancy}{Capacity}\right)
  \]
- Base price: `$10`
- Simple, interpretable, occupancy-based

### ✅ Model 2: Demand-Based Pricing
- Uses multiple demand drivers:
  - Utilization, Queue Length, Traffic Level, Special Days, Vehicle Type
- Normalized demand score controls price:
  \[
  Price_t = BasePrice \cdot (1 + \lambda \cdot NormalizedDemand)
  \]
- More adaptive and business-aware

---

## 📈 Visualizations

Interactive visualizations created using **Bokeh**:
- % Occupancy per lot over time
- Average hourly occupancy across days
- Dynamic price evolution for each model

All visualizations are available in the notebook and rendered in the report.

---

## 🧪 Installation & Usage

Clone the repository and open the main notebook in Google Colab:

```bash
git clone https://github.com/your-username/urban-parking-pricing.git
