# DHT11 Sensor Data Logger

## Overview

This is a simple Arduino code example for reading data from a DHT11 temperature and humidity sensor and logging it to the Serial Monitor. The code uses the DHT library to interface with the sensor and then outputs the humidity and temperature data to the Serial Monitor at a specified interval.

## Hardware Requirements

- Arduino board (e.g., Arduino Uno)
- DHT11 sensor
- Jumper wires
- A computer with the Arduino IDE installed

## Library

The code utilizes the "DHT" library, which is required to interface with the DHT11 sensor. Make sure to install this library before uploading the code to your Arduino board. I used this library as it provides an easy and convenient way to communicate with the DHT11 sensor.

- [DHT Library Reference](https://github.com/adafruit/DHT-sensor-library): This library reference provides information on how to install and use the DHT library. It was helpful in understanding the functions and methods available for interacting with the DHT11 sensor.

## Pin Configuration

- Connect the DHT11 sensor's data pin to digital pin 21 on the Arduino. You can change the `DHTPIN` value to match your actual pin configuration if needed.

## Code Explanation

- The code starts by including the "DHT" library and defining some constants for the DHT sensor type and the data pin.

- The DHT object is created using these constants.

- In the `setup()` function, the serial communication is initialized at a baud rate of 115200, and the DHT sensor is initialized.

- The `loop()` function runs repeatedly, with a delay of 1000 milliseconds (1 second) between each iteration.

- Inside the `loop()` function, the code reads the humidity and temperature from the DHT sensor using the `readHumidity()` and `readTemperature()` methods.

- It checks if the data obtained is valid (not a NaN or "Not a Number" value). If the data is invalid, an error message is printed to the Serial Monitor.

- If the data is valid, it is printed to the Serial Monitor with appropriate labels for humidity and temperature.

## Usage

1. Connect your DHT11 sensor to your Arduino board following the pin configuration mentioned in the code.

2. Install the "DHT" library using the Arduino IDE if you haven't already.

3. Upload the code to your Arduino board.

4. Open the Serial Monitor (Ctrl+Shift+M) to view the temperature and humidity data being read from the DHT11 sensor.

5. You should see a continuous stream of data on the Serial Monitor, displaying humidity in percentage and temperature in degrees Celsius.

## Resources

- [DHT Library Reference](https://github.com/adafruit/DHT-sensor-library): Reference for the DHT library used in the code.
- [DHT11 Datasheet](https://www.sparkfun.com/datasheets/Sensors/Temperature/DHT11.pdf): Datasheet for the DHT11 sensor, providing detailed technical information.
- [Arduino Official Website](https://www.arduino.cc/): Official website for Arduino, where you can find documentation and tutorials.

## Troubleshooting

- If you encounter issues, double-check your wiring and make sure the DHT library is installed correctly.

- Ensure that your DHT11 sensor is functioning properly.

- You can adjust the data update interval by changing the delay time in the `loop()` function to your desired value.
