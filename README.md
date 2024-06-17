There are two stages to programming your arduino to initiate the spells:

1. Wiring the Digital Output pins accordingly
2. Training the speech module on your voice

The code has it set up where
D7 - Incendio
D8 - Avada Kedavra
D10 - Lumos

After the training and loading is complete, these pins will activate to your voice.

BEGIN:
1. To begin, you must plug the TX, RX, VDD, and GND into the pins D2, D3, 5v, and GND respectively. (may have D2 and D3 flipped)
2. Plug in the arduino to a computer, open the "Wand_working..." file and upload up the arduino code. (You may need to adjust your port/bootloader settings to upload)
3. In the serial monitor, you'll see a menu for training the Speech recognizer (make sure mic is plugged in). Training goes as follows...
3a. type "train #" (replacing the "#" symbol with 1-8) into the serial monitor
3b. follow the prompts, you'll repeat the spell twice
3c. Once it's successful, type "load #" using the same number as before
3d. repeat for all the other spells!

Training numbers (1-8):
1 - Incendio
2 - Lumos
3 - Nox
4 - Avada Kedavra
5 - Incendio (extra)
6 - Lumos (extra)
7 - Nox (extra)
8 - Avada Kedavra (extra)

4. Then you're done! Following the DEBUGGING section for testing


DEBUGGING:
Once everything is trained and loaded, I recommend power cycling, then testing. 

First, apply power to arduino (with speech module connected), open up the serial monitor (your trained spells will automatically be loaded).
Try saying the spell into the mic! If it succeeds, then you'll see the spells name appear in the serial monitor and your digital output pin will go to a HIGH state. 
I recommend probing directly to ensure it is working properly.
The voila! use for any projects you desire.


NOTE:
Lumos turns on D10 and it will stay on until NOX is said.
Incendio activates for 3 seconds
Avada Kedavra activates for 0.5 seconds.
