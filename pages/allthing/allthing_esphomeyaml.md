---
title: Documentation 
last_updated: July xx, 2018
summary: "Summary"
series: "ACME series"
weight: 3
sidebar: allthing_sidebar
permalink: allthing_esphomeyaml.htm
folder: allthing
# Don't forget to add a reference in _data/sidebars/allthing_sidebar.yml and/or _data/topnav.yml 
---

### Creating your own HAL templates
You'll need to mount the /config folder to esphomeyaml/config. There is already 
an entry in .env, you'll just have to comment out the bottom reference esphomeyaml_live_mount. 
In production, the esphomeyaml/config folder isn't created, so you'll have to run ```mkdir -p esphomeyaml/config``` 
from the technocore folder. 

### Repo
https://github.com/OttoWinter/esphomeyaml

---
## Useful Docs pages
### Getting Started
https://esphome.io/guides/getting_started_hassio.html

### Automations: Meat of how to program ESPs. Not very long.
https://esphome.io/guides/automations.html

### Filters: How to manipulate and correct readings
https://esphome.io/components/sensor/index.html#sensor-filters

### Configuration Types - Good bit on using substitutions:
https://esphomelib.com/esphomeyaml/guides/configuration-types.html

---
## Useful devices pages
### NodeMCU2 (ESP8266) pin map AND explanation:
https://esphome.io/devices/nodemcu_esp8266.html?highlight=led

### ESP32 - NodeMCU pin map and quirks: 
https://esphome.io/devices/nodemcu_esp32.html

### Direct integration with Home Assistant services: 
https://esphome.io/components/api.html#api-services

### time - Great for kicking off automation at a given time
https://esphome.io/components/time.html

### Analog to Digital sensors: 
https://esphomelib.com/esphomeyaml/components/sensor/adc.html
Attenuation: https://esphome.io/components/sensor/adc.html#adc-esp32-attenuation
Adc information (Great for calibration): https://docs.espressif.com/projects/esp-idf/en/latest/api-reference/peripherals/adc.html
https://docs.espressif.com/projects/esp-idf/en/latest/api-reference/peripherals/adc.html#adc-api-adc-calibration

### Great list of 3rd party devices that ESP Home supports (Teckin, Sonoff...) and what the important pin are
https://esphome.io/devices/sonoff.html

### Home Assistant sensor: Import any Home Assistant Entity state? Cool.
https://esphome.io/components/sensor/homeassistant.html

### Esp32 Camera:
https://esphome.io/components/esp32_camera.html

### Sonoff pin mapping for Teckin SP10:
The SP10 doesn't do energy monitoring - it is only a switch. 
https://github.com/arendst/Sonoff-Tasmota/wiki/Teckin-sp10
---


## Ideas for usage:
### Hook calibrate linear up to a lambda that allows for stored calibration.
- I'm not sure I can just stick a lambda anywhere. I'll have to figure out what datatype gets returned. It's some kind of key/value pair array. 
- Could use MQTT or Home Assistant to allow for storage across device flashes
- Could store somewhere on esp to survive across 
- Do both?
https://esphome.io/components/sensor/index.html#sensor-filter-calibrate-linear
https://esphome.io/components/sensor/homeassistant.html
---

### Introduction on using esphomeyaml with Home Assistant
https://www.home-assistant.io/blog/2018/06/05/esphomelib/

### I needed to increase the number of inotify watchers in order to get Guard to work: 
https://github.com/guard/listen/wiki/Increasing-the-amount-of-inotify-watchers

### Example calibrating a sensor
https://esphomelib.com/esphomeyaml/components/sensor/hx711.html?highlight=calibrate

### How to use specific esphome-core version.
https://esphome.io/components/esphomeyaml#esphomeyaml-esphomelib-version

### A little about setting up esphomeyaml as a stand alone service.
https://community.home-assistant.io/t/esphomelib-help-docker/62383/10

### Esphomeyaml supports most of Home Assistant's !directives (!include, !secret... etc.). 
https://esphomelib.com/esphomeyaml/guides/faq.html?highlight=include
Here is a page about them:
https://www.home-assistant.io/docs/configuration/splitting_configuration/

### Teckin with EspHome - GREAT 
https://blog.quindorian.org/2019/02/home-assistant-10-wifi-energy-meter-with-esphome.html/


### Custom SPI 
https://esphome.io/custom/spi.html?highlight=spi

{% include links.html %}
