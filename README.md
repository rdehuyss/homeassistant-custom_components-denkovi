# HomeAssistant - Denkovi
Custom component for - switch platform - for [Denkovi](http://denkovi.com) relay modules in HomeAssistant

Currently tested with [
smartDEN IoT Internet / Ethernet 16 Relay Module - DIN Rail BOX](http://denkovi.com/smartden-lan-ethernet-16-relay-module-din-rail-box)

## Installation
Copy the folder denkovi and all it's contents in your custom_components folder.

## Usage:
Add to configuration.yaml:

```
switch:
  - platform: denkovi
    resource: http://192.168.1.200
    password: !secret denkovi_floor_0_password
    relays:
      1:
        name: Living light
      2:
        name: Kitchen light
      3:
        name: Garden lights
```


Here the important configuration variables are:
- resource: the url to your denkovi relay module, including http://
- password: the password to connect to the relay module (default=admin)
