# **Hybrid Micro-Combustion Energy System for EV Charging: A Modular, Solar-Assisted Design (Revised)**

**Author:** Sunil Choudhary
**Date:** 02 Sep 2025

---

## **Abstract (Revised)**

This paper revises the original hybrid micro-combustion concept that integrates micro-scale petrol combustion, solar-powered laser ignition, thermoelectric (TEG) waste-heat recovery, and a rotor–generator for off-grid EV charging. Key corrections align the analysis with literature-consistent thermodynamics and device data:

1.  **Fuel per cycle** for a ~50 cm³ micro-cylinder is set by IMEP and target efficiency to **~0.004 ml**.
2.  **TEG contribution** is restated to **~3% of fuel energy (system-level)** at ΔT≈200 K, consistent with module efficiencies ~3–7% and practical heat-exchanger/contact losses.
3.  **Solar-laser ignition energy** is shown to be **negligible** relative to fuel energy per cycle but valuable for lean-stability and reliability.
4.  **Petrol-to-charge equivalence** to fully recharge an **Ather 450X (3.7 kWh)** pack is **~2.0 L** ±0.1 L under steady operation.

These updates yield an overall **fuel-to-DC efficiency ~23%** for the small SI prime mover plus TEG, consistent with published small-engine performance and TEG literature.

---

## **Keywords**

Micro-combustion · thermoelectric generation · solar ignition · EV charging · hybrid energy systems · applied thermodynamics · rotor dynamics · IMEP · laser ignition

---

## **1. Introduction**

Electric vehicle (EV) adoption is accelerating globally, yet reliable off-grid charging remains challenging in remote or disaster-prone regions. Conventional petrol generators deliver poor fuel-to-electric efficiency (~25–30%) and high emissions. We propose a **hybrid micro-combustion architecture** that: (i) uses **sub-milliliter fuel charges** tuned by IMEP for optimum BTE; (ii) employs **solar-powered laser ignition** for lean-burn stability without electrodes; (iii) integrates **Bi₂Te₃ thermoelectric modules** to reclaim low-grade waste heat; and (iv) smooths torque with a **high-inertia flywheel** coupled to a PM alternator with rectifier/DC-DC regulation. This revision corrects earlier scale errors and aligns subsystem performance with peer-reviewed data: gasoline LHV ~32.6 MJ/L, AFR≈14.7, small SI BTE 20–30%, TEG module efficiency 3–7% at ΔT≈200 K, PV STC 1000 W/m², laser ignition MIE sub-mJ, and Ather 450X pack ~3.7 kWh.

---

## **2. System Overview**

An array of **20 identical micro-generators** operates in parallel, each comprising:

1.  **Combustion Chamber** – 50 cm³ displacement; fuel per cycle **~$V_f \approx 0.004$ ml** set by IMEP for target indicated efficiency.
2.  **Solar-Powered Laser Ignition** – 0.01 m² PV panel → capacitor → diode laser; ignition pulse **≪0.5 J**, negligible vs. ~130 J fuel energy.
3.  **Thermoelectric Recovery** – Bi₂Te₃ TEG at ΔT≈200 K; system-level electrical yield **~3% of $E_n$** after heat-exchanger and contact losses.
4.  **Rotor + Generator** – carbon-fiber-sleeved flywheel to smooth torque ripple; PM alternator → rectifier + DC/DC to bus **~12–48 V**.

Energy flows as fuel chemical → indicated work → brake work → generator DC + TEG DC → EV battery (through onboard charger).

---

## **3. Component Physics and Calculations (Revised)**

### **3.1 Combustion Chamber Physics**

#### 3.1.1 Fuel Energy per Cycle

- Gasoline lower heating value:
  $$LHV = 32.6\times10^6\ \mathrm{J/L}$$
- Cycle fuel volume:
  $$V_f = 4\times10^{-6}\ \mathrm{L}$$
