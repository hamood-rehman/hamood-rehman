# Hamood Rehman

**3rd year Ph.D. student @ Power Switch Lab

I'm 3rd year Ph.D. student at Power Switch Lab, NSF GRAPES Center, at University of Arkansas, Fayetteville. My current research focus is on development of 20kV SiC switch using 6.5kV SiC MOSFETs with integrated gate-driver, isolate power supply, and active dv/dt control.  In summer 2026 I was an intern at Tesla, Palo Alto, CA, where I was part of Power Conversion Hub (PCH) team working on Tesla Powerwall 3.

[ORCID](https://orcid.org/0000-0003-4044-2703) · [Google Scholar](https://scholar.google.com/citations?user=B7MW3XgAAAAJ) · [LinkedIn](https://www.linkedin.com/in/hamoodurrehman/) · rehman@uark.edu

---

## Current focus

- **Series-connected SiC MOSFET** for 10–20 kV applications such as MV converters and solid-state circuit breakers
- **Active dv/dt control** for dynamic voltage balancing without snubbers or extra isolated supplies
- **Isolated gate-driver power supplies** with high voltage-insulation and low coupling capacitance
- **Measurement-driven sensitivity analysis** that links device parameter spread to switching behavior

## Selected work

### 10 kV SiC switch from stacked 3.3 kV MOSFETs, toward a 20 kV platform
*Ph.D. project: 20 kV High Voltage SiC Switch for Next Generation Energy Conversion and Grid Modernization*

- Three Wolfspeed 3.3 kV / 52 A SiC MOSFETs in series, with signal, power, and control integrated at every stage. Each device has its own board with a gate driver, V<sub>DS</sub> sensing, and a local dv/dt controller, powered by an on-board two-stage, multichannel isolated auxiliary supply rated for 12 kV insulation. The boards stack modularly, so blocking voltage scales with the number of stages and the isolation rating of the supply.
- **Voltage balancing:** a low-voltage NPN BJT in each MOSFET's Kelvin-source path acts as a voltage-controlled resistor during the turn-off Miller plateau. V<sub>DS</sub> is sampled and held on every pulse, and a PI loop sets the BJT base drive to slow or speed that device's turn-off dv/dt on the next pulse. Because the BJT emitter sits at the MOSFET source, the controller shares the gate driver's rail, so no additional isolated supply is needed per device.
- **Status:** the 10 kV-rated prototype is built, and the balancing method has been validated experimentally on it at reduced bus voltage. The 20 kV version is the current design effort, using 6.5 kV-class devices and a single-stage, multichannel RF-switched auxiliary supply with 20 kV isolation. It has not yet been built or tested.

### Which device mismatches actually cause voltage imbalance?
*IEEE APEC 2026, oral presentation*

- Characterized five Wolfspeed 3.3 kV SiC MOSFETs (V<sub>th</sub>, g<sub>m</sub>, C<sub>gs</sub>, C<sub>gd</sub>, C<sub>ds</sub>) and recorded 448 double-pulse measurements on series-connected pairs from 1 to 4 kV and 10 to 40 A, across device-position and gate-driver configurations.
- Fit a Gaussian-process surrogate to the measurements (test R² ≈ 0.95), then used Sobol indices and SHAP values to separate individual effects from interactions.
- **Result:** imbalance is driven mainly by interactions between mismatches rather than by any single one. C<sub>gs</sub> and V<sub>th</sub> mismatch carry roughly 50% and 30% of the SHAP attribution, and g<sub>m</sub> mismatch was negligible under the tested conditions. The practical takeaway is to screen devices for series stacks on C<sub>gs</sub> and V<sub>th</sub> first.

### Wireless gate-driver power supply for MV SiC MOSFETs
*IEEE ECCE 2025*

- 6 W, +15 V / −5 V supply: GaN full-bridge inverter at 2.8 MHz, PCB air-core transformer with a 12.7 mm gap (about 38 kV theoretical air insulation), and full-bridge rectifiers.
- Compared four compensation networks (S-S, LCC-S, S/S-CL, LCL-S) on identical hardware while double-pulse testing a 3.3 kV SiC MOSFET at a 2.5 kV bus, measuring coupling capacitance, output stability under dv/dt, and thermal behavior.
- **Result:** the matching network and rectifier, not only the transformer gap and insulation, change coupling capacitance and common-mode immunity. Networks with fewer reactive elements held up better under high dv/dt.

<p align="center">
  <img src="assets/wpt-gdps-prototype.jpg" width="680" alt="Wireless gate-driver power supply prototype: GaN H-bridge, fixture for resonant networks, 128 x 116 mm PCB air-core transformer with 12.7 mm gap, and -5 V / +15 V rectifier outputs">
</p>

### Other projects

- **650 V GaN three-level flying-capacitor inverter building block (2024–2025):** three-phase, 25 kVA, 800 V DC bus. Implemented single-phase-shift modulation on a TI TMS320F28379D and designed the output LC filter for ripple, THD, and resonance; output-current THD of about 2.6%.
- **Automated air-core PCB transformer design:** NSGA-III multi-objective optimization with ANSYS electromagnetic simulation.
- **Switched-inductor buck-boost DC–DC converter (M.S. thesis):** topology development, efficiency analysis, and control for low-power applications, published in *IET Power Electronics* (2023).

## Publications

**Medium-voltage SiC**

- **H. U. Rehman**, X. Song, and Y. Zhao, "Dynamic Voltage Balancing in Series-Connected SiC MOSFETs: Impact Quantification of Device and Circuit Parameter Variations," *IEEE APEC*, San Antonio, TX, 2026.
- X. Zheng, **H. U. Rehman**, X. Song, and Y. Zhao, "A Simplified and Low-Cost Voltage Balancing Control Method for Series-Connected SiC MOSFETs," *IEEE APEC*, San Antonio, TX, 2026.
- **H. U. Rehman** and X. Song, "Performance Analysis of Matching Networks in Wireless Gate-Driver Power Supply for MV SiC MOSFETs," *IEEE ECCE*, Philadelphia, PA, 2025. [doi:10.1109/ECCE58356.2025.11259774](https://doi.org/10.1109/ECCE58356.2025.11259774)
- *Under review:* **H. U. Rehman**, X. Zheng, X. Song, and Y. Zhao, "A 10kV SiC Switch Enabled by Voltage-Balanced 3.3kV MOSFETs Stacking."

**Earlier work**

- **H. U. Rehman**, N. Ahmed, H. A. Sher, A. Al-Durra, and H. M. Hasanien, "Comprehensive analysis and design of a switched-inductor type low inductance-requirement DC-DC buck-boost converter for low power applications," *IET Power Electronics*, vol. 16, no. 7, pp. 1239–1254, 2023.
- **H. U. Rehman**, "Modified Switched-Inductor Based DC-DC Buck-Boost Converter for Low-Power Applications," *IEEE IECON*, 2021.
- **H. U. Rehman**, B. Ali, and M. Javed, "Data Incremental Learning for Fault Detection and Classification in Photovoltaic Arrays," *IEEE SDEMPED*, Dallas, TX, 2021, pp. 310–315.
- F. A. Khattak and **H. U. Rehman**, "Improved Selective Harmonics Elimination Strategy for Multilevel Inverters with Optimal DC Values," *IEEE ICEPT*, 2021.

## Tools

| Area | Tools |
|---|---|
| Circuit and system simulation | LTspice, PSpice, PLECS, MATLAB/Simulink |
| Electromagnetic design | ANSYS Maxwell, Q3D, HFSS, Simplorer |
| PCB and mechanical | Altium Designer (multilayer high-voltage boards), SolidWorks |
| Embedded control | TI C2000 (TMS320F28379D), Code Composer Studio, C / Embedded C |
| Test and characterization | Double- and multi-pulse testing, Keysight B1505A curve tracer, Keysight E4990A impedance analyzer, Tektronix MSO5 series, isolated HV probing |
| Analysis and optimization | Python (Gaussian-process regression, tree ensembles, SHAP, Sobol), PSO, GA, NSGA-III |

## Background

- **Ph.D., Electrical Engineering**, University of Arkansas, Fayetteville (2024–present)
- **Power Electronics Intern**, Tesla Energy (summer 2026)
- **Laboratory Instructor**, GIK Institute, Pakistan (2020–2024): upgraded the Linear Control Systems and DSP labs with Siemens S7-1214C PLCs and OMAP-L138 DSP kits, including new manuals and trainer boards
- **M.S., Electrical Engineering**, GIK Institute, Pakistan (2017–2019)
