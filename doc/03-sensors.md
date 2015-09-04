# Sensors

The Telegea platform currently supports the following sensors:

* DS18B20 1-wire temperature sensor
* DHT22/AM2303 1-wire temperature/humidity sensor
* SHT21 temperature/humidity sensor
* Wireless sensors (XRF modules)

<br>

### Temperature sensors

The **DS18B20 1-wire temperature sensor** can be connected on a 1-wire bus. Each sensor has a unique ID built in. Up to 10 sensors can easily be handled. It is convenient to use the water proof version which is provided with a 3-wire cable which is used for the data line and power supply. This cable should be connected to an RJ11 plug for easy installation of the bus. The bus itself can be realized using a standard 4-wire flat telephone cable with RJ11 male plugs on each end. The cables and sensors are connected with each other with 1 to 2 Female RJ11 splitters.  

![DS18B20 waterproof temperature sensor](pictures/ds18b20-waterproof.jpg "DS18B20 waterproof temperature sensor")

<br>

### Temperature/Humidity sensors

The **DHT22/AM2303 sensor** provides both temperature and humidity measurements and also uses a 1-wire protocol. But it doesn't support a master/slave architecture and therefore cannot be connected together with other sensors on the same bus. That means one dedicated GPIO pin is needed for each sensor. This sensor doesn't support long cables and should be located close to the Smartbox (<1m) to allow for reliable sensor readings.  

![DHT22/AM2302 temperature and humidity sensor - wired](pictures/am2302-with-wire.jpg "DHT22/AM2302 temperature and humidity sensor - wired")


The **SHT21 sensor** also provides temperature and humidity measurements but uses a 2-wire I2C bus interface. This is more reliable then the 1-wire bus but needs an additional clock wire. All sensors are provided with the same fixed I2C bus address which cannot be changed and therefore it needs two dedicated GPIO pins for each sensor.

![SHT21 temperature and humidity sensor](pictures/sht21.jpg "SHT21 temperature and humidity sensor")

<br>

### Wireless sensors

*TODO*