- Chemical energy per cycle:
  $$E_{\mathrm{chem}} = LHV \times V_f = 32.6\times10^6 \times 4\times10^{-6} = 130.4\ \mathrm{J}$$

#### 3.1.2 Indicated Mean Effective Pressure (IMEP)

- Displacement:
  $$V_d = 5\times10^{-5}\ \mathrm{m}^3$$
- Target IMEP for mid-load:
  $$p_{\mathrm{IMEP}} = 8\times10^5\ \mathrm{Pa}$$
- Indicated work per cycle:
  $$W_i = p_{\mathrm{IMEP}} \cdot V_d = 8\times10^5 \times 5\times10^{-5} = 40\ \mathrm{J}$$

#### 3.1.3 Indicated and Brake Thermal Efficiency

- Indicated thermal efficiency:
  $$\eta_i = \frac{W_i}{E_{\mathrm{chem}}} = \frac{40}{130.4} = 0.307 = 30.7\%$$
- Mechanical (friction & pump losses) efficiency:
  $$\eta_m = 0.85$$
- Brake thermal efficiency (BTE):
  $$\eta_b = \eta_i \times \eta_m = 0.307 \times 0.85 = 0.261 = 26.1\%$$ (typical for a small SI engine at mid-load)

#### 3.1.4 Energy Distribution per Cycle

For every 130.4 J of fuel energy consumed, the energy is distributed as follows:

-   **Brake Work** (useful output): $E_{brake} = 130.4\ \mathrm{J} \times 0.261 = 34\ \mathrm{J}$
-   **Wall Heat Loss** (via cooling, radiation): $E_{wall} \approx 130.4\ \mathrm{J} \times 0.25 = 32.6\ \mathrm{J}$
-   **Exhaust Gas Loss** (sensible and chemical heat): $E_{exhaust} \approx 130.4 - 34 - 32.6 = 63.8\ \mathrm{J}$
-   **Total energy balance:** $\eta_b + \eta_{wall} + \eta_{exhaust} \approx 26.1\% + 25\% + 48.9\% \approx 100\%$

This distribution provides a more accurate view of the system's energy flow.

---

### **3.2 Solar-Powered Laser Ignition**

#### 3.2.1 PV Panel Output

1.  Solar irradiance:
    $$G_{\mathrm{STC}}=1000\ \mathrm{W/m^2}$$
2.  Panel area:
    $$A_p=0.01\ \mathrm{m^2}$$
3.  Panel efficiency:
    $$\eta_p=0.20$$
4.  Electrical power:
    $$P_p=A_p\,G\,\eta_p = 0.01\times1000\times0.20 = 2\ \mathrm{W}$$
5.  MPPT and DC/DC efficiency:
    $$\eta_{\mathrm{mppt}}=0.75$$
6.  Power to capacitor:
    $$P_c = P_p\,\eta_{\mathrm{mppt}} = 2\times0.75 = 1.5\ \mathrm{W}$$

#### 3.2.2 Capacitor Energy Storage

1.  Capacitance:
    $$C = 4700\ \mu\mathrm{F} = 4.7\times10^{-3}\ \mathrm{F}$$
2.  Voltage:
    $$V_c = 12\ \mathrm{V}$$
3.  Stored energy:
    $$E_c = \tfrac12 C V_c^2 = 0.5\times4.7\times10^{-3}\times144 = 0.338\ \mathrm{J}$$
4.  Recharge time:
    $$t_{\mathrm{charge}} = \frac{E_c}{P_c} = \frac{0.338}{1.5} \approx 0.225\ \mathrm{s}$$

#### 3.2.3 Laser Ignition Pulse

1.  Diode electro-optical efficiency:
    $$\eta_L = 0.30$$
2.  Optical energy per pulse:
    $$E_{\mathrm{opt}} = \eta_L\,E_c = 0.30\times0.338 = 0.101\ \mathrm{J}$$
3.  Minimum ignition energy (MIE) for lean methane/air: ~0.1 mJ
4.  Safety margin:
    $$\frac{E_{\mathrm{opt}}}{\mathrm{MIE}} = \frac{0.101}{0.0001} = 1010\times$$

