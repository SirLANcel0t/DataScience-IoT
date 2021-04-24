# DataScience-IoT
## About this project
For this course we had to create an IoT pipeline using a Raspberry Pi and a sensor.
I have chosen to work with a PIR (motion) sensor, which I will be using to turn on my Philips Hue lights.
The reason I chose this, is because I have been thinking about getting a motion sensor for a while and I thought it would be a fun experiment to set it up myself.

## Pipeline of IoT Project
Pipeline of this IoT project can be found in :"IoT Pipeline.png".

## Used stuff
### Hardware components
- Raspberry Pi 3 model A+
- 8GB Micro SD Card
- 3x F-M jumperwires
- HC-SR501 PIR Motion Sensor
- Power adapter Raspberry Pi 4 Micro USB
- Philips Hue lights and Bridge (refer to Philips Hue documentation to set this up on your local network)

### Software
- Python 3

## Hardware Setup
In this section, the process of connecting the motion sensor to Raspberry Pi is described
### Overview of DHT22 
HC-SR501 is a simple motion sensor which can be directly connected to the Raspberry Pi.
connector descriptions are as followed:
- Connector 1 = VCC, power supply
- Connector 2 = DATA, data out
- Connector 3 = GND, ground
### HC-SR501 and Pi Circuit
Steps to connect HC-SR501 to Raspberry Pi are described in this section. A circuit diagram can be found in the respiratory:"PIR and Pi Circuit.png"
1. Wire Physical Pin 2 Pi(power) to Connector 1 HC-SR501. (refer to red wire)
2. Wire Physical Pin 16 Pi(GPIO 23) to Connector 2 HC-SR501. (refer to yellow wire)
3. Wire Physical Pin 6 Pi(ground) to Connector 3 HC-SR501. (refer to black wire)

### Preparing raspberry pi
Plug in the power adapter and connect it to the Raspberry Pi. Connect to WiFi.


## Software Setup
To setup your new Raspberry Pi, refer to "THE OFFICIAL Raspberry Pi Beginner's Guide, Chapter 2". 
1. Once it's all set and ready, let's proceed to updating the Raspberry Pi by running the following commands:
* sudo apt full-upgrade
* sudo reboot
2. First, install the prerequisites:
* sudo apt install -y build-essential tk-dev libncurses5-dev libncursesw5-dev libreadline6-dev libdb5.3-dev libgdbm-dev libsqlite3-dev libssl-dev libbz2-dev libexpat1-dev liblzma-dev zlib1g-dev libffi-dev tar wget vim
3. Now, let's install both python 3 and pip with the following command:
* sudo apt  install python3-dev python3-pip
4. Then, update the setuptools, wheel and pip of python packages to the latest version:
* sudo python3 -m pip install --upgrade pip setuptools wheel

## Preparing the connection with Philips Hue
After having set up the hardware as above, the code to run this project can be found in "motion.py".
What the code does and where it does this can be found in the file with comments.
I used the meethue API, which is an official Philips Hue API, it was rather simple to implement.
What the code eventually does, is read the sensor's input, and based on this send a True/False value to the API.

## Running the code on the Raspberry Pi
Use Putty to run the Python file directly. The codes with comments can be found in motion.py in this repository. Make sure that the pins are wired like written above.

## Visualization of Data on the Raspberry Pi
Unfortunately due to transportation issues, I was not able to receive the sensor in time.

## Video
Unfortunately due to transportation issues, I was not able to test my code out and show it working in a video.
