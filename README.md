# Lab Power Supply
![Robot_Front](https://github.com/jerryok826/Battery-PWR-Board/blob/main/Pictures/IMG_7550.jpeg)

## Project Description
I always thought that most laborary power supplies (LPS) take up to much bench space. This design is just 2.5 inches by 5.5 inches and runs off a wall wart or it can be powered from a lithium battery pack. The unit's specs are 0 to 15 volts output with a maximum output current of 1.5 amps. It has two output adjustable voltage presets with defaults of 5 and 3.3 volts. It has two rotary encoders, one for voltage control and the other for current limiting. Pressing an encoder button will change it's adjustement range. There is one additional button for output enable. The LPS can also be controlled remotely via USB using ModBus. There is also a realtime analog current bar graph on the oled display.

The control processor is a stm32f103c8t6, an Arm Cortex-M3 MCU with 64 Kbytes of flash memory and a 72 MHz CPU. The current code runs on libopencm3 and FreeRTOS. The display is a 256x128 OLED display. It is driven by uGui software. The unit is composed of two boards. The top board is the control and display board. The board below is the regulator board. The regulator board is composed of a low voltage drop linear regulator and a highly efficient switching regulator. Because of the combined efficiency of the switching and linear regulator not much of a heat sink is required. To reduce the noise generated by the switcher to a minimum, the switcher has large imput capacitors and a 3KHz loop pass filter on its output feeding the linear regulator. The switcher output voltage set to maintain a two voltage drop across the linear regulator.
### Project Status
The project is basically complete. I am working on converting the design to Kicad and STM32 IDE Cube.

## Design Files
### Electrical Design Files
This project was initially designed with Altium Designer and is now being updated with Kicad 7.X The control software is C code runing on FreeRTOS. 


