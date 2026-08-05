<p align="center">
  <a href="README.md">Русский</a> | <b>English</b> | <a href="README.de.md">Deutsch</a>
</p>

# Coaxial Transmission Line Simulation (2.4 GHz)

This repository contains the results of the design, analytical calculation, and 3D electromagnetic simulation of a coaxial transmission line optimized to operate at **2.4 GHz**.

The primary objective of the project is to synthesize the coaxial structure geometry to achieve a target characteristic impedance (50 Ohm) and to verify the performance parameters using numerical analysis.

---

## Project Structure

* `/cad` — solid 3D model of the coaxial structure in SolidWorks format (`.sldprt`).
* `/calculations` — analytical calculations of coaxial cable parameters in Mathcad (`.xmcd`).
* `/simulation` — full-wave electromagnetic simulation project in CST Studio Suite (`.cst`).
* `/docs/images` — graphical assets and simulation screenshots.

---

## 1. Analytical Parameter Calculation

Mathematical calculations of the physical dimensions (inner conductor diameter $d$ and outer dielectric diameter $D$) were performed in Mathcad, taking into account the properties of the filling dielectric — PTFE ($\varepsilon = 2.1$). The calculated characteristic impedance of the line is approximately 53 Ohm.

![Analytical Calculation](docs/images/calc_analytical_coaxial.png)

---

## 2. 3D Modeling

Based on the analytical parameters, a solid 3D model of the coaxial transmission line was prepared in SolidWorks for subsequent import and analysis within CST Studio Suite.

![3D Model](docs/images/simulation_3d_model.png)

---

## 3. Electromagnetic Simulation Results

### 3.1. Matching and Impedance

The matching evaluation of the transmission line confirms close agreement between the analytical results and the numerical simulation. At the center operating frequency of 2.4 GHz, the Voltage Standing Wave Ratio (VSWR) is 1.138.

**VSWR Plot:**
![VSWR](docs/images/simulation_vswr.png)

**Z-Parameters (Input Impedance):**
![Z-Parameters](docs/images/simulation_z_parameters.png)

### 3.2. Field Distribution (TEM Mode)

The vector distribution of the electric ($E$) and magnetic ($H$) field strengths in the cross-section of the coaxial line at 2.5 GHz is shown below. The port impedance obtained during simulation is 53.3 Ohm.

**Electric Field Strength (E-field):**
![E-field](docs/images/simulation_e_field.png)

**Magnetic Field Strength (H-field):**
![H-field](docs/images/simulation_h_field.png)

## License

Copyright (c) 2026 Ilya Kornilov

This source describes Open Hardware and is licensed under the CERN-OHL-P v2. 
You may redistribute and modify this source and make products using it under 
the terms of the CERN-OHL-P v2 (https://cern.ch/cern-ohl).

This source is distributed WITHOUT ANY EXPRESS OR IMPLIED WARRANTY, 
INCLUDING OF MERCHANTABILITY, SATISFACTORY QUALITY AND FITNESS FOR A 
PARTICULAR PURPOSE. Please see the CERN-OHL-P v2 for applicable conditions.