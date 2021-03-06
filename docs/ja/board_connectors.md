---
layout: doc_toc_ja
title: board connectors
---
# ボードコンピュータ　コネクタ配置
CHIRIMENボードコンピュータのコネクターおよびスイッチの配置を紹介します。

## コネクタ配置図

![chirimen_board_front](../images/chirimen_board_front.jpg) 

![chirimen_board_back](../images/chirimen_board_back.jpg) 

1. USB OTG  
開発用ホストコンピュータを接続するためのMicroUSB Type BのUSBポートです
1. Micro HDMI type video connector  
HDMIビデオモニタを接続するためのコネクタです
1. USB UART
この端子は、多くのケースで使用しません。SoCが搭載するUARTxポートをUSBに変換した信号が出力されます。
1. 5V power in  
5Vの電源の入力コネクタです。外径2.5mmのDCコネクタです。
1. USB HOST  
ネットワークアダプタやポインティングデバイスなどを接続するためのUSB Type Aポートです。
1. Recover mode switch  
ファームウェアのアップデートのために主に使用するスイッチです。
1. CN1 (Connector1)  
GPIO, I2C, UART, SPIなどの信号が集約されたスルーホールの多用途入出力端子です。端子の信号配置図は後の章を参照してください。
1. CN2  (Connector2)  
もうひとつの多用途入出力端子です。
1. Micro SD Slot  
MicroSDスロットです。2016年2月現在まだOSはサポートしていません。

## 多用途入出力端子のピン配置
Note: Currently UART, SPI and PWM are re-assigned to GPIO.

||CN1 (Connector1)| |CN2 (Connector2)|
|------------|:--:|:----------:|:----------------:|
|Number|Description (sysfs name)| |Description (sysfs name)
|1|GND| |GND|
|2|I2C-2 SDA| |GND|
|3|I2C-2 SCL| |GND|
|4|GPIO-3 D3 (gpio283)| |GND|
|5|GPIO-3 D4 (gpio284)| |Audio L out|
|6|ADC-0 in| |Audio R out|
|7|GPIO-1 A4 (gpio196)| |Audio L in|
|8|GPIO-1 A5 (gpio197)| |Audio R in|
|9|GPIO-1 A6 (gpio198)| |Audio GND|
|10|GPIO-1 A7 (gpio199)| |GPIO-0 A3 (gpio163)|
|11|GPIO-1 C4 (gpio244)| |I2C-0 SCL|
|12|GPIO-1 C3 (gpio243)| |I2C-0 SDA|
|13|GPIO-1 C6 (gpio246)| |GPIO-0 A1 (gpio193)|
|14|GPIO-1 C5 (gpio245)| |GPIO-0 A0 (gpio192)|
|15|GND| |GPIO-6 A1 (gpio353)|
|16|VCC 3.3V| |Power ON|
|17|VCC 3.3V| |GND|
|18|VCC 5V| |VSYS 5V|

<!-- (ORIGINAL) 
||CN1 (Connector1)| |CN2 (Connector2)|
|------------|:--:|:----------:|:----------------:|
|Number|Description| |Description
|1|GND| |GND|
|2|I2C-2 SDA| |GND|
|3|I2C-2 SCL| |GND|
|4|UART-3 RX| |GND|
|5|UART-3 TX| |Audio L out|
|6|ADC-0 in| |Audio R out|
|7|SPI-0 CS| |Audio L in|
|8|SPI-0 CLK| |Audio R in|
|9|SPI-0 RX| |Audio GND|
|10|SPI-0 TX| |PWM-0|
|11|SPI-1 CS| |I2C-0 SCL|
|12|SPI-1 CLK| |I2C-0 SDA|
|13|SPI-1 RX| |UART-0 TX|
|14|SPI-1 TX| |UART-0 RX|
|15|GND| |GPIO-6 A1|
|16|VCC 3.3V| |Power ON|
|17|VCC 3.3V| |GND|
|18|VCC 5V| |VSYS 5V|
-->
