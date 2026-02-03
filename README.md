# 10-DAYS-RISC-V-MYTH-WORKSHOP-BY-VSD
Documentation of Workshop by VSD - NASSCOM RFISC-V MYTH.

Day 1: 30-01-2026
Actions done: 
1. GitHub Codespace setup: riscv codespace link provided with intro mail opened a codespace. Followed  " Code--> Codespaces-->Create a codespace om the main"
   <img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/1cffd514-075a-4770-b686-5f45814121d0" />
   
2. Verified setupo and Sample program run in codespace
   <img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/ed73971a-7ac5-4069-b17a-4ea0ca5be713" />
   
3. Linux setup done in cloud
   a. Clicked on Follow forwarded address link of noVNC Desktop Port under PORTS Tab in the codespace
   <img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/2bb596ff-c927-42eb-948c-d114885252ed" />
   
   b. new window appeared
   <img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/a53db4b1-1c0c-4ec1-8386-176071b2bd50" />
   
   c. Clicked on vnc_lite.html,
   <img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/2358c356-3d6a-4059-b189-51cd08083f34" />
   
   d. opened a terminal in the linux screen appeared in browser tab
   <img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/69863b12-5e0a-4313-a07f-9422a11d9538" />
   
   e. Navigated to samples folder using the following commands
   
      > cd /workspaces/vsd-riscv2
      > 
      > cd samples
      > 
      > ls -ltr
   <img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/71f4d047-00cf-4527-b2b1-0ec8d3628657" />
   
   d. ran sample program to find sum and saw output using following commands (using Native GCC (x86))
   
      > gcc sum1ton.c
.     >  ./a.out
   <img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/d62a7e79-d7fc-4741-8ccd-1ab45f471831" />
   
   e.  compiled the same program for RISC-V and ran it on the Spike ISA simulator
   
      > riscv64-unknown-elf-gcc -o sum1ton.o sum1ton.c
      > 
      > spike pk sum1ton.o
   <img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/a514839e-ebf2-45af-87a1-57588021fa40" />
   
   f. opened sum1ton.c on gedit
   
      > gedit sum1ton.c &
   <img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/91c6cd55-fb67-4c7c-b135-dc262ffe22eb" />
   
   g. tried to change value and save, output changed
   <img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/5ee08b92-3a99-41d7-b70c-f73515499312" />


Day 1 outcomes

Launched a full Linux desktop inside GitHub Codespaces
Compiled and executed a C program with native GCC
Compiled and executed the same program on a RISC-V target using Spike
Edited and rebuilt the code using a GUI editor over noVNC


Day 2: Watching workshop videos

RV Day 1 - Introduction to RISC-V ISA and GNU compiler toolchain

D1SK1 - Introduction to RISC-V basic keywords

0-RV_D1SK1_L1_Introduction

ISA - 

C program to run on a chip layout, compiled in its assembly language [program, thren binary format--> these bits get inside the chip layout and provide re2quired output

Between RISC V and layout we have RTL- hardware description lamguage

RISC V is some specifications, RTL implements these specifications, so from RTL to layout is a standard RTL to GDSII flow 

The flow: Starts from architecture --> implemented using an RTL ---> Then it goes to layout??(didnt understand that part clearly)

<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/3fdc5d15-c6fe-40e3-9cac-439ff0da90b4" />

1-RV_D1SK1_L2_From Apps To Hardware

How an app runs on a hardware?
Apps written in high level languages gets converted to assembly language by compilers (sccording to the OS). The result is instruction set(varies with different hardware. eg, ARM, x86, RISC-V). Instruction set is converted to machine language(hex, ie binary) which lets the chip layout to execute specific instructions.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/ba37bd69-6766-4214-a74f-9c2e9ce16030" />

The abstract interface betwween the high level language code and the chiplayout is called Instruction Set Architecture. It represents the hardware(Architecture of the computer). 

In between compiler and layout, there is assembler that taskes instrictions and give binary pattern. This is possible due to RTL implementation. RTL understands instructions like "add x6, x10, x6". 

high level RTL --> netlist --> physical design implementation

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/873dba66-da1a-48eb-9669-f2e3d3b33e0e" />

RV_D1SK1_L3_Detailed Description Of Course Content

pseudo instructions

base integer instructions RV64I

multiply extension RV64M

single and double precision floating point extension RV64F & RV64D

Application Binary Interface

memory allocation and stack pointer

RV_D1SK2_L1_C Program To Compute Sum From 1 to N

<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/cab28558-5d05-488f-a337-1e612bc2a784" />

RV_D1SK2_L2_RISCV GCC compile And Disassemble

<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/bd5e5e36-b4ce-40bd-804d-fdb577805864" />





