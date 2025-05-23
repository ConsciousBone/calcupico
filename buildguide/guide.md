# CalcuPico Build Guide  
<details><summary><b>Changelog</b></summary>
    
| Version | Date     | Comments          |
|---------|----------|-------------------|
| 0.0.0   | 22/05/25 | Created guide.md. |
| 0.1.0   | 24/05/25 | Added skeleton for the guide. |
      
</details>  
  
> [!CAUTION]
> I am not responsible for any damages that may occur to your property while following this guide.  
> By following this guide, you assume all responsibility for any damages that may occur.
  
## Required Parts  

| Part                  | Link                       | Notes                                                                                                                                                                     |
|-----------------------|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Raspberry Pi Pico 2 W | [The Pi Hut]() | Any Pi Pico *should* work, but a Pico 2 W is recommended for its increased storage and processing power, and this guide assumes a Pico 2 W.                                           |
| 0.9" I2C OLED display | [The Pi Hut]() | The display comes with a connector soldered, which will have to be removed.                                                                                                           |
| Wire                  | [The Pi Hut]() | 30AWG wire is used throughout this guide, and is recommended due to it fitting nicely inside the calculator, however other wire gauges *may* work.                                    |
| Kapton tape           | [The Pi Hut]() | This is not required, but is highly recommended.                                                                                                                                      |
| Casio fx-85GT CW      | [Amazon]() | Other calculators *may* work, however this guide assumes the fx-85GT CW. If you decide to use a different calculator, ensure it has enough space inside to fit all of the components. I will not be able to provide hardware based support if you decide to use anything other than the Casio fx-85GT CW as I do not own every scientific calculator on the market. |

You will also need a way to strip the wire (if you use wire that isn't already stripped), a screwdriver to open the calculator, a way to put holes into the calculator's back panel to access the BOOTSEL button and USB port of the Pi Pico, and a soldering iron to solder the wires to the vias on the PCB and to the display.

## Guide  
### Opening the calculator
Unscrew the 6 Philips head screws on the back of the calculator, then remove the battery cover and back panel.  
TODO: add images here  

## Desoldering the solar panel
TODO: write guide

## Modifying the back panel
TODO: write guide

## Preparing the PCB
TODO: write guide

## Preparing the wires
TODO: write guide

## Mounting the display
### Option 1: Tape
TODO: write guide
### Option 2: 3D printed bracket
TODO: write guide + design bracket 

## Soldering the wires
TODO: write guide

## Installing CalcuPico software
### Flash MicroPython
TODO: write guide
### Copy CalcuPico apps to Pi Pico
TODO: write guide

## Testing
TODO: write guide  

**All done!** Now you have a fully functional CalcuPico. Feel free to continue onto [developing apps](#), or browse the app store for the apps and games you can install to your device!
