# Puster
## motivation
i’ve been struggling with dust mite allergies for years, which makes clean indoor air more than just a comfort. dust mites thrive in humid environments, and their microscopic waste can trigger sneezing, watery eyes, and breathing difficulties. Since people spend more than 90% of their time indoors, often exposed to pollutant concentrations 2–5 times higher than outdoors (Environmental Science & Technology, 2023), the impact on health is significant.

poor indoor air quality is linked not only to allergies and asthma but also to reduced cognitive performance, sleep disruption, and higher risks of cardiovascular disease (Environmental Health Perspectives, 2015; Building and Environment, 2023). with the Puster, my goal is to reduce allergens like dust mites while also addressing the invisible but harmful pollutants that affect daily life.

## mechanicals
### parts list
- **1x FY0194/30 (for phillips 800 series)**  
  widely available through many different sources 
- **1x ESP32C6 based PCB**  
  More infos/files can be found in /electronics/  
  <img width="181" height="199" alt="image" src=images/pcb_3D.png />  
- **1x USB-C cable for powering the Puster**  
  this needs to be quite long as it acts as the power cable  
  also used to flash the firmware  
- **1x 4-Pin 12V PWM Fan**  
  i used a noctua fan as they are well built, quite and the color scheme suits my version of Puster  
- **1x base**  
  I routed mine out of reclaimed bankirai wood but you could also print this.  
  <img width="181" height="199" alt="image" src=images/base.png />  
- **1x lid**  
  3D printed out wood-filled-filament but you can use whatever filament you like. Feel free to get creative.:)  
  <img width="181" height="199" alt="image" src=images/lid.png />  
- **1x cage**  
  3D printed out wood-filled-filament but you can use whatever filament you like. Feel free to get creative.:)  
  <img width="181" height="199" alt="image" src=images/cage.png />  
- **1x adapter**  
  3D printed out wood-filled-filament but you can use whatever filament you like. Feel free to get creative.:)  
  <img width="181" height="199" alt="image" src=images/fan_adapter.png />  
- **4x rubber feet**  
  these could easily be 3d printed but i used off the shelf parts i had laying around  
  [20mm diameter, 12mm height, 4mm thorugh hole]  
- _x screws
  TODO


## electronics
### the pcb 
you can order the pcb through the following link:  
https://aisler.net/p/XLGCRZIT  
i added a stencil to help me with assembly.

the ESP32-C6 was chosen as the core of the Puster PCB because it offers modern wireless connectivity while staying flexible for different smart home ecosystems. with support for Wi-Fi 6, Bluetooth Low Energy 5.0, Zigbee and Thread (Matter), it can easily integrate into existing setups, whether that’s a Zigbee network, Matter-over-Thread, or simple Wi-Fi control. this makes the device adaptable for the future without locking it to one protocol.

for fan control, I used the EMC2101, a dedicated I²C fan controller. this chip simplifies reliable 4-pin PWM fan operation by:  

- generating the Intel-spec compliant PWM signal.
- monitoring the fan tachometer feedback for RPM validation.
- allowing precise control of fan speed directly over the I²C bus.

by offloading the fan PWM and tachometer handling to the EMC2101, the ESP32-C6 remains free for wireless communication and higher-level logic. this approach ensures smooth and safe operation of 12V PC-style fans without risking glitches or timing issues from software-driven PWM and tacho pulse counting.  

routing turned out to be quite the challenge as the board is only 2cm wide but i managed to somehow squeeze it all in:  
<img alt="image" src="images/pcb_routing.png"/>   

### assembly 
TODO - pictures of my assembly process
### testing
TODO -pictures of pcb testing



### the fan
the pcb was built around this type of fan connector(TODO specific kind):  

(from Noctua PWM specifications 
white paper)

*Its important that only 12V fans are used, as other fans might get damaged by being overvolted.*

the pwm lines are driven at 5V, as per intel specification  

## software
## zigbee setup
With the current configuration this device acts as a zigbee router. THat means it will extend your zigbee mesh. I decided to this because I don't have tight power constraints as its plugged into the wall.   


 <img width="449" height="436" alt="image" src="https://github.com/user-attachments/assets/85f76b60-7411-4906-b821-5ad95e437fb9" />  

 
the Zigbee data model is set up in a way, that the tachometer data (actual fan rpm) can be read from the device over Zigbee and the fan pmw (desired fan rpm) can be set over Zigbee. I haven't tried this yet but you might be able to close the control loop with this.  
TODO. actual cLuster/endpoint architecture

<img width="761" height="531" alt="image" src="https://github.com/user-attachments/assets/7cfe78c7-0729-4ae6-a66b-1f582baacd58" />  


### why zigbee?
That decision was simple, i already had a working zigbee mesh network. I've been interested in Matter over Thread lately but thats a story for another time.

*im sure its easily adapted to matter over thread, wifi or whatever other radio protocolls your using in your smarthome*


### pairing
TODO

### resetting
TODO
### flashing custom firmware
TODO - which port to use, links to implementation help/wikis
If anyone adapts this to other protocolls, feel free to share it so other people can benfit too

