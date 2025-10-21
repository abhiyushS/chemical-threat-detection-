CBRN Threat Detection & Evacuation Modeling System
📘 Overview

This project models and simulates chemical threat detection and evacuation planning for CBRN (Chemical, Biological, Radiological, and Nuclear) emergencies.

Developed as part of an AI Research Internship at DRDO–INMAS, this simulation generates synthetic data for multiple hazardous chemicals, models exposure risks, and visualizes plume spread, toxicity levels, and evacuation timelines to support emergency response and training operations.

🧩 Key Features

✅ Chemical Threat Simulation

Models events for multiple agents (Ammonia, Sarin, Mustard Gas, Glyphosate, etc.).

Computes LD₅₀, LC₅₀, IC₅₀ values, vapor pressure, and toxicity parameters.

✅ Dynamic Risk Classification

Uses probabilistic modeling to classify threats as Low, Medium, or High.

✅ Evacuation Path Modeling

Estimates exposure duration and evacuation times based on chemical volatility and affected area radius.

✅ Synthetic Data Generation

Produces large-scale, randomized datasets for training ML models and visual simulations.

✅ Visual Analytics

Generates dynamic plots for risk probability, chemical concentration, and distance vs exposure using Matplotlib.

                  ┌────────────────────────┐
                  │   Input Parameters      │
                  │  (Chemicals, Dates)     │
                  └──────────┬──────────────┘
                             │
                             ▼
              ┌───────────────────────────────┐
              │  Threat Simulation Engine      │
              │  • Random event generation     │
              │  • Toxicity & risk computation │
              └──────────┬─────────────────────┘
                         │
                         ▼
        ┌──────────────────────────────────┐
        │  Exposure & Evacuation Modeling   │
        │  • Time-series exposure curves    │
        │  • Evacuation time estimation     │
        └──────────┬────────────────────────┘
                   │
                   ▼
         ┌────────────────────────────┐
         │ Visualization & Analytics  │
         │ • Matplotlib-based charts  │
         │ • Risk heatmaps (future)   │
         └──────────┬─────────────────┘
                    │
                    ▼
           ┌────────────────────┐
           │ Output (CSV, PNGs) │
           │ Simulation results │
           └────────────────────┘

⚙️ Tech Stack
Component	Description
Language	Python 3
Libraries	NumPy, Pandas, Matplotlib, UUID, Datetime, Random
Output	CSV dataset, plots (PNG/Matplotlib)
Future Expansion	GeoPandas, Folium, scikit-learn

🧪 How It Works
🧬 1. Chemical Dataset Initialization

Each agent has predefined toxicity constants and environmental parameters (e.g., LD₅₀, LC₅₀, IC₅₀, vapor pressure).

🧾 2. Event Simulation

Randomized CBRN threat events are generated using custom date and exposure functions to simulate temporal and spatial variability.

⚗️ 3. Threat Computation

Exposure index is calculated as:

Exposure Index
=
𝑓
(
Toxicity
×
Concentration
×
Volatility
)

Exposure Index=f(Toxicity×Concentration×Volatility)

This helps classify each event into Low, Medium, or High threat categories.

🚨 4. Evacuation Modeling

Time–distance–exposure relationships are modeled to estimate safe evacuation windows and the severity of population exposure during chemical dispersion.

📊 5. Visualization

Automatically generates risk probability curves, exposure severity distributions, and chemical concentration–time plots using Matplotlib.



🧰 Setup & Usage
Installation
git clone https://github.com/<your-username>/CBRN-Threat-Detection.git
cd CBRN-Threat-Detection
pip install numpy pandas matplotlib

Run the Simulation
python model3.py

Outputs

simulation_output.csv → contains event data.

Plots → show risk distributions and evacuation trends.







🧑‍💻 Author

Abhiyush Satyam
AI Research Intern, DRDO – INMAS
📧 abhiyushsatyam@gmail.com

🔗 LinkedIn


