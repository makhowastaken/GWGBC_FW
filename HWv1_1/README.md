# GWGBC_FW

THIS SECTION OF THE REPO IS ONLY FOR V1.1 HARDWARE. If you have have V1.0 or newer, this firmware will NOT work on your device. No warranty, flash at your own risk, etc. etc. The firmware for the circuit that deals with updates is separate from the firmware for the rest of the device so a failed update is as easy to recover from as just attempting to update again. That being said, the firmware updates can be extremely tempermental. Sometimes it just works, sometimes it doesn't work no matter what and it just starts working again later. You have been warned.

These devices started shipping with v0.9 but I only have v1.02. Do NOT update your device if you think you may wish to roll back to v0.9 because until FP distributes the FW, this is not possible. 

My video on the v1.0 hardware which should have all the same features and functionality:

[![Funnyplaying GWGBC -- FPGA BASED GAME BOY COLOR](https://img.youtube.com/vi/T4LSHpKfPGs/0.jpg)](https://www.youtube.com/watch?v=T4LSHpKfPGs)

 

## Updating

So you've decided to tinker despite the numerous warnings. I certainly don't blame you but keep in mind that I am NOT funnyplaying nor am I on their payroll. We just have a good working relationship via mutual partners. If you run into technical issues updating, no support will be provided. You have been warned. Again. 

Instructions on this process in video linked above; skip to the one hour mark.

To update: 
* On your favorite Windows PC (10/11 tested and verified, older versions should work too), download the firmware "update.bin" file for the firmware you wish to flash.
* File must be named "update.bin". You cannot rename after copying. 
* Switch FPGA GBC on with no game inserted
* Plug console into PC via USB C data cable (USB 2.0 is fine but USB 3.0 or USB C host type cables should also work)
* Copy "update.bin" file over to 1MB "FUNNY_PLAY_" file system
* Device will automatically update and reboot
* Device may now be disconnected or switched off (or just played, I don't judge) once file copy completed

Note that sometimes file copy may fail or get stuck at around 27% and device may only be partially updated. If this happens, unplug device, power cycle, and repeat steps. If this happens repeatedly, you may attempt to copy via powershell. If it's still failing, restart your PC and try again or try a different PC.

  Powershell example: `Copy-Item .\update.bin -Destination e:`
  
  Copy-Item *<path to "update.bin" file>* -Destination *<drive letter of "FUNNY_PLAY_">*

# Version Notes: *work in progress*

These firmware files have been provided to me via Funnyplaying directly and published with their permission. I have not coded, compiled, or had any involvement on the technical side here. My only direct involvement was an unpaid* QA role. They provided me the device and firmware files, I provide(d) them actionable feedback on the device. If you have feature requests or bug reports, I recommend you contact funnyplaying directly.

> Quotes

are from funnyplaying directly, 

* bullet points are me paraphrasing.

I don't have proper change logs for these updates. I only have context clues from funnyplaying directly and they communicate via a translator so sometimes context is lost. Internal build numbers just look to be based on the compilation date so build `0725` is an unknown version but it was compiled from the main branch `July 25th (of 2023)`. Sometimes there are two firmware updates the same day and FP will tack on a `.1` or `01` interchangeably. 

### Unknown Build
* Version 0.9 in the menu
* Initial firmware on v1.1 hardware revisions
* Unknown changes

### [2024.1](2024.1)
* Version 1.02 in the menu
* Updated boot screens now use Funnyplaying logos instead of Nintendo logos
> Optimised left and right channels
* Fixed Tetris multiplayer link
* Latest test version.
