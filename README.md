# VLSI design and analysis of 6T SRAM device Using Cadence EDA Tool.
<br>
<h2>1. Abstract :</h2> 
SRAM is now widely used in System on Chip and high performance VLSI circuit.
Adjustment of performance parameters may results in total chip performance
optimization. SRAM cell read and write stability are key challenges in
nanoscale CMOS technology. SNM fluctuation is also detected when the 
supply voltage varies. This paper implements 6T SRAM cell with read and write operation.
and also Static Noise Margin observation. CMOS SRAM cell is very less
power consuming and high speed device and have less read time time.
pmos transistor with less width reduce the power consumption. and lastly 
this paper also included the layout design of 6T SRAM cell.
<br>Keyword- SRAM
<br>
<br>
<h2>2. Introduction :</h2>
Static Random Access (SRAM) constitues a large percentage of area
in the VLSI designs due to the high number of transistors for a single
SRAM cell. Mobile devies battery life may be estimated using this tool.
SRAM speed is determined by the amount of time it takes to read and 
write data. As long as power is being provided it keeps data bits in its memory.
SRAM is quite simiar to latch in which two inverters are connected in cross-coupled.
The cell requires six trasistor per bit. Nanometer scale design present a wide range
of design challenges.SRAM cell design has a major issue with stability. MOSFET aspect 
ratio and operating conditions have an impact on memory stability. Stability of memory refers 
to its capacity to perform its intended functions. Static Noice Margin(SNM) measures
the reliability of SRAM cells.All the simulations are done in cadence virtuoso tool with 180nm technology. 
<br>
<br>
<h2>3. Design :</h2>
<h3>A. Conventional SRAM 6T Cell-</h3>
The design of an SRAM 6T cell is similar to a latch in 
which two CMOS inverters are connected back to back (M1-
M2 and M3-M4) with two secondary nmos transistors (M5-
M6) are connected to the paired bit line BL and bit line bar 
BLB.These two transistors are connected to the word line 
to perform the access of read and write operation as shown in 
Fig.<br>
<br>
<br>

![Screenshot (63)](https://github.com/user-attachments/assets/13342a3b-04e0-4a93-b34b-9856e236e7ff)

<br>
<br>
<br>
<br>

![Screenshot (62)](https://github.com/user-attachments/assets/188c27ea-a1dc-4adc-9072-011dc09a0f66)
<br>


<br>
<br><h2>4. Working operation :</h2>
The SRAM cell performs three operation
<br>
I- Write operation
<br>
II- Read operation 
<br>
III- Hold operation
<br>
<br>

 <h3>Write operation -</h3>
In case of write operation, If you want to write 1 in memory cell then
first let Q=0 means now 0 is stored in the memory cell. you want to write 1.
step 1: Forecefully connect bit bar =0 by initially discharging capacitor.
<br>
step 2: Apply write pulse at gate of NM2 and NM4. when write pulse is applied,
NM2 and NM4 will turn on. Q bar is 1 means NM1 is on . But after apply Write 
pulse voltage difference occur between Q bar and bit bar and voltage will going to
decrease at Q bar and less than threshold voltage of NM1. NM1 will turn off and
Q will becomes 1. See below fig for write operation
<br>
<br>
<br>
![Screenshot (65)](https://github.com/user-attachments/assets/c22a5160-283b-4077-8178-e9319d0543cf)

<br>
<br>
<br>
 <h3>Read operation -</h3>
 In case of read operation, Let Q=1 and you want to read 1.
 So you have to check wheather logic 1 is stored or not.
 Step 1: Bit and Bit bar line are precharge to logic 1. 
 Means Both capacitor are precharged to logic 1. 
 <br>
 Step 2: Apply Read Pulse at the gate of NM2 and NM4 . When Read pulse is 
 applied, NM2 and NM4 will turn on. In this time since Q bar is 0 so, 
 a voltage difference will occur between q bar and bit bar. capacitor will
 discharge through NM4. bit bar will decrese.
 <br>
 Step 3: Connect a comparator or Sense amplifier between bit and bit bar line.
 Now, bit line is grater than bit bar line voltage . So in this case the output we get 
 is logic 1. In this way we can read the value. See below fif for Read operation.
<br>
<br>
<br>
![Screenshot (66)](https://github.com/user-attachments/assets/ac4600f5-c139-4ae7-8eef-1423a2367455)

<br>
<br>
<br>
<h3> Sense amplifier :</h3>
The sense amplifier is based on the voltage mode's 
operation on the differential voltage created by the bit-lines, The circuit is composed of 
cross-coupled inverters that turn the bit-line voltage differential at their input into 
a full-swing output. The voltage mode sensing amplifier circuit is illustrated in the figure.
<br>
<br>

![Screenshot-19](https://github.com/user-attachments/assets/9c614303-b22a-4216-ac3a-a60eff595054)
<br>
<br>
<br>
![Screenshot (64)](https://github.com/user-attachments/assets/04f11f06-645b-43c5-a644-de0222795686)

<br>
<br>
<br>
![Screenshot-20](https://github.com/user-attachments/assets/6ce88fdd-fdaa-45b9-ab52-20ed0c9fa4bb)
<br>
<br>
<br>
<h3>Hold Operation -</h3>
For the hold operation, make the word line (WL) 
from 1 to 0. That means no read-and-write operation will 
be done and the data will remain in the hold state into SRAM.
<br>

<BR>
<H2>IV. Simulations :</H2>
<br>
<br>


![Screenshot-24](https://github.com/user-attachments/assets/76543f9b-9d4a-48ea-b3f1-b28d6d9749ff)
<br>
<br>
<br>

![Screenshot-21](https://github.com/user-attachments/assets/a4d21d1e-92a8-436a-ba98-b91bac325d61)
<br>
<br>
<br>
![Screenshot-23](https://github.com/user-attachments/assets/a7076f67-cd8a-43ec-8a12-5edee512b951)

<br>
<h2>V. Layout :</h2>
<br>
<br>

![Screenshot (61)](https://github.com/user-attachments/assets/add6c404-b7ac-4e42-aebb-93da3110d50e)



<br>
<h2>5. Results & Conclusion :</h2>
The project examine the performance of a
conventional 6T SRAM in read and write operations in 
terms of power-delay product. The results were performed
in 180nm technology, which demonstrates that as the 
precharge voltage is decreased, power dissipation is 
improved. For the stability of the memory cell to be 
maintained, the supply voltage must be chosen properly. 
By utilizing various low-power the performance 
of 6T SRAM cells can be further improved.









