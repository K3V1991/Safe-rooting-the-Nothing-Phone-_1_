<p align="center"><img src="https://github.com/K3V1991/Safe-rooting-the-Nothing-Phone-_1_/blob/main/Safe-Rooting.png" width="200"></a>
<h1 align="center"><b>Safe rooting the Nothing Phone (1)</b></h1>
<br />

<p align="center">
<a href="https://ko-fi.com/k3v1991" alt="Ko-fi"><img src="https://img.shields.io/badge/Ko--fi-F16061?style=for-the-badge&logo=ko-fi&logoColor=white"> &emsp;
<a href="https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=HW8B98TVDLKWA" alt="PayPal"><img src="https://img.shields.io/badge/PayPal-00457C?style=for-the-badge&logo=paypal&logoColor=white"> &emsp;
<a href="https://github.com/K3V1991/Donate-Crypto/blob/main/README.md" alt="Crypto"><img src="https://img.shields.io/badge/Bitcoin-000?style=for-the-badge&logo=bitcoin&logoColor=white">
</p>
<hr />
<br />

## Requirements:
* Firmware File (Full)
* A PC
* A USB Cable
* USB Driver for your Device, [Google Driver](https://developer.android.com/studio/run/win-usb) or [Universal ADB Driver](https://adb.clockworkmod.com)
* payload-dumper-go - [GitHub](https://github.com/ssut/payload-dumper-go)
* Platform Tools - [Android Developers](https://developer.android.com/studio/releases/platform-tools) or ADB & Fastboot++ - [GitHub](https://github.com/K3V1991/ADB-and-FastbootPlusPlus)
* Magisk - [GitHub](https://github.com/topjohnwu/Magisk)
<br />

## Note:
You can skip to Step 10 if you installed Magisk Manager & download my pre-patched Boot Image under [Release Tab](https://github.com/K3V1991/Safe-rooting-the-Nothing-Phone-_1_/releases)
<br />
<br />

## How-To:
1. Download a Firmware Zip
2. Extract the download Firmware Zip
3. Move the "payload.bin" inside the payload-dumper-go Directory, and run it by double clicking on the payload-dumper-go.exe
4. Move the extracted "boot.img" to the Phone
5. Download and install "Magisk Manager"
6. Tap on the Install Button, choose "Select and Patch a File"
7. A File Manager will pop up. Select the Boot Image that you pushed earlier and let Magisk patch it
9. Extract the downloaded Platform Tools Zip & open a Coammand Prompt
9. Pull the patched Image with this Command: adb pull /sdcard/Download/magisk_patched_[random_strings].img (Change [random_strings] with the real Name of your File) <br />
10. Type: adb reboot bootloader (Phone reboots to Bootloader) <br />
11. Type: fastboot devices (Lists Devices in Fastboot) <br />
12. Type: fastboot boot /path/to/magisk_patched_[random_strings].img (Change [random_strings] with the real Name of your File) <br />
13. Type: fastboot reboot (Boots Phone to System) <br />
14. Open "Magisk Manager" click on "Install" > Direct Install (Recommended) > after Installation, Reboot
15. After restart open "Magisk Manger" to verify Root
16. Done.
<br />
<br />

## Enable Developer Options & USB Debugging:
<details>
  <summary>Click to expand</summary>
  
1. Install the USB Driver for your Device or Universal Adb Driver
2. On your Device, go to Settings > About. Find the Build Number and tap on it 7 times to enable Developer Options
3. Now enter System > Developer Options and find "USB debugging" and enable it
4. Plug your Device into the Computer and change it from "Charge only" to "File Transfer" Mode
5. On your Computer, browse to the Directory where you extracted the Portable Version or use Tiny ADB & Fastboot++ Shortcut
6. Launch a Command Prompt with Open CMD.bat or use Tiny ADB & Fastboot++ Shortcut
7. Once you’re in the Command Prompt, enter the following Command:
```
adb devices
```
8. System is starting the ADB Daemon (If this is your first Time running ADB, you will see a Prompt on your Phone asking you to authorize a Connection with the Computer. Click OK.)
9. Succesful enabled USB Debugging
</details>

## Unable to connect to ADB:
<details>
  <summary>Click to expand</summary>
  
1. AMD Bug - [XDA Thread](https://forum.xda-developers.com/t/fix-fastboot-issues-on-ryzen-based-pcs.4186321/)
2. Switch Device from "Charging" to "File Transfer" Mode
3. Install the latest Device Driver or Universal USB Driver
4. Try another USB Cable
5. Use another USB Port (USB 3.0 Port to USB 2.0)
6. Try to execute Fastboot Command without connecting your Device, and once it says "waiting for device" plug in your USB Cable
7. Windows: Click "Change advanced power setting" on your chosen Plan and expand "USB Settings". Under "USB Settings" Section, expand "USB selective suspend setting" and change it to "Disabled" for On Battery and Plugged In
8. Try another PC
</details>
