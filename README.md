# Full-Bit-Adder
<!-- TODO: One-line summary, e.g. "Structural Verilog 1-bit full adder verified with an exhaustive testbench, synthesized in Vivado, and programmed on a Basys 3 FPGA." -->

# 1-Bit Full Adder in Verilog on a Basys 3 FPGA

![Verilog](https://img.shields.io/badge/HDL-Verilog-blue) ![Vivado](https://img.shields.io/badge/Tool-Xilinx%20Vivado-red) ![Board](https://img.shields.io/badge/Board-Digilent%20Basys%203-green) ![Device](https://img.shields.io/badge/FPGA-Artix--7%20xc7a35t-orange)

ECE 25 (Digital Design) · Lab <!-- TODO: lab number -->

<!-- TODO: Short description of the project. -->


## TL;DR

| | |
|---|---|
| **Goal** | <!-- TODO --> |
| **Logic** | <!-- TODO: e.g. `sum = a ⊕ b ⊕ cin`, `cout = a·b + cin·(a ⊕ b)` --> |
| **Verification** | <!-- TODO --> |
| **Hardware** | <!-- TODO --> |
| **Key finding** | <!-- TODO --> |


### Gate-level structure

```
TODO: ASCII diagram of the circuit
```

### Source: `src/<design>.v`

```verilog
// TODO: paste design source
```

### Truth table

| a | b | cin | sum | cout |
|:-:|:-:|:---:|:---:|:----:|
| 0 | 0 | 0 |   |   |
| 0 | 0 | 1 |   |   |
| 0 | 1 | 0 |   |   |
| 0 | 1 | 1 |   |   |
| 1 | 0 | 0 |   |   |
| 1 | 0 | 1 |   |   |
| 1 | 1 | 0 |   |   |
| 1 | 1 | 1 |   |   |

<!-- TODO: one-sentence interpretation -->


## Verification

### Testbench: `sim/<testbench>.v`

<!-- TODO: describe the testbench -->

```verilog
// TODO: paste testbench source
```

### Simulation waveform

![Behavioral simulation waveform](docs/simulation_waveform.png)


## Synthesis & Implementation

### Elaborated design (RTL view)

<!-- TODO -->

![Elaborated schematic](docs/elaborated_schematic.png)

### Synthesized design

<!-- TODO -->

![Synthesized schematic](docs/synthesized_schematic.png)

### Device view

![Device floorplan](docs/device_view.png)

---

## Hardware Demo

<!-- TODO: which switches/LEDs are used -->

![Basys 3 running the design](docs/basys3_board.jpg)

---

## How to Reproduce

**Requirements:** Xilinx Vivado (any recent version), Digilent Basys 3 board, micro-USB cable.

1. Create a new **RTL Project**, target device **`xc7a35tcpg236-1`**.
2. Add `src/<design>.v` as a **design source**.
3. Add `sim/<testbench>.v` as a **simulation source**.
4. Add `constraints/basys3.xdc` as a **constraints source**.
5. **Run Simulation → Run Behavioral Simulation.** Confirm the waveform matches the truth table.
6. **Run Synthesis → Run Implementation → Generate Bitstream.**
7. Plug in the board, then **Open Hardware Manager → Open Target → Auto Connect → Program Device**.
8. Flip the input switches and confirm the LEDs follow the truth table.

---

## Concepts Covered

<!-- TODO -->

---

## What I'd Improve Next

<!-- TODO -->

---

## Repository Structure

```
.
├── src/            # Design source (Verilog)
├── sim/            # Testbench
├── constraints/    # Basys 3 pin constraints (.xdc)
├── docs/           # Waveform, schematics, device view, board photo
├── LICENSE
└── README.md
```

## Tools

- Xilinx Vivado (RTL analysis, behavioral simulation, synthesis, Hardware Manager)
- Digilent Basys 3 (Artix-7 `xc7a35tcpg236-1`)
- Verilog HDL
