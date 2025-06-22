---
title: "RP2040 mini SDR"
author: "Keyaan"
description: "A Receive-only mini SDR capable of decoding FM, AM(Airband) and NOAA APT"
created_at: "2025-06-16"
---

# 16 June 2025

Okay, so i have thought of making an SDR, and yeah, i would love to make one using the Great RP2040. The idea is very rough yet, i have to work on it too much

What I(and a little bit of gpt) came up with:
#### this is [excalidraw](https://excalidraw.com) btw

![Block Diag](images/16/bd.png)


### Time Spent Today: 30 mins

# 18 June 2025

Okay, so today i found a few components for the mini SDR. Here they are:  
LNA: PSA4-5043+  
Mixer: ADE-11X+  
ADC: ADS7042  
Processor/Controller: RP2040: Arguable the best MCU ever Made  

### Time Spent on June 18: About 1 hour

# 22 June 2025

I chose an LO. Here is the list of the updated parts:  
LNA: [PSA4-5043+](https://www.lcsc.com/product-detail/RF-Amplifiers_Mini-Circuits-PSA4-5043_C5240848.html)  
Mixer: [ADE-11X+](https://lcsc.com/product-detail/RF-Mixers_Mini-Circuits-ADE-11X_C3176636.html)  
LO: [Si5351](https://www.lcsc.com/product-detail/Clock-Generators-PLLs-Frequency-Synthesizers_SKYWORKS-SILICON-LABS-SI5351A-B-GTR_C504891.html)  
LO AMP: [GALI-84+](https://lcsc.com/product-detail/RF-Amplifiers_Mini-Circuits-GALI-84_C3193261.html)
ADC: [ADS7042](https://lcsc.com/product-detail/Analog-to-Digital-Converters-ADC_Texas-Instruments-ADS7042IDCUR_C701641.html)  
Processor: [RP2040](https://www.lcsc.com/product-detail/Microcontrollers-MCU-MPU-SOC_Raspberry-Pi-RP2040_C2040.html)  
LPF: Simple LC Circuit  

### Updated Block DIag:
![22/bd.png](/images/22/bd.png)

### Time Spent Today: 2 hours 30 mins