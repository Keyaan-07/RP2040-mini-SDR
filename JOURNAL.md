---
title: "RP2040 mini SDR"
author: "Keyaan"
description: "A Receive-only mini SDR capable of decoding FM, AM(Airband) and NOAA APT"
created_at: "2025-06-16"
---
----
# 16 June 2025

Okay, so i have thought of making an SDR, and yeah, i would love to make one using the Great RP2040. The idea is very rough yet, i have to work on it too much

What I(and a little bit of gpt) came up with:
#### this is [excalidraw](https://excalidraw.com) btw

![Block Diag](images/16/bd.png)


### Time Spent Today: 30 mins
----
# 18 June 2025

Okay, so today i found a few components for the mini SDR. Here they are:  
LNA: PSA4-5043+  
Mixer: ADE-11X+  
ADC: ADCS7676 (old: ADS7042)  
Processor/Controller: RP2040: Arguable the best MCU ever Made  

### Time Spent on June 18: About 1 hour
----
# 22 June 2025

I chose an LO. Here is the list of the updated parts:  
LNA: [PSA4-5043+](https://www.lcsc.com/product-detail/RF-Amplifiers_Mini-Circuits-PSA4-5043_C5240848.html)  
Mixer: [ADE-11X+](https://lcsc.com/product-detail/RF-Mixers_Mini-Circuits-ADE-11X_C3176636.html)  
LO: [Si5351](https://www.lcsc.com/product-detail/Clock-Generators-PLLs-Frequency-Synthesizers_SKYWORKS-SILICON-LABS-SI5351A-B-GTR_C504891.html)  
LO AMP: [GALI-84+](https://lcsc.com/product-detail/RF-Amplifiers_Mini-Circuits-GALI-84_C3193261.html)  
ADC: [ADCS7476](https://lcsc.com/product-detail/Analog-to-Digital-Converters-ADC_Texas-Instruments-ADCS7476AIMFX-NOPB_C91530.html) (old: [ADS7042](https://lcsc.com/product-detail/Analog-to-Digital-Converters-ADC_Texas-Instruments-ADS7042IDCUR_C701641.html))  
Processor: [RP2040](https://www.lcsc.com/product-detail/Microcontrollers-MCU-MPU-SOC_Raspberry-Pi-RP2040_C2040.html)  
Crystal for RP2040: [ABM8-272-T3](https://lcsc.com/product-detail/Crystals_Abracon-LLC-ABM8-272-T3_C20625731.html)   
LPF: Simple LC Circuit  
XTAL: [XXGBBCNANF-25.000000MHZ
](https://lcsc.com/product-detail/Crystals_TAITIEN-Elec-XXGBBCNANF-25-000000MHZ_C521601.html)  

### Updated Block DIag:
![22/bd.png](/images/22/bd.png)

Umm okay, i did i BIT of schematic(or most of it cuz idk how much is left). Gonna take a break now, i think i might do some more later, so, will update the schematic later.

### Big Change: I am changing my ADC to the [ADCS7476](https://lcsc.com/product-detail/Analog-to-Digital-Converters-ADC_Texas-Instruments-ADCS7476AIMFX-NOPB_C91530.html)

Most of the schematic is now done. only connections to the rp2040 remaining prolly. Image:

![schematic on 22 june](/images/22/schematic.png)  
HELL YEAH! So much work done in a single day!!  

### Time Spent Today: 4 hours
----


# 23 June 2025

Yup, todya i am working on completing scheamtic, assigning and gathering footprints, and starting with the PCB. 

I want to make the footprint like Cyao has made in his [ESP-USB](https://github.com/cheyao/esp-usb). So i started out to make my own footprint, but after having less luck with myself, i just took it from [Cyao](https://github.com/cheyao/esp-usb/tree/main/hardware/esp-usb-lib.pretty). Hehehe thanks Cyao. This is the shit i thought i was cooking lol
![alt text](images/23/failed_usb.png)

I was thinking of using LEDs on SPI and I2C lines, but then GPT told me it was not ideal, so i did not simply put it!

oh yeah, btw i forgot to explain some stuff. This project uses a few RF ICs to convert the incoming frequencies into IF(Intermediate Frequency). This IF is then read by an ADC at 1 MSPS(Mega Samples Per second). ADC converts Analog values to digital values and RP2040 reads via SPI. this is then sent to PC where it is read by some other software.

![final schematic](/images/23/schematic_final.png)

did a bit of PCB, will upload the images later
Here are the images: 
![pcb](/images/23/pcb.png)

### Total Time Spent Today: 2 hours 30 mins
----
# June 24 2025

Hell yeah, i worked on my PCB in the school today, i got permission to bring my laptop hahaha. here is the progress:

oh hell nah, i forgot the ss and continued further, so nvm, here is the current progress:
![pcb](/images/24/pcb.png)