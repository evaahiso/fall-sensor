# fall-sensor
This repository contains the code used to program a fall sensor created using an Adafruit Circuit Playground Bluefruit board.

This project was part of UCL Biomedical Engineering scenario week. The main goal of this scenario was to create an item of wearable technology that has an application in the field of healthcare.

This fall sensor is aimed at people who are at risk of falling and needing external help, such as the elderly or people with epilepsy. When a fall is detected, the sensor sends a message to a family member with the person's location. Due to the lack of a Wi-Fi sensor, it uses Bluetooth to send a message using the UART protocol to the wearer's phone. This message is received using the Bluefruit Connect app, from where it is uploaded to the selected Adafruit IO feed using MQTT. The notification (which can be set to SMS, email, etc) is sent using IFTTT. An IFTTT applet is set so that it triggers a notification whenever the feed receives new data (in this case saying that the person wearing the sensor has fallen). 
