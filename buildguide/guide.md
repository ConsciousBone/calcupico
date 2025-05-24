# CalcuPico Build Guide  
<details><summary><b>Changelog</b></summary>
    
| Version | Date     | Comments          |
|---------|----------|-------------------|
| 0.0.0   | 22/05/25 | Created guide.md. |
| 0.1.0   | 24/05/25 | Added skeleton for the guide. |
| 0.2.0   | 24/05/25 | Began writing guide, added links. |
      
</details>  
  
> [!CAUTION]
> I am not responsible for any damages that may occur to your property while following this guide.  
> By following this guide, you assume all responsibility for any damages that may occur.
  
## Required Parts  

| Part                  | Link                       | Notes                                                                                                                                                                     |
|-----------------------|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Raspberry Pi Pico 2 W | [The Pi Hut](https://thepihut.com/products/raspberry-pi-pico-2-w) | Any Pi Pico *should* work, but a Pico 2 W is recommended for its increased storage and processing power, and this guide assumes a Pico 2 W. Ensure your Pico has no headers, as they will not fit inside of the calculator's housing (either buy one without headers, or desolder them from a Pico you already own). |
| 0.9" I2C OLED display | [The Pi Hut](https://thepihut.com/products/0-91-oled-display-module) | The display comes with a connector soldered, which will have to be removed.                                                     |
| Wire                  | [The Pi Hut](https://thepihut.com/products/ultra-fine-stranded-wire-spool-10-meters-30awg-black) | 30AWG wire is used throughout this guide, and is recommended due to it fitting nicely inside the calculator, however other wire gauges *may* work.          |
| Kapton tape           | [The Pi Hut](https://thepihut.com/products/polyimide-tape) | This is not required, but is highly recommended.                                                                                          |
| Casio fx-85GT CW      | [Amazon](https://www.amazon.co.uk/Casio-FX-85GTCW-Black-Scientific-Calculator/dp/B0BVW38KQH/) | Other calculators *may* work, however this guide assumes the fx-85GT CW. If you decide to use a different calculator, ensure it has enough space inside to fit all of the components. I will not be able to provide hardware based support if you decide to use anything other than the Casio fx-85GT CW as I do not own every scientific calculator on the market. |

You will also need a way to strip the wire (if you use wire that isn't already stripped), a screwdriver to open the calculator, a way to put holes into the calculator's back panel to access the BOOTSEL button and USB port of the Pi Pico, a Micro USB cable to connect the Pi Pico to a computer to upload the software, and a soldering iron to solder the wires to the vias on the PCB and to the display.

# Guide  
### Opening the calculator
Unscrew the 6 Philips head screws on the back of the calculator, then remove the battery cover and back panel.  
TODO: add images here  

### Desoldering the solar panel
Locate the pads labelled `SP+` and `SP-`. Desolder the wires from these pads, unclip them from the clips on the back of the display, and carefully remove the solar panel.
TODO: add images

### Modifying the back panel
Moving to the back panel, you will notice there is some plastic where the PCB is, holding it in place. We will need to remove some of this to make room for the Pi Pico.  
Using a tool available to you, look at the image below and cut the circled plastic supports off of the back panel, ending up with something like the image. You can leave the rest intact.  
  
TODO: add images  
  
Next, we need to make some holes in the case for accommodating the BOOTSEL button and the USB port of the Pi Pico. You may use any suitable tool for this, I used a soldering iron and melted the required holes in the back panel.  
Look at the image below, and create holes in your back panel where they are positioned in the image.  

TODO: add images  

Finally, the solar panel has some support material behind and around it which will need removing.  
Locate it using the images below, and cut it out.  

TODO: add images.

### Preparing the PCB
*These next few steps are the hardest, so be prepared.*  
Locate the required vias on the PCB using the image below, and scrape off the black coating over them using a sharp object. This will expose some metal that we will be soldering to.  
TODO: add images  

Once you have removed the coating from the required vias, look at the image below, and mask off these areas with kapton tape. This will prevent any shorts that may occur. Please note that one of the vias is located under a plastic part of the display. Using a thin tool (such as a flat head screwdriver), this can be slightly pried up and safely cut out, giving you access to the required via.  

TODO: add images  

### Preparing the wires
Using the wire of your choice (preferably 30AWG if possible), cut 8 medium sized wires, and 4 longer ones. The medium wires will run from the Pi Pico to the vias, and the 4 longer ones will run to the display.  
An ideal size for the medium wires is around 9-10cm, and 14-15cm for the longer ones.   
Once you have made the wires, strip them on both ends, and tin the ends.  
  
TODO: add images.  

### Mounting the display
**Option 1: Tape**  
Exactly how you mount the display is up to you, but I have included some images below as to how I recommend the display be taped in place.

TODO: add images.
 
**Option 2: 3D printed bracket**  
*This option is not yet ready*, so for now, use Option 1, and if you decide to in the future, you can open the calculator back up and mount the display using the 3D printed bracket.  
TODO: design bracket.  

### Soldering the wires
This is the hardest step, as occaisonally the vias will not solder. Take your time, have patience, and it will work eventually.  
Looking at the table and image below, solder the 8 medium sized wires to the vias. You can either label them, or solder them to the Pico as we go.  
  
Next, solder the 4 longer wires to the display, using the table below.  
  
TODO: add images, add table  

### Installing CalcuPico software
**Flash MicroPython**  
TODO: write guide  

**Copy CalcuPico apps to Pi Pico**  
TODO: write guide  

### Testing
TODO: write guide  

**All done!** Now you have a fully functional CalcuPico. Feel free to continue onto [developing apps](#), or browse the app store for the apps and games you can install to your device!
