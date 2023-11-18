# GWGBC_FW
Historical firmware repository for the Funnyplaying FPGA GBC. No warranty, flash at your own risk, etc. etc. 

To update: 
* Switch FPGA GBC on (with no game inserted)
* Plug console into PC via USB C data cable (USB 2.0)
* Copy "update.bin" file over to 1MB "FUNNY_PLAY_" file system
* Device will automatically update and reboot
* Device may disconnected or switched off (or just played, I don't judge) once file copy completed


Note that sometimes file copy may fail or get stuck at around 27% and device may only be partially updated. If this happens, unplug device, power cycle, and repeat steps. If this happens repeatedly, you may attempt to copy via BASH or powershell.

  File MUST be named "update.bin" or update WILL fail. 

  Powershell example: `Copy-Item .\update.bin -Destination e:`
  
  Copy-Item <path to "update.bin" file> -Destination <drive letter of "FUNNY_PLAY_">

Per Funnyplaying:
  > Suggested upgrade  0.88  10.25

  > 10.25.1 There's a big problem

Version Notes: *work in progress*

Quotes are from funnyplaying directly, bullet points are me paraphrasing. 

# 0725
* No internal version number -- Fixes audio pop on start and adds stereo support to speaker
* Not first firmware version but first firmware version that can be flashed without a dedicated FPGA programmer. 

# 0823
* No internal version number -- Fixes GB Camera and Pokemon Crystal (US) compatibility and other SRAM/FRAM cart compatibility
* Engineering test build -- menu open on every boot (may simply be closed)

# 082301
* Unknown changes, no notes

# 0928
> This version is unstable Other new problems have emerged

> The timing is already saturated  ，Further details need to be optimized

> It's better not to update yet  Waiting for my new version

# 1005
* No internal version number -- added variable clock control
* Version 0.86? I think my notes are wrong
* Looks to be missing a screen display mode, full + pixel grid

IMPORTANT -- When updating to this build or newer from an older build, it is possible to glitch your display mode. Full Screen + Pixel Grid mode was REMOVED but the configuration does NOT reset upon reflashing. Recommend change display mode before updating. If your display mode gets glitched, roll your firmware back to an earlier version, change display modes, then try again. 

# 1010
* Version 0.87 in the menu
> Optimized some games with abnormal sound
> Volume brightness minimum
> This version will serve as the initialization version


# 1015
* Unknown changes, no notes

# 10.25
* Version 0.88 in the menu
* Unknown changes, no notes
* Latest stable version
* **This is probably the version you want for now.** 

# 10.25.1
* Unknown changes, no notes
> There's a big problem

# 1117
* Version 0.89 in the menu
* Unknown changes, no notes
* Latest test version. 
