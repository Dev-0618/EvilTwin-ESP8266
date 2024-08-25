# ESP-EVTwin
100% Working ESP8266 EVIL TWIN ATTACK
ESP-EVTwin is an educational project that allows you to deauthenticate a target WiFi access point and create an Evil-Twin AP to capture passwords with verification against the original access point. You can perform both attacks simultaneously. This tool is designed for educational purposes only; please ensure that you comply with local regulations before using it.

## Features

- **Deauthenticate a Target WiFi Access Point**: Disconnect devices from the network.
- **Create Evil-Twin AP**: Set up a fake AP to capture passwords.
- **Simultaneous Attacks**: Run both deauthentication and Evil-Twin AP attacks at the same time.

## Installation

### Prerequisites

- Install the [Arduino IDE](https://www.arduino.cc/en/software).

### Steps

1. Go to [ESP Huhn](https://esp.huhn.me/) and connect your NodeMCU board by selecting the appropriate port.
2. Choose the provided `.bin` file and upload/flash it to your board.

### Adding the Board URL

1. Open Arduino IDE and navigate to `File` -> `Preferences`.
2. Add the following URL to the "Additional Boards Manager URLs":  
   ```
   https://raw.githubusercontent.com/SpacehuhnTech/arduino/main/package_spacehuhn_index.json
   ```

### Installing the Deauther Package

1. Go to `Tools` -> `Board` -> `Boards Manager`.
2. Search for `deauther` and install the package.

### Downloading ESP-EVTwin

1. Open ESP-EVTwin in Arduino IDE.
2. Go to `Tools` -> `Board` and select `ESP8266 Deauther` as your board.

### Uploading the Code

1. Connect your device to your computer.
2. Select the correct serial port (`Tools` -> `Port`).
3. Click `Upload` to flash the code to your device.

## Usage

1. **Connect to AP**: On your phone or PC, connect to the AP at `127.4.7.8` using the password `deauther`.
2. **Select Target AP**: Refresh the list of available APs (the list refreshes every 30 seconds, so you'll need to reload the page).
3. **Start Attacks**: 
   - Click `Start Deauthing` to kick devices off the network.
   - Click `Start Evil-Twin` to create the fake AP.
4. **Stop Attacks**: 
   - Visit `192.168.4.1/admin` (while connected to the Evil-Twin AP).
   - Alternatively, reset the ESP8266 to stop all attacks.
5. **View Results**: 
   - After a password is captured, the AP will reset to its default settings (`127.4.7.8` / `deauther`).
   - The captured password will be displayed at the bottom of the table.

## Disclaimer

This project is for educational purposes only. Misuse of this tool may violate local laws and regulations. The developers are not responsible for any misuse or damage caused by this tool.

## Credits

- Original code and project by [SpacehuhnTech](https://github.com/SpacehuhnTech/esp8266_deauther).
