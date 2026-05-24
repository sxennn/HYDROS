# HYDROS
### Hyperbaric Underwater Dissolved Oxygen Respirant Station
**NEMO Labs — Famaran, Cordova, Manabat, Ancheta — May 2026**

HYDROS is a fixed-depth underwater life support station that extracts dissolved oxygen directly from seawater and supplies it continuously to six divers at 20 metres depth — no compressed gas tanks required.

---

## How It Works

Seawater enters through three axial turbines at 1.5 m/s. A 3.47 m² polysulfone hollow-fiber membrane extracts dissolved oxygen passively using Henry's Law and Fick's Law. Exhaled CO2 is neutralised by a Sodasorb soda lime scrubber in a closed breathing loop. Clean oxygen is stored in a 228-litre buffer tank and distributed to six divers through a manifold and umbilical hoses.

---

## Key Numbers

| Parameter | Value |
|---|---|
| Operating depth | 20 m |
| Hydrostatic pressure | 201,105 Pa (2.0 atm) |
| Dissolved O2 at depth | 7.2 mg/L |
| Membrane surface area | 3.47 m² |
| Extraction efficiency | 20% per pass |
| Seawater flow minimum | 1,493 L/min |
| Seawater flow actual | 109,800 L/min |
| Hydraulic safety margin | 73x |
| Reynolds number | 1,006,500 |
| Turbine power Betz | 1,251 W |
| Turbine power practical | 450-500 W |
| Frame safety factor | 3.32 |
| CO2 scrubber duration | 48.5 hours |
| Emergency O2 reserve | 34 minutes for 6 divers |
| Total station mass | 2,346 kg |

---

## 9 Model Layers

| Layer | Colour | Component | Dimensions |
|---|---|---|---|
| FRAME | White | ASTM A36 steel cage | 4.0 x 3.0 x 2.0 m |
| MEMBRANE | Yellow | Polysulfone hollow-fiber vessel | 700mm OD, 3000mm L |
| SCRUBBER | Green | CO2 soda lime scrubber | 360mm OD, 600mm H |
| BUFFER | Magenta | O2 pressure buffer tank | 360mm OD, 2000mm L |
| MANIFOLD | Red | 6-diver gas distributor | 100mm header, 6x 50mm ports |
| HOSE | Blue | Umbilical hoses x6 | 50mm OD, 2400mm each |
| TURBINE | Cyan | Axial flow turbines x3 | 760mm span, 25 degree pitch |
| EMERGENCY | Orange | Backup O2 tanks x2 | 160mm OD, 207 bar |
| BALLOON | Light Blue | Buoyancy sphere | 1700mm diameter |

---

## Gas Flow Path

```
SEAWATER IN
    |
[3x TURBINES] — 109,800 L/min — Re = 1,006,500
    |
[MEMBRANE VESSEL] — 3.47 m² polysulfone — 20% O2 extracted
    |
[GAS RISER PIPE]
    |
[CO2 SCRUBBER] — Ca(OH)2 + CO2 → CaCO3 + H2O — 48.5 hr life
    |
[BUFFER TANK] — 228 L at 3 atm
    |
[6-PORT MANIFOLD]
    |
[6x UMBILICAL HOSES] → DIVERS BREATHE
    |
[CO2 RETURN CHANNEL] → back to scrubber
```

---

## Governing Laws

| Law | Governs | Key Result |
|---|---|---|
| Henry's Law | Dissolved O2 concentration | 7.2 mg/L at 20 m |
| Fick's First Law | O2 flux through membrane | 3.47 m² area required |
| Dalton's Law | CO2 partial pressure safety | pCO2 below 500 Pa |
| Reynolds Number | Flow regime | Re = 1,006,500 turbulent |
| Betz's Law | Turbine power | 1,251 W theoretical |
| Archimedes' Principle | Buoyancy mooring | SF cord = 113 |

---

## Simulation and Validation

| Simulation | Tool | Result | vs Manual Calc |
|---|---|---|---|
| CFD seawater flow | SimScale RANS k-ω SST | Re confirmed 1,006,500 | 2.3% deviation |
| FEA frame stress | SimScale linear static | Max stress 78.1 MPa | 3.7% deviation |
| Gas properties | PhET | pO2 = 42,000 Pa confirmed | visual match |
| Buoyancy | PhET | Net upward = 2,820 N | 0.14% deviation |

All simulations agree with manual calculations within 3.7%.

---

## Repository Structure

```
HYDROS/
├── docs/
│   ├── HYDROS_Complete_PSR_Package.docx
│   ├── HYDROS_Technical_Manual.docx
│   └── HYDROS_Technical_Calculations.docx
├── cad/
│   ├── HYDROS_MASTER.dwg
│   └── drawings/
│       ├── A101_Front_Elevation.pdf
│       ├── A101_Section_AA.pdf
│       └── A101_Manifold_Detail.pdf
├── simulation/
│   ├── SimScale_CFD/
│   ├── SimScale_FEA/
│   └── PhET_screenshots/
├── calculations/
│   └── computation_sheet.pdf
└── README.md
```

---

## References

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
NEMO Labs, May 2026.
