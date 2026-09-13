# Multi-Stage Differential Audio Power Amplifier design

A fully discrete hybrid (CMOS + BJT) differential power amplifier designed and simulated in LTspice.

## Key Specifications
- **Supply Voltage:** ±10V
- **Power Dissipation:** < 150mW (Quiescent Power ~ 60mW)
- **Load Impedance:** 50 Ω
- **Architecture:** NMOS Differential Input Stage, BJT Gain/Driver Stage, Class-AB Push-Pull Output Stage.

## Circuit Architecture
- **Input Stage:** Active-loaded NMOS differential pair for high input impedance ($R_{in} \approx \infty$).
- **Intermediate Stage:** BJT Common-Emitter gain stage with tailored current mirror biasing to optimize swing headroom and prevent negative cycle clipping.
- **Output Stage:** Push-Pull Class-AB configuration driving a heavy 50Ω load with minimal crossover distortion.

## How to Run
1. Clone this repository.
2. Open `project.asc` in LTspice.
3. Run `.tran 0 10m 0` to observe transient signal integrity.
