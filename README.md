# RP2040 Mini SDR
This is an SDR, as the name says, and it can function in the FM, Airband and NOAA-APT bands ONLY AS A RECEIVER. This is completely legal to make and use.  
I have used RP2040 and ADE-11X+ mixer and SI5351 controllable clock. I thought that i would use a PCB trace USB but then i didn't do it because it would make the board cost go BOOOOM. So, normal USB-A.

I am in no way an RF expert and would love it if someone pointed out my errors and mailed them to [me](mailto:keyaan.1911@gmail.com) or DM on [hackclub](https://hackclub.com) Slack ```@Keyaan```

I think I am gonna make another RF board that could legally transmit too! but that's just an idea for now. 

I am not making a 3D model for this project as i feel this is not required for now. 

## Why I chose to make this project
I have always wanted to try out stuff with RF, especially receiving images from NOAA with my own stuff(I have used [WebSDRs](https://websdr.org) before).  
So i thought that why not make it FM too. And then GPT told me i could legally listen to airband signals too. 

So, i planned to make out an SDR using the goated RP2040 chip and a few mixers and oscillators.  

I have used an SMA connector as it is the most common one i think. 

## How to make and bake it!
Your take the gerber files from this repository and then you upload them to your desired PCB manufacturer. I am using [PCB Power](htttps://pcbpower.com) as they support hcb cards and are only about 350km from my home. and you also order the parts listen in the BOM, i wont order everything, as i have a few things from my previous orders. so, in the BOM, there is Do Not Order column(DNO) that shows what i wont order but you would have to order if you wanna make it. Then you prep the PCB with solder paste. Then you just use the ibom from this repo and place the components and bake it up.

I have set prices to 0 for the components that i have already but i have linked them down.

# Images:
![Schematic](/images/26/schematic.png)

![PCB final prolly](/images/27/pcb_final_probably.png)

![3d model final prolly](/images/27/3d_1.png)

![3d model final prolly](/images/27/3d_2.png)

# BOM
|ITEM NAME                 |ITEM PRICE|FUNCTION                                                          |URL                                                                                                                                                        |OTHERS|
|--------------------------|----------|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|------|
|PCB Manufacturing(4 Layer)+Stencil|$29.14    |The Main PCB + Stencil                                                     |https://jlcpcb.com                                                                                                                                       |      |                                                               |      |
|PCB Components            |$23.49    |Components on PCB                                                 |https://lcsc.com                                                                                                                                           |      |
|Tape Measure and SMA Cable|$5.57     |tape measure for a dipole antenna and sma to connect it to the PCB|https://www.amazon.in/FREEMANS-IKON-5m-Unbreakable-Bi-material/dp/B010M5GQ78/ , https://www.amazon.in/3AN-Telecom-Coaxial-Extension-Security/dp/B08GKXS915/|      |
|Total                     |$58.20    |                                                                  |                                                                                                                                                           |      |  

### Update 2: i updated the stencil to be ordered from jlcpcb instead of pcbpower, as it was wayy expensive. Thank You.

### Update: I updated the pcb manufacturer from pcbpower to jlcpcb as pcbpower was way too expensive, and i didn't change the stencil if i add stencil on jlcpcb, the stencil+pcb would jump from $15 to $52 because shipping would be so much more, so i will order pcb from jlc for $15 incl. shipping and the stencil from pcbpower only because that would make it overall cheaper. Basically both from jlc would have been $52 and pcb from jlc and stencil form pcbpower is $42, so we save $10.
----
### Note: There are a few resistors and capacitors, which had very high minimum order quantity(MOQ), about 100 pieces so i had to forcefully include those, which i will be utilising in my next highway projects. And tbh the prices were very less(about $0.002 per piece) so i think it is alright.

# PCB Component Breakdown

|Id |Designator                                                           |Designation       |MPN                    |Footprint                          |DNO - Do Not Order|DNP|MOQ|price |Quantity|Amount|LCSC Part No.|Supplier Link                                                                                                                     |
|---|---------------------------------------------------------------------|------------------|-----------------------|-----------------------------------|------------------|---|---|------|--------|------|-------------|----------------------------------------------------------------------------------------------------------------------------------|
|1  |C1, C10, C11, C12, C13, C14, C15, C17, C18, C20, C21, C26, C6, C7, C9|100n              |GRM155R61H104JE14D     |402                                |Yes               |No |-  |0     |15      |0     |             |https://lcsc.com/product-detail/Multilayer-Ceramic-Capacitors-MLCC-SMD-SMT_Murata-Electronics-GRM155R61H104JE14D_C426067.html     |
|2  |C16, C8                                                              |1u                |GRM155R61H105KE05D     |402                                |Yes               |No |-  |0     |2       |0     |             |https://lcsc.com/product-detail/Multilayer-Ceramic-Capacitors-MLCC-SMD-SMT_Murata-Electronics-GRM155R61H105KE05D_C1518208.html    |
|3  |C19, C22, C4, C5                                                     |10u               |CL21A106KBYQNNE        |805                                |No                |No |Yes|0.0509|10      |0.509 |             |https://lcsc.com/product-detail/Multilayer-Ceramic-Capacitors-MLCC-SMD-SMT_Samsung-Electro-Mechanics-CL21A106KBYQNNE_C2932476.html|
|4  |C2, C3                                                               |15p               |GJM1555C1H150FB01D     |402                                |Yes               |No |-  |0     |2       |0     |             |https://lcsc.com/product-detail/Multilayer-Ceramic-Capacitors-MLCC-SMD-SMT_Murata-Electronics-GJM1555C1H150FB01D_C441742.html     |
|5  |C23, C24                                                             |22p               |GJM1555C1H220FB01D     |402                                |No                |No |Yes|0.0379|20      |0.758 |             |https://lcsc.com/product-detail/Multilayer-Ceramic-Capacitors-MLCC-SMD-SMT_Murata-Electronics-GJM1555C1H220FB01D_C882567.html     |
|6  |C25                                                                  |10n               |CC0402JRX7R9BB103      |402                                |No                |No |Yes|0.0016|100     |0.16  |             |https://lcsc.com/product-detail/Multilayer-Ceramic-Capacitors-MLCC-SMD-SMT_YAGEO-CC0402JRX7R9BB103_C272878.html                   |
|7  |D1                                                                   |ESDS314DBVR       |ESDS314DBVR            |ESDS314BVR_SOT95P280X145-5N        |Yes               |No |-  |0     |1       |0     |             |https://lcsc.com/product-detail/ESD-and-Surge-Protection-TVS-ESD_Texas-Instruments-ESDS314DBVR_C1847859.html                      |
|8  |IC1                                                                  |PSA4-5043+        |PSA4-5043+             |PSA45043                           |No                |No |No |2.22  |1       |2.22  |             |https://lcsc.com/product-detail/RF-Amplifiers_Mini-Circuits-PSA4-5043_C5240848.html                                               |
|9  |IC2                                                                  |ADE-11X+          |ADE-11X+               |ADE-11X+_SOTFL254P691X284-6N       |No                |No |No |4.87  |1       |4.87  |             |https://lcsc.com/product-detail/RF-Mixers_Mini-Circuits-ADE-11X_C3176636.html                                                     |
|10 |IC3                                                                  |SI5351A-B-GTR     |SI5351A-B-GTR          |SI5351_SOP50P490X110-10N           |No                |No |No |0.92  |1       |0.92  |             |https://lcsc.com/product-detail/Clock-Generators-PLLs-Frequency-Synthesizers_SKYWORKS-SILICON-LABS-SI5351A-B-GTR_C504891.html     |
|11 |IC4                                                                  |GALI-84+          |GALI-84+               |GALI5                              |No                |No |No |4.3   |1       |4.3   |             |https://lcsc.com/product-detail/RF-Amplifiers_Mini-Circuits-GALI-84_C3193261.html                                                 |
|12 |IC5                                                                  |ADCS7476AIMFX_NOPB|ADCS7476AIMFX_NOPB     |ADCS7476_SOT95P280X145-6N          |No                |No |No |1.9   |1       |1.9   |             |https://lcsc.com/product-detail/Analog-to-Digital-Converters-ADC_Texas-Instruments-ADCS7476AIMFX-NOPB_C91530.html                 |
|13 |J1                                                                   |Conn_Coaxial_Small|BWSMA-KE-P001          |SMA_Amphenol_132289_EdgeMount      |No                |No |No |0.38  |1       |0.38  |             |https://lcsc.com/product-detail/Coaxial-Connectors-RF_BAT-WIRELESS-BWSMA-KE-P001_C496550.html                                     |
|14 |J2                                                                   |USB_A             |USB-212-BCW            |USB_A_Connfly_DS1098_Horizontal    |No                |No |Yes|0.0819|5       |0.4095|             |https://lcsc.com/product-detail/USB-Connectors_XUNPU-USB-212-BCW_C720521.html                                                     |
|15 |L1, L2                                                               |220n              |FEC0805CP-R22G-LRH     |805                                |No                |No |Yes|0.0618|10      |0.618 |             |https://lcsc.com/product-detail/Inductors-SMD_PSA-Prosperity-Dielectrics-FEC0805CP-R22G-LRH_C346387.html                          |
|16 |L3, L4                                                               |15u               |YWLD2012-150K          |805                                |No                |No |Yes|0.0391|10      |0.391 |             |https://lcsc.com/product-detail/Inductors-SMD_YJYCOIN-YWLD2012-150K_C5339219.html                                                 |
|17 |R1, R7                                                               |10k               |RCS040210K0FKED        |402                                |Yes               |No |-  |0     |2       |0     |             |https://lcsc.com/product-detail/Chip-Resistor-Surface-Mount_Vishay-Intertech-RCS040210K0FKED_C3020235.html                        |
|18 |R2, R3                                                               |27                |ERJ2GEJ270X            |402                                |Yes               |No |-  |0     |2       |0     |             |https://lcsc.com/product-detail/Chip-Resistor-Surface-Mount_PANASONIC-ERJ2GEJ270X_C278580.html                                    |
|19 |R4, R5                                                               |1k                |ERJPA2F1001X           |402                                |Yes               |No |-  |0     |2       |0     |             |https://lcsc.com/product-detail/Chip-Resistor-Surface-Mount_PANASONIC-ERJPA2F1001X_C427241.html                                   |
|20 |R6                                                                   |50                |RT0402BRE0750RL        |402                                |No                |No |Yes|0.0207|20      |0.414 |             |https://lcsc.com/product-detail/Chip-Resistor-Surface-Mount_YAGEO-RT0402BRE0750RL_C853312.html                                    |
|21 |SW1                                                                  |SW_Push           |PTS810SJM250SMTRLFS    |SW_SPST_PTS810                     |No                |No |No |0.6   |3       |1.8   |             |https://lcsc.com/product-detail/Tactile-Switches_C-K-PTS810SJM250SMTRLFS_C116501.html                                             |
|22 |U1                                                                   |RP2040            |RP2040                 |QFN-56-1EP_7x7mm_P0.4mm_EP3.2x3.2mm|No                |No |No |1.131 |1       |1.131 |             |https://lcsc.com/product-detail/Microcontrollers-MCU-MPU-SOC_Raspberry-Pi-RP2040_C2040.html                                       |
|23 |U2                                                                   |W25Q128JVS        |W25Q128JVS             |SOIC-8_5.3x5.3mm_P1.27mm           |Yes               |No |-  |0     |1       |0     |             |https://lcsc.com/product-detail/NOR-FLASH_Winbond-Elec-W25Q128JVSIM_C2613930.html                                                 |
|24 |U3                                                                   |AMS1117S-3.3      |AMS1117S-3.3           |SOT-89-3                           |yes               |No |-  |0     |1       |0     |             |https://lcsc.com/product-detail/Voltage-Regulators-Linear-Low-Drop-Out-LDO-Regulators_JSMSEMI-AMS1117S-3-3_C917152.html           |
|25 |Y1                                                                   |Crystal_GND24     |ABM8-272-T3            |Crystal_SMD_3225-4Pin_3.2x2.5mm    |No                |No |No |0.3731|2       |0.7462|             |                                                                                                                                  |
|26 |Y2                                                                   |Crystal_GND24     |XXGBBCNANF-25.000000MHZ|Crystal_SMD_3225-4Pin_3.2x2.5mm    |No                |No |Yes|0.1459|5       |0.7295|             |https://lcsc.com/product-detail/Crystals_TAITIEN-Elec-XXGBBCNANF-25-000000MHZ_C521601.html                                        |
|   |Rounding Errors                                                      |1.2338            |USD                    |                                   |                  |   |   |      |        |      |             |                                                                                                                                  |
|   |Shipping                                                             |3.74              |USD                    |                                   |                  |   |   |      |        |      |             |                                                                                                                                  |
|   |Total                                                                |23.49             |USD                    |                                   |                  |   |   |      |        |      |             |                                                                                                                                  |
