# 3T PTL NAND Gate

This project implements a **modified 3-transistor Pass Transistor Logic (PTL) NAND gate** using **LTspice XVII**.

An existing 3T NAND topology consisting of **two NMOS and one PMOS transistor** was modified by replacing the PMOS transistor with an **NMOS transistor**. The proposed design was compared with conventional and existing NAND implementations at **32 nm and 0.9 V** based on **power, propagation delay, and power-delay product (PDP)**.

The proposed NAND gate was also analyzed at **16 nm, 22 nm, 32 nm, and 45 nm** technology nodes. **Transient analysis and noise-margin analysis** were performed, and a **2:4 decoder** was implemented at **180 nm** as an application circuit.

---

## Proposed Design

The existing 3T NAND topology consists of:

* **2 NMOS transistors**
* **1 PMOS transistor**

In the proposed design, the **PMOS is replaced with an NMOS**, resulting in a 3-transistor NAND implementation using three NMOS transistors.

<img width="690" height="380" alt="image" src="https://github.com/user-attachments/assets/d80dff07-1862-4ef4-a427-a50e35590933" />


---

## 32 nm Performance Comparison

The three NAND implementations were compared at **32 nm and 0.9 V**.

| Parameter              | Conventional CMOS NAND | Existing 3T NAND [15] | Proposed 3T PTL NAND |
| ---------------------- | ---------------------: | --------------------: | -------------------: |
| Number of Transistors  |                      4 |                     3 |                    3 |
| Technology Node        |                  32 nm |                 32 nm |                32 nm |
| Average Power (µW)     |                 0.0299 |                  14.4 |                 6.81 |
| Propagation Delay (ps) |                   25.3 |                 -4.24 |                 9.35 |
| PDP (aJ)               |                  0.755 |                 -61.1 |                 63.7 |
| Static Power (µW)      |              0.0000851 |                  3.22 |             0.000019 |
| Total Power (µW)       |                   0.03 |                  17.6 |                 6.81 |

> **Note:** The values for the existing 3T NAND are retained as reported in the reference/simulation data, including the negative delay and PDP values.

---

## Technology-Node Analysis

The proposed 3T PTL NAND was analyzed at different technology nodes.

| Technology Node | Pavg (µW) | tpd (ps) | PDP (aJ) |    EDP (J·s) |
| --------------- | --------: | -------: | -------: | -----------: |
| 16 nm           |      2.00 |     23.6 |     47.3 | 1.10 × 10⁻²⁷ |
| 22 nm           |      3.71 |     29.5 |      110 | 3.24 × 10⁻²⁷ |
| 32 nm           |      6.81 |     9.35 |     63.7 | 5.95 × 10⁻²⁸ |
| 45 nm           |      10.7 |     1.09 |     11.6 | 1.27 × 10⁻²⁹ |

---

## Transient Analysis

Transient analysis was performed on the proposed NAND gate to verify its switching behavior and NAND logic operation.

<img width="772" height="366" alt="image" src="https://github.com/user-attachments/assets/a64f1219-cc71-4793-acf9-9d74ac5094a0" />


---

## Noise Margin Analysis

The proposed NAND gate was evaluated for **high noise margin (NMH)** and **low noise margin (NML)** at different technology nodes.

| Technology Node | NMH (V) | NML (V) |
| --------------- | ------: | ------: |
| 16 nm           |    0.50 |    0.54 |
| 22 nm           |    0.60 |    0.54 |
| 32 nm           |    0.63 |    0.45 |
| 45 nm           |    0.54 |    0.54 |



<img width="787" height="371" alt="image" src="https://github.com/user-attachments/assets/638ab761-0c53-4c25-954a-e511fca7f1f9" />


## Application: 2:4 Decoder

The proposed NAND gate was used to implement a **2:4 decoder** at **180 nm**.

### Truth Table

|  A |  B | Active Output |
| -: | -: | ------------- |
|  0 |  0 | Y0            |
|  0 |  1 | Y1            |
|  1 |  0 | Y2            |
|  1 |  1 | Y3            |

### Decoder Circuit

<img width="752" height="691" alt="image" src="https://github.com/user-attachments/assets/7b095e15-de70-4c61-b0b0-7d50fa87d1a2" />


### Decoder Transient Analysis

Transient analysis was performed to verify the decoder output for different combinations of the input signals.

<img width="978" height="447" alt="image" src="https://github.com/user-attachments/assets/4882d8ed-aec0-4b50-bb0c-e15393c12337" />


---

## Tools and Technologies

* **LTspice XVII**
* **Pass Transistor Logic (PTL)**
* **CMOS circuit design**
* **Transistor-level simulation**
* **Technology-node analysis**
* **Transient analysis**
* **Noise-margin analysis**

---

```

