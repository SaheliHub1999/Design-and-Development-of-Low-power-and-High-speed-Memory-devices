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

![Screenshot-1](https://github.com/user-attachments/assets/ced1966a-2fa8-4b69-80e5-5edb422c35e9)
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
In case of write operation When word line (WL) is high, the data should be 
written on Q is 0 and QB is 1 and the word line is enabled 
1 to access the lines BL and BLB. The BL and BLB act 
as input. The BLB is connected to the ground because QB 
is 1. There will be some voltage difference, the voltage will decrease for transistors M1 and M2. If the voltage is 
less than the threshold voltage of M2 then M2 is turned off 
and M1is turned on. That means output Q will be 1. So 
input Q is 0 and output Q=1 means data is written.
<br>



 <h3>Read operation -</h3>
WL is high, t memory should hold some value. 
Now Q is 1 and QB is complementing 0.Now 
memory has some value stored and to read BL and BLB 
now act as output lines and these lines will be precharged 
by voltage VDD at both nodes Q and QB. Now there is 
no voltage difference at node Q =1 and T5 so there will 
be no discharge but on another side QB = 0 and the 
voltage is VDD and there is a voltage difference so there 
will be discharge at node QB and node voltage at BLB 
will start discharging. Now the values stored in BL and 
BLB will be sent to the sense amplifier which helps as a 
comparator and it says if BLB decreases then the output 
will be 1 it means we successfully read from the memory 
because the memory has a value of 1 and getting read 1 
as output.
<br>
<br>
<h3>B. Sense amplifier :</h3>
The sense amplifier is based on the voltage mode's 
operation on the differential voltage created by the bit-lines, The circuit is composed of cross-coupled inverters 
that turn the bit-line voltage differential at their input into 
a full-swing output.The voltage mode sensing 
amplifier circuit is illustrated in the figure.
<br>
<br>

![Screenshot-19](https://github.com/user-attachments/assets/9c614303-b22a-4216-ac3a-a60eff595054)
<br>
<br>
<br>The column bit-lines of the cell are connected to 
the BL and BLB(BL_)inputs. M2-M4 and M3-M1 work 
together to create the inverters, which change the 
differential voltage on the bit lines into a full swing at the 
output. Pre-charging the internal nodes Q, and QB of this 
circuit through the bit-lines is accomplished by the pre-charge circuitry. To enable the sense amplifier, the 
memory cell is connected to it via M1 and M2. M5 is 
utilized to activate the sense amplifier. The nodes inside 
the output inverters insulate the sense amplifier from the 
external load. Voltage based sense amplifier action 
occurs in two stages. Bit-lines and the nodes Q and QB 
are pre-charged high while the Pre charge circuit (PCH)
is kept inactive during the first phase, also known as the 
pre-charge phase. In the evaluation step, the select line is 
brought down to link the sense amplifier to the memory 
cell Fig.

<br>
<br>

![Screenshot-20](https://github.com/user-attachments/assets/6ce88fdd-fdaa-45b9-ab52-20ed0c9fa4bb)
<br>
<br>
<br>
<h3>Hold Operation -</h3>
For the hold operation, turn off the word line WL 
from 1 to 0. That means no read-and-write operation will 
be done and the data will remain in the hold state.
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

![Screenshot-29](https://github.com/user-attachments/assets/00a87306-9d36-4fc3-a390-0d568bd51895)


<br>
<h2>VI. Results & Conclusion :</h2>
Hence, the project examine the performance of a
conventional 6T SRAM in read and write operations in 
terms of power-delay product. The results were performed
in 180nm technology, which demonstrates that as the 
precharge voltage is decreased, power dissipation is 
improved. For the stability of the memory cell to be 
maintained, the supply voltage must be chosen properly. 
Even though power consumption and delay are reduced, 
strategies, stability should be maintained for reliability 
concerns.By utilizing various low-power the performance 
of 6T SRAM cells can be further improved.









