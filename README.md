# Pseudo-Noise-Sequence-to-Triangular-and-Sinusoidal-Wave-Converter
## Table of Contents
1 Abstract 
2 Reference Circuit Design
3 Reference Waveforms
4 Circuit Details
5 Softwares Used
6 Circuit Diagram in eSim
7 Netlists
8 NgSpice Plots
9 Acknowlegdements
10 References
##  Abstract
This project aims at the realisation of a device which converts a PN Sequence to a Triangular as well as Sinusoidal Wave. An implementation of a mixed signal design, this may find various applications. The PN Sequence generator is written in verilog and foprms the digital part of the circuit wheras the conversion to triangular and sinusoid forms the analog part. Due to certain constraints, the output for the sinusoid wave could not be obtained hence the design stands errenous.
## Reference Circuit Design
![image](https://user-images.githubusercontent.com/67062356/194713623-ecf67077-c2d1-4375-8712-71fecaea58f2.png)

Digital Circuit Design part
![image](https://user-images.githubusercontent.com/67062356/194713644-b55bddd1-6d21-4c40-a66a-5605b8f0f4e7.png)

Analog Circuit Design part
## Reference Waveform
![image](https://user-images.githubusercontent.com/67062356/194713703-96e84045-1c3e-4be2-8ecd-29b54bb35e35.png)

## Circuit Details
PN sequences are generated by Linear Feedback Shift Registers (LFSR)

When a square wave input is applied to an integrator circuit it generates triangle wave in the output. An integrator circuit can be built using operational amplifier, one resistor and a capacitor. When a constant voltage is given to capacitor through resistor, it charges to max voltage and produces linear ramp. So, this principle is used to convert square wave into triangle wave. Finally, another resistor capacitor configuration is used to convert triangle wave to sine wave
## Softwares Used
### eSim
It is an Open Source EDA developed by FOSSEE, IIT Bombay. It is used for electronic circuit simulation. It is made by the combination of two software namely NgSpice and KiCAD.
For more details refer:
https://esim.fossee.in/home

### NgSpice
It is an Open Source Software for Spice Simulations. For more details refer:
http://ngspice.sourceforge.net/docs.html

### Sky130 Process Development Kit
The Skywater 130nm technology is developed by Google for 130nm node. The PDK is open source and current under development.
For more details refer:
https://skywater-pdk.readthedocs.io/en/main/#
## Circuit Diagram in eSim
![image](https://user-images.githubusercontent.com/67062356/194713981-c4075dd3-745a-4a6f-b0c2-770409b8bb9b.png)

### Verilog Code
![image](https://user-images.githubusercontent.com/67062356/194714127-270a2025-8f15-40fd-babe-b0df42129650.png)

### MakerChip Output
![image](https://user-images.githubusercontent.com/67062356/194714163-9c70828b-7646-4696-b768-dd03ac7e0ea1.png)

### Netlist
![image](https://user-images.githubusercontent.com/67062356/194714192-03556dbb-87f4-4439-8434-246879264ae3.png)

### NGSpice Plots
![image](https://user-images.githubusercontent.com/67062356/194714497-2709d933-ad76-464d-8e6b-1522d25e8f75.png)

Triangular Wave Output
![image](https://user-images.githubusercontent.com/67062356/194714527-2b2383e5-5def-43ad-962b-69f942be29ea.png)

PN Sequence input
### Steps to run generate NgVeri Model
Open eSim
Run NgVeri-Makerchip
Add top level verilog file in Makerchip Tab
Click on NgVeri tab
Add dependency files
Click on Run Verilog to NgSpice Converter
Debug if any errors
Model created successfully
## Acknowlegdements
FOSSEE, IIT Bombay
Steve Hoover, Founder, Redwood EDA
Kunal Ghosh, Co-founder, VSD Corp. Pvt. Ltd. - kunalpghosh@gmail.com
Sumanto Kar, eSim Team, FOSSEE

##	References
https://www.engineersgarage.com/waveform-converter-circuits/
http://tjeyamy.blogspot.com/2012/05/pseudo-random-sequence-generator-in.html
