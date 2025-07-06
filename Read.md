# 🚗 Dynamic Pricing for Urban Parking Lots

**Capstone Project – Summer Analytics 2025**  
Hosted by Consulting & Analytics Club × Pathway

---

## 📌 Project Objective

Urban parking spaces are often inefficiently priced due to fixed-rate systems.  
This project builds an intelligent **real-time dynamic pricing system** for 14 parking lots using only Python, NumPy, Pandas, and Bokeh — from scratch — to:

- Maximize lot utilization
- Balance demand during peak hours
- Adapt pricing to traffic, special events, and competition

---

## 🧰 Tech Stack Used

| Tool/Library     | Purpose                          |
|------------------|----------------------------------|
| **Python 3.x**   | Core programming language        |
| **Pandas**       | Data manipulation & preprocessing|
| **NumPy**        | Mathematical operations          |
| **Bokeh**        | Real-time visualization          |
| **Geopy**        | Distance computation (competition model) |
| **(Optional) Pathway** | For streaming (simulated in Colab) |

---

## 🏗️ Architecture Flow

```text
                 +--------------------+
                 |  Input Dataset     | ← CSV with 14 lots × 18 time points
                 +--------------------+
                           ↓
             +--------------------------+
             | Data Preprocessing (Pandas) |
             +--------------------------+
                           ↓
             +--------------------------+
             |  Model 1: Linear Pricing  |
             +--------------------------+
                           ↓
             +--------------------------+
             | Model 2: Demand-Based    |
             +--------------------------+
                           ↓
             +--------------------------+
             | Model 3: Competitive     |
             +--------------------------+
                           ↓
             +--------------------------+
             |  Real-Time Simulation    |
             |  + Bokeh Visualizer      |
             +--------------------------+
                           ↓
                    📊 Pricing Output


📁 dynamic-parking-pricing/
├── images/
│   └── architecture.png  ← Upload architecture diagram here
💡 Models Implemented
🔹 Model 1: Baseline Linear
Price(t+1) = Price(t) + α * (Occupancy / Capacity)

🔹 Model 2: Demand-Based
Weighted function using:

Occupancy

Queue length

Traffic level

Special day

Vehicle type weight

Price = BasePrice * (1 + λ * NormalizedDemand)

🔹 Model 3: Competitive Adjustment
Compares with nearby lots using Lat-Long

Adjusts price based on competition logic

📊 Real-Time Simulation
Simulated using time.sleep() + looped pricing logic

Plotted using Bokeh for each lot

No need for Pathway runtime (Colab-safe)

📁 Repository Structure
vbnet
Copy
Edit
📦 dynamic-pricing-parking/
├── dataset.csv
├── Dynamic_Pricing_for_Urban_Parking_Lots.ipynb
├── README.md
├── images/
│   └── architecture.png (to be added)
└── (Optional) report.pdf
📝 Assumptions
Base price = $10 (bounded between $5 and $20)

Vehicle types affect duration → pricing weight

Traffic and special days directly influence demand

Demand normalization ensures smooth variation

Distance threshold = 1.5 km for competition

✅ Submission Checklist
 📊 All 3 pricing models implemented

 🧠 Demand function + assumptions explained

 📉 Real-time simulation using Bokeh

 📁 Proper repo structure with code + images

 📄 README with tech stack, architecture flow, and diagram

 (Optional) 📃 Report file (if required)