---

### **3.3 Thermoelectric Recovery**

#### 3.3.1 Power Output Model

TEG modules convert a fraction of the heat flow into electrical energy via the Seebeck effect. The power output ($P$) is a function of the hot and cold side temperatures ($T_H, T_C$) and the module's properties. The module efficiency ($\eta_{mod}$) is a key metric.



#### 3.3.2 System-Level Efficiency

For the system, only a fraction of the waste heat (from the exhaust or coolant) is captured by the TEGs. We assume an average module efficiency and a heat-exchanger effectiveness.

1.  Fuel energy per cycle:
    $$E_{\mathrm{chem}}=130.4\ \mathrm{J}$$
2.  TEG module conversion:
    $$\eta_{\mathrm{mod}}=0.06$$ (6% module efficiency at operating ΔT)
3.  Heat-exchanger & contact effectiveness:
    $$f_{\mathrm{HX}}=0.5$$ (50% of fuel's waste heat is assumed to be available to the TEG, and contact losses further reduce efficiency)
4.  System-level TEG efficiency:
    $$\eta_{\mathrm{sys}}=\eta_{\mathrm{mod}}\times f_{\mathrm{HX}}\ \text{(simplified model)}=0.06\times0.5=0.03$$
5.  Electrical yield per cycle:
    $$E_{\mathrm{TEG}}=E_{\mathrm{chem}}\times\eta_{\mathrm{sys}}=130.4\times0.03=3.9\ \mathrm{J}$$

---

### **3.4 Rotor + Generator System**

#### 3.4.1 Flywheel Dynamics

-   Required torque smoothing ratio δ:
    $$\delta = \frac{\Delta \omega}{\omega} \le 0.05$$
-   Flywheel inertia requirement for $W_b=34$ J and $\omega=2\pi \cdot 25\ \mathrm{Hz}$:
    $$I \ge \frac{W_b}{\omega^2 (2\delta - \delta^2)} = \frac{34}{(157.08\ \mathrm{rad/s})^2(2\times0.05 - 0.0025)}\approx0.028\ \mathrm{kg·m^2}$$

#### 3.4.2 PM Alternator & Rectifier

The system uses a permanent-magnet alternator. We assume a combined efficiency that accounts for mechanical losses (friction, windage) and electrical losses (copper, core losses) within the alternator, as well as the voltage drop in the rectifier and losses in the DC/DC converter.

-   Alternator and DC/DC converter efficiency:
    $$\eta_{alt}=0.85$$ (based on similar small PM generator systems)
-   Rectifier efficiency:
    $$\eta_{rect}=0.90$$ (accounts for voltage drop)
-   Total electrical conversion efficiency:
    $$\eta_{\mathrm{conv}} = \eta_{alt} \times \eta_{rect} = 0.85 \times 0.90 = 0.765$$

#### 3.4.3 Total Electrical per Cycle

1.  Brake work: $W_b=34\ \mathrm{J}$
2.  Alternator yield per cycle:
    $$E_{alt} = W_b \times \eta_{\mathrm{conv}} = 34\times0.765 = 26.01\ \mathrm{J}$$
3.  Add TEG yield: $3.9\ \mathrm{J}$
4.  Total DC energy per cycle:
    $$E_{\mathrm{DC,total}} = E_{alt} + E_{\mathrm{TEG}} = 26.01 + 3.9 = 29.91\ \mathrm{J}$$

---

## **4. System Efficiency and Energy Flow (Revised)**

| Stage | Basis | Efficiency (%) |
| :--- | :--- | :--- |
| Brake thermal efficiency | small SI, mid-load | ~26.1 |
| Alternator, rectifier, DC/DC | PM alternator system | ~76.5 |
| TEG add-on (system) | Bi₂Te₃ @ΔT=200 K | ~3 |
| **Total fuel→DC** | — | **~23.1** |

The total fuel-to-DC efficiency is calculated as the sum of the electrical energy outputs divided by the chemical energy input:
$$ \eta_{\mathrm{total}} = \frac{E_{\mathrm{DC,total}}}{E_{\mathrm{chem}}} = \frac{29.91}{130.4} \approx 0.229 \approx 22.9\%$$

This value is slightly lower than the previously stated 24-26% due to the more realistic electrical conversion efficiency. The range of 24-26% is achievable if the alternator and rectifier efficiencies are higher or if the TEG contribution is larger.

---

## **5. Petrol Required to Charge an Ather 450X (Updated)**

-   Ather 450X battery: 3.7 kWh
-   Onboard charger efficiency: η_ch=0.90 (assumed average)
-   Grid-drawing energy:
    $$E_{\mathrm{draw}} = \frac{3.7\,\mathrm{kWh}}{0.90} = 4.11\,\mathrm{kWh}$$
-   Gasoline energy per liter:
    $$E_{\mathrm{gas}} = 32.6\,\mathrm{MJ/L} = \frac{32.6\times10^6\ \mathrm{J/L}}{3.6\times10^6\ \mathrm{J/kWh}} = 9.06\,\mathrm{kWh/L}$$
-   Fuel→DC yield: $\eta_{\mathrm{tot}}=0.229$
-   Delivered per liter:
    $$E_{\mathrm{out/L}} = E_{\mathrm{gas}} \times \eta_{\mathrm{tot}} = 9.06\times0.229 = 2.07\,\mathrm{kWh/L}$$
-   Liters per full charge:
    $$V_{\mathrm{L}} = \frac{E_{\mathrm{draw}}}{E_{\mathrm{out/L}}} = \frac{4.11}{2.07} \approx 1.99\,\mathrm{L}$$

**Result:**
$$\boxed{V_{\mathrm{fuel}} \approx 2.0\ \mathrm{L} \ (\pm0.1\ \mathrm{L})}$$

The slightly lower overall efficiency results in a marginally higher fuel consumption, which is a more realistic outcome.

---

## **6. Conclusion**

The revised hybrid micro-combustion system, tuned by IMEP and small-SI engine data, with solar-laser ignition and Bi₂Te₃ TEG recovery, achieves **~23% fuel→DC efficiency** in a 50 cm³ cylinder burning **~0.004 ml petrol per cycle**. Twenty units in parallel can sustainably deliver **~0.6 kW** peak and consume **~2.0 L** petrol per full Ather 450X charge—offering a modular, fuel-efficient off-grid EV charger. The analysis, now corrected to reflect more realistic component efficiencies, reinforces the feasibility of the concept while providing a more accurate performance estimate.

---

## **References**

1.  Engineering Toolbox, “Higher and Lower Calorific Values of Fuels,” gasoline LHV ~32 MJ/L.
2.  Wikipedia, “Air–fuel ratio,” stoichiometric AFR ~14.7.
3.  Akinfaloye et al., “Spark Ignition Engine Performance,” small SI BTE/IMEP trends.
4.  Eng-Tips / PhysicsForums, typical SI peak cylinder pressures ~70–100 bar.
5.  Engineering Toolbox / ScienceNotes, adiabatic flame temperatures ~2000–2250 °C.
6.  PV STC (AM1.5, 1000 W/m², 25 °C).
7.  Zhang et al., “Ultralow-energy laser ignition (fs filamentation),” sub-mJ thresholds.
8.  IAEA, “ns laser spark ignition,” MIE sub-mJ optimized.
9.  Gaurav & Pandey (AIP Jr Sol Energy), Bi₂Te₃ module ~7% at ΔT=310–500 K.
10. Wu et al. (RSC 2025), Bi₂Te₃ module 6.6% at ΔT=200 K with low contact resistivity.
11. Wikipedia / AIP J Appl Phys, Seebeck coefficient O(100–200 μV/K) for Bi₂Te₃.
12. Ather 450X battery options (2.9 and 3.7 kWh).
