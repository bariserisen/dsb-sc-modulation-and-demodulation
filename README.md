# DSB-SC Modulation and Demodulation Circuit

This repository contains the design and documentation for a hardware-based **Double Sideband Suppressed Carrier (DSB-SC)** communication system.

## 📌 Project Overview
This project demonstrates the hardware implementation of DSB-SC modulation and demodulation.
The circuit is designed to multiply a message signal with a high-frequency carrier while suppressing the carrier component to improve power efficiency.

## ⚙️ Functional Blocks

### 1. Modulation Part
*   **Configuration:** Utilizes a balanced configuration with a transformer (XFR1) and diodes (D1, D2) to create the suppressed carrier signal.
*   **Precision Adjustment:** Features the **R5 module**, which allows the user to adjust the carrier signal's noise, minimize carrier leakage, and improve the overall quality of the modulation.
*   **Inputs:** The message signal is applied at **H1**, and the carrier signal is applied at **H2**.

### 2. Demodulation Part
*   **Signal Recovery:** Centered around the **LM741 Op-Amp (U1)**, this stage acts as a recovery circuit to extract the original message signal from the modulated wave.
*   **U2 Interface:** The **U2 pin** serves as a critical junction; it can be used to view the modulated signal or function as a low-pass filter (LPF) interface before demodulation is initiated.
*   **Output:** The final recovered/demodulated signal is retrieved at **H3**.

## 🛠 Technical Specifications
*   **Operational Amplifier:** LM741CN/NOPB.
*   **Switching Diodes:** 1N4148 (D1, D2).
*   **Filter Components:** 4.7kΩ resistors, 10nF/47nF capacitors, and 220uH inductors.
*   **Power Supply:** ±5V DC (U4).
