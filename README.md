# SoundBow-Midi-Router
Additional midi message handling Pure Data patches for SoundBow

## Setup 

SoundBow supports MIDI, so it can be connected with other devices. It is based on CoreMIDI, and has been tested on OSX, should work on other operating systems too. There is a really easy way to setup a midi network through your wireless internet connection, if you follow the guidelines [on this site](http://www.musicappblog.com/wireless-network-midi-ipad-to-mac/) There can be found several good videos also on how to get started. 

Once you are ready and set with your network midi session, just launch SoundBow and select your iOS device to connect it to your midi session. If everything goes well, you will receive MIDI note on events sent to channel 1, channel 2 and channel 3, depending on what color you are using within SoundBow. You can forward these messages to your favourite DAW system, or do more experimental things like driving lights, motors and objects by sending the midi data to an Arduino for example. Since the sound engine of SoundBow is made with [Pure Data] (http://puredata.info/), and it is a very useful tool for experimenting quickly, you can download two Pure Data patches that can be interfaced with SoundBow. These can give you a hint on how to receive the messages and how to do some interesting stuff with them. 

## The Patch

- midi-router.pd

    Basic example that shows how to receive midi messages. 
    Since SoundBow sends only noteon messages at a constant velocity, you can add noteoff messages to all messages delayed by a certain value if you wish. It is good for instruments that are constantly giving sounds until they receive a note off. The velocity can also be applied here manually. The three different channels have three different controllers.


All code is under GPLv3 Licensed unless otherwise stated. (c) Agoston Nagy / 2016

