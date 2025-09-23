# Puster
## motivation
TODO - dust mite allergy, health benefits 

## mechanicals
### parts list
1x FY0194/30 (for phillips 800 series)
1x ESP32C6 based PCB
1x USB-C cable for powering the Puster
1x 4-Pin 12V PWM Fan 
1x base
1x lid
1x cage
1x adapter
_x screws TODO


### the fan
the pcb was built around this type of fan connector:  
<img width="181" height="199" alt="image" src="https://github.com/user-attachments/assets/0771c44b-f6ae-481e-86ad-8eea22dc403c" />  
(from Noctua PWM specifications 
white paper)

*Its important that only 12V fans are used, as other fans might get damaged by being overvolted.*

the pwm lines are driven at 5V, as per intel specification  

## software
### why zigbee?

*im sure its easily adapted to matter over thread, wifi or whatever other radio protocolls your using in your smarthome*


### pairing


### resetting

