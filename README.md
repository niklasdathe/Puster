# Puster
## motivation
TODO - dust mite allergy, health benefits 

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

