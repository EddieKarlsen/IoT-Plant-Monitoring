# IoT-Plant-Monitoring
This project aims to implement a complete soloution to remotley monitoring plants soilhumidity. 
To achivie this it uses an ESP-32 and a serverless Webapplication in AWS. The system allows the user to vissulaize historical moisture readings and handles waterreminders through a discord webhook

## Table of Contents
- [License](#license)
- [Requirements](#requirements)
- [How to use](#how-to-use)
- [Demonstration](#demonstration)


## License
This project is licensed under the MIT License – see the [LICENSE](./LICENSE) file for details.

![MIT License](https://img.shields.io/badge/License-MIT-green.svg)

##System Architecture
this projekt aims to build the system described in the following image
![systemArchitecture](/assets/systemArchitecture.png)

The **IoT part** of this project is described in: [humiditySensor-repository](https://github.com/EddieKarlsen/humiditySensor)

and **the web part** is described in: 
[flowerWatcher_amplify-repository](https://github.com/EddieKarlsen/flowerWatcher_amplify)

## Requirements
* `an AWS account if you want to get the api:s to work and  host it` 
* `a ESP-32`
* `a Flower`
* `a soil moisture sensor:` https://www.amazon.se/Jord-fuktsensor-kapacitiv-modul-kabel/dp/B08BJTWRJR

## How to use: 
1. `follow the instruction in` :[flowerWatcher_amplify-repository](https://github.com/EddieKarlsen/flowerWatcher_amplify)

2. `configure you're sensor as descirbed in`[humiditySensor-repository](https://github.com/EddieKarlsen/humiditySensor)
