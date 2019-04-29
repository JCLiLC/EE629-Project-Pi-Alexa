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
* Plug in all the devices. In your Raspberry Pi Terminal, type 'arecord -l' to see your input devices. In this case, your device is 'card 1,device 0'. 

        **** List of CAPTURE Hardware Devices ****    
       card 1: VR [1MORE Spearhead VR], device 0: USB Audio [USB Audio]    
       Subdevices: 0/1    
       Subdevice #0: subdevice #0    
* Type 'aplay -l‘ to see your output devices. In this case, device is 'card 0, device 0'.

          **** List of PLAYBACK Hardware Devices ****
              card 0: ALSA [bcm2835 ALSA], device 0: bcm2835 ALSA [bcm2835 ALSA]
               Subdevices: 7/7
               Subdevice #0: subdevice #0
               Subdevice #1: subdevice #1
               Subdevice #2: subdevice #2
               Subdevice #3: subdevice #3
               Subdevice #4: subdevice #4
               Subdevice #5: subdevice #5
               Subdevice #6: subdevice #6
              card 0: ALSA [bcm2835 ALSA], device 1: bcm2835 ALSA [bcm2835 IEC958/HDMI]
               Subdevices: 1/1
               Subdevice #0: subdevice #0
* Type

       nano /home/pi/.asoundrc
 and then paste the following codes, save the file. This is to let Raspberry Pi knows which devices to use.

          pcm.!default {
        type asym
            playback.pcm {
                type plug
                slave.pcm "hw:0,0" .    #0,0 means output: card 0, device 0 
            }
            capture.pcm {
                type plug
                slave.pcm "hw:1,0" .  #1,0 means input: card 1, device 0 
            }
            
Register a new product
---
* Go to https://developer.amazon.com, log in to your account
* Go to https://developer.amazon.com/alexa/console/avs/home, choose PRODUCT->CREATE PRODUCT
* Fullfill product information, click next
* Click CREATE NEW PROFILE, fill the imformations, click next
![Image text](https://github.com/JCLiLC/EE629-Project-Pi-Alexa/blob/master/images/Screen%20Shot%202019-04-29%20at%204.33.39%20PM.png)
* Choose Other devices and platforms, generate your ID, then download your config.json profile
![Image text](https://github.com/JCLiLC/EE629-Project-Pi-Alexa/blob/master/images/Screen%20Shot%202019-04-29%20at%204.37.28%20PM.png)


