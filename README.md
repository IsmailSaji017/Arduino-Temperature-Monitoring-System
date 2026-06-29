# Arduino-Temperature-Monitoring-System
This project demonstrates a simple Temperature and Humidity Monitoring System using an Arduino UNO and a DHT22 sensor. The system reads real-time environmental data and displays the values on the Serial Monitor.
# Overview
This project demonstrates a simple Temperature and Humidity Monitoring System using an Arduino UNO and a DHT22 sensor. The system reads real-time environmental data and displays the values on the Serial Monitor.

The project is designed for beginners learning Arduino programming, sensor interfacing, and embedded systems simulation using Tinkercad or Wokwi.

# Features
Real-time temperature monitoring
Humidity measurement
Serial Monitor output
Error detection for sensor read failures
Easy to simulate without physical hardware
# Components Required
Arduino UNO
DHT22 Temperature & Humidity Sensor
Jumper Wires
Tinkercad Circuits / Wokwi Simulator
# Circuit Connections
DHT22 Pin| Arduino UNO VCC| 5V DATA| Digital Pin 2 NC| Not Connected GND| GND

<img width="807" height="765" alt="Screenshot 2026-06-21 201759" src="https://github.com/user-attachments/assets/4ea89286-a741-4da0-ae79-53e6d68ea195" />

# Architecture
DHT22 Sensor → Arduino UNO → Serial Monitor

# Arduino Code
#include "DHT.h"

#define DHTPIN 2 #define DHTTYPE DHT22

DHT dht(DHTPIN, DHTTYPE);

void setup() { Serial.begin(9600); dht.begin(); }

void loop() {

float temp = dht.readTemperature(); float hum = dht.readHumidity();

if (isnan(temp) || isnan(hum)) { Serial.println("Sensor Error"); return; }

Serial.print("Temperature: "); Serial.print(temp); Serial.print(" °C ");

Serial.print("Humidity: "); Serial.print(hum); Serial.println("%");

delay(2000); }

# How to Run
Open Tinkercad Circuits or Wokwi Simulator.
Create a new Arduino UNO project.
Add the DHT22 sensor.
Connect the circuit as shown above.
Upload the Arduino code.
Start the simulation.
Open the Serial Monitor to view temperature and humidity values.
# Sample Output
Temperature: 29.5 °C Humidity: 65% Temperature: 29.7 °C Humidity: 64% Temperature: 29.8 °C Humidity: 65%
<img width="1202" height="663" alt="Screenshot 2026-06-21 203810" src="https://github.com/user-attachments/assets/4a09fb3b-8d11-4b7c-bd54-e79d5ab2a0ac" />

# Applications
Weather monitoring systems
Smart home automation
Industrial environmental monitoring
IoT sensor data acquisition
Educational Arduino projects
# Future Enhancements
16×2 LCD display integration
High-temperature buzzer alert
IoT cloud connectivity using ThingSpeak
Data logging and visualization
Mobile dashboard monitoring
# Author
Ismail Saji Electronics and Communication Engineering (ECE) Here's a professional GitHub README for your project
