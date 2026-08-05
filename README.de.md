<p align="center">
  <a href="README.md">Русский</a> | <a href="README.en.md">English</a> | <b>Deutsch</b>
</p>

# Simulation einer Koaxialleitung (2,4 GHz)

Dieses Repository enthält die Ergebnisse des Entwurfs, der analytischen Berechnung und der elektromagnetischen 3D-Simulation einer Koaxialleitung, die für eine Betriebsfrequenz von **2,4 GHz** optimiert ist.

Das Hauptziel des Projekts besteht darin, die Geometrie der Koaxialstruktur für eine bestimmte Wellenimpedanz (50 Ohm) zu berechnen und die Leistungsparameter mittels numerischer Analyse zu überprüfen.

---

## Projektstruktur

* `/cad` — Geometrisches 3D-Volumenmodell der Koaxialstruktur im SolidWorks-Format (`.sldprt`).
* `/calculations` — Analytische Berechnungen der Koaxialkabelparameter in Mathcad (`.xmcd`).
* `/simulation` — Elektromagnetisches Vollwellen-Simulationsprojekt in CST Studio Suite (`.cst`).
* `/docs/images` — Grafische Materialien und Screenshots der Simulationsergebnisse.

---

## 1. Analytische Parameterberechnung

Die mathematische Berechnung der physikalischen Abmessungen (Innendurchmesser des Leiters $d$ und Außendurchmesser des Dielektrikums $D$) wurde in Mathcad unter Berücksichtigung der Eigenschaften des füllenden Dielektrikums — PTFE ($\varepsilon = 2,1$) — durchgeführt. Die berechnete Wellenimpedanz der Leitung beträgt ca. 53 Ohm.

![Analytische Berechnung](docs/images/calc_analytical_coaxial.png)

---

## 2. 3D-Modellierung

Basierend auf den analytischen Parametern wurde in SolidWorks ein 3D-Volumenmodell der Koaxialleitung für den anschließenden Import und die Analyse in CST Studio Suite erstellt.

![3D-Modell](docs/images/simulation_3d_model.png)

---

## 3. Ergebnisse der elektromagnetischen Simulation

### 3.1. Anpassung und Impedanz

Die Bewertung der Leitungsanpassung zeigt eine gute Übereinstimmung zwischen den analytischen Ergebnissen und der numerischen Simulation. Bei der zentralen Betriebsfrequenz von 2,4 GHz beträgt das Stehwellenverhältnis (VSWR) 1,138.

**VSWR-Diagramm:**
![VSWR](docs/images/simulation_vswr.png)

**Z-Parameter (Eingangsimpedanz):**
![Z-Parameter](docs/images/simulation_z_parameters.png)

### 3.2. Feldverteilung (TEM-Mode)

Unten ist die vektorielle Verteilung der elektrischen ($E$) und magnetischen ($H$) Feldstärke im Querschnitt der Koaxialleitung bei 2,5 GHz dargestellt. Die im Simulationsmodell ermittelte Torimpedanz beträgt 53,3 Ohm.

**Elektrische Feldstärke (E-Feld):**
![E-Feld](docs/images/simulation_e_field.png)

**Magnetische Feldstärke (H-Feld):**
![H-Feld](docs/images/simulation_h_field.png)

## Lizenz

Copyright (c) 2026 Ilya Kornilov

Diese Quelle beschreibt Open Hardware (offene Hardware) und ist unter der CERN-OHL-P v2 lizenziert. 
Sie dürfen diese Quelle unter den Bedingungen der CERN-OHL-P v2 (https://cern.ch/cern-ohl) 
weiterverbreiten, modifizieren und Produkte auf deren Grundlage herstellen.

Diese Quelle wird OHNE JEGLICHE AUSDRÜCKLICHE ODER STILLSCHWEIGENDE GEWÄHRLEISTUNG vertrieben, 
EINSCHLIESSLICH DER GEWÄHRLEISTUNG DER MARKTGÄNGIGKEIT, ZUFRIEDENSTELLENDEN QUALITÄT ODER EIGNUNG 
FÜR EINEN BESTIMMTEN ZWECK. Die geltenden Bedingungen entnehmen Sie bitte der CERN-OHL-P v2.