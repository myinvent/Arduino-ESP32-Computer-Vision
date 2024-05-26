# Hands-On Learning Preparation
Prior to hands-on learning to learn how to `control the actuators` and `acquire data from the sensors` on NodeMCU ESP32, we have to make sure the hardware and software (3 things below) is readily accesible on your desk and on your PC:
1. **NodeMCU ESP32** and a **USB cable Type-A to Type-C**.
2. **Arduino IDE**. Download it from it's official website [Arduino Software](https://www.arduino.cc/en/software) page and install it on your PC. Current version is 2.2.3.

<p align="center"><img src="https://github.com/myinvent/hibiscus-sense/raw/main/references/arduino-ide-download.png" width="800"></a></p>

Or you can directly download from here:
* [Windows 10 and newers (64 bits)](https://downloads.arduino.cc/arduino-ide/arduino-ide_2.3.2_Windows_64bit.exe)
* [Linux AppImage (64 bits)](https://downloads.arduino.cc/arduino-ide/arduino-ide_2.3.2_Linux_64bit.AppImage)
* [Linux Zip File (64 bits)](https://downloads.arduino.cc/arduino-ide/arduino-ide_2.3.2_Linux_64bit.zip)
* [Mac OS Intel, 10.15: "Catalina" or newer (64 bits)](https://downloads.arduino.cc/arduino-ide/arduino-ide_2.3.2_macOS_64bit.dmg)
* [Mac OS Apple Silicon, 11: "Big Sur" or newer (64 bits)](https://downloads.arduino.cc/arduino-ide/arduino-ide_2.3.2_macOS_arm64.dmg)

3. **Arduino core for the ESP32** in the Arduino IDE, [Github](https://github.com/espressif/arduino-esp32). If you don't install it yet on your Arduino IDE, follow this [instructions](#install-esp32-arduino-core-using-arduino-ide-boards-manager-7-steps).

Once all required tools are available and accesible, you can [Connect Hibiscus Sense to your PC](#connect-hibiscus-sense-to-your-pc-6-steps).

### Install ESP32 Arduino Core using Arduino IDE Boards Manager (7 Steps)

1. On the Arduino IDE, go to menu: ***File > Preferences***.
2. Click on ***Window icon*** beside the Additional board manager URLs field.

<p align="center"><img src="https://github.com/myinvent/hibiscus-sense/raw/main/references/arduino-ide-menu-preferences-boards.png" width="800"></a></p>

3. Copy the URLs below and paste it into the ***Additional Boards Manager URLs*** field and click the ***OK*** button.
**`https://espressif.github.io/arduino-esp32/package_esp32_index.json`**

<p align="center"><img src="https://github.com/myinvent/hibiscus-sense/raw/main/references/arduino-ide-menu-preferences-board-url.png" width="800"></a></p>

4. Click the ***OK*** button to exit the Preferences window.
5. Open the ***Boards Manager*** on the left panel and search keyword: ***esp32***
6. Look for ***esp32** by Espressif Systems* and click the **INSTALL** button (Current version is 2.0.15).

<p align="center"><img src="https://github.com/myinvent/hibiscus-sense/raw/main/references/arduino-ide-hardware-library-esp32-install.png" width="800"></a></p>

7. Wait until the installation process is done, which would take several minutes, until the status on the board is *`2.0.x installed`*.

<p align="center"><img src="https://github.com/myinvent/hibiscus-sense/raw/main/references/arduino-ide-hardware-library-esp32-installed.png" width="800"></a></p>

Great! The required software are succesfully installed, let's connect Hibiscus Sense to your PC, follow this [instructions](#connect-hibiscus-sense-to-your-pc-6-steps). If your PC not able to detect Hibiscus Sense COM port number, you need to download and install the [CP210x USB to UART Bridge VCP Drivers](#download-usb-driver-in-your-pc)

## Connect Hibiscus Sense to Your PC (6 Steps)
1. Connect the USB cable Type-C to Hibiscus Sense and Type-A to your PC.
2. On the Arduino IDE, choose the correct *COM port* interfaced to CP2104 USB driver on Hibiscus Sense.

`On Windows OS` Example: *COM5*
<p align="center"><img src="https://github.com/myinvent/hibiscus-sense/raw/main/references/arduino-ide-com-port.png" width="800"></a></p>

`On Mac OS` Example: */dev/cu.usbserial-XXXXXXXXX*
<p align="center"><img src="https://github.com/myinvent/hibiscus-sense/raw/main/references/arduino-ide-com-port-mac.png" width="800"></a></p>

3. On the board selection, choose *ESP32 Dev Module*.

`On Windows OS`
<p align="center"><img src="https://github.com/myinvent/hibiscus-sense/raw/main/references/arduino-ide-com-board.png" width="800"></a></p>

`On Mac OS`
<p align="center"><img src="https://github.com/myinvent/hibiscus-sense/raw/main/references/arduino-ide-com-board-mac.png" width="800"></a></p>

Hibiscus Sense, shipped with default sketch to check the sensors and list available Wi-Fi networks at your place. Let's continue to test it!

4. Click the *magnifying glass* icon at the right side of the Arduino IDE to open the *Serial Monitor*.
5. Set the Baud Rate to `115200`.
6. Click the `IO0` button on Hibiscus Sense. You will see the result of the sensor and Wi-Fi checking on the Serial Monitor.

<p align="center"><img src="https://github.com/myinvent/hibiscus-sense/raw/main/references/hibiscus-first-time-monitor.png" width="800"></a></p>

If you did not see any result on the Serial Monitor or having challenges to connect the board to your PC, please contact Mr. Ariffin via [WhatsApp](https://api.whatsapp.com/send?phone=60177875232&text=Hi%20Mr.%20Ariffin,%20please%20help.%20My%20Hibiscus%20Sense,%20seems%20not%20working%20for%20the%20first%20time.), he can assist you.

## Download USB Driver in Your PC

[CP210x Universal Windows Driver](https://www.silabs.com/documents/public/software/CP210x_Universal_Windows_Driver.zip)

Installation instruction by Darren Robinson, [ESP32 Com Port – CP2102 USB to UART Bridge Controller](https://blog.darrenjrobinson.com/esp32-com-port-cp2102-usb-to-uart-bridge-controller/)

<p align="right"><a href="https://forms.gle/UgpDSFc46K4MkvTM8">&#128640; Tutorial Improvement & Suggestions</a></p>