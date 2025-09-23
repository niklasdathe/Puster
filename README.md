# Puster
## motivation
v’ve been struggling with dust mite allergies for years, which makes clean indoor air more than just a comfort. dust mites thrive in humid environments, and their microscopic waste can trigger sneezing, watery eyes, and breathing difficulties. Since people spend more than 90% of their time indoors, often exposed to pollutant concentrations 2–5 times higher than outdoors (Environmental Science & Technology, 2023), the impact on health is significant.

poor indoor air quality is linked not only to allergies and asthma but also to reduced cognitive performance, sleep disruption, and higher risks of cardiovascular disease (Environmental Health Perspectives, 2015; Building and Environment, 2023). with the Puster, my goal is to reduce allergens like dust mites while also addressing the invisible but harmful pollutants that affect daily life.

## mechanicals
### parts list
- 1x FY0194/30 (for phillips 800 series)
- 1x ESP32C6 based PCB  
  <img width="181" height="199" alt="image" src=images/pcb_3D.png />
- 1x USB-C cable for powering the Puster
- 1x 4-Pin 12V PWM Fan   
- 1x base  
  <img width="181" height="199" alt="image" src=images/base.png />
- 1x lid  
  <img width="181" height="199" alt="image" src=images/lid.png />
- 1x cage  
  <img width="181" height="199" alt="image" src=images/cage.png />
- 1x adapter  
  <img width="181" height="199" alt="image" src=images/fan_adapter.png />
- _x screws TODO


## electronics
### 
the ESP32-C6 was chosen as the core of the Puster PCB because it offers modern wireless connectivity while staying flexible for different smart home ecosystems. with support for Wi-Fi 6, Bluetooth Low Energy 5.0, Zigbee and Thread (Matter), it can easily integrate into existing setups, whether that’s a Zigbee network, Matter-over-Thread, or simple Wi-Fi control. this makes the device adaptable for the future without locking it to one protocol.

for fan control, I used the EMC2101, a dedicated I²C fan controller. this chip simplifies reliable 4-pin PWM fan operation by:  

- generating the Intel-spec compliant PWM signal.
- monitoring the fan tachometer feedback for RPM validation.
- allowing precise control of fan speed directly over the I²C bus.

by offloading the fan PWM and tachometer handling to the EMC2101, the ESP32-C6 remains free for wireless communication and higher-level logic. this approach ensures smooth and safe operation of 12V PC-style fans without risking glitches or timing issues from software-driven PWM and tacho pulse counting.

### assembly 
TODO - pictures of my assembly process
### testing
TODO -pictures of pcb testing



### the fan
the pcb was built around this type of fan connector(TODO specific kind):  
<img width="181" height="199" alt="image" src="https://github.com/user-attachments/assets/0771c44b-f6ae-481e-86ad-8eea22dc403c" />  
(from Noctua PWM specifications 
white paper)

*Its important that only 12V fans are used, as other fans might get damaged by being overvolted.*

the pwm lines are driven at 5V, as per intel specification  

## software
### why zigbee?

*im sure its easily adapted to matter over thread, wifi or whatever other radio protocolls your using in your smarthome*


### pairing
TODO

### resetting
TODO
### flashing custom firmware
TODO - which port to use, links to implementation help/wikis

