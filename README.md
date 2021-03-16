# Mystery Box
This installation uses the ESP32 in Soft Access Point mode, allowing viewers to connect to the box using their smartphones. Viewers can then scan the QR code on the box, which takes them to a webpage which delivers messages inspired by Twitter accounts such as @MagicRealismBot and @conceptsbot. A ‘try again’ button allows the user to receive additional messages. Each message also comes with a different background color. While the tone of this color is random, the brightness of the background color is determined by the light levels in the room. This is achieved using a photoresistor connected to the ESP32.

### Materials
- ESP32
- Breadboard
- Photoresistor
- 10kΩ resistor
- Connecting wires
- 9V battery
- Printer/paper

### Setup
Connect one end of the photoresistor to GPIO pin 33 and to -3.3V using the 10kΩ resistor. Connect the other end to ground.

To make modifications to the webpage, edit the sc.html file included in this repository, and minify and convert to C-string both halves of the file (the split is located on line 322). Then, replace String html1 and String html2 in accesspoint.ino with these two new strings. If you don't want to make any changes, then sc.html is not needed.

Upload accesspoint.ino to the ESP32. Attach a 9V battery to the ESP32, and place it inside a box. Print the network ssid, password, and QR code that links to the IP address of the ESP32 onto a piece of paper and attach this to the box.

Power on the ESP32, and the installation is ready to be used.

View the installation in action [here](https://youtu.be/qYD5cYmW8cE).
