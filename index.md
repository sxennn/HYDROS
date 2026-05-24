---
layout: default
title: HYDROS – Underwater Life Support Station
description: Self-sustaining underwater oxygen extraction system for 6 divers at 20m depth
---

# HYDROS
## Hyperbaric Underwater Dissolved Oxygen Respirant Station

**NEMO Labs — Famaran, Cordova, Manabat, Ancheta — May 2026**

![HYDROS System](assets/hydros-banner.png)

---

## Revolutionary Underwater Engineering

HYDROS is a fixed-depth underwater life support station that extracts dissolved oxygen directly from seawater and supplies it continuously to six divers at 20 metres depth — **no compressed gas tanks required**.

### The Problem Solved
- ❌ Divers dependent on heavy compressed air tanks
- ❌ Limited bottom time due to tank capacity
- ❌ Complex decompression procedures
- ❌ Risk of nitrogen narcosis at depth

### The HYDROS Solution
- ✅ Continuous oxygen extraction from surrounding seawater
- ✅ Unlimited bottom time (subject to CO2 scrubber life)
- ✅ Closed-loop breathing system
- ✅ Passive membrane extraction (Henry's Law)
- ✅ Buoyancy-stable deployment

---

## How It Works

Seawater enters through **three axial turbines** at 1.5 m/s, powering the system passively. A **3.47 m² polysulfone hollow-fiber membrane** extracts dissolved oxygen using Henry's Law and Fick's Law. Exhaled CO2 is neutralised by a **Sodasorb soda lime scrubber** in a closed breathing loop. Clean oxygen is stored in a **228-litre buffer tank** and distributed to six divers through a **manifold** and **umbilical hoses**.

### Gas Flow Path
```
SEAWATER IN
    ↓
[3x TURBINES] — 109,800 L/min — Re = 1,006,500
    ↓
[MEMBRANE VESSEL] — 3.47 m² polysulfone — 20% O2 extracted
    ↓
[CO2 SCRUBBER] — 48.5 hour life
    ↓
[BUFFER TANK] — 228 L at 3 atm
    ↓
[6-PORT MANIFOLD]
    ↓
[6x UMBILICAL HOSES] → DIVERS BREATHE
```

---

## The 9 Component Layers

| Layer | Component | Colour | Dimensions |
|---|---|---|---|
| **FRAME** | ASTM A36 steel cage | White | 4.0 × 3.0 × 2.0 m |
| **MEMBRANE** | Polysulfone hollow-fiber vessel | Yellow | 700mm OD × 3000mm L |
| **SCRUBBER** | CO2 soda lime scrubber | Green | 360mm OD × 600mm H |
| **BUFFER** | O2 pressure buffer tank | Magenta | 360mm OD × 2000mm L |
| **MANIFOLD** | 6-diver gas distributor | Red | 100mm header × 6×50mm ports |
| **HOSE** | Umbilical hoses (×6) | Blue | 50mm OD × 2400mm each |
| **TURBINE** | Axial flow turbines (×3) | Cyan | 760mm span × 25° pitch |
| **EMERGENCY** | Backup O2 tanks (×2) | Orange | 160mm OD × 207 bar |
| **BALLOON** | Buoyancy sphere | Light Blue | 1700mm diameter |

---

## Key Specifications

| Parameter | Value |
|---|---|
| **Operating Depth** | 20 m |
| **Hydrostatic Pressure** | 201,105 Pa (2.0 atm) |
| **Dissolved O2 at Depth** | 7.2 mg/L |
| **Membrane Surface Area** | 3.47 m² |
| **Extraction Efficiency** | 20% per pass |
| **Seawater Flow (Actual)** | 109,800 L/min |
| **Reynolds Number** | 1,006,500 (turbulent) |
| **Turbine Power (Theoretical)** | 1,251 W (Betz) |
| **Turbine Power (Practical)** | 450–500 W |
| **Frame Safety Factor** | 3.32 (exceeds ASME 3.0) |
| **CO2 Scrubber Duration** | 48.5 hours per charge |
| **Emergency O2 Reserve** | 34 minutes for 6 divers |
| **Total Station Mass** | 2,346 kg |

---

## Governing Physics

Six fundamental laws govern HYDROS operation:

### 1. **Henry's Law** — Oxygen Dissolution
Dissolved O₂ concentration is proportional to partial pressure above seawater.
- **Result:** 7.2 mg/L dissolved O₂ at 20m depth

### 2. **Fick's First Law** — Membrane Diffusion
O₂ flux through the membrane depends on concentration gradient and membrane area.
- **Result:** 3.47 m² membrane area required for extraction

### 3. **Dalton's Law** — Partial Pressure Safety
Total gas pressure equals sum of individual gas partial pressures.
- **Safety Constraint:** pCO₂ below 500 Pa (prevents hypercapnia)

### 4. **Reynolds Number** — Flow Regime
Dimensionless number predicting turbulent vs laminar flow.
- **Result:** Re = 1,006,500 → fully turbulent flow through turbines

### 5. **Betz's Law** — Turbine Power Extraction
Maximum theoretical power from flowing fluid.
- **Result:** 1,251 W theoretical; 450–500 W practical efficiency

### 6. **Archimedes' Principle** — Buoyancy
Buoyant force equals weight of displaced fluid.
- **Result:** 2,820 N net upward force (mooring safety factor 113)

---

## Validation & Simulation

All calculations validated through professional simulation tools:

| Simulation | Tool | Result | Accuracy |
|---|---|---|---|
| **CFD Seawater Flow** | SimScale RANS k-ω SST | Re = 1,006,500 confirmed | ±2.3% |
| **FEA Frame Stress** | SimScale Linear Static | Max stress 78.1 MPa | ±3.7% |
| **Gas Properties** | PhET Interactive | pO₂ = 42,000 Pa | Visual match |
| **Buoyancy** | PhET Interactive | Net force = 2,820 N | ±0.14% |

**Conclusion:** All simulations agree with manual calculations within **3.7%** deviation.

---

## Project Repository

Full technical documentation, CAD files, and simulation outputs available on GitHub:

📁 **[github.com/sxennn/HYDROS](https://github.com/sxennn/HYDROS)**

### Repository Contents
- **docs/** — Complete PSR package, technical manual, calculations
- **cad/** — AutoCAD master file and engineering drawings
- **simulation/** — SimScale CFD/FEA results and PhET outputs
- **calculations/** — Detailed computation sheet with working

---

## The Team

**NEMO Labs — May 2026**

- **Famaran, Ryan Andrei F.** — Lead Systems Engineer
- **Cordova, Sean Jhaydele H.** — Hydraulics & Turbine Design
- **Manabat, John Ivan C.** — Membrane Systems & Gas Chemistry
- **Ancheta, Mackenzie N.** — Structural Analysis & Safety

---

## Academic References

1. Ahmed et al. (2004). Oxygen transfer characteristics of hollow-fiber composite membranes. *Advances in Environmental Research.*
2. Betz, A. (1926). *Wind-energie und ihre Ausnutzung durch Windmühlen.*
3. Garcia & Gordon (1992). Oxygen solubility in seawater. *Limnology and Oceanography.*
4. Lee et al. (2018). Theoretical model for underwater oxygen extraction. *Scientific Reports.*
5. Lim et al. (2020). CO2 absorbents in closed-circuit diving rebreathers. *Diving and Hyperbaric Medicine.*
6. Merckelbach et al. (2025). Artificial gill membranes for underwater fuel cells. *Advanced Science.*
7. Pleil et al. (2021). The physics of human breathing. *Journal of Breath Research.*
8. Sander (2023). Henry's law constants for water as solvent. *Atmospheric Chemistry and Physics.*
9. White (2011). *Fluid Mechanics, 7th Edition.* McGraw-Hill.
10. ASME (2019). *Boiler and Pressure Vessel Code Section VIII.*
11. WHOI (2010). *Mooring Systems Engineering Guide.*

---

## License

Academic and research use only. Non-commercial education license.

**NEMO Labs, May 2026**
