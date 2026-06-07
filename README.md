# 72V-Battery-Pack-Design-Verification-Chemistry-Performance-Analysis
Since your project revolves around battery engineering, testing, and validation (specifically looking at pack metrics like NMC vs. LFP, voltage limits, and thermal boundaries), you can go far beyond basic bar charts. MATLAB is incredibly powerful for simulating and visualizing electrochemical and BMS (Battery Management System) data.
An engineering toolset and visualization suite developed in MATLAB to validate the operational boundaries of a custom **72V battery pack** and evaluate performance trade-offs between Lithium Nickel Manganese Cobalt Oxide (**NMC**) and Lithium Iron Phosphate (**LFP**) chemistries.

---

## 📌 Project Overview
This repository contains the simulation models, data visualization scripts, and validation metrics for a final year engineering project focused on Battery Management Systems (BMS) and pack design. The project focuses on two main engineering objectives:
1. **Design Verification:** Cross-referencing experimental lab data against safe theoretical target boundaries (Voltage and Thermal).
2. **Comparative Analysis:** Quantitative evaluation of NMC vs. LFP cells across structural, thermal, and lifecycle parameters to determine application suitability.

---

## 📊 System Specifications & Lab Results

### 1. Operational Hardware Validation
The design was subjected to a **25A constant current discharge profile** to verify critical safety trip-points and thermal stability.

| Design Metric Parameter | Theoretical Target Boundary | Measured Lab Value | Operational Verdict Status |
| :--- | :--- | :--- | :--- |
| **Open Circuit Voltage (Full Charge)** | 72.0V - 72.4V Nominal | 72.42V Actual | **Pass** (Within Bounds) |
| **Peak Thermal Rise (25A Profile)** | < 45.0°C Absolute Ceiling | 42.1°C Stabilized | **Pass** (Thermal Range Safe) |
| **High Overvoltage Interlock Trip** | 84.0V Fault Shunt Target | 83.92V Isolation Actuation | **Pass** (Protection Verified) |
| **Low Undervoltage Interlock Trip** | 60.0V Fault Shunt Target | 60.05V Isolation Actuation | **Pass** (Protection Verified) |

### 2. Battery Chemistry Benchmark (NMC vs. LFP)
| Chemical Characteristic | NMC (LiNiMnCoO2) | LFP (LiFePO4) |
| :--- | :--- | :--- |
| **Nominal Cell Voltage** | 3.6V - 3.7V | 3.2V |
| **Specific Gravimetric Density** | 150 - 220 Wh/kg (High) | 90 - 120 Wh/kg (Medium) |
| **Peak Current Capability** | Up to 10C - 15C Transient | 3C - 5C Continuous |
| **Thermal Runaway Threshold** | ~210°C (Moderate Risk) | ~270°C (Highly Stable) |
| **Cycle Longevity (80% DoD)** | 1,000 - 2,000 Cycles | 2,000 - 5,000+ Cycles |

---

## 🛠️ MATLAB Visualization Toolkit
The included scripts generate three distinct engineering diagrams to visualize the core datasets:

* **Figure 1: Target vs. Lab Verification Plot** — A dual-axis, high-contrast bar graph comparing actual hardware responses to design ceiling thresholds, featuring automated validation text overlays.
* **Figure 2: Transient Discharge Profile (25A)** — Simulates dynamic cell polarization under a heavy discharge cycle, mapping real-time Pack Voltage (Left Y-Axis) and Temperature Rise (Right Y-Axis) concurrently.
* **Figure 3: Chemistry Trade-off Matrix & SOH Fade Curve** — Features a custom multi-attribute radar chart detailing performance trade-offs, alongside a long-term capacity retention forecast modeling degradation up to 4,000 cycles.

---
