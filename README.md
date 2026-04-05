# DICELEDPCB
Using IC's NE555, and CD4017, to create a random rolling generator for a dice (I also added a few designs to be part of the roll)
KiCanvas Demo Link! https://kicanvas.org/?repo=https%3A%2F%2Fgithub.com%2Fdharmasothvaibhav0-dev%2FDICELEDPCB%2Ftree%2Fmain%2FKiCad%2520Source%2520files

<img width="747" height="582" alt="3drender" src="https://github.com/user-attachments/assets/b62fa8f2-d81d-4cc2-8d3b-76b3ff61ee61" />


_______________________________________________________________________________________________________

# The Schematic
<img width="1143" height="557" alt="schematic" src="https://github.com/user-attachments/assets/acbfb2ff-05d9-4e52-ba42-443a6ec37d8f" />
The actual schematic probably took the longest because the design and wiring. I used 2 Capacitors of 1uF and 0.01uF, 14 LEDS, 6 Transistors, 26 resistors which consisted of values of 10k and 220, 1 push button, and 2 IC's: A NE555, and a CD4017.

Essentially what happens in the circuit is, the NE555 in its astable option, send currents to the CD4017 which acts as a clock, and whenever it recieves the current it cycles through each output. When you push the button it cycles through, and when you let go of the button it gives you an output of a number 1-6 OR one of the 2 special designs i put in.

___________________________________________________________________________________________________________________

# PCB Designs

Front :
<img width="671" height="531" alt="PCBFront" src="https://github.com/user-attachments/assets/8451000b-1b5a-4142-bd1d-b8efb9bb7727" />

Back: 
<img width="670" height="528" alt="PCBBack" src="https://github.com/user-attachments/assets/357889dd-5d76-416d-9587-89ec84cad1af" />
