# IoT-Plant-Monitoring
This project aims to implement a complete soloution to remotley monitoring plants soilhumidity. 
To achivie this it uses an ESP-32 and a serverless Webapplication in AWS. The system allows the user to vissulaize historical moisture readings and handles waterreminders through a discord webhook

## Table of Contents
- [License](#license)
- [Requirements](#requirements)
- [How to use](#how-to-use)
- [Demonstration](#demonstration)
- [Project Reflection & Technical Challenges](#project-reflection--technical-challenges)

## License
This project is licensed under the MIT License – see the [LICENSE](./LICENSE) file for details.
![MIT License](https://img.shields.io/badge/License-MIT-green.svg)



## System Architecture
this projekt aims to build the system described in the following image
![systemArchitecture](/assets/systemArchitecture.png)

The **IoT part** of this project is described in: [humiditySensor-repository](https://github.com/EddieKarlsen/humiditySensor)

and **the web part** is described in: 
[flowerWatcher_amplify-repository](https://github.com/EddieKarlsen/flowerWatcher_amplify)

## Security
this project uses aws authioritysation to handele login and user creation, and all communication uses TLS or HTTPS. There is however an flaw that i could not fix for my HTTP API:s namley that they lack API keys so they were a vulnerability

## Scalability
the project is scalabel in the sesnse that the limiting factor is the number of humidity sensors and ESP32:s and follows the moddel pay as you go whith aws. All data is stored in Dynamodbv2 tabbles but some such as the flower meta data and 
perhaps images of the flowers could be put for more longterm storage e.g S3

## Requirements
* `an AWS account if you want to get the api:s to work and  host it` 
* `a ESP-32`
* `a Flower`
* `a soil moisture sensor:` https://www.amazon.se/Jord-fuktsensor-kapacitiv-modul-kabel/dp/B08BJTWRJR

## How to use: 
1. `follow the instruction in` :[flowerWatcher_amplify-repository](https://github.com/EddieKarlsen/flowerWatcher_amplify)

2. `configure you're sensor as descirbed in`[humiditySensor-repository](https://github.com/EddieKarlsen/humiditySensor)

## Project Reflection & Technical Challenges
This project was developed within a focused timeframe (starting in the evening of Friday the 28th of November 2025  and finished for presentation on Wensday the 3:d of December in the afternoon), serving as a fast-paced learning experience.

### Time Allocation Summary:

| Area | Estimated Time Spent | Primary Challenges Encountered |
| :--- | :--- | :--- |
| **Frontend & Web Backend (Amplify/APIs)** | 70-80% | TypeScript and React state management, troubleshooting Cross-Origin Resource Sharing (CORS) issues between the API Gateway and the hosted frontend, and data serialization. |
| **IoT Firmware & AWS Integration (ESP32)** | 20-30% | getting certificetse into firmware and calibrating the sensor|

**Key Takeaways:**

* Gained experience with TypeScript and React development patterns.
* implemented a fully secure MQTT connection (TLS) from an embedded device (ESP32) to a serverless AWS backend.
* Learned to debug and resolve CORS issues in a multi-service AWS environment.
