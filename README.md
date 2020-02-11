# weather_station

The weather station is using a DHT11, for measuring air humidity, a TMP102, for measuring air temperature a BMP180, for measuring the pressure and a prototyping PCB to build it.
The waether station measures the temperature in Celsius(it could be changed to Fahrenheit), the pressure in PSI - Pounds per square Inch and humidity in percentage. It also has deep sleep mode that can be controlled, by default is set on 5 minutes.

Step 1: Info About Adafruit HUZZAH ESP8266 (ESP-12E)
The ESP8266 processor from Espressif is an 80 MHz microcontroller with a full WiFi front-end (both as client and access point) and TCP/IP stack with DNS support as well.
Technical details:

>>Reset button,
>>User button that can also put the chip into bootloading mode,
>>Red LED you can blink,Level shifting on the UART and reset pin,
>>3.3V out,
>>500mA regulator (you'll want to assume the ESP8266 can draw up to 250mA so budget accordingly)
>>Two diode-protected power inputs (one for a USB cable, another for a battery)
>>Two parallel, breadboard-friendly breakouts on either side give you access to:
>>1 x Analog input (1.8V max)
>>9 x GPIO (3.3V logic), which can also be used for I2C or SPI2 x UART pins
>>2 x 3-12V power inputs,
>>reset,
>>enable,
>>LDO-disable,
>>3.3V output


Step 2: Info About DHT11
The DHT11 is a basic, ultra low-cost digital temperature and humidity sensor. It uses a capacitive humidity sensor and a thermistor to measure the surrounding air, and spits out a digital signal on the data pin (no analog input pins needed). Its fairly simple to use, but requires careful timing to grab data. The only real downside of this sensor is you can only get new data from it once every 2 seconds, sensor readings can be up to 2 seconds old.


Step 3: Info About TMP102
TMP102 is a super small digital temperature sensor. The TMP102 is a digital sensor (I2C a.k.a. TWI), has a resolution of 0.0625°C, and is accurate up to 0.5°C. This is a very handy sensor that requires a very low-current.

Communication with the TMP102 is achieved through a I2C serial interface. There is no on-board voltage regulator, so supplied voltage should be between 1.4 to 3.6VDC. Filtering capacitors and pull-up resistors are included.


Step 4: Info About BMP180
This is a breakout board for the Bosch BMP180 high-precision, low-power digital barometer. The BMP180 offers a pressure measuring range of 300 to 1100 hPa with an accuracy down to 0.02 hPa in advanced resolution mode. It’s based on piezo-resistive technology for high accuracy, ruggedness and long term stability. These come factory-calibrated, with the calibration coefficients already stored in ROM. What makes this sensor great is that it is nearly identical to its former rev, the BMP085!


Step 5: Tools & Materials for the Project
Parts:
Adafruit HUZZAH ESP8266 Breakout 
Headers - Male 
Headers - Female 
Prototyping PCB
BMP180 - Pressure sensor
DHT-11 - Temperature and humidity sensor 
TMP102 - Temperature sensor
Battery - rechargeable or not, I am using Li-ion 3.7v 2900 mah
Jumpers - Female to Female
FTDI cable.

Tools:
Soldering iron
Hot glue gun
Clips


Step 6: Making the Circuit Board
Make it with the help of the prototyping board. Connect the SDA and SCK pins of the TMP102 and BMP180 sensors to pins 5 and 4 (like on Arduino UNO) of the HUZZAH module and the DHT sensor to pin 2. GND to GND on the board and the power input of the sensors to +3 V pin of the HUZZAH board. If you want put a hardware reset button so you can reset the board. Also add a battery connector so you can power it with a battery like me. Also you have to put jumper between pin 16 and RST of the HUZZAH board so the board wake up.

By default the time for sleep is set on 300s - 5 minutes, if you want you can change it.



Step 8: Setting Up Adafruit IO




