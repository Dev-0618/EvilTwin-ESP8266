**ESP-EVTwin**

_**FEATURES:**_
Deauthenticate a target WiFi access point
Create Evil-Twin AP to capture passwords with verification against the original access point
Perform both attacks simultaneously
DISCLAIMER: For educational use only. Check local regulations before use.


_**Installation Steps:**_
Install Arduino IDE.

once done go to https://esp.huhn.me/ > Connect > (Choose nodemcu board port) then choose the bin file given > upload/flash 
ALL set...

Add Board URL: Go to File -> Preferences and add https://raw.githubusercontent.com/SpacehuhnTech/arduino/main/package_spacehuhn_index.json to Additional Boards Manager URLs.

Install Deauther Package: Go to Tools -> Board -> Boards Manager, search for and install the deauther package.

Download ESP-EVTwin: Open ESP-EVTwin in Arduino IDE.

Select Board: Go to Tools -> Board and choose an ESP8266 Deauther board.

Connect and Upload: Connect your device, select the serial port (Tools -> Port), and click Upload.

_**Usage:**_

Connect to AP: Connect to **127.4.7.8** with password **deauther** from your phone/PC.

Select Target AP: Refresh the list of available APs (every 30 seconds, page reload required).

Start Attacks: Click Start Deauthing to kick devices off the network and Start Evil-Twin to create the fake AP.

Stop Attacks: Visit 192.168.4.1/admin (connected to Evil-Twin AP) or reset the ESP8266.

View Results: Once a password is captured, the AP will reset to default **127.4.7.8** / **deauther**, and the password will be displayed at the bottom of the table.


**Credits:**
https://github.com/SpacehuhnTech/esp8266_deauther
