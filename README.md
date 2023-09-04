![alt text](https://github.com/WainingForests/Xiao-flex/blob/main/Images/_DSC1255.JPG?raw=true)
# Xiao-flex
Xiao nRF52840 breakout board with JST and FPC connections for easy building.

PCB project files are for EasyEDA - Standard. Simply install, and import the Schematic and PCB files.

Dimensions
H33.4mm x W39.4mm
Battery extends 5mm past top for easy removal (Recommend Kapton tape if shorts are a concern for some reason)

Components and ICs
Seeed Studios Xiao nRF52840
Battery mount - LR2450 (alternatively remove mount and solder to pads polarity is on board)
Battery low voltage cutoff from FS312F-6 Battery Protection IC and Cutoff Mosfet from FS8205
Shift register - RS0101YH6
Power switch is cutting BATT+ from XIAO.

FPC connections 8p and 10p (thumbs) 0.5mm pitch. The headers dual contact headers. 
JST SH headers are used. All 6p


LED & Shift Register Circuit;
The switch toggles from 5v with shift register data, to no contact (half switch protection), to 3.3v (from XIAO) and 3.3v pin logic. 

Thumb row selection is done via a 2.54mm jumper. Unconnected will leave the Row pad disconnected. 

![alt text](https://github.com/WainingForests/Xiao-flex/blob/main/Images/Xiao-Flex-diagram.png?raw=true)

V1.1 - Poly fuse added to GND side. Added through holes for regulated (switch) LED power and LED data.
V1.2 - Added through holes for 1.10 1.00 and 0.16 for SPI / I2C / more columns or rows if wanted!

Pinout

	C1 - P0.05		R1 - P0.02		LEDDATA - P0.09
	C2 - P1.11		R2 - P0.03
	C3 - P1.12		R3 - P0.28
 	C4 - P1.13		R4 - P0.29
	C5 - P1.14		R5 - P0.04
	C6 - P1.15		R6 - P0.10

FPC specific pinout:
  Perspective: viewing device with USB closer to you. Top is farthest away from USB.

Fingers - GND

	R4
	GND
	R3
	GND
	R2
	GND
	R1
	GND

Fingers LED

	LED+
 	LEDDATA
	R5
 	R4
 	R3
 	R2
 	R1
 	GND
 	Thumbs
 	GND

Thumbs

	GND
 	THUMBROW - Jumper Selection for R5 or R6
	C1
	C2
	C3
	C4
	C5
	C6
	GND
	LED+

Access to all work is under Copyright from Marshall Somerville 2023 CC BY-NC-SA 4.0
