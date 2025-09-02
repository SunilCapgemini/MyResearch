# **Hybrid Micro‑Combustion Energy System for EV Charging: A Modular, Solar‑Assisted Design (Revised)**

**Author:** Sunil Choudhary  
**Date:** 02 Sep 2025

---

## **Abstract (Revised)**
This paper revises the original hybrid micro‑combustion concept that integrates micro‑scale petrol combustion, solar‑powered laser ignition, thermoelectric (TEG) waste‑heat recovery, and a rotor–generator for off‑grid EV charging. Key corrections align the analysis with literature‑consistent thermodynamics and device data: (i) the **fuel per cycle** for a ~50 cm³ micro‑cylinder is set by IMEP and target efficiency to **~0.003–0.005 ml**, not 0.2 ml; (ii) **TEG contribution** is restated to **~2–4% of fuel energy (system‑level)** at ΔT≈200 K, consistent with module efficiencies ~3–7% and practical heat‑exchanger/contact losses; (iii) the **solar‑laser ignition energy** is shown to be **negligible** relative to fuel energy per cycle but valuable for lean‑stability and reliability; and (iv) the **petrol‑to‑charge equivalence** to fully recharge an **Ather 450X (3.7 kWh)** pack is **~1.8 L** ±0.1 L under steady operation. These updates yield an overall **fuel‑to‑DC efficiency ~24–26%** for the small SI prime mover plus TEG, consistent with published small‑engine performance and TEG literature.  
**Sources:** heating value and AFR for gasoline; SI engine BTE/IMEP ranges; adiabatic flame temperatures; TEG efficiencies at ΔT≈200 K; PV STC; laser ignition minimum energy; Ather 450X capacity; onboard charger efficiency. [1–12]

---

## **Keywords**
Micro‑combustion, thermoelectric generation, solar ignition, EV charging, hybrid energy systems, applied thermodynamics, rotor dynamics, IMEP, laser ignition.

---

## **1. Introduction**
As EV adoption grows, compact, fuel‑efficient off‑grid chargers remain relevant for remote and resilience use‑cases. Conventional petrol generators sacrifice efficiency and emissions. We revisit a **hybrid micro‑combustion architecture** that uses **solar‑powered laser ignition** for precise, electrode‑less ignition and a **Bi₂Te₃ TEG** to reclaim a portion of waste heat, all coupled to a high‑inertia rotor and PM alternator. The present revision corrects energetic inconsistencies and grounds subsystem performance in published data: **gasoline LHV ~32 MJ/L** (from ~42–46 MJ/kg and ρ≈0.74 kg/L), **AFR≈14.7**, **SI BTE typically 20–30% (up to ~41% research)**, **TEG module ~3–7% at ΔT≈200 K**, **PV STC 1000 W/m²** and **laser MIE sub‑mJ** in optimized regimes. [1–8]

---

## **2. System Overview**
The system comprises an array of **20 parallel micro‑generators**. Each micro‑generator contains:
1. **Combustion Chamber** – hardened steel liner, **~50 cm³** displacement (nominal), stoichiometric or mildly‑lean operation; **fuel per cycle ~0.003–0.005 ml** set by IMEP and target indicated efficiency (Section 3.1).  
2. **Solar‑Powered Laser Ignition** – a **small PV panel** charges a capacitor that drives a laser ignition module; ignition energy is **≪ fuel energy per cycle** (Section 3.2).  
3. **Thermoelectric Recovery** – **Bi₂Te₃ TEG** at **ΔT≈200 K** delivering **~2–4% of fuel energy** as electricity **at the system level**, after HX and interface losses (Section 3.3).  
4. **Rotor + Generator** – carbon‑fiber‑sleeved flywheel smooths torque ripple; **PM alternator** with rectifier and DC/DC provides regulated DC (Section 3.4).

---

## **3. Component Physics and Calculations (Revised)**

### **3.1 Combustion Chamber Physics**

