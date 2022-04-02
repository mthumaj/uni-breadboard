# Universal Breadboard (uni-breadboard)

Breadboard based on 4mm banana plugs designed for easier connection of device with test environment while developing/debugging/testing.

![Breadboard](/02_Mechanical_Design/Renders/Assembly_Render_1.JPG)

**Features:**
* 24 banana plugs (4mm) screwed-in on custom PCB (10 x 10cm)
* Switch and button to power on/off - for easy power reset of device
* LIN Bus input (LIN_IN) with selection option to connect to LIN_1 or/and LIN_2 channel
* 2 D-SUB9 LIN/CAN interfaces
* 5 General purpose ports (A-E)
* D-SUB9 connector dedicated as port interface (optimized for Vector VN1640 Digital/Analog IO interface (CH5))

## Detailed Description

Breadboard is composed from PCB and 3D printed case/box. 
Plugs/connectors from case are connected to the PCB by wires and screw terminals. 

### Front Panel

**Banana plugs**

| Number 	| Signal 	|
| :---: 	| :---: 	|
| 1 		| GND 		|
| 2 		| V_OUT 	|
| 3 		| LIN_IN 	|
| 4 		| PORT_A 	|
| 5 		| PORT_B 	|
| 6 		| PORT_C 	|
| 7 		| PORT_D 	|
| 8 		| PORT_E 	|

*Note: Numbering starts from left

### Switches (from left)

**Power switch**
* Top position: 	Power OFF
* Bottom position:	Power ON (V_IN --> V_OUT)
	
**Power reset button** - only if Power switch is in bottom position (Power is ON)
* Released:			Power ON
* Pressed:			Power OFF
	
**LIN selector switch**
* Left position: 	LIN_IN --> LIN_1
* Middle position:	LIN_IN - not connected
* Right position:	LIN_IN --> LIN_2
	
**LIN_1 and LIN_2 connection switch**
* Top position: 	LIN_1 and LIN_2 not connected
* Bottom position:	LIN_1 and LIN_2 connected

### Back Panel

**Banana plugs**
| Number 	| Signal 	|
| :---: 	| :---: 	|
| 1 		| V_IN 		|
| 2 		| GND 		|

*Note: Numbering starts from left

**Right D-SUB9 Connector - LIN/CAN Interface 1**

| Number 	| Signal 			|
| :---: 	| :---: 			|
| 2 		| CAN_L_1 			|
| 3 		| GND 				|
| 7			| LIN_1/CAN_H_1		|

Others are not connected

**Left D-SUB9 Connector - LIN/CAN Interface 2**

| Number 	| Signal 			|
| :---: 	| :---: 			|
| 2 		| CAN_L_2 			|
| 3 		| GND 				|
| 7			| LIN_1/CAN_H_2		|

Others are not connected

### Right Panel

**D-SUB9 Connector - Analog/Digital Interface**

| Number 	| Signal 	|
| :---: 	| :---: 	|
| 1 		| A_IN 		|
| 2 		| NC 		|
| 3 		| NC 		|
| 4 		| D_IN_1 	|
| 5 		| D_IN_2 	|
| 6 		| A_GND 	|
| 7 		| NC	 	|
| 8 		| D_OUT 	|
| 9			| D_GND		|

*Refer to: https://cdn.vector.com/cms/content/products/VN16xx/docs/VN1600_Interface_Family_Manual_EN.pdf chapter 2.6.8*

Ports connection (PORT_A - PORT_E) to Analog/Digital Interface can be established by jumpers/wires on J7 

![PCB Top](/01_PCB/Breadboard/Breadboard_Top.jpg)
![PCB Top](/01_PCB/Breadboard/Breadboard_Bottom.jpg)

## Build Manual/Notes

1. 3D Print [breadboard box](/01_PCB/Breadboard/BreadboardBox_1.STL)
	* No supports needed
	* 0.6mm nozzle can be used to speed up printing
2. Insert and glue M3 hex nuts.
3. Assembly the PCB 
	* gerber files to manufacture are available [here](/01_PCB/Breadboard/gerbers)
	* BOM is available here
	* When assembling screw terminals, make sure that wire openings are oriented inside the board (see picture), so wires can be easily inserted to the terminal, when board is already mounted on top of case.
4. Solder cables for banana plugs, switches and D-SUB9 connectors
	* For V_IN, V_OUT and GND connection use cable with cross section at least 1,5mm^2

5. Mount banana plugs/switches/D-SUB9 connectors to the case
	* When mounting banana plugs, use serrated lock washer (washer with "teeth") to prevent releasing when plug and unplug connectors to the plugs.

6. Connect wires to the respected screw terminals
7. ...and it's done.





