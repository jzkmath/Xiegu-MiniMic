# Xiegu-MiniMic
A Small Microphone for the Xiegu G90, X5105 and X6100 Radios. I have designed this to be assembled mostly by JLCPCB. (See below for instructions on how to order them)

After looking at the larger Microphone that comes with the radio, it appears to be a clone of the ICOM HM151 Hand Mic. Knowing this, I was able to use the service manual to create this PCB.

This is designed using KiCad Version 6.0.9

The Enclosure can be 3D Printed and requires 4 M2x20mm Socket Head Screws and 4 M2 Nuts. I used McMaster Carr Part numbers 91292A013 and 90591A111 for this project.

## Version History:

Rev. A: Initial Design

Rev. B: Found that the EM6022P Microphone Element was wired backwards. Fixed it in this revision.

![Mic Size Comparison](https://github.com/jzkmath/Xiegu-MiniMic/blob/master/Mic%20Size%20Comparison.jpg)

![Enclosure Close up](https://github.com/jzkmath/Xiegu-MiniMic/blob/master/Enclosure%20Close%20Up.jpg)

![PCB Render](https://github.com/jzkmath/Xiegu-MiniMic/blob/master/Xiegu%20MiniMic.jpg)


## PCB Assembly Instructions:

1. Download this repository by clicking on "code" then downloading as a ZIP file. Extract the ZIP file.
2. Go to https://jlcpcb.com/quote
3. Click "Add Gerber File" upload the `Xiegu-MiniMic-GERBER.zip` file found in the `GERBER` folder.
4. Adjust settings. The only ones you should change (if you want) is PCB Qty, PCB Color, and Surface Finish. 
  - If you just want the PCB you may click "Save to Cart" and place your order.
  - If you want assembly, proceed to step 5.
5. Scroll don and tick the slider to the right of "PCB Assembly"
6. Leave it set to "Assemble Top Side" and click "Confirm"
7. For the "BOM File" upload `Xiegu MiniMic.csv` in the `ASSEMBLY` folder.
8. For the "CPL File" upload `Xiegu MiniMic-top-pos.csv` in the `ASSEMBLY` folder.
9. For Usage, I recommend you set it to "Research/Education/DIY/Entertainment > DIY HS Code 902300" (You can really set it to whatever you want)
10. Click "Next"
11. Make sure the BOM is complete (except for the RJ45 connector) 
  - If one of the parts are out of stock, you can substitute with a similar part. 
  - For resistors and capacitors, the main thing to ensure is the value and the case is 0805 (except for C3)
  - C3 is an electrolytic capacitor. Specs needed: 10uF, at least 16V, Diameter: 4mm, Length: 5.4mm (SMD)
  - Zener Diodes are 9.1v, and have a SOD-123 package
  - Inductor L1 is 33uH and has a 1008 package size
12. Once any substitutions are made, click "Next"
13. Inspect the render to make sure the orientation is correct. C3 should have the plus line up and the diodes should have their negative on the right side, matching up with the silkscreen.
14. Click "Add to Cart" then place your order.

You will likely need to order the RJ45 connector (54602-908LF) and microphone (EM6022P) from Digikey or Mouser and solder them yourself. 
