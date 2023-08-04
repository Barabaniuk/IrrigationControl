# IrrigationControl
Irrigation control system with sensors GSM connection and control with web interface
Based on Arduino controller equipped by sensors which control tepreture humidity and water consumption. The system is controlled via a web interface from a local network and informing via SMS

## Main functions
Сontrol of soil moisture using Immersion sensor
Сontrol of air humidity sensor


## Main system parameters:
* The maximum load switched by the relay
  - for alternating current -  10A 250V
  - for direct current -       10A 30V
* Flow sensor - FS300A G3/4"
  - Maximum flow - 60 l/min
  - Can be used as a dry running sensor
  - Calibration required after installation for accurate flow readings
* Leak sensor - HDS10
* Temperature and humidity sensor   DHT22
  - Humidity measurement range:     0-100%
  - humidity measurement accuracy:  ±2% RH
*	Ethernet module -  ENC28J60
*	GSM-module -       SIM900 GSM/GPRS;


## Irrigation control web interface
Main functions of web interface:
* Display of current sensor readings:
  - Air humidity in %
  - Soil moisture in %
  - Water consumption in l/min
  - Leak sensor status
* Enable/disable automatic control (operating range is set in the settings)
* Manual on/off pump irrigation
* Manual on/off air humidifier
* Manual on/off emergency power
* Activation of SMS-informing
* Settings:
  - Set the humidity limit to automatically turn on the humidifier
  - Set the soil moisture limit to automatically turn on irrigation
  - Set consumption limit, below which the pump will automatically shut off
  - Set leak sensor value,  below which emergency turn-off will be activated
  - Set phone number for SMS informing
  - Show device ID and firmware version

 

## Components


## Wiring diagram
![Irrigation control Wiring diagram](https://github.com/Brabn/IrrigationControl/blob/main/Wiring_dagram/Irrigation_control.Wiring_diagramEN.png)

## Possible further improvements


## Photos
