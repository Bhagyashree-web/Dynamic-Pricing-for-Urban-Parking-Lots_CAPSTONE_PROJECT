# 🚗 Dynamic Pricing for Urban Parking Lots

**Capstone Project – Summer Analytics 2025**  
Hosted by Consulting & Analytics Club × Pathway

---

## 📌 Objective

Urban parking spaces are limited and often inefficiently priced. This project develops a real-time **Dynamic Pricing Engine** that adjusts parking prices for 14 lots based on:

- Occupancy levels
- Queue lengths
- Traffic congestion
- Special event days
- Vehicle type
- Competition from nearby lots

---

## 🧠 Models Implemented

### 1. **Baseline Linear Model**
- Simple linear formula:  
  `Price(t+1) = Price(t) + α * (Occupancy / Capacity)`

### 2. **Demand-Based Model**
- Demand = weighted sum of:  
  `Occupancy / Capacity`, `QueueLength`, `TrafficLevel`, `IsSpecialDay`, `VehicleTypeWeight`
- Price = `BasePrice * (1 + λ * NormalizedDemand)`

### 3. **Competitive Model** (Optional)
- Adjusts price based on proximity and pricing of nearby lots using geolocation (lat/long)
- Example logic: If nearby lots are cheaper → decrease price or reroute

---

## 📊 Real-Time Simulation

Since **Pathway** isn't supported in Google Colab, real-time behavior is simulated using:

- `time.sleep()` delays for stream-like updates
- `Bokeh` for live visualization of pricing trends

---

## 📁 Folder Structure
📦 dynamic-parking-pricing/
├── dataset.csv # Sample or real input dataset
├── Dynamic_Pricing.ipynb # Google Colab notebook (main logic)
├── README.md # This file
├── report.pdf # Optional project report with explanation and plots
└── /images # (Optional) Screenshots or visualizations

---

## 📝 Assumptions

- Base price = `$10`, bounded between `$5` and `$20`
- Demand and pricing are smoothed and normalized
- Only `numpy`, `pandas`, and `bokeh` used (no ML libraries)
- Vehicle types affect parking duration and hence pricing logic

---

## 📦 Technologies Used

| Component         | Library     |
|------------------|-------------|
| Data Processing   | `pandas`, `numpy` |
| Visualization     | `bokeh` |
| Geospatial Logic  | `geopy` |
| Real-Time Sim     | `time.sleep()` |
| Streaming (Alt)   | `pathway` *(recommended for deployment, simulated here)* |

---

## 📈 Sample Visualization

![Bokeh Visualization](images/sample_pricing_plot.png)

---

## 🧾 License

This project is built as part of the Summer Analytics 2025 Capstone and is for educational use only.

---

## ✅ Final Deliverables

- ✔️ `Dynamic Pricing for Urban Parking Lots.ipynb` (https://colab.research.google.com/drive/1nGbMcQ_3kFoBA1IgEkketV4uPRDkDXm-#scrollTo=5qEB6IreHKDP)
- ✔️ All models implemented from scratch
- ✔️ Real-time pricing simulation
- ✔️ Bokeh visualization
- ✔️ Demand logic, assumptions, and competition modeled

> 🎯 Ready for submission or deployment!

