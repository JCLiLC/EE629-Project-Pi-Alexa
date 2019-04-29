# EE629-Project-Pi-Alexa

An alexa smart speaker based on Raspberry Pi
===
Required hardware
---
* Raspberry Pi 3, power cable and a monitor
* An USB 2.0 microphone with a build-in sound card
* An external speaker with 3.5mm audio cable

Input and output setups
---
* In your Raspberry Pi Terminal, type 'arecord -l' to see your input devices. In this case, your device is card 1,device 0. 
    **** List of CAPTURE Hardware Devices ****    
    card 1: VR [1MORE Spearhead VR], device 0: USB Audio [USB Audio]    
       Subdevices: 0/1    
     Subdevice #0: subdevice #0    


Register a new product
---
* Go to https://developer.amazon.com, log in to your account
* Go to https://developer.amazon.com/alexa/console/avs/home, choose PRODUCT->CREATE PRODUCT
* Fullfill product information, click next
* Click CREATE NEW PROFILE, fill the imformations, click next
![Image text](https://github.com/JCLiLC/EE629-Project-Pi-Alexa/blob/master/images/Screen%20Shot%202019-04-29%20at%204.33.39%20PM.png)
* Choose Other devices and platforms, generate your ID, then download your config.json profile
![Image text](https://github.com/JCLiLC/EE629-Project-Pi-Alexa/blob/master/images/Screen%20Shot%202019-04-29%20at%204.37.28%20PM.png)

