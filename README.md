# 8-bit Microcomputer 💻

**An 8-bit Von-Neumann MicroComputer in Verilog HDL**

This computer is based on the Von Neumann architecture (same memory shared between program and data). The VerilogModules folder contains all the Verilog source codes to simulate the 8-bit computer and also the testbench file. The modules required for the computer are defined separately and then combined and interfaced in a common module named `CPU.v`. It also contains a testbench file named `CPU_tb.v` which is used to simulate the behaviour of the computer.

The parent folder contains the Assembly language compiler in the form of a python script as well as a `DemoProgram.asm` file which is essentially a 16 byte executable assembly code. The compiler accepts the compilable text file as an argument in the compilation line and automatically updates the `RAM.v` module with the binary instructions.

The outputFiles folder contains the output obtained from the testing of the modules.

## 📊 Simulation Waveform

<div>
<img src="./outputFiles/output.png" style="width:100%; height:auto;"></img>
</div>

## Using The Assembler

In order to use the assembler, please use below mentioned syntax:

```bash
python Assembler_v2.py <input_filename_with_extension>
```

Or,

```bash
python3 Assembler_v2.py <input_filename_with_extension>
```

And press Enter.

Now the `RAM.v` module in the VerilogModules folder will be updated with the new set of instructions. No need to copy paste anything into the RAM module.

**THIS METHOD IS RECOMMENDED!!**

## System Requirements

* Make sure you have Python3 installed in your system.
* Make sure you have iverilog (abbreviation of Icarus Verilog) installed.
* Make sure you have GTKWave (waveform analyzer tool) installed.
* Make sure you have the latest version of make (to run the Makefile).

## Recommended Way To Use

Install iverilog (an open source verilog code synthesizer) from [here](https://bleyer.org/icarus/).

Now, just execute the following command on cmd (for windows) or terminal (linux or mac):

```bash
make
```

That's it!

This "make" command will now create and open the waveform for the Verilog module - `CPU_tb.v` and you will be able to see it in GTKWave.

### Alternative Method (Windows/Manual)

If you are on Windows and the Makefile is not working for you, try the following:

* Open the cmd and 'cd' to the directory of the GitHub repository.
* Use the following commands:

```bash
cd VerilogModules
iverilog CPU_tb.v
vvp a.out
gtkwave dump.vcd
```

Now the GTKWave program (also an open source waveform viewer) will display the output of the 8bit Computer in a new window.

## 📁 Project Structure

```
.
├── VerilogModules/   # Contains all the Verilog source code for the computer's components
├── outputFiles/      # Holds the simulation outputs, including the waveform dump
├── Assembler_v2.py   # The custom assembler script (recommended)
├── DemoProgram.asm   # An example assembly program to run on the computer
└── Makefile          # Automates the compilation and simulation workflow
```

**THANK YOU !!!**
