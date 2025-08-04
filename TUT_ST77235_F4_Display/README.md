# Interfacing Stm32f411re nucleo board with 1.8 TFT SPI 1280\*160 v1.1 display

In this project I am turning on the TFT display.



I have used SPI2 with the following parameters:

&nbsp;	Mode: Full duplex

&nbsp;	Prescaler: 8

&nbsp;	Baud Rate: 5.25 MBits/s

all other parameters are the default values.



In the RCC I have set the 

&nbsp;	High Speed Clock to BYBASS clock

&nbsp;	Low Speed Clock to Crystal/Ceramic 

But I'm not sure if it's important or it can be ignored.



I have added 3 .c files to the Src folder. The files are

 	fonts.h

 	GFX\_FUNCTIONS.h

 	ST77735.h



I have added 3 .h files to the Inc folder. The files are 

&nbsp;	fonts.h

&nbsp;	GFX\_FUNCTIONS.h

&nbsp;	ST77735.h


The Connections are as following:


&nbsp;	TFT side        Microcontroller side



&nbsp;	VCC Pin    ->   3.3V  Pin   

&nbsp;	LED Pin    -> 	3.3V  Pin
	GND Pin    -> 	GND   Pin
	SDA Pin    -> 	MOSI  Pin     in case of SPI2(PC3)

&nbsp;	SCK Pin    ->   SPI Clock Pin in case of SPI2(PB10)



The other 3 Pins are (RST, CS, A0) are connected to any 3 Pins which are configured as GPIO\_Output.

The 3 Pins which are configured as an output and the used SPI should be added to the code to the file ST773.h.



extern SPI\_HandleTypeDef hspi2;

\#define ST7735\_SPI\_PORT hspi2



\#define CS\_PORT GPIOB

\#define CS\_PIN  GPIO\_PIN\_6

\#define DC\_PORT GPIOA

\#define DC\_PIN  GPIO\_PIN\_9

\#define RST\_PORT GPIOC

\#define RST\_PIN  GPIO\_

