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

**Example: ADD r3,r1,r2**
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

### 15 Unique instructions: 

#### Instructions: 
All of these are referenced from 

##### Image 1
![Image 1](https://github.com/user-attachments/assets/18f62720-66f6-47d0-b747-4881de58a708)   
![image](https://github.com/user-attachments/assets/1f50842c-6d18-471a-9fa9-2c3982027e0c)


##### Image 2
![Image 2](https://github.com/user-attachments/assets/c59af6a0-115e-474a-96fd-60c257ff54d4)
![image](https://github.com/user-attachments/assets/179da90c-17cc-4d55-9ff6-ec6bbc52813a)


##### Image 3
![Image 3](https://github.com/user-attachments/assets/d3d56790-9943-4573-acc0-6ccbfa6169cd)
![image](https://github.com/user-attachments/assets/1fcaa41c-acda-46a6-a79e-3842234013c5)


##### Image 4
![Image 4](https://github.com/user-attachments/assets/17111d89-6b18-4d1a-97e0-9cf32b9adb49)
![image](https://github.com/user-attachments/assets/136364e4-32d7-4b93-ba71-6b01933fd7df)


##### Image 5
![Image 5](https://github.com/user-attachments/assets/224dec09-1377-4553-b07b-b66ac8f3f6ee)
![image](https://github.com/user-attachments/assets/b0266bcf-c6c6-4d55-bab4-9c8d45a89ccd)


##### Image 6
![Image 6](https://github.com/user-attachments/assets/442caa30-6254-40d1-8ace-0d82cb84a393)
![image](https://github.com/user-attachments/assets/52c66fdb-5219-4ed7-8a34-317710687aa5)


##### Image 7
![Image 7](https://github.com/user-attachments/assets/5df76f64-8274-4489-8725-72a9704a298d)
![image](https://github.com/user-attachments/assets/63418f79-df9f-4b81-9e9e-3a914f3980c6)


##### Image 8
![Image 8](https://github.com/user-attachments/assets/f0eb2f7c-8454-4803-9c55-f9316fb0d309)
![image](https://github.com/user-attachments/assets/106f50a5-3766-4a20-adb9-0afe51b37865)


##### Image 9
![Image 9](https://github.com/user-attachments/assets/5d450aec-3f62-4611-affe-c30c0f007077)
![image](https://github.com/user-attachments/assets/2b88806e-3881-41e5-9731-782df4dc47a0)


##### Image 10
![Image 10](https://github.com/user-attachments/assets/729e8568-d1f4-4700-b9c5-5ebf126687c3)
![image](https://github.com/user-attachments/assets/f584b99e-dcba-4593-870a-e59894a70576)


##### Image 11
![Image 11](https://github.com/user-attachments/assets/34dc0994-e3cc-4ae7-b361-e1de0f0db23f)
![image](https://github.com/user-attachments/assets/11f1c87b-674c-4c15-8775-3cdfbbf84746)


