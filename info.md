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
