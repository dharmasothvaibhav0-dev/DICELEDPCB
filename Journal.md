
## Dice LED IC project:

## 3/32/2026
I've done some research online on different project ideas online to try and find something that can peak my interest, and I've decided to do a Dice Design to where, when you push a button LEDS will start rolling(Flashing), and once you release it will give you a side of the die you've rolled. 

During the initial stages of research, I noticed that I can use the IC NE555 in order to actually generate the roll, and after further research looking online I also found that I can use the IC CD4017 to cycle through the numbers during the roll to actually create an end result.

I want to 7 LEDS on the circuit to showcase an actual dice. Something like these

<img width="1633" height="980" alt="image" src="https://github.com/user-attachments/assets/87c3e9a6-c533-4f7e-a913-5be04894616d" />



## 3/32/2026
I first took time to research both the NE555 and the CDE4017 to figure out how they work, where are the input pins/output pins, etc. (around 15 minutes total research for the pins)

Once done researching how the two work, following the datasheet for the NE555, I created a schematic of the Astable configuration and added a push button to the end of the output pin because the astable circuit should only run while the button is being pushed. I also added an LED before in order to ensure that the current is flowing through correctly. Once the next IC is created, I have to connect it to pin 14 (The clock pin), because the clock will determine the output. It recieves the signal from the astable ne555, and will cycle through  1 2 3 4 5 6
<img width="525" height="409" alt="image" src="https://github.com/user-attachments/assets/f74488db-0181-444f-8b9f-50919e75e3dd" />



Next I must connect the ne555 to the CD4017 IC, so that 4017 is able to run through all the possible outcomes on a die, such as 1 2 3 4 5 6.

Looking at the reference image above for a die, and looking at example projects like this, it was clear in order to make the outcomes proper, we would have to separate the dots into groups
<img width="423" height="375" alt="image" src="https://github.com/user-attachments/assets/84192c5c-d395-4ea3-abfd-2b3af7b796ad" />

So for example if the outcome is 1 or 2, the LED linked to 1 or 2, would light up. And then if the outcome was 3, we would have to make it so that the LEDS with 3 AND 1, would all simultaneously light up. That's the main focus for the CD4017.

<img width="873" height="448" alt="image" src="https://github.com/user-attachments/assets/d7c77be0-7fbf-410c-9ebc-daf0bb590120" />


This is the finished CD4017 circuit. How it works is basically when the electrical signal gets sent to the clock from the astable timer, it iterations through each LED meaning that when the first current flows it lights up the first function, the next current lights up the second function, etc etc. One of the important things to note here from this is connecting the 5th pin to the reset pin on the CD4017, what this means is that whenever the clock reaches the 6th function,  it resets the clock making it restart at the first function. 

### Time taken: 90 mins

## 4/4/2026 
After taking a couple days to think about how I could make this better/more unique itself,  I came to the conclusion of adding a couple more designs + more LEDS!! 

<img width="749" height="484" alt="image" src="https://github.com/user-attachments/assets/734b3b05-13fa-498a-995c-ae1051e6c845" />

I lowkey changed my mind about all the LEDS attached to G, because its just too many but, now all we have to do is add the LEDS attached to E, and F, and change the reset pin to pin 7, that way as as the 7th function ends the clock will reset back to the first function.

It didn't take long to add the new functions LEDS into the schematic, and because it was just adding on, I just had to wire it correctly.

This is the final schematic for the CD4017 clock
<img width="864" height="577" alt="image" src="https://github.com/user-attachments/assets/a17b77a0-bbe8-4ad9-97f0-4e602e5ffadc" />


It may look pretty confusing, but if you create a diagram with laying out which functions you need to connect it becomes pretty easy.
<img width="1113" height="603" alt="image" src="https://github.com/user-attachments/assets/6f81c498-903b-4331-8873-4d51223cf2d1" />

This is the total final schematic for the circuit.

Now that the actual schematic is done, its time to add the footprints. This was relatively simple as it was just copying and pasting from footprint names. After adding all the footprints I updated my PCB with my schematic, and am organizing it to make wiring easier

While I was wiring I was trying my hardest to figure out how I could wire it all on one layer, but after an hour and a half of trial and error I realized it wasn't possible at all, so I had to resort wiring some parts of the PCB on the back layer.
<img width="815" height="585" alt="image" src="https://github.com/user-attachments/assets/0bf16c2d-7ef8-4037-af34-5233995db529" />

This is what the final PCB looks like 

3d Render of front: 
<img width="841" height="592" alt="image" src="https://github.com/user-attachments/assets/2c2c44a9-38c1-473f-a8db-0e58751c33f9" />

3d Render of back: 
<img width="783" height="582" alt="image" src="https://github.com/user-attachments/assets/daf4ba49-813c-4f9a-89c8-4b12610f392a" />

## Time taken adding to Schematic + PCB + wiring: 3 hours
## Time taken Journaling : 45 minutes combined both days
## Total Time Taken both days: 5.25 hours
