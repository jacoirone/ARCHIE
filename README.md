# ARCHIE
> Electronic Board for Test Stand Development of the THRUST Student Project.

ARCHIE is a ESP32 based data logging and actuation capable system that is able to record and control:
* 4 Thermocouples,
* 3 Pressure Sensors (4-20mA sensors), 
* 3 Mosfet Actuated Electrovalve, 
* 1 Load Cell



<p align="center">
  <img src="https://github.com/jacoirone/ARCHIE/blob/main/Figures/TSPCB_Front_Tilt.PNG" width="300" height = "600" />
  <img src="https://github.com/jacoirone/ARCHIE/blob/main/Figures/TSPCB_Back_Tilt.PNG" width="300" height = "600"/> 
</p>

## MCU
The choice for the MCU of this project has fallen upon the [Adafruit HUZZAH32](https://www.adafruit.com/product/3405), an ESP 32 based board by Adafruit. The ESP32 is a great MCU being powerful, efficient and cheap. Its Dual-core 250Mhz processor is powerful enough for the data logging task that we need, while the bluetooth and Wifi functionalities can come in handy if we need to trasmit data wirelessly. The ESP32 is also widely available and supported all over the world. 

<p align="center">
<img src="https://github.com/jacoirone/ARCHIE/blob/main/Figures/TSPCB_Front_MCU.png" width="600">
</p>

## Temperature
Temperature information are supplied by the four indipendent thermocouples channel that are powered by the [Adafruit MAX 31856 Board](https://www.adafruit.com/product/3263). This Breakout is capable of reading temperature measurement from all type of thermocouples thanks to the [MAX 31856](https://datasheets.maximintegrated.com/en/ds/MAX31856.pdf) integrated chip. 

<p align="center">
<img src="https://github.com/jacoirone/ARCHIE/blob/main/Figures/TSPCB_Front_Temp.png" width="600">
</p>


## Pressure
Pressure datas are supplied by 4-20mA Pressure transducers. This type of sensors can be easily read by the [Adafruit ADS1115](https://www.adafruit.com/product/1085) ADC thanks to a simple 200 Ohms resistor that provides a range of voltages from 0.8V (4mA) to 4V (20mA) to the ADC. Any 4-20mA sensor can actually be connected to these channels. 

<p align="center">
<img src="https://github.com/jacoirone/ARCHIE/blob/main/Figures/TSPCB_Front_Pressure.png" width="600">
</p>


## Force
Thrust Measurement are maybe one of the most important datas that one can gather from rocket motor's testing. ARCHIE uses a [INA 122P](https://www.ti.com/lit/ds/symlink/ina122.pdf) chip for amplifing the coming voltage from the load cell. The signal will then be fed to the [Adafruit ADS1015](https://www.adafruit.com/product/1083) ADC that will record the input at a max speed of about 3000 samples per second. 

<p align="center">
<img src="https://github.com/jacoirone/ARCHIE/blob/main/Figures/TSPCB_Front_LoadCell.png" width="600">
</p>


## Electrovalves
The electrovalves actuation circuit is based around a standard [N channel logic level Mosfet](https://www.infineon.com/dgdl/irlr8743pbf.pdf?fileId=5546d462533600a4015356719c7e26ff) that is responsible for connecting the valves to the power upon a signal from the microcontroller. The circuit consist also of two resistor, the first one of about 100 Ohms is used to limit the amount of current that is drawn from the microcrontroller. The second one is a 10k Ohms pull down resistor to avoid an unwanted actuation of the valves. The circuit is completed by a diode that is used to eliminate problems related to flyback current. 

<p align="center">
<img src="https://github.com/jacoirone/ARCHIE/blob/main/Figures/TSPCB_Front_Valves.png" width="600">
</p>


## Power
Power in the board is supplied by the USB port on the [ESP32](https://www.adafruit.com/product/3405). This particular board has a pin labelled USB that is directly connected to the USB 5V pins. All the other 5V components are powered from this pin. The 24V required for the Mosfet circuit and the 4-20mA sensor channels is supplied by a standard screw connector.

<p align="center">
<img src="https://github.com/jacoirone/ARCHIE/blob/main/Figures/TSPCB_Front_Power.png" width="600">
</p>


## Contributions
ARCHIE's gerber files are available in the [hardware directrory](https://github.com/thrust-team/electronics/tree/main/Test%20Stand/Hardware/Test%20Stand%20PCB) of this repository along side the footprints and schematic symbols used. All the development has been made using the open source software [Kicad](https://kicad.org/)

Jacopo Irone  
THRUST Team  
University of Padua  

<p align="center">
<img src="https://github.com/jacoirone/ARCHIE/blob/main/Figures/logo_thrust.png" width="400">
</p>

