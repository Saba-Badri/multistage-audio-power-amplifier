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
1. **Differential Input Stage:** Active-loaded NMOS pair providing near-infinite input resistance ($R_{in} \approx \infty$) and high Common-Mode Rejection Ratio (CMRR)[cite: 1].
2. **Voltage Amplification Stage (VAS):** BJT Common-Emitter amplifier biased by a stable current mirror to provide high open-loop voltage gain and sufficient drive swing[cite: 1].
3. **Biasing & Thermal Stability:** $V_{BE}$-multiplier network ($Q_7, Q_{11}, R_8$) to mitigate crossover dead-zones and stabilize quiescent current ($I_Q$) against thermal drift[cite: 1].
4. **Output Power Stage:** Complementary Class-AB Darlington topology ($Q_8/Q_9$ and $Q_{10}/Q_1$) designed to supply up to $160\,\text{mA}$ peak currents into a heavy $50\,\Omega$ load[cite: 1].
5. **Global Negative Feedback:** Voltage-series topology sampling directly from the output node to stabilize gain, drastically reduce THD, and lower output impedance down to $15.2\,\text{m}\Omega$[cite: 1].

---

##  Simulation & Testing Protocol

The circuit was rigorously tested in **LTspice** across multiple domains[cite: 1]:

* **DC Operating Point Analysis:** Confirmed balanced differential current distribution and negligible DC offset voltage at the output node ($V_{out,DC} = 13.5\,\text{mV}$)[cite: 1].
* **Transient Analysis (`.tran`):** Evaluated sinusoidal signal integrity up to $16.7\,\text{V}_{pp}$ swing without clipping[cite: 1].
* **Harmonic Distortion (`.four`):** Evaluated at $1\,\text{kHz}$ fundamental frequency under clean and noisy current mirror conditions[cite: 1].
* **Real-World Audio Signal Test:** Validated system dynamic response using a single-channel $44.1\,\text{kHz}$ mono WAV file (`testtt.wav`), producing a clean, unclipped output recording (`output.wav`)[cite: 1].
