![4](https://github.com/yuanyong2024/picoduino/assets/163154773/f443fb34-c6ab-4f50-a258-28a81ed303fb)
# Introduction
This is a Raspberry Pi Pico W hardware in arduino form factor.And it's name is picoduino

Unlike all the other wireless solutions for RP2040 on market(which almost all use the ESP wireless chip).
This board is equipped with a module that have the same chipsets like Pico W from Raspberry Pi. A microcontroller RP2040 from Raspberry Pi and a wireless chip CY43439 from Infineon.

# Features
1. totally compatible with arduino form factor.
2. fw developed for pico  w can easily ported to picoduino without any change(especially all the wireless features).
3. using analog switch so that 3 ADC ports can connect to 6 pins from A0 to A5 on picoduino board.
4. use a dedicated voltage reference to improve the accuracy of the ADC.
5. use two DC-DC regulators instead of LDO to improve the efficiency as well as increasing the maximum input voltage to 24V.
6. exposed all the GPIOs from RP2040 chip.
7. USB type C interface.
8. all the deisgn files are open-sourced and designed in Kicad.
    
# Limitations
1. During my test, I found out the antenna's performance still cannot match the official Pico w.
2. Still need more time and energy to tuning the antenna
3. No shield cover for the module on this version yet.
   
# considering support me?
Building the module and the picoduino definitley take time and energy.And also it's cost a lot. The module itself is a six layer board and I'm using the expensive Infineon chip. 
So I would appreciate anyone who can support me by purchase it from [this link](https://www.elecrow.com/picoduino.html)

# setup
For every board that you purchased, it's preflashed with a fw that can easily connect to local network as long as the wifi is available.
1. Plug picoduino to computer via USB type C cable.(A serial port should be available now)
2. Use some serial debug tool like arduino IDE's tool and type in your local WiFi name and then click send to send the WiFi name to picoduino.
3. it then will show the input WiFi name and ask you to type the password.
4. And send the password, picoduino will try to connect to the WiFi network with quick blink green led.
5. Once success, it will keep the green led on and you can copy the ip address to browser and then hit enter.
6. A webpage for controlling the green led is alive and you can control the led by click the webpage buttons.

![setup_1](https://github.com/yuanyong2024/picoduino/assets/163154773/be988514-2f7a-4296-be63-00dcd634ba4b)

![setup_2](https://github.com/yuanyong2024/picoduino/assets/163154773/806a8995-01f7-4954-a563-5d6b92b7542d)





# What's next?
After this picoduino, I will design a adafruit feather compatible one by using the same pico w module.
I will also make a programmable power supplier shield for picoduino.
## Stay tuned!

# useful links:
[pico w datasheet](https://datasheets.raspberrypi.com/picow/pico-w-datasheet.pdf?_gl=1*pez2dw*_ga*NTM5ODUxMTkxLjE3MTE2MzI0NTI.*_ga_22FD70LWDS*MTcxMTYzMjQ1Mi4xLjAuMTcxMTYzMjQ1Mi4wLjAuMA..)

[raspberry pi pico documentation](https://www.raspberrypi.com/documentation/microcontrollers/raspberry-pi-pico.html#raspberry-pi-pico-w)

[pico w module design file](https://github.com/yuanyong2024/pico_w_module)


