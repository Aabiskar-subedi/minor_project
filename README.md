# 📡 Cable Fault Detection System using Time Domain Reflectometry (TDR)

A low-cost, educational **Time Domain Reflectometry (TDR)** based system to detect and locate faults in underground coaxial cables. This project demonstrates how short-duration electrical pulses and reflected signals can be used to identify **open-circuit and short-circuit faults** and estimate their distance accurately.

🎓 **Minor Project – Electronics Engineering**  
🏫 **Kantipur Engineering College (Affiliated to Tribhuvan University)**

---

##  Project Overview

Underground cable fault detection is difficult due to buried infrastructure and the need for manual excavation. Traditional methods are slow, costly, and inefficient.

This project implements a **TDR-based fault detection system** using:

- A **NE555 timer** to generate fast pulses  
- **Signal reflection analysis** to detect impedance discontinuities  
- **NodeMCU (ESP8266)** for processing and display  
- **Analog signal conditioning** using **LM358** and **Schmitt trigger**

The system is designed for **academic, laboratory, and small-scale practical applications** with cable lengths up to **~100 meters**.

---

##  Objectives

- Design a low-cost and reliable underground cable fault detection system  
- Detect open-circuit and short-circuit faults  
- Calculate fault distance using TDR principles  
- Display results on a local OLED display  
- Demonstrate TDR behavior using standard lab instruments (oscilloscope)

---

##  Key Features

-  Pulse generation using **NE555 timer (monostable mode)**
-  Fault detection using signal reflection
-  Distance calculation using TDR equation
-  Real-time fault distance display on OLED
-  Uses easily available and affordable components
-  Suitable for educational demonstrations and labs

---

##  Working Principle (TDR)

1. A short-duration voltage pulse is injected into the cable.  
2. The pulse propagates as a **TEM wave**.  
3. When the pulse encounters an impedance discontinuity, part of it is reflected.  
4. The time delay between transmitted and reflected pulses is measured.  
5. Fault distance is calculated using:

```text
Distance = (Time Delay × Propagation Velocity) / 2
where Propagation velocity ≈ 8.4*3 *10⁸ m/s for rg-6 (75 ohm ) coax cable
```
```text

Cable-Fault-Detection-TDR/
│
├── docs/
│   ├── minor_project_report.pdf      # Complete project report
│   ├── presentation.pptx             # Project presentation slides
│
├── hardware/
│   ├── schematics/                   # Circuit schematics
│   ├── proteus_simulation/           # Proteus design & simulation files
│   └── block_diagram.png             # System block diagram
│
├── firmware/
│   ├── tdr_nodeMCU.ino               # Arduino code for NodeMCU
│   └── libraries/                    # Required Arduino libraries
│
├── results/
│   ├── oscilloscope_waveforms/       # TDR input & reflected waveforms
│   └── screenshots/                 # OLED display & test outputs
│
├── README.md                         # Project documentation
└── LICENSE                           # License information
```

 System Architecture

Main Blocks:

Pulse Generator (NE555)

Schmitt Trigger (74HC14)

Cable Under Test (Coaxial Cable)

Signal Amplifier (LM358)

Processing Unit (NodeMCU ESP8266)

Display Unit (OLED)

- Observation Instrument (Oscilloscope)

---

##  Hardware Components

| Component | Description |
|---------|------------|
| NodeMCU (ESP8266) | Microcontroller & processing |
| NE555 Timer IC | Pulse generation |
| LM358 Op-Amp | Signal amplification |
| 74HC14 | Schmitt trigger |
| 1N4148 Diode | Fast switching & protection |
| OLED Display (I2C) | Fault distance display |
| BNC Connector | High-frequency signal interface |
| Coaxial Cable (75Ω) | Cable under test |
| Power Supply (5V) | System power |

---

##  Software Tools

- **Arduino IDE** – Programming the NodeMCU  
- **Proteus Design Suite** – Circuit simulation and testing  
- **Oscilloscope** – Pulse and reflection observation  



## Cost Estimation
Item	Cost (NPR)
Total Estimated Cost	~ Rs. 4,180

A budget-friendly design suitable for students and labs.

 Applications

Underground cable fault localization

Educational demonstrations of TDR

Power and communication cable diagnostics

Reduced manual digging and downtime

Foundation for future IoT-based monitoring systems

##  References

1. B. Gustavsen *et al*., “High-frequency modeling of underground power cables and the use of TDR for fault location,”  
   *IEEE Transactions on Power Delivery*, vol. 25, no. 3, pp. 1153–1161, Jul. 2010.

2. R. Patel and M. Shah, “IoT-Based Underground Cable Fault Detection Using NodeMCU,”  
   *International Journal of Research in Engineering, Science and Management (IJRESM)*,  
   vol. 4, no. 6, pp. 45–48, Jun. 2021.

3. R. Sharma *et al*., “Advanced Underground Cable Fault Detection Using TDR and Machine Learning,”  
   *IEEE Sensors Letters*, vol. 6, no. 5, pp. 1–4, May 2022.

4. S. Ramharack and S. Bahadoorsingh, “Wavelet Transform Techniques for Step-Pulse TDR in Cable Fault Detection,”  
   *Electric Power Systems Research*, vol. 215, Article no. 108986, 2023.




📄 License

This project is intended for academic and educational use.
Feel free to fork, study, and improve it with proper attribution.

