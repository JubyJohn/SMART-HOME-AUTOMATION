# PROJECT SMART HOME AUTOMATION


## AIM

To print smart home automation guide on serial monitor for lighting system


## COMPONENTS

1.	ESP8266 NodeMCU
2.	LDR Sensor Module
3.	USB cable
4.	Jumper Wire


## CONNECTION

### LDR Sensor Module Pin Diagram

![LDR-Sensor-Module](https://github.com/JubyJohn/SMART-HOME-AUTOMATION/assets/81866407/d162a298-7b5f-4b1a-93cd-f3eabb30e631)

 
<br> S  = Output     ---->  A0
<br> Middle    = power supply  ---->  3V3
<br> GND   = ground   ---->  GND


## PROCEDURE

<br> Step 1 : Interface ESP8266 microcontroller to Arduino IDE using port.
<br> Step 2: Interface ESP8266 microcontroller with LDR and print analog resistance values on serial monitor.
<br> Step 3 : Modify the program to get desired outputs on serial  monitor


## PROBLEMS 

### Error 1 -   After uploading , serial monitor shows nothing
#### How to rectify:
After uploading, we need to press RST button of ESP8266. It is because that after uploading the sketch,it works for as long as you don’t open the serial monitor, but stops the moment you open it.

### Error 2 -   Analog reading loop keeps working,its not getting out the loop.
#### How to rectify:
You need to add "return 0" instead your loop to get outside when it gets data other than mentioned  data.


## OUTPUT

<br> On serial monitor , when RST button of ESP8266 pressed prints
<br> SMART HOME
<br> a) Auto Mode       b) Manual Mode      	 c) exit 
<br> Choose Your option....
<br> Type -> a
<br> Auto Mode Activated
<br> DAY TIME - LED OFF       // when light is detected by LDR, LED turned OFF
<br> NIGHT TIME - LED ON   // when no light is detected by LDR, LED turned ON
<br> Type -> c
<br> SMART HOME
<br> a) Auto Mode       b) Manual Mode      	 c) exit 
<br> Choose Your option......
<br> Type -> b
<br> Manual Mode Activated
<br> Type -> a for LED ON         Type -> b for LED OFF
<br> Type -> c
<br> SMART HOME
<br> a) Auto Mode       b) Manual Mode      	 c) exit 
<br> Choose Your option......
