# DICELEDPCB
Using IC's NE555, and CD4017, to create a random rolling generator for a dice (I also added a few designs to be part of the roll)
KiCanvas Demo Link! https://kicanvas.org/?repo=https%3A%2F%2Fgithub.com%2Fdharmasothvaibhav0-dev%2FDICELEDPCB%2Ftree%2Fmain%2FKiCad%2520Source%2520files

<img width="829" height="536" alt="image" src="https://github.com/user-attachments/assets/cbf36b83-01e0-4c9b-ab22-62b763bb81d3" />



_______________________________________________________________________________________________________

# The Schematic
<img width="1423" height="787" alt="image" src="https://github.com/user-attachments/assets/ebece15e-94bc-40ae-9a5e-f2adafdb9518" />

The actual schematic probably took the longest because the design and wiring. I used 2 Capacitors of 1uF and 0.01uF, 14 LEDS, 6 Transistors, 26 resistors which consisted of values of 10k and 220, 1 push button, and 2 IC's: A NE555, and a CD4017.

Essentially what happens in the circuit is, the NE555 in its astable option, send currents to the CD4017 which acts as a clock, and whenever it recieves the current it cycles through each output. When you push the button it cycles through, and when you let go of the button it gives you an output of a number 1-6 OR one of the 2 special designs i put in.

___________________________________________________________________________________________________________________

# PCB Designs

Front :
<img width="956" height="592" alt="image" src="https://github.com/user-attachments/assets/702dcf89-6a81-45af-9310-acc6ff714f6c" />

Back: 
<img width="878" height="584" alt="image" src="https://github.com/user-attachments/assets/a4d628dc-1010-401b-927c-812c88110dd8" />

