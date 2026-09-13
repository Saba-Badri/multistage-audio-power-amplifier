#  Multi-Stage Audio Power Amplifier with Global Negative Feedback
A fully customized, multi-stage discrete audio power amplifier engineered and simulated in **LTspice** to drive a low-impedance heavy load ($50\,\Omega$) with minimal crossover distortion, low total power dissipation, and stable closed-loop voltage gain.

---

##  Executive Summary & Key Highlights

This project presents the complete design and performance evaluation of a high-fidelity discrete audio amplifier. The system incorporates a **MOSFET differential input stage**, a **BJT voltage amplification stage (VAS)** with tailored current biasing, a **Class-AB Darlington push-pull output stage**, and a **global voltage-series negative feedback loop**.

###  Key Benchmarks Achieved

| Parameter | Required Target | Measured Design Result | Status |
| :--- | :---: | :---: | :---: |
| **Supply Voltage ($V_{CC} / V_{EE}$)** | $\pm 10\,\text{V}$ | **$\pm 10\,\text{V}$** | Pass |
| **Closed-Loop Gain ($A_{v,\text{closed}}$)** | $18 \text{ to } 22 \text{ (at } 1\,\text{kHz})$ | **$19.65$ ($25.87\,\text{dB}$)** | Pass |
| **Clean Output Swing ($V_{out,pp}$)** | $\ge 16\,\text{V}_{pp}$ | **$16.7\,\text{V}_{pp}$** | Pass |
| **Quiescent Power Dissipation** | Optimized | **$\sim 60\,\text{mW}$** | Pass |
| **Total Power ($P_{\text{total}}$ @ $50\,\text{mV}_{in}$)** | $\le 190\,\text{mW}$ | **$74.83\,\text{mW}$** | Pass |
| **Output Stage Efficiency ($\eta_{\text{out}}$ @ $16\,\text{V}_{pp}$)** | $> 60\%$ | **$66.89\%$** | Pass |
| **Total Harmonic Distortion (THD)** | $< 0.08\%$ | **$0.0637\%$** | Pass |
| **THD with Noise Source** | $< 1.00\%$ | **$0.0640\%$** | Pass |
| **Differential Input Impedance ($R_{in,\text{diff}}$)** | $> 1\,\text{M}\Omega$ | **$\infty$** (MOSFET inputs) | Pass |
| **Output Impedance ($R_{\text{out}}$)** | $< 50\,\Omega$ | **$15.2\,\text{m}\Omega$** | Pass |
| **Component Cost Index** | $\le 200$ | **$157$** | Pass |

---
