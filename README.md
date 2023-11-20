# Wi-Fli-Zero
Adding Integrated Wi-Fi possibilities to the flipper zero.

## Materials

- [WEMOS ESP32-S3 (Lolin)](https://www.wemos.cc/en/latest/s3/s3_mini.html)
- Flipper Zero
- 2 positions switch
- Wires 
- Connectors

## 3D Models

Print the 3D models (or make them printed by your preferred manufacturer).

Test the Flipper Zero fit in your new case before modifying the electronics or adding any element in it !

Then test the switch fitting in the hole made for it (you may need to make the hole bigger, either modify the 3D model or use a Dremel for that).

Also the 3D model used is different than the Flipper's 3 pins so the middle pin won't fit, you may need to modify this part (just open it like on the picture), I will work on a fix later and add it to the repository.

## Mounting instructions

Once your fitting tests are done, you are good to modify your flipper Zero and add integrated Wi-Fi to it.

I used a ESP32-S3 Mini but any ESP that works with the FZero and small enough to fit in it will work.

Identify the 3V, GND, RX and TX pins on your ESP card, then you can solder all of them except the 3V one and keep it for later.

Unmount the Flipper Zero (you can use the following [documentation](https://www.ifixit.com/Teardown/Flipper+Zero+Teardown/151455)) until you got the case and electronic parts separated (step 8):

![[2023-11-20_21-51.png]]

Once done, test the fitting in the new case. If everything goes well, you can proceed to the removal of the NFC/RFID card and battery, then remove the screen protector, NFC antenna (be careful with this !) and infrared cover from the old Fzero case.

Once you have removed the battery, identify the RX, TX, GND and 3V pins and solder them as follows (solder a connector on the 3V):
1. RX
2. TX
3. GND
4. 3V

![[IMG_5054.jpg]]

You can put a piece of kapton tape as I've done but this part is optional here.
Now place your battery temporarily to measure the wires length you'll need to place the ESP32, take the battery off and solder the cables on the card (for the 3V part, don't forget you should solder the other part of the connector !):
1. TX (RX FZ <-> TX card)
2. RX (RX card <-> TX FZ)
3. GND
4. 3V

![[IMG_5055.jpg]]
![[IMG_5056.jpg]]

Once you are good with this step, mount the battery, your flipper will automatically boot, just turn it off.

As our flipper will have a card between the NFC/RFID card and the NFC antenna, we will need to reconnect them using connectors (so the rear part of the FZero will still be removable). To do so, solder connectors on the NFC/RFID card as on the picture below:

![[IMG_5058.jpg]]

Replace it on the FZero main board and reconnect it to the rest of the Fzero electronics.

Solder a connector (the other side of it) to the switch and glue the switch in place (3), then solder connectors on the NFC antenna pads (1 & 2):
![[IMG_5061 1.jpg]]

> This time the kapton tape is important.

Now take the rear case of the Fzero and glue the antenna to it (either with double sided tape or with the original tape if you removed it well).

If you want to flash marauder on your S3 mini, that's your time to do it.

Once all of this is done you are ready to plug all of the connectors together, put you SD card in the FZero and initiate your first test of it !
![[IMG_5062.jpg]]
![[IMG_5067.png]]

おめでとう !!

## Improvements
- Reajusting the pins
- Allowing to flash the ESP firmware from the Fzero
- Improve the 3d model
