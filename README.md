# RTL8720dn-Deauther With Advanced Capabilities
![GitHub Issues or Pull Requests](https://img.shields.io/github/issues/lizardman343242/RTL8720dn-Deauther-Advanced-Capabilities)
![GitHub License](https://img.shields.io/github/license/lizardman343242/RTL8720dn-Deauther-Advanced-Capabilities)
![GitHub Repo stars](https://img.shields.io/github/stars/lizardman343242/RTL8720dn-Deauther-Advanced-Capabilities?style=flat)
![GitHub forks](https://img.shields.io/github/forks/lizardman343242/RTL8720dn-Deauther-Advanced-Capabilities?style=flat)
![logo](https://github.com/user-attachments/assets/ab8ebf84-eee2-4298-8975-2e8dad13c1b3)

My ESP32-Deauther ported to the RTL8720dn, allowing users to deauthenticate on 5Ghz now!
# DISCLAIMER
This tool has been made for educational and testing purposes only. Any misuse or illegal activities conducted with the tool are strictly prohibited. I am **not** responsible for any consequences arising from the use of the tool, which is done at your own risk.
## Building
Building is done using the ArduinoIDE. Make sure you have added the board manager URL for Realtek MCUs and installed them in the board manager.
1) Clone this repo using `git clone https://github.com/lizardman343242/RTL8720dn-Deauther-Advanced-Capabilities.git`
2) Open the cloned folder in the Arduino IDE
3) Connect your board and hit upload
### Notes
Most RTL8720dn devboards have the upload and log serial ports isolated. Make sure to bridge **LOG_UART_TX** and **LP_UART_TX**, as well as **LOG_UART_RX** and **LP_UART_RX** during uploading.
## Using RTL8720dn-Deauther
The RTL8720dn hosts a WiFi network with the name of `RTL8720dn-Deauther` and a password of `0123456789`. Connect to this network and type the IP of your RTL8720dn (typically **192.168.1.1**) into a webbrowser of a choice.
### Rescan networks
Rescan and detect all WiFi networks in your area. After a successful scan, the networks are listed in the above table.
### Launch Deauth-Attack
Deauthenticates all clients connected to one or multiple networks. Select the networks you want to deauth in the table above and click **Start Attack!**.
### Stopping a Deauth-Attack
To stop an ongoing attack, hit the **Stop** button.
### Launch Becon-Attack
Sends out fake wifi networks to all devices in range, decide and customise the amount and names of these fake wifi networks.
### Leds
The RTL8720dn-Deauther utilizes the RGB led that most devboards have. This is what the different colors indicate:
* Red: The system state. Lights up when the system is usable.
* Green: Lights up when a HTTP communication between a device and the Deauther is happening.
* Blue: Flashes when a deauth frame is being sent.
## License
All files within this repo are released under the GNU GPL V3 License as per the LICENSE file stored in the root of this repo.
## Intentions
this fork of the orginal is intended to increase the capabilites of the RTL8720dn by implementing becon, probe and phising attacks along side this i am mainly going to base it off another project made for a diffrent chip the esp8266 [spacehuns deauther](https://github.com/SpacehuhnTech/esp8266_deauther) project had some shortcomings with not being able to deauth on 5ghz because of the hardware capabilites of the esp8266
