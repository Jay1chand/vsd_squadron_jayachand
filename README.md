# VSD_SQUADRON MINI RISC-V TRAINING

## **Basic details**
* **Name:** S.V.Jaya Chand
* **College:** IIT Indore 
* **Email ID:** [Jaya chand](svjayachand@gmail.com) 
* **GitHub Profile:** [Jay1chand](https://github.com/Jay1chand/vsd_squadron_jayachand)

----------------------------------------------------------------------------------------------------------------

<details>
	
<summary> <b>Task 1 :</b></summary>

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
</details>

------------------------------------------------------------------------------------------------------------------

<details>
<summary><b>Task 2:</b></summary> 

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

</details>

------------------------------------------------------------------------------------------------------------------

<details>
<summary><b>Task 3:</b></summary>

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
All of these are referenced from the above code I have compiled in the virtual box, The below Image set each contains an image of the instruction code(hexadecimal)
and assembly language corresponding to it.

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
![image](https://github.com/user-attachments/assets/8c252bd6-1313-450a-9efb-3e0510c9b171)

</details>

------------------------------------------------------------------------------------------------------------------

<details>
<summary><b>Task 4:</b></summary>

Reference github repository with existing code for a RISC machine is : [![GitHub](https://img.shields.io/badge/-GitHub-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/vinayrayapati/rv32i/blob/main/iiitb_rv32i.v)

GTK Wave already installed so no need to follow the step from above github readme
Then the following steps are followed to open the gtk wave simulation of the above source code:
1. Create a new directory with your name
2. Create two files namely jayrv32.v jayrv32_tb.v  
3. Copy the code from the reference github repo and paste it in your verilog and testbench files.
4. To run and simulate the verilog code, enter the following command:  
	```
	$ iverilog -o jayrv32i jayrv32.v jayrv32_tb.v
	$ ./jayrv32i
	```
5. To see the simulation waveform in GTKWave, enter the following command:
	```
	$ gtkwave iiitb_rv32i.vcd
	```

6. The GTKWave will be opened and following window will be appeared  
  
![image](https://github.com/user-attachments/assets/8ebb8c40-d549-4bd2-9521-92a4200b617c)

As shown in the figure below, all the instructions in the given verilog file is hard-coded, the designer has hard-coded each instructions based on their own pattern. Hence the 32-bits instruction that we generated in above task will not match with the given instruction.

![image](https://github.com/user-attachments/assets/512edc06-4524-43f7-833f-e3d087869a38)

The below is simulated outputs of the above verilog code given to us as cloned from https://github.com/vinayrayapati/rv32i.gitmy_riscv_project

I have written the explanation below the corresponding images as i have'nt run the opcodes once each time, I have run them all together so we understand what
instructions underwent through opcode (in the form of PC) and the registers which are below it.

![image](https://github.com/user-attachments/assets/ef3dce57-b286-479e-911e-52dfafaf4007)

The explanations for this case is as follows:

##### Instruction 1: ADD R6, R2, R1

0x02208300 represents the operation add r6, r1, r2. 
Addition 1 + 2, resulting in 3

##### Instruction 2: SUB R7, R1, R2

0x02209300 represents the operation SUB R8, R1, R3.
Substraction 1-2, resulting in -1

##### Instruction 3: AND R8, R1, R3

0x0230A400 represents the operation AND R8, R1, R3.
And 3 and 1 results in 1

##### Instruction 4: OR R9, R2, R5

0x02513480 represents the operation OR R9, R2, R5
OR operation (0010 | 0101) results in 7

##### Instruction 5: XOR R10, R1, R4

0x024005c0 represents the operartion XOR R10, R1, R4
XOR (0001 ^ 0100) results in 5

##### Instruction 6: SLT R1, R2, R4

0x024155080 represents the operation SLT R1, R2, R4
2 < 4, the output is 1

##### Instruction 7: ADDI R12, R4, 5

0x00520693 represnts the operation  ADDI R12, R4, 5
R4 (4) added to the immediate value (5) results in 9

![image](https://github.com/user-attachments/assets/d5d569b3-89ed-4567-9c1a-db0e75078db8)

##### Instruction 8: BEQ R0, R0, 15

0x00F00802 represents the operartion BEQ R0, R0, 15
Both values equal so PC incremented by 15 PC=PC+15

##### Instruction 9: BNE R0, R1, 20

0x01409002 represnts the operation BNE R0, R1, 20
both values not equal PC updated to PC+20 =46

And from 130 seconds the default value will be shown which is useless as we didnt provide any instructions after that particular time.
</details>

------------------------------------------------------------------------------------------------------------------

<details>
<summary><b>Task 5:</b></summary> 

	
## IMPLEMENTATION OF 2 BIT COMPARATOR:

### Comparator:

A 2-bit comparator is a digital circuit designed to compare two 2-bit binary numbers and determine their relative magnitude. This comparison results in three possible outputs: whether the first number is less than, equal to, or greater than the second number.

#### Working:

**Given two 2-bit binary numbers, A=A1A0 and B=B1B0**
*	A1 and B1 are the most significant bits (MSB).
*	A0 and B0 are the least significant bits (LSB).
**The 2-bit comparator will produce three outputs**
*	A < B: High (1) when AA is less than BB.
*	A = B: High (1) when AA is equal to BB.
*       A > B: High (1) when AA is greater than BB.

##### TRUTH TABLE:

![image](https://github.com/user-attachments/assets/19978a61-59bc-47c2-a9a4-c8edbe552293)

###### **COMPONENTS REQUIRED**

*  VSD Squadron mini
*  Push Buttons for Input of binary data
*  3 LED for displaying output data
*  Breadboard
*  Jumper Wires
*  VS Code for Software Development
*  PlatformIO multi framework professional IDE

###### **HARDWARE CONNECTIONS**

* **Input:** Four input of single bit are connected to the GPIO pins of VSDSquadron Mini via push buttons mounted on the breadboard. 
* **Outputs:** Three LEDs are connected to display the result of COMPARATOR
* The GPIO pins are configured according to the Reference Mannual, ensuring the correct flow of signals between the components

###### Circuit diagram:

![image](https://github.com/user-attachments/assets/642beb60-dda3-446f-842a-41fd61db28c4)


##### HOW TO PROGRAM

```
// 2-Bit Comparator Implementation

// Included the required header files
#include<stdio.h>
#include<debug.h>
#include<ch32v00x.h>

// Defining the Logic Gate Function 
int and(int bit1, int bit2)
{
    int out = bit1 & bit2;
    return out;
}
int or(int bit1, int bit2)
{
    int out = bit1 | bit2;
    return out;
}
int not(int bit)
{
    int out = ~bit & 0x1;
    return out;
}
int xor(int bit1, int bit2)
{
    int out = bit1 ^ bit2;
    return out;
}

// Configuring GPIO Pins
void GPIO_Config(void)
{
    GPIO_InitTypeDef GPIO_InitStructure = {0}; // structure variable used for GPIO configuration
    RCC_APB2PeriphClockCmd(RCC_APB2Periph_GPIOD, ENABLE); // to enable the clock for port D
    RCC_APB2PeriphClockCmd(RCC_APB2Periph_GPIOC, ENABLE); // to enable the clock for port C
    
    // Input Pins Configuration
    GPIO_InitStructure.GPIO_Pin = GPIO_Pin_1 | GPIO_Pin_2 | GPIO_Pin_3 | GPIO_Pin_4;
    GPIO_InitStructure.GPIO_Mode = GPIO_Mode_IPU; // Defined as Input Type
    GPIO_Init(GPIOD, &GPIO_InitStructure);

    // Output Pins Configuration
    GPIO_InitStructure.GPIO_Pin = GPIO_Pin_5 | GPIO_Pin_6 | GPIO_Pin_7;
    GPIO_InitStructure.GPIO_Mode = GPIO_Mode_Out_PP; // Defined Output Type
    GPIO_InitStructure.GPIO_Speed = GPIO_Speed_50MHz; // Defined Speed
    GPIO_Init(GPIOC, &GPIO_InitStructure);
}

// The MAIN function responsible for the execution of program
int main()
{
    uint8_t A1, A0, B1, B0; // 2-bit inputs A and B
    uint8_t A_eq_B, A_lt_B, A_gt_B; // Outputs: A equals B, A less than B, A greater than B
    uint8_t not_A1, not_A0, not_B1, not_B0;
    uint8_t eq_bit1, eq_bit0, lt_bit1, lt_bit0, gt_bit1, gt_bit0;
    
    NVIC_PriorityGroupConfig(NVIC_PriorityGroup_2);
    SystemCoreClockUpdate();
    Delay_Init();
    GPIO_Config();

    while(1)
    {
        // Reading the 2-bit inputs
        A1 = GPIO_ReadInputDataBit(GPIOD, GPIO_Pin_1);
        A0 = GPIO_ReadInputDataBit(GPIOD, GPIO_Pin_2);
        B1 = GPIO_ReadInputDataBit(GPIOD, GPIO_Pin_3);
        B0 = GPIO_ReadInputDataBit(GPIOD, GPIO_Pin_4);
        
        // Calculating A == B
        eq_bit1 = not(xor(A1, B1));
        eq_bit0 = not(xor(A0, B0));
        A_eq_B = and(eq_bit1, eq_bit0);

        // Calculating A < B
        not_A1 = not(A1);
        not_A0 = not(A0);
        lt_bit1 = and(not_A1, B1);
        lt_bit0 = and(eq_bit1, and(not_A0, B0));
        A_lt_B = or(lt_bit1, lt_bit0);

        // Calculating A > B
        not_B1 = not(B1);
        not_B0 = not(B0);
        gt_bit1 = and(A1, not_B1);
        gt_bit0 = and(eq_bit1, and(A0, not_B0));
        A_gt_B = or(gt_bit1, gt_bit0);

        /* Output A == B */
        if(A_eq_B == 0)
        {
            GPIO_WriteBit(GPIOC, GPIO_Pin_5, SET);
        }
        else
        {
            GPIO_WriteBit(GPIOC, GPIO_Pin_5, RESET);
        }

        /* Output A < B */
        if(A_lt_B == 0)
        {
            GPIO_WriteBit(GPIOC, GPIO_Pin_6, SET);
        }
        else
        {
            GPIO_WriteBit(GPIOC, GPIO_Pin_6, RESET);
        }

        /* Output A > B */
        if(A_gt_B == 0)
        {
            GPIO_WriteBit(GPIOC, GPIO_Pin_7, SET);
        }
        else
        {
            GPIO_WriteBit(GPIOC, GPIO_Pin_7, RESET);
        }
    }
}

```

##### **CONCLUSION OF TASK 5:**

*  Input Pins:
*	GPIOD, Pin_1: A1 (Most Significant Bit of A)
*	GPIOD, Pin_2: A0 (Least Significant Bit of A)
*	GPIOD, Pin_3: B1 (Most Significant Bit of B)
*	GPIOD, Pin_4: B0 (Least Significant Bit of B)
*  Output Pins:
*	GPIOC, Pin_5: A==B (LOW if A equals B)
*	GPIOC, Pin_6: A<B (LOW if A is less than B)
*	GPIOC, Pin_7: A>B (LOW if A is greater than B)

In each case the rest 2 bulbs are on only the corresponding case is off.
</details>

------------------------------------------------------------------------------------------------------------------

<details>
<summary><b>Task 6</b></summary>

Build:

![image](https://github.com/user-attachments/assets/8d81f25a-e0bb-4fc7-9fae-dbdcc2ac77ee)

 Upload:

 ![image](https://github.com/user-attachments/assets/f2063a21-255d-4272-8bc2-f98c5d04d0ce)

 Results:

 ![WhatsApp Image 2024-08-15 at 15 27 35_9b22f53f](https://github.com/user-attachments/assets/c35d9113-3fa5-4a5a-91d2-21983f6c349a)

![WhatsApp Image 2024-08-15 at 15 27 36_fc84d81e](https://github.com/user-attachments/assets/57b7704c-2c3f-4fa6-93c0-c791f8560c82)

https://drive.google.com/file/d/13NWGFUxkBlCk39niQ2MiFVxlKv8TUmZk/view?usp=sharing

</details>


------------------------------------------------------------------------------------------------------------------
