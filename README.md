# Smart Lighting System Using LDR

## Overview
This project demonstrates a Smart Lighting System using Arduino and an LDR (Light Dependent Resistor). The system automatically turns an LED ON or OFF based on the surrounding light intensity.

## Features
- Automatic light control
- Uses LDR as a light sensor
- Energy-efficient lighting

## Components Used
- Arduino Uno
- LDR (Light Dependent Resistor)
- LED
- 220Ω Resistor
- 10kΩ Resistor
- Breadboard
- Jumper Wires

## Working Principle
- The Arduino continuously reads the LDR value.
- During daylight, the LED remains OFF.
- In darkness, the LED automatically turns ON.

## Circuit Diagram

<img width="881" height="507" alt="image" src="https://github.com/user-attachments/assets/64005dd7-b447-4bb2-98b2-010724d58c86" />


## Arduino Code


const int ldrpin = A0; 
const int ledpin = 13; 
const int threshold = 400; 
void setup() { 
    pinMode(ledpin, OUTPUT); 
    Serial.begin(9600); } 
void loop() { 
    int lightvalue = analogRead(ldrpin); 
    Serial.print("Light Level : "); 
    Serial.println(lightvalue); 
    if (lightvalue < threshold) { 
        digitalWrite(ledpin, HIGH); } 
    else { 
        digitalWrite(ledpin, LOW); } 
 delay(200);

## Applications
- Smart Homes
- Street Lighting
- Garden Lighting
- Energy Saving Systems

## Software Used
- Arduino IDE
- Tinkercad

## Author
**Rohan Kumar**

B.Tech Electronics & Communication Engineering
