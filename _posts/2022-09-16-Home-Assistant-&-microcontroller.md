---
layout: post
title:  "Home Assistant & Microcontroller"
date:   2022-09-16 01:19:00 +0200
categories: project update homeassitant esp32
---
# Home Assistant OS

Nach langem Bemühen Home Assistant über Docker Container laufen zu lassen, wurde heute umgeschwenkt:
Anstelle eines Linuxserver wird Home Assistant OS verwendet um weitere Verzögerungen zu vermeiden. Home Assistant OS kann leicht und schnell eingerichtet werden und ist sehr gut dokumentiert. In dieser Version können auch problemlos zusätzliche Addons, wie [NodeRed](https://nodered.org/) oder [ESPHome](https://esphome.io/) leicht hinzugefügt werden und die Administration ist gemeinhin auch übersichtlicher.
IoT-Geräte wie Microcontroller können so auch schneller und flexibler mit YAML Konfigurationsdateien integriet werden. Somit steigert sich die Effektivität und Produktivität des Projektes, sodass das die Deadline wieder in greifbare Nähe rückt.

### ESP8266 on-Board LED als Entity

![simple-ha-entity-control](/assets/2022-09-16-simple-ha-entity.gif)

Hier ist ein einfaches Beispiel einer Entität in Home Assistant.

#### Zugehöriger Snippet aus der YAML Konfiguration des Microcontrollers:

>```yaml
>light:
>  - platform: monochromatic
>    name: "OnBoard LED"
>    output: onboard_output
>    effects:
>      # Customize parameters
>      - random:
>          name: "My Slow Random Effect"
>          transition_length: 30s
>          update_interval: 30s
>      - random:
>          name: "My Fast Random Effect"
>          transition_length: 1s
>          update_interval: 2s
>  
>output:
>>  - id: onboard_output
>>    platform: esp8266_pwm
>>    pin:
>>      number: D0
>>      inverted: true
>```

### Ausblick

Mithilfe dieses einfachen Beispiels lässt sich in den nächsten Tagen das gewünschte Moodlighting implementieren. Zudem wird ESPHome noch für einige andere kleinere IoT Anwedungen nützlich werden.
Einlesen zum Automatisieren einiger IoT Abläufe erfolgt momentan noch.
