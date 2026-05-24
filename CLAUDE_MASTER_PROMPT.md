# HYDROS Master Context Prompt for Claude

**Use this prompt at the start of any Claude conversation to give it complete project context instantly.**

---

## COPY EVERYTHING BELOW THIS LINE AND PASTE INTO CLAUDE

```
You are assisting with HYDROS, a complete engineering project 
for an underwater life support station.

PROJECT OVERVIEW:
HYDROS (Hyperbaric Underwater Dissolved Oxygen Respirant Station) is a 
fixed-depth underwater life support system that extracts dissolved oxygen 
directly from seawater and supplies it continuously to six divers at 20m 
depth without requiring compressed gas tanks.

TEAM:
Famaran, Ryan Andrei F. | Cordova, Sean Jhaydele H. | 
Manabat, John Ivan C. | Ancheta, Mackenzie N.
NEMO Labs, May 2026

---

SYSTEM SPECIFICATIONS:

Operating Depth: 20 metres
Hydrostatic Pressure: 201,105 Pa (2.0 atm)
Dissolved O2 at depth: 7.2 mg/L
Divers supported: 6
Total station mass: 2,346 kg

KEY COMPONENTS:

1. FRAME (White) — ASTM A36 steel cage, 4.0 x 3.0 x 2.0 m
   Safety factor: 3.32 (exceeds ASME minimum 3.0)

2. TURBINES (Cyan) — 3x axial flow turbines
   Span: 760mm, Pitch: 25°
   Flow rate: 109,800 L/min
   Reynolds number: 1,006,500 (turbulent regime)
   Hydraulic safety margin: 73x

3. MEMBRANE VESSEL (Yellow) — Polysulfone hollow-fiber
   Surface area: 3.47 m²
   Dimensions: 700mm OD, 3000mm L
   Extraction efficiency: 20% per pass
   Governing laws: Henry's Law, Fick's First Law

4. CO2 SCRUBBER (Green) — Soda lime scrubber
   Dimensions: 360mm OD, 600mm H
   Chemistry: Ca(OH)2 + CO2 → CaCO3 + H2O
   Duration: 48.5 hours per charge
   Governs: Dalton's Law (pCO2 < 500 Pa)

5. BUFFER TANK (Magenta) — O2 pressure storage
   Dimensions: 360mm OD, 2000mm L
   Volume: 228 litres
   Pressure: 3 atm
   Emergency reserve: 34 minutes for 6 divers

6. MANIFOLD (Red) — 6-diver gas distributor
   Header: 100mm
   Ports: 6x 50mm

7. UMBILICAL HOSES (Blue) — x6 hoses
   Diameter: 50mm OD
   Length: 2400mm each

8. EMERGENCY O2 (Orange) — Backup tanks x2
   Diameter: 160mm OD
   Pressure: 207 bar

9. BUOYANCY SPHERE (Light Blue)
   Diameter: 1700mm
   Net buoyancy: 2,820 N
   Safety factor (mooring cord): 113

---

GAS FLOW PATH:

Seawater IN → [3x Turbines: 109,800 L/min] 
→ [Membrane vessel: 3.47 m² extraction] 
→ [Gas riser pipe] 
→ [CO2 Scrubber: 48.5 hr life] 
→ [Buffer tank: 228 L at 3 atm] 
→ [6-port manifold] 
→ [6x umbilical hoses] → DIVERS BREATHE
→ [CO2 return channel] → back to scrubber

---

GOVERNING LAWS & FORMULAS:

1. HENRY'S LAW: C = kH × P
   Result: 7.2 mg/L dissolved O2 at 20m depth

2. FICK'S FIRST LAW: J = -D × (dC/dx)
   Result: 3.47 m² membrane area required

3. DALTON'S LAW: P_total = P_O2 + P_CO2 + P_N2
   Safety constraint: pCO2 below 500 Pa

4. REYNOLDS NUMBER: Re = ρ × v × D / μ
   Result: Re = 1,006,500 (fully turbulent flow)

5. BETZ'S LAW: P_max = (8/27) × ρ × A × v³
   Theoretical power: 1,251 W
   Practical power: 450-500 W

6. ARCHIMEDES' PRINCIPLE: F_buoyancy = ρ × g × V_displaced
   Result: 2,820 N net upward force

---

SIMULATION VALIDATION:

All simulations completed using SimScale and PhET Interactive.
All results agree with manual calculations within 3.7% deviation.

CFD (SimScale RANS k-ω SST):
- Confirmed Reynolds number: 1,006,500 (2.3% deviation)
- Seawater flow regime validated

FEA (SimScale Linear Static):
- Maximum frame stress: 78.1 MPa (3.7% deviation)
- Safety factor 3.32 confirmed

Gas Properties (PhET):
- pO2 = 42,000 Pa confirmed
- Buoyancy net force = 2,820 N (0.14% deviation)

---

REPOSITORY STRUCTURE:

docs/
├── HYDROS_Complete_PSR_Package.docx
├── HYDROS_Technical_Manual.docx
└── HYDROS_Technical_Calculations.docx

cad/
├── HYDROS_MASTER.dwg
└── drawings/
    ├── A101_Front_Elevation.pdf
    ├── A101_Section_AA.pdf
    └── A101_Manifold_Detail.pdf

simulation/
├── SimScale_CFD/
├── SimScale_FEA/
└── PhET_screenshots/

calculations/
└── computation_sheet.pdf

README.md

---

KEY REFERENCES:

1. Ahmed et al. (2004) — Oxygen transfer characteristics of hollow-fiber 
   composite membranes. *Advances in Environmental Research.*

2. Betz, A. (1926) — Wind-energie und ihre Ausnutzung durch Windmühlen.

3. Garcia & Gordon (1992) — Oxygen solubility in seawater. 
   *Limnology and Oceanography.*

4. Lee et al. (2018) — Theoretical model for underwater oxygen extraction. 
   *Scientific Reports.*

5. Lim et al. (2020) — CO2 absorbents in closed-circuit diving rebreathers. 
   *Diving and Hyperbaric Medicine.*

6. Merckelbach et al. (2025) — Artificial gill membranes for underwater 
   fuel cells. *Advanced Science.*

7. Pleil et al. (2021) — The physics of human breathing. 
   *Journal of Breath Research.*

8. Sander (2023) — Henry's law constants for water as solvent. 
   *Atmospheric Chemistry and Physics.*

9. White (2011) — *Fluid Mechanics, 7th Edition.* McGraw-Hill.

10. ASME (2019) — *Boiler and Pressure Vessel Code Section VIII.*

11. WHOI (2010) — *Mooring Systems Engineering Guide.*

---

DESIGN QUALITY ASSURANCE CHECKLIST (PSR):

✅ All 9 component layers modeled and dimensioned
✅ All 6 governing laws applied and validated
✅ All calculations documented with working shown
✅ CFD simulation confirms flow regime
✅ FEA simulation confirms frame integrity
✅ PhET simulation confirms buoyancy and gas properties
✅ Frame safety factor 3.32 exceeds ASME minimum 3.0
✅ CO2 scrubber duration 48.5 hours (adequate)
✅ Emergency O2 reserve 34 minutes for 6 divers
✅ Hydraulic safety margin 73x (excellent redundancy)
✅ All references cited and verified
✅ Repository documented with README, CAD, and simulation outputs

---

When I ask you about HYDROS, you now have complete context about:
- Every component, dimension, and specification
- All calculations and governing laws
- Simulation results and validation
- Repository structure and files
- Design iterations and team members
- All technical references

You can now assist with analysis, documentation, troubleshooting, 
calculations, design review, or any engineering questions about the project.
```

---

**How to Use:**
1. Copy the entire section marked "COPY EVERYTHING BELOW THIS LINE"
2. In any Claude conversation, paste it before asking your question
3. Claude will have instant, complete context about HYDROS
4. No need to re-explain or paste files separately

**Time Saved:** Instead of 10+ messages explaining the project, Claude understands it in one paste.
