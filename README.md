# Simple 9-Bit Processor (Verilog)

## Overview

A simple multi-cycle 9-bit processor designed in structural Verilog.
The processor uses an FSM-based control unit, shared internal bus, register file, and arithmetic unit to execute basic instructions including move, immediate load, addition, and subtraction. 

---

## Features

### Supported Instructions

| Opcode | Instruction | Description                       |
| ------ | ----------- | --------------------------------- |
| `000`  | `mv Rx,Ry`  | Move data between registers       |
| `001`  | `mvi Rx,#D` | Load immediate data into register |
| `010`  | `add Rx,Ry` | Add two registers                 |
| `011`  | `sub Rx,Ry` | Subtract two registers            |

## How It Works

1. Instruction is loaded from `DIN` into `IR`
2. FSM decodes opcode and generates control signals
3. Multiplexer selects bus source
4. Registers or ALU operate depending on instruction
5. Result is written back to destination register
6. `done` signal indicates instruction completion


