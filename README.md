ws2812b-chibios-SPIDMA
======================

Small driver for ws2812b LEDs with chibiOS/RT

Here we 'hack' the board SPI so that it sends data at the appropriate speed to the WS2812b in theur weird protocol.
This code is only tested on the stm32f4xx boards so I won't promess anything on the other ones (even though it should just be about setting the proper SPI speed I guess).

To use this code, simply include the leds and hsv2rgb files in your source code.
Call `leds_init();` and then, voilà ! You can set your leds colors using the API in the leds.h file (I chose to use hsv2rgb structs to lower the amount of code I have to write, but it is easily changeable so that you pass 3 uint8_t).

You will also need to plug your LED strip on the MOSI of the SPI you are using, and configuring the pin to the appropriate Alternate Function (e.i. SPI).

Have fun !

If you have issues with this lib, you can contact me at gamaz3ps on gmail.