#### 3.1.1 Fuel energy per cycle (literature‑consistent)
Take **gasoline LHV ≈ 32.6 MJ/L** (from ~45–46 MJ/kg, ρ≈0.74 kg/L). For a representative **fuel per cycle** 
$$V_f = 0.004\,\text{ml} = 4\times10^{-6}\,\text{L}$$
$$E_{\text{chem,cycle}} = 32.6\times10^6\,\frac{\text{J}}{\text{L}} \times 4\times10^{-6}\,\text{L} \approx 130\,\text{J}.$$
**AFR (stoich)** ≈ 14.7:1 → mass flows scale accordingly. [1,2]

#### 3.1.2 IMEP‑based work and consistency
Indicated work per cycle for a cylinder of volume $$V_d$$ is
$$W_i = \text{IMEP}\cdot V_d.$$
For **$$V_d = 50\,\text{cm}^3 = 5\times10^{-5}\,\text{m}^3$$** and a mid‑load **IMEP ≈ 8 bar (8×10⁵ Pa)**, 
$$W_i \approx 40\,\text{J}$$. With **indicated efficiency** $$\eta_i\approx0.35$$ (SI, well‑phased), the required fuel is $$E_f=W_i/\eta_i\approx 114\,\text{J}\Rightarrow V_f\approx 3.5\,\mu\text{L}$$, which sits inside the **0.003–0.005 ml** range used above. This reconciles work with realistic **peak cylinder pressures ~70–100 bar** and observed BMEP. [3,4]

#### 3.1.3 Adiabatic flame temperature and heat loss bounds
Adiabatic flame temperature for gasoline‑air in air is **~2130–2250 °C** at stoich (constant‑pressure tables), reducing with excess air; in‑cylinder temperatures are further lowered by heat loss and dissociation. Wall heat losses in small SI engines are typically **~20–30%** of fuel energy, consistent with BTE ranges used later. [5,3]

#### 3.1.4 Work output and power scaling
Brake work per cycle $$W_b\approx 0.85 W_i\approx 34\,\text{J}$$ assuming mechanical efficiency 85%. Electrical conversion in the alternator–rectifier at ~90% yields **~31 J electrical per cycle** on the mechanical path. At **3000 rpm** (4‑stroke, 1 power stroke per 2 revs) → **25 power strokes/s** per cylinder → **~0.78 kW**/micro‑generator (mechanical path) plus TEG (Section 3.3). The exact number depends on phasing and losses; this order of magnitude matches small SI engine power densities. [3]

---

### **3.2 Solar‑Powered Laser Ignition**

#### 3.2.1 PV and storage
At STC (**1000 W/m², AM1.5, 25 °C**) a **0.01 m²** panel at **η≈20%** gives **2 W**; with MPPT/DC wiring, assume **~75%** to the capacitor → **1.5 W**. Charging a **4700 µF** capacitor to **12 V** stores **~0.338 J**; recharge time in sun is **~0.23–0.5 s** including control overhead. [6]

#### 3.2.2 Laser energy vs MIE
With ~30% electro‑optical efficiency in a diode/optics chain, an optical pulse **~0.10 J** is available—orders of magnitude above **sub‑mJ** **minimum ignition energies** demonstrated for femtosecond filament ignition in lean methane/air and a comfortable margin over few‑mJ ns laser sparks. Thus, **energy cost of ignition is negligible** relative to the **~130 J fuel energy per cycle**; the benefit is **robust, electrode‑less, lean‑capable ignition** and precise timing. [7,8]

> **Qualitative advantages:** improved ignition reliability, tolerance to high EGR/lean mixtures, reduced electrode wear, and flexible kernel placement—at the cost of optical alignment and safety controls. [7,8]

---

### **3.3 Thermoelectric Recovery (Revised)**

