# vsd_squadron
## Task 1:

Firstly, I have downloaded the virtual box from the links provided to us and
loaded a linux version with image dock file sent, Then I have successfully run the
virtual machine and compiled the tasks.

Initial task is:-

### write a program to compile the sum of first n natural numbers in c:

![image](https://github.com/user-attachments/assets/c5c65959-0f66-48b3-8686-d626c63d6d2d)


This is the code to run in terminal to get output:


![image](https://github.com/user-attachments/assets/06bc9aeb-f7b3-4572-b44f-719e189ea46b)


A program is run to obtain risc-v version of the code previously written in c:
![image](https://github.com/user-attachments/assets/bec40d22-d99e-416a-82db-03d99369ab9e)





As the whole version of above code looks lengthier with different commands, we have obtained the required main 
part to compare the execution in assembly language:



![image](https://github.com/user-attachments/assets/04d8a662-db78-40e4-8614-c7000e83b5f0)



## Task 2:

For this task, we are instructed to observe the spike simulation and understand the execution of assembly code using -o1 and -ofast directives, I understood the principle
and working of the whole program and how various registers like stack pointer and r5 are increasing, understood how the interface explains the process itself.

### Dump file RISC-V assembly code:

![image](https://github.com/user-attachments/assets/a86e0441-2dab-4380-a2c6-965ca58aab54)

### -o1 execution (sub task 1):

![image](https://github.com/user-attachments/assets/47950e9d-820a-41d6-a746-459fcd0a3652)

### -o fast execution (sub task 2):

![image](https://github.com/user-attachments/assets/92abae19-ea09-40e9-8835-7ece050036b2)

### Multiplication of first n natural numbers (C program) (sub task 3):

![image](https://github.com/user-attachments/assets/78089dfa-df92-4466-86b3-d6497982396d)

### Spike file for the new c program (sub task 4):

Dump file:

![image](https://github.com/user-attachments/assets/de84c4b0-b891-433f-a001-acd95ddc0ab2)

Spike simulation:

![image](https://github.com/user-attachments/assets/e16a2aa1-139d-449c-ad9f-3275ec63ec7e)

## Task 3:

Various instructions of the RISC-V processor:

### INTRODUCTION:

Firstly to understand, there are two releases of RISC-V documentation namely, Unpreviliged and Previliged specifications. We can read any one of them to understand the instruction 
set of RISCV processor. The very important use of learning these formats is the very intention of understanding the instruction decoding and the way it is getting compiled.
Some of the other uses are:

1. **Instruction Set properties** 

2. **Debugging** 

3. **Easy Design**

4. **Pipelining**

### RISC-V R-Type Instructions

R-type instructions are used for operations that functions among registers only. These instructions generally perform arithmetic, logical, and shift operations.

#### Format: ![image](https://github.com/user-attachments/assets/522d5257-b978-4c93-9412-330372e1ab66)


- **opcode**: Specifies the operation .
- **rd**: Destination register.
- **funct3**:specifies the operation.
- **rs1**: First source register.
- **rs2**: Second source register.
- **funct7**:specifies the operation.


### S-Type Instructions

#### Format:![image](https://github.com/user-attachments/assets/04aca468-7811-480b-9f7c-d0cf30334753)


**Example: SW rs1, imm(rs4)**
- **opcode**: types of instruction
- **imm**: Immediate value (seperated into immediate[11:5] and immediate[4:0])
- **rs1**: Base address register
- **rs2**: Source register to be stored
-  **funct3**: 010 (for SW)

### B-Type Instructions

#### Format: ![image](https://github.com/user-attachments/assets/795c5e09-e97d-4df6-99b6-ab896b26880a)


**Example: BEQ rs3, rs2, imm**
- **opcode**: type of instruction like branch
- **imm**: Immediate value (seperated into immediate[12], immediate[10:5], immediate[4:1], immediate[11])
- **rs1**: Source register 1
- **rs2**: Source register 2

### U-Type Instructions

#### Format:

![image](https://github.com/user-attachments/assets/baf64187-b5aa-4464-8a42-f89520c549ec)

**Example: LUI rd, imm**
- **opcode**: intstruction type
- **imm**: Upper 20 bits of the immediate value
- **rd**: Destination register

### J-Type Instructions

#### Format:

![image](https://github.com/user-attachments/assets/c4a497dc-e025-4177-b4d5-b56fa85efbf9)


**Example: JAL rd, imm**
- **opcode**: instruction type
- **imm**: Immediate value (seperated into imm[20], imm[10:1], imm[11], imm[19:12])
- **rd**: Destination register (stores the return address)

