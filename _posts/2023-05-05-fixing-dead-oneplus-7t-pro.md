---
layout: post
title: Fixing Dead OnePlus 7T Pro
date: '2023-05-05 15:39:46 +0400'
categories: [Smartphone, OnePlus7TPro]
tags: [oneplus,7tpro,deadphone, op7tpro, oneplus7tpro, op7tp]
author: geekroid
commets: true
---

## Introduction
Hey everyone! Today we will be working on fixing dead OnePlus 7T Pro. I usually break my phones after installing custom ROMs so if your here proabably out of curiosity or you have a dead smartphone. **Let's Get Started!**

## Downloadables
Based on your phone where you got your phone from (EU or International or India), you can download the unbrick tool
### HD01AA Tools (International and Indian Firmware)
#### Android 10
[10.0.3](https://androidfilehost.com/?fid=4349826312261628475)
[10.0.4](https://androidfilehost.com/?fid=4349826312261684937)
[10.0.5](https://androidfilehost.com/?fid=4349826312261684661)
[10.0.7](https://androidfilehost.com/?fid=4349826312261732252)
[10.0.8](https://androidfilehost.com/?fid=4349826312261785391)
[10.0.11](https://androidfilehost.com/?fid=10763459528675559912)
[10.0.12](https://androidfilehost.com/?fid=10763459528675586246)
[10.0.13](https://androidfilehost.com/?fid=17248734326145684336)
[10.0.14](https://androidfilehost.com/?fid=2188818919693750610)

#### Andriod 11
[11.0.5.1](https://androidfilehost.com/?fid=2981970449027569861)

### HD01BA Tools (European Firmware)

#### Android 10

[10.0.3](https://androidfilehost.com/?fid=4349826312261631928)
[10.0.4](https://androidfilehost.com/?fid=4349826312261684936)
[10.0.5](https://androidfilehost.com/?fid=4349826312261684660)
[10.0.7](https://androidfilehost.com/?fid=4349826312261732251)
[10.0.8](https://androidfilehost.com/?fid=4349826312261785390)
[10.0.11](https://androidfilehost.com/?fid=10763459528675559911)
[10.0.13](https://androidfilehost.com/?fid=17248734326145684337)

#### Android 11
[11.0.5.1](https://androidfilehost.com/?fid=2981970449027569862)

### OnePlus USB Drivers
Download the USB drivers from the below link
[OnePlus USB Drivers](https://oneplususbdrivers.com/)

When you install it and it is stuck at `executing commands`:
* Cancel the installation 
* Disable the windows defender `Real Time Protection` and `Tamper Protection`
* Remove what was insalled from Control Panel `One Plus USB Drivers`
* Rerun the installer again it will install successfully.
* You will be prompted with Message saying the Log File already exists just Click `Ignore` This will overwrite what was installed earlier.

### Android Platform Tools 
Download Platform Tools from google based on the OS you are using.

[Platform Tools](https://developer.android.com/tools/releases/platform-tools)

### Download All in one Tool
[All in one Tool](https://toolaio.tk/download/)

## Step By Step Guide
### Install TWRP Recovery
Now this is out of the way we need to put the Phone in Fastboot mode

Press the Power button, Volume up and Volume down together for 10 seconds. You will note the oneplus logo and Fastboot underneath.

Connect your phone to the compuer and open All in One Tool. It will detect the phone in Fastboot mode.

In my case the phone was completely dead not able to reach discovery so from the all in one tool select `Recovery Flasher and Device Rooter` 

The popup will prompt you with `2 Versions of TWRP Recover` Select any of them and click flash.

A CMD will run at background showing the progress and the phone will have TWRP recovery

Once you see on the screen
```shell
Press any Key to Continue
```
Press Enter and Lets move to the next Step

### Put the Phone in EDL Mode
For some reason holding the Power button, volume up and down letting them go didn't put my phone in EDL mode. so I used this solution as alternative.

Once the Phone is in Fastboot mode use the volume up button to select the option `Boot To Recover`. Press the Power button to continue to Recovery.

The Tool will detect the phone is in recvoery mode. Then press Reboot to EDL. In my case the phone went completely black screen I assume that is normal. 

### Unbrick The Phone

Open MSM Tool we downloaded earlier and click `Enum`. The phone status should be connected. In the Target choose `India or O2` based on the frimware you downloaded. and Finally click `Start`.

The Process took about `10 - 15 minutes` to complete and the phone is back to normal state. 

Once completed now you can setup the Phone normally and make sure to upgrade to latest version of Oxygen OS as we downloaded old one using the MSM Tool.

I hope this helped :blush::blush::blush::blush::blush::blush:
## References
[One Plus Community Server](https://onepluscommunityserver.com/list/Unbrick_Tools/)

[XDA Developers OnePlus 7TPro Recovery](https://forum.xda-developers.com/t/op7tpro-oos-hd01aa-hd01ba-unbrick-tool-to-restore-your-device-to-oxygenos.4002909/)

[XDA Developers Tool to All in One](https://forum.xda-developers.com/t/tool-tool-all-in-one-drivers-unlock-twrp-factory-image-stock-recovery.3358711/)