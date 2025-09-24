# VeriCore-8: An 8-bit Microcomputer in Verilog 💻

Welcome to **VeriCore-8**! 🚀 This is a complete 8-bit microcomputer designed and simulated entirely from the ground up in Verilog. This project brings classic computer architecture to life, featuring a custom-built CPU, a unique assembly language, and a full toolchain for simulation and verification.

This isn't just a CPU; it's a complete, functional computer system built on the Von Neumann architecture, where both instructions and data share the same memory space.

## ✨ Core Features

-   🧠 **Custom 8-bit CPU:** A modular CPU design with an Arithmetic Logic Unit (ALU), program counter, instruction controller, and registers, all written in Verilog.
-   🐍 **Full Toolchain:** Includes a custom assembler built in Python that translates human-readable assembly code into machine-executable binary for the CPU.
-   🏛️ **Von Neumann Architecture:** A classic design where 16 bytes of RAM are shared for both program instructions and data.
-   📈 **Simulation & Verification:** Comes with a Verilog testbench and a `Makefile` for easy, one-command simulation using Icarus Verilog and waveform analysis with GTKWave.

## 📊 Simulation Waveform

The waveform below shows the successful execution of the demo assembly program, visualizing the activity on the bus and the changing values in the registers over time.

<div>
<img src="./outputFiles/output.png" style="width:100%; height:auto;"></img>
</div>

## 🛠️ Getting Started

To get this project up and running, you'll need a few open-source tools.

### Prerequisites

-   **Icarus Verilog (`iverilog`):** An open-source Verilog compiler.
-   **GTKWave:** A waveform viewer for digital logic simulation.
-   **Python 3:** To run the assembler.
-   **Make:** To automate the simulation process.

### ⚡ Quick Start

1.  **Assemble the Program:**
    First, run the Python assembler to convert the assembly code (`DemoProgram.asm`) into a Verilog-compatible RAM module.

    ```shell
    python3 Assembler_v2.py DemoProgram.asm
    ```

2.  **Run the Simulation:**
    With the RAM module updated, just use the `make` command to compile, simulate, and view the results.

    ```shell
    make
    ```

This command will automatically compile the Verilog files, run the simulation, and open the waveform (`dump.vcd`) in GTKWave for you to analyze.

## 📁 Project Structure
```
.
├── VerilogModules/   # Contains all the Verilog source code for the computer's components.
├── outputFiles/      # Holds the simulation outputs, including the waveform dump.
├── Assembler_v2.py   # The custom assembler script.
├── DemoProgram.asm   # An example assembly program to run on the computer.
└── Makefile          # Automates the compilation and simulation workflow.
```
