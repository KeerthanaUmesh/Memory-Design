
# Memory-Design
Design of 4X4 16-bit SRAM Memory Array Using Cadence Virtuoso tool.

## About
The project involves the design of a 4X4 16-bit SRAM Memory Array using *Cadence Virtuoso* built using *GPDK 180nm* Technology node.

## Introduction
![Picture1](https://github.com/KeerthanaUmesh/Memory-Design/assets/147648970/bca1c502-a462-4d61-84f6-fdd75aa42d70)

-------------

### **SRAM(Static Random Access Memory )** 
* Is a type of random access memory (RAM) that is volatile, meaning retains data bits in its memory as long as the  power is being supplied.
* In the *Memory Hierarchy* ,SRAM is often used for cache memory, which sits between the CPU and the main memory(DRAM).
* Unlike DRAM, SRAM does not require refreshing, making it faster and more energy-efficient.
* SRAM comes with a trade-off, it is more expensive and less dense compared to DRAM.
<!---
-------------
### **Applications of SRAM**

SRAM is widely used in various applications due to its speed, low power consumption, and suitability for cache memory. Some key applications include:

1. **Cache Memory:** SRAM is commonly used as cache memory in CPUs to provide fast access to frequently used data.

2. **Register Files:** SRAM is used in register files within microprocessors for storing temporary data during computation.

3. **Networking Devices:** SRAM is employed in networking devices for buffering and storing routing tables.

4. **Embedded Systems:** SRAM finds applications in embedded systems, providing quick access to critical data.
-->


--------
### **Objectives**

The main goal of this project is to develop a thorough understanding  of SRAM by designing a 6T SRAM cell, along with its associated peripheral circuitry, utilizing Cadence Virtuoso tools on the 180nm technology(GPDK180).This project aims to explore various aspects of  SRAM design with a focus on optimizing read and write  stability by carefully selecting transistor sizes.


------
# SRAM Memory Architecture
![Screenshot 2024-04-02 220311](https://github.com/KeerthanaUmesh/Memory-**Design/assets/147648970/33227bd5-99c6-484a-96b7-2fca1a0370d4)


SRAM (Static Random Access Memory) architecture comprises key components including word lines, which activate specific rows of memory cells, bit lines for data input and output, and decoders for both row and column selection. When data needs to be read or written, the row decoder selects the appropriate row by activating the corresponding word line, while the column decoder enables the desired column by activating the appropriate bit lines. This efficient arrangement facilitates rapid access to data stored in the memory array
-------------------------
# Design Methodology

This section outlines the comprehensive design flow for a 6T SRAM cell, encompassing both the cell itself and the design considerations for its essential peripheral circuits.

## SRAM Cell Design

When designing an SRAM cell, careful consideration of transistor sizing, particularly the W/L ratio, is essential to ensure optimal performance. The following points outline the critical aspects:

*Preservation of Stored Information (Avoiding Read Upset ):
Transistor sizing, specifically the W/L ratio, must be chosen to prevent the destruction of stored information during the data-read operation.

*Allow Data Modification during Write Operation:
The SRAM cell design should facilitate the modification of stored information during the data-write phase.

**The sizing of the transistors in an SRAM cell is determined by two key parameters:**
a) **Cell Ratio (CR)** :
 - The data-read operation should not destroy the stored information in the SRAM Cell i.e., Read Upset.To accomplish this, it is important to maintain appropriate transistor sizing.
 -For this project, I've utilized a cell ratio, β, of 1.5 and set the width of all PMOS transistors, Wp, to 400 nm.
```
 Cell ratio, β ={ (W\L) of pull down transistor(NMOS) } / {(W\L) of access transistor(NMOS) } 
```

B) **Pull Down (PR)** :
 - The cell should allow the modification of the stored information during the data- write phase.To accomplish this, it is important to maintain appropriate transistor sizing.
 -For this project, I've utilized a Pull up ratio,PR, of 0.85 and set the width of all PMOS transistors, Wp, to 400 nm.
```
 Pull Up ratio, PR ={ (W\L) of pull up transistor(PMOS) } / {(W\L) of access transistor(NMOS) } 
```








