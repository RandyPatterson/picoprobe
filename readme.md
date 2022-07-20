# Pico Probe 
Using the Raspberry Pi Pico as a SWD (Software Debug) Probe.  Simple schematic and PCB to easily setup a Raspberry Pi PICO and a Pico Probe

## platformio.ini settings 
```ini
[env:pico]
;https://arduino-pico.readthedocs.io/en/latest/platformio.html
platform = https://github.com/maxgerhardt/platform-raspberrypi.git
board = pico
framework = arduino
upload_protocol = picoprobe
debug_tool = picoprobe
;start debugging at sketch setup() otherwise start in RTOS main
debug_init_break = tbreak setup 
```
> **NOTE** 
> ___
> Use a different *platform* that supports the Pico Probe until it's merged with the main branch. see [this](https://arduino-pico.readthedocs.io/en/latest/platformio.html)

![finished board](content\finishedproduct.jpg)

![PCB](content\3dview.png)

![Schematic](content\schematic.png)
