# I2S-simultaneous-D20400
VHDL code for converting standard I2S data (64fs) to the offset-binary data needed for D20400 DAC (tested on DAC0013 module), configured in the TDA1541A like mode (ultraanalog-d20400-application-note-ap02-pdf - section: 4.5 Simultaneous / Inverted Clock / Inverted WS/LOAD).

Intel Quartus project file (21.1 lite version) : https://drive.google.com/file/d/1agQUHeOUo__oH1g8aJaTiGjtgnUCEvN5/view?usp=sharing


Pinout for the CPLD:
- I2S - CPLD converter:
- - BCK - 5
- - DATA - 7
- - LRCK - 15
- - GND with CPLD GND (next to the pin 21)
- CPLD converter - DAC:
- - 21 - CL (clock for DAC)
- - 28 - DL (data Left)
- - 26 - DR (data Right)
- - 19 - LE (Latch)
- - 17 - Hold
- - DAC GND (2x) with CPLD GND (next to the pin 21)
- Power supply - CPLD converter:
- - psu +5V with CPLD +5V pin (next to the pin 56 or the black power connector) ... or alternatively a higher voltage (max. +12Vdc)
- - psu GND with CPLD GND pin (next to the pin 55 or the black power connector)
