# Puster
## motivation
people spend more than 90% of their time indoors, often exposed to pollutant concentrations that are two to five times higher than outdoors. for individuals with dust mite allergies, this can be particularly harmful. dust mites thrive in warm, humid environments, and their microscopic waste particles easily become airborne, triggering symptoms such as sneezing, watery eyes, and breathing difficulties. over time, prolonged exposure to indoor allergens like dust mites can worsen asthma and other respiratory conditions.

improving indoor air quality is therefore not just about comfort, but about protecting long-term health and well-being. studies show that fine particulate matter (PM2.5), volatile organic compounds, and elevated CO₂ levels can significantly reduce cognitive performance and increase the risk of cardiovascular problems, sleep disruption, and chronic illnesses. clean air supports better sleep, sharper focus, and a healthier immune system.

the Puster was designed with this in mind: to help reduce allergens like dust mites while also tackling the invisible but harmful indoor pollutants that affect daily life. by combining reliable filtration with smart electronics, it provides a simple step towards a healthier home environment. 

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