#### 3.3.1 Module vs system efficiency
For **Bi₂Te₃** modules at **ΔT≈200 K**, peer‑reviewed data show **module efficiencies ~6–7%** under optimized interfaces; commercial modules typically realize **~3–5%**. When integrated with finite heat exchangers and contacts, **system‑level electrical recovery** is a realistic **~2–4% of fuel energy** in compact engine applications. [9,10]

#### 3.3.2 Example per‑cycle numbers
Using $$E_f\approx114\,\text{J}$$ per cycle (Section 3.1), take **3%** system‑level TEG ⇒ $$E_{TEG}\approx3.4\,\text{J}$$ electrical per cycle. This adds to the alternator path (~31 J) for a **total ~34–35 J** per cycle at the DC bus.

#### 3.3.3 Seebeck sizing and load match
Open‑circuit voltage per leg pair $$V_{oc}=S\Delta T$$ with **S ~200 µV/K** yields ~40 mV at ΔT=200 K; series‑connecting ~100–200 junctions provides several volts. Maximum power occurs near **$$R_L=R_i$$**; DC/DC should track this point as ΔT varies. [11]

---

### **3.4 Rotor + Generator System**

#### 3.4.1 Flywheel smoothing
To limit speed ripple to $$\delta=\Delta\omega/\omega$$, the flywheel inertia must satisfy
\[ I \ge \frac{W_b}{\omega^2 (2\delta-\delta^2)}. \]
Choose $$\delta\le5\%$$ for good rectifier/DC ripple and acoustic comfort.

#### 3.4.2 PM alternator and rectifier
The EMF $$\mathcal{E}=NBA\omega$$. Size $$N$$ so that at **minimum rpm**, $$\mathcal{E}$$ exceeds the regulated DC after rectification (with headroom). Use copper/iron loss models to ensure thermal limits are respected.

---

## **4. System Efficiency and Energy Flow (Revised)**

| Stage | Basis | Efficiency (typ.) | Notes |
|---|---:|---:|---|
| Brake thermal efficiency | Small SI, steady | **~25%** | Typical small SI engines under realistic loads; research engines up to **~41%** BTE. [3] |
| Generator + rectifier | PM alternator | **~90%** | Well‑designed kW‑scale alternators. |
| TEG add‑on | Bi₂Te₃, ΔT≈200 K | **~2–4% of fuel energy** | Module 3–7% of heat through module; system‑level 2–4% of fuel. [9,10] |
| **Total fuel→DC** | — | **~24–26%** | Alternator path (~22.5%) + TEG (~2–4%). |

---

## **5. Petrol Required to Charge an Ather 450X (Updated)**
Ather 450X has a **~3.7 kWh** pack (variant) [12]. Assuming **AC onboard charger efficiency ≈ 90%**, energy drawn from the generator for full charge ≈ **3.7/0.90 ≈ 4.1 kWh**. Gasoline energy ≈ **9.06 kWh/L** (32.6 MJ/L ÷ 3.6). With **24–26%** fuel→DC efficiency, delivered **2.17–2.36 kWh/L**. Therefore,
$$\text{Liters per full charge} \approx \frac{4.1}{2.17\text{–}2.36} \approx 1.74\text{–}1.89\,\text{L} \;\Rightarrow\; \mathbf{\sim 1.8\,L\ (\pm0.1\,L)}.$$
This supersedes the earlier **~0.94 L** claim, which would imply **~42%** total efficiency—beyond validated small‑engine + TEG performance. [1,3,9,10,12]

---

