# 🧠 TohCore – A Custom Single-Cycle RISC-V Processor

**TohCore** is a fully custom-designed single-cycle RISC-V processor, built using [Logisim Evolution](https://github.com/logisim-evolution/logisim-evolution). It faithfully implements a core subset of the RISC-V instruction set architecture, demonstrating how real-world processors decode, execute, and interact with memory at the hardware level.

This project is a hands-on demonstration of digital design and computer architecture — featuring ALU control, register file management, PC logic, and branching/jumping mechanisms, all designed from the gate level up.

---

### ⚙️ Key Features

- 🧮 **RISC-V Instruction Set Support**  
  Implements core instructions including:
  - Arithmetic: `add`, `sub`, `and`, `or`, `sll`, `sra`, `slt`, `sltu`
  - Immediate: `addi`, `andi`, `ori`, `xori`, `slli`, `srai`, `slti`, `sltiu`
  - Memory: `lw`, `sw`
  - Branching: `beq`, `bne`
  - Jumping: `jal`, `jalr`

- 🧠 **Single-Cycle CPU Architecture**  
  All instruction stages — fetch, decode, execute, memory, and write-back — occur in one clock cycle, enabling a clean, educational design ideal for hardware simulation and learning.

- 🧰 **Custom ALU**  
  A logic-constructed Arithmetic Logic Unit that performs a range of binary and arithmetic operations based on ALU control signals derived from instruction decoding.

- 🧾 **Register File Implementation**  
  32 general-purpose registers with two asynchronous read ports and one synchronous write port, all fully functional within the datapath.

- 🔁 **PC Logic & Control Flow**  
  Instruction-based branching, jumping, and PC update logic built from control signals — including full support for immediate encoding formats and offsets.

- 💾 **Memory System**  
  Separate instruction and data memory with address decoding and proper load/store alignment handling.

---

### 📁 Project Structure

```
cpu/             # Logisim circuit files (.circ) for the CPU and its components
tests/           # RISC-V assembly test cases
tools/           # Assembler and conversion tools for testing and memory loading
harnesses/       # Autograder and verification harnesses
test.sh          # Script to assemble, run, and verify tests
README.md        # You're here!
metadata.yml     # Project configuration file
```

---

### 🧪 How to Test

You can verify the CPU using prewritten RISC-V assembly test cases:

```bash
./test.sh
```

This script assembles the test cases, loads them into the CPU design, and verifies the output against reference logs.

---

### 📚 Learning Highlights

Through building this CPU, I explored:
- Digital logic design using multiplexers, adders, and control gates
- Modular hardware construction and datapath design
- Instruction decoding and control signal generation
- State machine behavior and clock-synchronous logic
- Memory-mapped I/O and register-based architecture

---

### 🔮 Future Extensions

- ⏩ **Multi-cycle or pipelined version**
- ✅ **Hazard detection and forwarding logic**
- 🧵 **I/O peripherals for basic system interaction**
- 📈 **Cycle-accurate performance monitoring**

---

### 👤 Author

**Stacey Toh**  
CPU built using Logisim Evolution  
Created to explore the fundamentals of modern processor design

---

### 📜 License

MIT License — free to fork, build, and improve!

---

Whether you're a student, hobbyist, or computer architecture nerd — feel free to try it, break it, and build your own microarchitecture on top of it.

