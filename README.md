# Stranger-Things-Light-Wall-with-ESP
A Stranger Things Light Wall made with an ESP and WS2811 LEDs

I used: 

-ESP8266

-Buck converter x2 (5v and 12v)

-Level converter (3.3v to 5v.  From ESP to LEDs)

-String of WS2811 lights

-330 Ohm resistor

------------------------------------------------------------------------------------------------------------
Basic wiring:

ESP D2 to 330ohm resistor to LV1 of level converter

ESP 3.3v to LV of level converter

ESP ground to low side ground of level converter

HV1 on level converter to signal/data wire for WS2811

Buck conveter1 (set to 5v) positive to HV on level converter

Buck converter1 (set to 5v) ground to ground on HV side of level converter

Buck converter2 (set to 12v) positive to WS2811 positive

Buck converter2 (set to 12v) ground to WS2811 ground

Buck converter2 (set to 12v) ground to ESP ground

Don't mix up buck converter1 and buck converter2

----------------------------------------------------------------------------------------------------------------
Changes for your setup:

If you are going to replicate this project, you may need to adjust this bit of code to match your setup:
 
  43, 42, 41, 40, 39, 38,   // A–F
  
  37, 36, 23, 24, 25, 26, // G–L
  
  27, 28, 29, 30, 31, 19, // M–R
  
  18, 17, 16, 15, 14, 13, // S–X
  
  12, 11              // Y–Z

I used a 50 count string of lights.  I started at the bottom left of a 36x48 board. I first ran a line along the very bottom edge (from left to right) then came up 12 inches, then ran a string right to left, then up 12 inches, then left to right, then up a 12 inches, then right to left.  This is how I got the number to letter combination above.  Your setup may be / is likely different.  To tailor it for you, set your lights out, then count the individual LEDs starting at 0 (0 is the LED #1 in computer code.  So a 50 string of lights would have 0-49 in code).  Write down what LED should match what letter and update the code bit above.

You can add/change any of the sayings in the program by adding

Also, while it does have a WIFI access point, its a little glitchy.  You'll get a random misfires.  Its either a limitation of my programing knowledge or a limitation of the hardware I used.  Once you access the WIFI, it'll be glitchy until its reset, even if you leave the WIFI.

------------------------------------------------------------------------------------------------------------------
WIFI info:

AP default name: Stranger Wall

AP default password: upsideDown


Good luck!!!

#safety3rd
