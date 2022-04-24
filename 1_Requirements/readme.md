**Components**


Microcontroller Section

AT89C51 Microcontroller


AT89C51 Programmer Board

11.0592 MHz Quartz Crystal

33pF Ceramic Capacitor

2 x 10KΩ Resistor

10µF Electrolytic Capacitor

Push Button

16 X 2 LCD Display

10KΩ POT


Temperature Sensor Section

LM35,
ADC0804,
10KΩ Resistor,
150pF Ceramic Capacitor,
1KΩ x 8 Resistor Pack





Load Section

2N2222 NPN Transistor,
1N4007 Diode,
12V Relay,
1KΩ Resistor,
Fan






**Configuring ADC0804 for this Project**


The configuration of the ADC0804 is explained here. First, we need to connect the 5V regulated power supply to the Vcc pin (Pin 20). Then, connect the analog and digital ground pins (Pins 8 and 10) to the GND.

In order to use the internal clock, we need to connect a 10KΩ resistor between CLK IN (Pin 4 and CLK R (Pin 19) and then, connect a 150pF cap between pins 4 and GND to complete the oscillator circuit.

The CS pin (Pin 1) is connected to GND to enable the ADC.

In order to read the data from the ADC continuously by the microcontroller, we need to connect the RD pin (Pin 2) to the GND.

For the ADC to continuously read the analog data from the sensor, we need to short the Write pin (Pin 3) with the Interrupt pin (Pin 5).

The analog output of the sensor (LM35) is connected to the Vin+ (Pin 6) of the ADC. The negative analog input pin i.e. Vin- of the ADC is connected to the GND.

The converted digital data which is an 8-bit data will be available at DB0 to DB7 (Pins 18 to 11).
