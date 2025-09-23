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
TODO - why i chose esp32c6 (wireles capabilities) and fan controller
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

