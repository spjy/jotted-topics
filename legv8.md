---
header: LEGv8 
description: Not as complicated as your ARM.
---

# Hardware Terminology

### Doubleword

Groups of 64 bits.

### Word

Groups of 32 bits.

### Registers

Registers are used for frequently accessed data.

In LEGv8, there are **32 registers** that are 64 bits wide. They are referred to by their number ranging from `X0-X30`. The final register is `XZR` which is the 'zero register' that always contains 0.

Registers|Purpose|Notes
:-----:|:-----:|:-----:
`X0`|Return value|The return value of a function is stored here.
`X1-X7`|Passed parameters|Function argument variable storage.
`X8`|Indirect result location register| 
`X9-X15`|Temporary variables| 
`X16-X17`|Scratch/temporary register|
`X18`|Platform/temporary register| 
`X19-X27`|Saved| 
`X28`|Stack Pointer (SP)|Points to the memory address of the top of the stack.
`X29`|Frame Pointer (FP)|Points to the memory address at the bottom of the stack.
`X30`|Link Register (LR)|Points to the return address after branching.
`XZR`|Zero Register (XZR)|Contains a constant value of 0.

### Memory

There are $2^{62}$ memory words. Memory is set up like a single dimensional array.

LEGv8 uses **byte addressing**, so each memory address index (with length of one byte) can be accessed. Therefore, since LEGv8 is a 64 bit architecture, memory addresses are split up into groups of 8 bytes or 64 bits (a [doubleword](#doubleword)).

```
Memory[0]
Memory[8]
Memory[16]
...
```

### Stack

A stack is a portion of memory allocated towards a program.

# Computer Instruction Representation


### Instruction

A series of 32 binary bits that represent an instruction.

## Fields

A segment of an instruction. Essentially, the instruction is broken up into a certain number of bits to represent a meaningful operand.

### opcode

An opcode is the type of operation that is being executed. For example `ADD`, `ADDI` or `LDUR`.

### Rm

Rm is the second register source operand

### shamt

shamt is the shift amount.

### Rn

Rn is the first register source operand.

### Rd

Rd is the destination register operand. It receives the result of the operation.

### address

Memory address offset

### op2

Opcode option.

### Rn

Rn is the CPU register.

### Rt

Rt is the memory address.

### immediate

Immediate is the constant.

### pc_offset

PC_Offset is the the program counter offset. This specifies how many bytes in the instruction memory to move from the current address the program counter is pointing to.

### R-Type Instruction (Register)

R-Type instructions manipulate registers.

**opcode**|**Rm**|**shamt**|**Rn**|**Rd**
:-----:|:-----:|:-----:|:-----:|:-----:
11 bits|5 bits|6 bits|5 bits|5 bits

In a normal machine instruction, this would look like: `opcode Rd, shamt, Rn, Rm`.

#### R-Type Instruction Example

A conversion from an instruction to a decimal representation of the instruction:

`ADD X1, X2, X3` $\implies$ `1112 3 0 2 1`

### D-Type Instruction (Data Transfer)

R-Type instructions manipulates data between the registers and memory.

**opcode**|**address**|**op2**|**Rn**|**Rt**
:-----:|:-----:|:-----:|:-----:|:-----:
11 bits|9 bits|2 bits|5 bits|5 bits

In a normal machine instruction, this would look like: `opcode Rt, [Rn, #address]`.

#### D-Type Instruction Example

A conversion from an instruction to a decimal representation of the instruction:

`LDUR X1, [X2, #3]` $\implies$ `1986 3 0 2 1`

### I-Type Instruction (Immediate)

R-Type instructions manipulate constants.

**opcode**|**immediate**|**Rn**|**Rd**
:-----:|:-----:|:-----:|:-----:|:-----:
10 bits|12 bits|5 bits|5 bits

In a normal machine instruction, this would look like: `opcode Rd, Rn, #immediate`.

#### I-Type Instruction Example

A conversion from an instruction to a decimal representation of the instruction:

`ADDI X1, X2, #3` $\implies$ `836 3 2 1`

### B-Type Instruction (Branch)

B-Type instructions handle branching (jumping).

**opcode**|**pc_offset**
:-----:|:-----:
6 bits|26 bits|

In a normal machine instruction, this would look like: `opcode pc_offset`.

#### B-Type Instruction Example

A conversion from an instruction to a decimal representation of the instruction:

`B Skip` $\implies$ `5 25`

where `Skip` is the number of bytes to skip. In this case, it will skip $25 bytes \cdot 4 = 100 bits$.

B-Type Instruction|Meaning|Note
:-----:|:-----:|:-----:
`B Label`|Branch|Jumps to `Label`.
`BR LR`|Branch to register|Jumps to register `LR`'s address
`BL Label`|Branch with link|Jumps to `Label` and stores the address of the next instruction.

### CB-Type Instruction (Condiitonal Branch)

CB-Type instructions handle conditional branching.

**opcode**|**pc_offset**|**Rt**
:-----:|:-----:|:-----:
8 bits|19 bits|5 bits

In a normal machine instruction, this would look like: `opcode Rt, pc_offset`.

#### CB-Type Instruction Example

A conversion from an instruction to a decimal representation of the instruction:

`CBZ X1, Skip` $\implies$ `181 25 1`

where `Skip` is the number of bytes to skip. In this case, it will skip $25 bytes \cdot 4 = 100 bits$.

### IW-Type Instruction (Immediate Wide)

IW-Type instructions handle large constants.

**opcode**|**block_number**|**constant**|**Rd**
:-----:|:-----:|:-----:|:-----:
9 bits|2 bits|16 bits|5 bits

In a normal machine instruction, this would look like: `opcode Rd, constant, block_number`.

#### IW-Type Instruction Example

A conversion from an instruction to a decimal representation of the instruction:

`MOVZ X1, 256, LSL 0` $\implies$ `421 1 256, 0`