## **6. Conclusion (Revised)**
A literature‑consistent analysis of a modular micro‑combustion charger with solar‑powered laser ignition and Bi₂Te₃ TEG recovery yields a **total fuel→DC efficiency ~24–26%**. The **fuel per cycle** for a ~50 cm³ chamber is **~0.003–0.005 ml** at IMEP≈8 bar and $$\eta_i\approx0.35$$, not 0.2 ml. TEG recovery at **ΔT≈200 K** credibly contributes **~2–4% of fuel energy** at the **system level**; higher module numbers must explicitly exclude interface/HX losses. Solar‑laser ignition materially aids **lean stability and reliability** with **negligible energy overhead**. For an **Ather 450X (3.7 kWh)** pack, expect **~1.8 L petrol** per full charge in steady conditions. Future work: (i) experimental **P–θ** traces with laser ignition to refine Wiebe parameters, (ii) co‑optimization of **TEG heat exchangers** and alternator cooling to stabilize ΔT, and (iii) array‑level **BSFC/NOx** validation across load points.

---

## **References**
[1] Engineering Toolbox, *Higher and Lower Calorific Values of Fuels* — gasoline LHV and density; ~32 MJ/L typical. https://www.engineeringtoolbox.com/fuels-higher-calorific-values-d_169.html  
[2] Wikipedia, *Air–fuel ratio* — gasoline stoichiometric AFR ≈ 14.7. https://en.wikipedia.org/wiki/Air%E2%80%93fuel_ratio  
[3] Akinfaloye et al., *Spark Ignition Engine Performance* — small SI efficiency/IMEP trends; plus SAE 2016‑01‑0709 reporting BTE > 41% on advanced engines. https://saudijournals.com/media/articles/SJEAT_68_232-241.pdf ; https://www.sae.org/publications/technical-papers/content/2016-01-0709/  
[4] Eng‑Tips forum; PhysicsForums — typical SI peak cylinder pressures ~70–100 bar, >100 bar under knock. https://www.eng-tips.com/threads/peak-cylinder-pressures.215499/ ; https://www.physicsforums.com/threads/gas-pressure-in-internal-combustion-gasoline-engine.356962/  
[5] Engineering Toolbox; ScienceNotes — adiabatic flame temperatures for gasoline/air ~2000–2250 °C. https://www.engineeringtoolbox.com/adiabatic-flame-temperature-d_996.html ; https://sciencenotes.org/adiabatic-flame-temperature-chart/  
[6] PV STC (AM1.5, 1000 W/m², 25 °C). https://www.alternative-energy-tutorials.com/photovoltaics/standard-test-conditions.html ; https://eepower.com/technical-articles/understanding-pv-system-standards-ratings-and-test-conditions/  
[7] Zang et al., *Ultralow‑energy laser ignition (fs filamentation)* — sub‑mJ thresholds in lean methane/air. https://www.nature.com/articles/s41377-021-00496-8.pdf  
[8] IAEA presentation — **ns laser spark ignition** MPE can approach sub‑mJ with optimized focusing. https://www-pub.iaea.org/MTCD/publications/PDF/P_1357_CD_web/presentations/s6-3s.pdf  
[9] Gaurav & Pandey (AIP, 2017) — TEG efficiency calculations; Bi₂Te₃ ~7% module around 310–500 K. https://pubs.aip.org/aip/jrse/article/9/1/014701/285332/Efficiency-calculation-of-a-thermoelectric  
[10] Wu et al., (RSC, 2025) — Bi₂Te₃ module 6.6% at ΔT=200 K with low contact resistivity. https://pubs.rsc.org/en/content/articlelanding/2025/tc/d4tc05059b  
[11] Wikipedia; AIP J. Appl. Phys. — Seebeck coefficients O(100–200 µV/K) for Bi₂Te₃; thin‑film enhancements context. https://en.wikipedia.org/wiki/Seebeck_coefficient ; https://pubs.aip.org/aip/jap/article/128/3/035108/157725/  
[12] Ather 450X battery options (2.9 and 3.7 kWh). https://www.zigwheels.com/newbikes/faqs/what-is-the-battery-capacity-of-ather-450x/2699794/

---

## **Appendix index**
Companion technical appendices (A–D) with expanded derivations (cycle modeling, PV–laser dynamics, TEG analysis, rotor–generator) are available as separate LaTeX files. (Request full 200+‑line versions if needed.)
