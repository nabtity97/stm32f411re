stm32f411re simple projects



Wiring of the ESP8266-01 WIFI module.



I have connected the WIFI module to the USB/TTL converter (It operates with 3.3 Volt)

 

 	ESP8266-01		USB/TTL

 	VCC		->	 3.3V

 	CH\_EN		-> 	 3.3V

 	But I used the 3.3V of the Nucleo board not from the USB/TTL, because the current of the TTL is not enough.

 	Attention: the Power led should be always

 	on.

 	RX  		->	  TX

 	TX		->	  RX

 



 

