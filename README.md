# RISC-V Internship Program powered by SAMSUNG and VSD

This RISC-V Internship using **VSDSquadron Mini** is based on the RISC-V architecture and leverages open-source tools to teach students about VLSI SoC Design and RISC-V. The program is guided by **Kunal Ghosh**, Founder of VSD.

## Basic Details

- **Name**: Gagan H  
- **College**: Sahyadri College of Engineering and Management, Mangaluru 575007  
- **Email**: [gaganhirinja2403@gmail.com](gaganhirinja2403@gmail.com)  
- **GitHub Profile**: [Gaganh2403](https://github.com/Gaganh2403)  
- **LinkedIn Profile**: [Gagan H](https://www.linkedin.com/in/gagan-h-ba69a9328?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app)  
# Task-1

<details>
<summary>Task-1: C based lab screenshots</summary>

Here are the screenshots for the C-based lab:

![C-Based Lab Screenshot 1](./TASK-1/c-lab-1.png)  
![C-Based Lab Screenshot 2](./TASK-1/c-lab-2.png)  
![C-Based Lab Screenshot 3](./TASK-1/c-lab-3.png)  

</details>

<details>
<summary>Task-1: RISC-V based lab screenshots</summary>

Here are the screenshots for the RISC-V based lab:

![RISC-V Based Lab Screenshot 1](./TASK-1/riscv-lab-1.png)  
![RISC-V Based Lab Screenshot 2](./TASK-1/riscv-lab-2.png)  
![RISC-V Based Lab Screenshot 3](./TASK-1/riscv-lab-3.png)  

</details>

# Task-2
<details>
<summary>SKIPE Simulation</summary>

Here are the screenshots for the SKIPE Simulation:

![SKIPE Simulation Screenshot 1](./TASK-2/skipe-sim-1.png)  
![SKIPE Simulation Screenshot 2](./TASK-2/skipe-sim-2.png)  

</details>

# Task 3
<details>
 <summary> RISC-V Instruction Decoding</summary>

Task 3 for the RISC-V Internship program, focusing on decoding RISC-V instructions. The task includes analyzing `riscv-objdump` output, identifying 15 unique instructions, and documenting their 32-bit binary instruction formats based on their respective types (R, I, S, B, U, and J).

---

## Task Objectives

1. **Understand RISC-V Instruction Types**  
   Review the RISC-V software documentation to study the following instruction formats:
   - **R-Type:** Register-register operations (e.g., ADD, SUB).
   - **I-Type:** Immediate operations (e.g., LW, JALR).
   - **S-Type:** Store instructions (e.g., SW).
   - **B-Type:** Branch instructions (e.g., BEQ, BNE).
   - **U-Type:** Upper immediate operations (e.g., LUI, AUIPC).
   - **J-Type:** Jump instructions (e.g., JAL).

2. **Identify Unique Instructions**  
   From the `riscv-objdump` output of application code, identify **15 unique instructions**.

3. **Decode Instructions**  
   For each of the identified instructions, determine the **32-bit binary instruction code** in their specific format.

---

## RISC-V Instruction Types

### 1. R-Type Format
R-type instructions perform operations between registers.
Example: `ADD` (x1 = x2 + x3)

### 2. I-Type Format
I-type instructions involve immediate values.
Example: `LW` (x4 = MEM[x5 + imm])

### 3. S-Type Format
S-type instructions are used for memory store operations.
Example: `SW` (MEM[x5 + imm] = x4)

### 4. B-Type Format
B-type instructions perform conditional branches.
Example: `BEQ` (if x6 == x7, branch to offset)

### 5. U-Type Format
U-type instructions load or modify upper immediate values.
Example: `LUI` (x1 = imm << 12)

### 6. J-Type Format
J-type instructions are used for jumps.
Example: `JAL` (x1 = PC + 4, PC = PC + offset)

---

## Instruction Decoding Table

The following table provides the 15 unique instructions, their types, and their 32-bit binary representations:

| **Instruction** | **Type**   | **Binary Pattern**               | **Explanation**                                   |
|------------------|------------|-----------------------------------|---------------------------------------------------|
| ADD              | R-Type     | `0000000 00010 00011 000 00100 0110011` | Adds values in registers x2 and x3, stores in x4. |
| SUB              | R-Type     | `0100000 00010 00011 000 00100 0110011` | Subtracts x3 from x2, stores in x4.              |
| LW               | I-Type     | `0000000 00010 00100 010 00001 0000011` | Loads a word from memory address into x1.         |
| SW               | S-Type     | `0000000 00101 00100 010 00001 0100011` | Stores word from x1 to memory at x5 + offset.    |
| BEQ              | B-Type     | `0000000 00110 00111 000 01000 1100011` | Branches if x6 equals x7.                        |
| BNE              | B-Type     | `0000000 00110 00111 001 01000 1100011` | Branches if x6 does not equal x7.               |
| JAL              | J-Type     | `0000000 00000 00101 000 00010 1101111` | Jumps to label, stores return address in x5.     |
| JALR             | I-Type     | `0000000 00001 00100 000 00000 1100111` | Jumps to address in x4 + imm, stores PC+4 in x1. |
| LUI              | U-Type     | `0000000 00000 00100 000 00000 0110111` | Loads upper immediate value to x4.              |
| AUIPC            | U-Type     | `0000000 00000 00100 000 00000 0010111` | Adds upper immediate value to PC, stores in x4. |
| NOP              | I-Type     | `0000000 00000 00000 000 00000 0000001` | No operation.                                    |
| AND              | R-Type     | `0000000 00010 00011 111 00100 0110011` | Logical AND of x2 and x3, result in x4.          |
| OR               | R-Type     | `0000000 00010 00011 110 00100 0110011` | Logical OR of x2 and x3, result in x4.           |
| XOR              | R-Type     | `0000000 00010 00011 100 00100 0110011` | Logical XOR of x2 and x3, result in x4.          |
| SLT              | R-Type     | `0000000 00010 00011 010 00100 0110011` | Sets x4 to 1 if x2 < x3.                         |

---

## Conclusion

In Task 3 of the RISC-V Internship program, the focus was on understanding and decoding various RISC-V instruction formats (R, I, S, B, U, and J). By analyzing the `riscv-objdump` output, we identified 15 unique instructions and provided their corresponding 32-bit binary representations. This task enhanced our understanding of RISC-V instruction formats and how they are encoded in machine language, helping in building a strong foundation for low-level programming and system design.

---
Here are the screenshots for the RISC-V Instruction Decoding:

![RISC-V Instruction Decoding](./TASK-3/image1.png)
![RISC-V Instruction Decoding](./TASK-3/image2.png) 
![RISC-V Instruction Decoding](./TASK-3/image3.png) 
 
 ---

## How to Run

### Steps to Analyze and Decode Instructions

1. **Setup RISC-V Toolchain**
   - Install RISC-V GCC and associated tools:
     ```bash
     sudo apt update
     sudo apt install gcc-riscv64-linux-gnu gdb-multiarch
     ```

2. **Generate `riscv-objdump` Output**
   - Compile application code to create an ELF file:
     ```bash
     riscv64-unknown-elf-gcc -o application.elf application.c
     ```
   - Generate the assembly dump:
     ```bash
     riscv64-unknown-elf-objdump -d application.elf > objdump_output.txt
     ```

3. **Decode Instructions**
   - Use the RISC-V manual to decode instructions from the dump.

---
</details>


# Task 4
<details>
 <summary> Functional Simulation of RISC-V Core</summary>
 
This project involves performing a functional simulation of a RISC-V core using a provided Verilog netlist and testbench. The task was completed as part of the RISC-V Internship Program.

### Objective
Simulate the RISC-V core using the provided Verilog netlist and testbench to verify its functionality. The simulation results are captured and visualized using waveform snapshots.
 
### Steps
# RISC-V Core Functional Simulation

This repository contains the necessary files and instructions to simulate a RISC-V core using Verilog. The simulation setup includes the RISC-V hardware description (netlist) and a testbench file for input stimuli.

## Steps to Run the Simulation

### 1. Download Files
- **Verilog Netlist**: The hardware description file for the RISC-V core (`netlist.v`).
- **Testbench**: The file (`testbench.v`) provides input stimuli and expected outputs for the simulation.

### 2. Set Up Simulation Environment

#### Install Required Tools
 Make sure the following tools are installed:
- **iverilog** for compiling Verilog code:
  ```bash
  sudo apt-get install iverilog
  ```
- **gtkwave** for waveform visualization:
  ```bash
  sudo apt-get install gtkwave
  ```
- **Prepare** Simulation Files
 Create a directory for organizing your simulation files:

  ```bash
  mkdir -/riscv_simulation
  ```
 Place netlist.v and testbench.v into this directory.
 

### 3. Load Verilog Files into the Simulator
Compile the Verilog netlist and testbench using iverilog:

  ```bash
  iverilog -o risc_v_simulation.vvp netlist.v testbench.v
  ```
This will generate the risc_v_simulation.vvp output file, which contains the compiled simulation.

### 4. Run Functional Simulation
Execute the simulation with the following command:

 ```bash
 vvp risc_v_simulation.vvp
 ```
### 5. Observe the Output
After running the simulation, you can observe the output signals generated by the RISC-V core. If you want to visualize the waveforms, use gtkwave:

 ```bash
 gtkwave output.vcd
 ```
This will open the waveform viewer for detailed signal analysis.

Here are the screenshots for the Functional Simulation of RISC-V Core:

![Functional Simulation of RISC-V Core](./TASK-4/image1.png)
![Functional Simulation of RISC-V Core](./TASK-4/image2.png) 
![Functional Simulation of RISC-V Core](./TASK-4/image3.png) 
![Functional Simulation of RISC-V Core](./TASK-4/image4.png) 
![Functional Simulation of RISC-V Core](./TASK-4/image5.png) 
 

---
</details>
