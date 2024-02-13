# Hardware Version 1.0

> [!CAUTION]
> THIS SECTION OF THE REPOSITORY IS ONLY FOR V1.0 HARDWARE. If you have have V1.1 or newer, this firmware will NOT work on your device. 

[![Funnyplaying GWGBC -- FPGA BASED GAME BOY COLOR](https://img.youtube.com/vi/T4LSHpKfPGs/0.jpg)](https://www.youtube.com/watch?v=T4LSHpKfPGs)

A Windows PC ([or Windows 10 Phone](https://twitter.com/makhowastaken/status/1727496794333237599)) is REQUIRED for Firmware updates. Ubuntu, macOS[^1], Android (Samsung), and iOS (iPadOS) all tested failed out of the box. There is, however, [experimental macOS support.](https://twitter.com/ShinyQuagsire/status/1749978350246941057)

## Updating

Instructions on this process in video linked above; skip to the one hour mark.

To update: 
* On your favorite Windows PC (10/11 tested and verified), download the firmware "update.bin" file for the firmware you wish to flash.
* File must be named "update.bin". You cannot rename after copying. 
* Switch FPGA GBC on with no game inserted (for safety -- a game won't interfere with the update process but the update could wipe your save) 
* Plug console into PC via USB C data cable (USB 2.0 is fine but USB 3.0 or USB C host type cables should also work)
* Copy "update.bin" file over to 1MB "FUNNY_PLAY_" file system
* Device will automatically update and reboot
* Device may now be disconnected or switched off (or just played, I don't judge) once file copy completed

Note that sometimes file copy may fail or get stuck at around 27% and device may only be partially updated. If this happens, unplug device, power cycle, and repeat steps. If this happens repeatedly, you may attempt to copy via powershell. If it's still failing, restart your PC and try again or try a different PC.

  Powershell example: `Copy-Item .\update.bin -Destination e:`
  
  Copy-Item *<path to "update.bin" file>* -Destination *<drive letter of "FUNNY_PLAY_">*

Occasionally, the saved display profile is corrupt and the console will display a garbled screen image on boot after updating to a different firmware version. 

To fix this, you need to blindly modify the settings. Try the following keypresses to save defaults and reset the console -- display should be usable from there. This is known to occur for users updating from 0.90 to 1.02 on v1.1 hardware and from 0928 or earlier builds to 1005 and later builds on v1.0 hardware. 

| [<img src="../media/purple_screen.jpg" width="350" />](../media/purple_screen.jpg) | Reset Corrupt OSD settings<br><br><ol><li>Open OSD</li><li>Press down on dpad 9 times</li><li>Press A</li><li>Press up on dpad 1 time</li><li>Press A</li></ol><br><br>[(credit: HDR)](https://twitter.com/MartinRefseth) |
| :---: | :--- |

# Version Notes: *work in progress*

These firmware files have been provided to me via Funnyplaying directly and published with their permission. I have not coded, compiled, or had any involvement on the technical side here. 

> Quotes

are from funnyplaying directly, 

* bullet points are me paraphrasing.

I don't have proper change logs for these updates. I only have context clues from funnyplaying directly and they communicate via a translator so sometimes context is lost. Internal build numbers just look to be based on the compilation date so build `0725` is an unknown version but it was compiled from the main branch `July 25th (of 2023)`. Sometimes there are two firmware updates the same day and FP will tack on a `.1` or `01` interchangeably. 

### [0725](0725)
* No internal version number -- Fixes audio pop on start and adds stereo support to speaker
* Not first firmware version but first firmware version that can be flashed without a dedicated FPGA programmer. Earlier versions not provided (and not yet dumped)

### [0823](0823)
* No internal version number -- Fixes GB Camera and Pokemon Crystal (US) compatibility and other SRAM/FRAM cart compatibility (insideGadgets and HDR carts)
* Adds GBC palette mode display option. Toggle this option if sprites do not render properly in games under the GBC core (e.g. GB game running under GBC core may require a different option than just using the GB core)
* "Engineering test build" -- menu open on every boot (may simply be closed)

### [082301](082301)
* Unknown changes, no notes, not tested

### [0928](0928)
> This version is unstable Other new problems have emerged

> The timing is already saturated  ，Further details need to be optimized

> It's better not to update yet  Waiting for my new version

* Unknown changes, not tested

### [1005](1005)
* No internal version number -- added variable clock rate control
* Version 0.86? I think my notes are wrong
* Looks to be missing a screen display mode, full + pixel grid

IMPORTANT -- When updating to this build or newer from an older build, it is possible to glitch your display mode. Full Screen + Pixel Grid mode was REMOVED but the configuration does NOT reset upon reflashing. Recommend change display mode before updating. If your display mode gets glitched, roll your firmware back to an earlier version, change display modes, then try again. 

### [1010](1010)
* Version 0.87 in the menu -- lowered speaker minimum volume 
* Fixed unknown (to me) audio issues in some games. I didn't press for specifics. 
* If you want factory firmware, this is it. 

### [1015](1015)
* Unknown changes, no notes, not tested

### [10.25](10.25)
* Version 0.88 in the menu
* Unknown changes, not tested
* Latest stable version
* **This is the version FP recommends.** 

### [10.25.1](10.25.1)
* Unknown changes, not tested
> There's a big problem

### [1117](1117)
* Version 0.89 in the menu
* Fixed backlight management and controls
* Experimental sleep mode -- press and hold menu button to sleep or wake device
* **This is the version I recommend.** 

### Unknown Build
* Version 0.9 in the menu
* Initial firmware on v1.1 hardware revisions
* Unknown changes

### [2024.1.old](2024.1.old)
* Version 1.02 in the menu
* Updated boot screens now use Funnyplaying logos instead of Nintendo logos
> Optimised left and right channels
* Fixed Tetris multiplayer link
* Graphical corruption on first boot[^2]
* Latest test version.


---

[^1]: Shiny Quagsire has posted a script to their github that can do updates from macOS however I have not personally tested nor proofread the script. It's probably fine but you should be cautious about running ANY script or command as root if you do not know explicitely what it does. You may find the script here: [https://gist.github.com/shinyquagsire23/b6322687a153114e5a0a46e4ff91e8c0](https://gist.github.com/shinyquagsire23/b6322687a153114e5a0a46e4ff91e8c0)

[^2]: After updating to the test version 1.02, my console experienced bootlooping and severe graphical corruption for the first several boots. After about five power cycles, the problem hasn't reocurred. I was able to reproduce this exact behavior on a second unit by going from the most recent firmware to this version. See HDR's fix above. 
