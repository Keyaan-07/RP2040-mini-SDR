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

# Images:
![Schematic](/images/26/schematic.png)

![PCB final prolly](/images/27/PCB_final_probably.png)

![3d model final prolly](/images/27/3d_1.png)

![3d model final prolly](/images/27/3d_2.png)