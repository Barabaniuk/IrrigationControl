# IrrigationControl
Irrigation control system with sensors GSM connection and control with web interface
Based on Arduino controller equipped by sensors which control tepreture humidity and water consumption. 
Designed to automatically control the watering of domestic plants that require constant maintenance of soil and air moisture.
To protect the pump from breakdown, there is a flow sensor in the system - if after some time after turning on the pump, the water flow is insufficient, the system turns off the pump to avoid damage when working without water
The system is equipped with a leakage sensor - if the sensor detects water, the system will turn off the power to prevent further flooding and a possible short circuit
The system can be controlled via a web interface from a local network (or global network if subnet has own static IP). 
Supports informing about the current status and events by sending SMS messages through the mobile network:
* Turn on watering
* Enable humidification
* Emergency shutdown due to leakage detection

## Main functions
* Automatic control of soil moisture 
* Automatic control of air humidity
* Leak protection
* Pump protection against dry running
* Remote control via web interface
* Informing about emerging events via SMS

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

## Irrigation control web interface
![Irrigation control web interface](https://github.com/Brabn/IrrigationControl/blob/main/Web_interface/Irrigation_control.Webinterface.png)
[Example of webiterface](https://htmlpreview.github.io/?https://github.com/Brabn/IrrigationControl/blob/main/Web_interface/Irrigation_control.Webinterface.html)

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
  ![Irrigation control web interface settings](https://github.com/Brabn/IrrigationControl/blob/main/Web_interface/Irrigation_control.Webinterface.settings.png)
  - Set the humidity limit to automatically turn on the humidifier
  - Set the soil moisture limit to automatically turn on irrigation
  - Set consumption limit, below which the pump will automatically shut off
  - Set leak sensor value,  below which emergency turn-off will be activated
  - Set phone number for SMS informing
  - Show device ID and firmware version

## Components
1. Arduino UNO controller
2. Four-channel relay
3. Leakage sensor HDS10
4. Tempreture and humidity sensor DHT22
5. Soil moisture sensor
6. Water flow sensor FS300A G3/4"
7. Ethernet module ENC28J60
8. GSM module SIM900 GSM/GPRS

## Wiring diagram
![Irrigation control Wiring diagram](https://github.com/Brabn/IrrigationControl/blob/main/Wiring_dagram/Irrigation_control.Wiring_diagramEN.png)

## Possible further improvements
* Several groups of sensors with independent control
* Activation of various events according to the schedule
* Sensors for volatile organic compounds (VOCs), CO2 (sometimes combined with VOCs) and a dust sensor with the inclusion of a damp fan in case of exceeding the permissible concentrations can be added to the system
* More precise setting of admissible limits of controlled values
* Web interface improvements with graphical indicators, mnemonic diagrams
* More detailed SMS messages with the current status of all sensors
* Turn on devices and manage settings by sending SMS
* Integration with instant messengers (Viber, Telegram) with current status and device management
* Management of system functions through a mobile application
* 
