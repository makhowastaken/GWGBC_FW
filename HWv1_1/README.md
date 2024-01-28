# Hardware Version 1.1

THIS SECTION OF THE REPO IS ONLY FOR V1.1 HARDWARE. If you have have V1.0 or any prototype devices, this firmware will NOT work on your device. No warranty, flash at your own risk, etc. etc. The firmware for the circuit that deals with updates is separate from the firmware for the rest of the device so a failed update is as easy to recover from as just attempting to update again. That being said, the firmware updates can be extremely tempermental. Sometimes it just works, sometimes it doesn't work no matter what and it just starts working again later. You have been warned.

My video on the v1.0 hardware which should have all the same features and functionality:

[![Funnyplaying GWGBC -- FPGA BASED GAME BOY COLOR](https://img.youtube.com/vi/T4LSHpKfPGs/0.jpg)](https://www.youtube.com/watch?v=T4LSHpKfPGs)

New on v1.1 (compared to v1.0)
* More accurate clock speed
* Faster charging (500mA -> 1A)
* Updateable on macOS
 

## Updating

So you've decided to tinker despite the numerous warnings. I certainly don't blame you but keep in mind that I am NOT funnyplaying nor am I on their payroll. We just have a good working relationship via mutual partners. If you run into technical issues updating, no support will be provided by me. You have been warned. Again. 

Instructions on this process in video linked above; skip to the one hour mark.

To update: 
* On your favorite PC (macOS tested and verified on v1.1, Linux and co. presumed working), download the firmware "update.bin" file for the firmware you wish to flash.
* File must be named "update.bin". You cannot rename after copying. 
* Switch FPGA GBC on with no game inserted
* Plug console into PC via USB Type C data cable (USB 2.0 is fine but USB 3.0 or USB Type C host type cables should also work)
* Copy "update.bin" file over to 1MB "FUNNY_PLAY_" file system
* Device will automatically update and reboot
* Device may now be disconnected or switched off (or just played, I don't judge) once file copy completed

# Version Notes: *work in progress*

These firmware files have been provided to me via Funnyplaying directly and published with their permission. I have not coded, compiled, or had any involvement on the technical side here. My only direct involvement was an unpaid* QA role. They provided me the device and firmware files, I provide(d) them actionable feedback on the device. If you have feature requests or bug reports, I recommend you contact funnyplaying directly.

> Quotes

are from funnyplaying directly, 

* bullet points are me paraphrasing.

### Unknown Build
* Version 0.9 in the menu
* Initial firmware on v1.1 hardware revisions
* Unknown changes

### [2024.1](2024.1)
* Version 1.02 in the menu
* Unknown changes over v0.9

### [2024.1.8](2024.1.8)
* Version 1.02 in the menu (same as above)
> 1. Modifying the startup logo
> 2. Partially removed GB mode color palette
> 3. Stability optimization

### [22024.1.25](2024.1.25)
* Version 1.04 in the menu
> 1. Reoptimized OSD architecture
> 2. Added support for EverDrive GB Model 17, Rev E's support
> 3. Optimized the layout of the startup logo

