# ESP-pwm-4ch

ESP32 based board with 4x PWM output channels.

This board is designed to be driven by an Olimex ESP32-POE, ESP32-POE-ISO or Wemos D1 Mini modules running Tasmota. If you want to use the ethernet interface present on the Olimex modules you will need to compile your own binaries enabling the corresponding features.

The design considers that the board will be mounted on a PCB DIN rail holder. The dimensions consider the holders offered by the Brazilian manufacturer Metaltex, check [here](https://www.metaltex.com.br/produtos/componentes/suportes/sp7-suporte-para-montagem-de-placa-de-circuito-impresso-em-trilho-din) for details.

The initial version of this board used a zero ohm gate resistor which provided a very fast switching of the MOSFET making the heat sinks unnecessary. Version 2 includes a 22 ohm gate resistor and has not yet been tested. Given the very low switching frequency and small loads I suppose they are still not necessary.

Expect some flicker when driving LEDs with the ESP8266. It gets much, much more stable when using the hardware PWMs of the ESP32.

![alt text](https://github.com/thermseekr/ESP-pwm-4ch/blob/main/V2/ESP-pwm_4ch-V2.png "ESP-pwm-8ch")
