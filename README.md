ANNOUNCING RECALBOX FOR THE RK3399 ROCKPRO64

After many efforts with much teamwork, collaboration, and testing, we are very excited to provide the release of RECALBOX for the ROCKPRO64 board!

-- The download is located under this repository's releases -- 
https://github.com/mrfixit2001/recalbox_rockpro64/releases

MrFixIt's custom kernel source is available here: https://github.com/mrfixit2001/rockchip-kernel

Recalbox's source is available on their repo: https://gitlab.com/recalbox

Details on the ROCKPRO64 SoC can be found here: https://www.pine64.org/?page_id=61454

For those of you unfamiliar with Recalbox: https://www.recalbox.com/ 
"Recalbox offers a wide selection of consoles and game systems. From the very first arcade systems to the NES, the MEGADRIVE, 32-bit platforms (such as the Playstation) and even Nintendo64. With Kodi already included, Recalbox also serves as a Media Center. By connecting it to your home network, you will be able to stream videos from any compatible devices (NAS, PC, External HDD, etc.)."

When reporting issues:
- Provide logs and/or screenshots of the issue so that we can see the error(s) you are seeing
- Provide detailed steps for us to follow in order to reproduce the issue

We STRONGLY recommend that you install a heatsink on the board
CPU intensive tasks, such as 4K playback and demanding emulators, can create a substantial amount of heat. You can monitor your board's temperature and stats by enter it's IP address in a browser.

Latest Improvements:
- Kernel updated to 4.4.171
- Additional mainline back-ports and custom fixes
- Additional drivers included in kernel
- PCIe now works with Wifi and Bluetooth all at the same time
- UART debug output enabled
- Custom "Rockpro Fan" toggle in menu under system settings
- Retroarch Updated to 1.7.6
- Newer versions of some emulators
- Pre-set optimized config for Mupen64
- Resolution for Mupen64, Reicast, and Retroarch can now be changed from recalbox.conf file
- Custom fix for widescreen's auto-stretching the picture (read the readme)
- On-Screen-Keyboard issue Resolved
- Custom patches to ES and Emulators to improve overall stability
- Additional fixes for XBox One and 8BitDo controllers


Some things that have been added to Recalbox that are Exclusive to my Pine64 releases:
- Upgraded Kodi (and addons) from version 17 (Krypton) to version 18 (Leia) alpha release
- Netflix Kodi app is included – you can login but it does not currently play anything (yet)
- Slight default overclock
- HDR and 4k Media Playback!
- Included Wolfenstein 3D (shareware version) in DosBox
- CEC working in KODI 
- IR working in KODI – supports multiple remotes out of the box, including the Pine64 / Rockbox remote
- Provided some emulator default settings, shader presets, and default cores
- Updated Library Versions with Buildroot 2018.2-3
- Custom patches to ES and Emulators to improve overall stability

A few things to know about this release:
When the image first boots, you can expect a delay as the partition is expanded to the full size of your disk. Please be patient and let this complete. It will not happen on every boot, but you should not interrupt this process or you may need to reimage.

Some controllers will work with KODI right out of the box without the buttons needing to be mapping (like the x360). For others, once you hit a button on the controller it will ask you to map them - you will need a keyboard to interact with KODI until your controller buttons are mapped.

N64 has multiple core options, different ROMS work better with different cores! So if your game isn't running well, try another core! So far even the most demanding games have been found to run perfectly with the right core selected.

Some emulators / cores are highly dependent on a valid BIOS files being installed (Dreamcast, for example). Be sure to read the documents in the system’s ROM folder for details on what BIOS files are needed. Further documentation is available on the Recalbox wiki.

A single ROM not working is not considered a "bug", it's often an incompatibility with the ROM and the emulator / core. We have provided multiple cores for some emulators to try and help maximize the number of ROMS that work.

If you are suddenly and unexpectedly thrown into KODI, then that means EmulationStation may have crashed. Please provide your /recalbox/es.log file so we can review.

Important Note about Widescreens: The majority of users will be using widescreen monitors and TVs with 16:9 aspect ratios these days, and most of these will automatically stretch a 4:3 video to 16:9 to make it full screen. This distorts the graphics and makes everything look stretched out and askew. So, I have added custom patches and new configuration settings to Mupen64, Reicast, and Retroarch to correct this so that the emulators will still render at the right scale after being stretched. :) This is ON by default. If you do not have a widescreen monitor, or your monitor does not have this auto-stretch feature, then your games may not be centered or look too thin. In this case, simply make the following one-time changes to the configurations to turn off these customizations:
- Retroarch: use the retroarch menu to change the default - Settings->Video->Aspect Ratio
- Reicast: change the setting "rend.FixAspect" to 0 in /recalbox/share/system/configs/reicast/emu.cfg
- Mupen64: each video plugin (core) has been given it's own setting, allowing you to customize each to your own needs, and GLES2N64 (n64 core) has it's own config file. The settings for these plugins are in /recalbox/share/system/configs/mupen64 in the files mupen64plus.cfg and gles2n64.conf. Just change the listed widths and left offsets to whatever your needs are.

"Where's the source code?" The source is being cleaned up and organized in preparation to be made available for the recalbox team to maintain, instead of having it hosted in this repository. Merging it with the recalbox repo allows them to maintain and update it, which ensures that you will receive their updates as they are made available.

Lastly, please remember this is a community build, and just something I've worked on in my free time. There's no pressure at all, but if you appreciate the work then feel free to send me a buck on Paypal: mrfixit2001 at gmail.

Special thanks go out to the LibreELEC and Recalbox teams, as well as LukasZ at Pine64 for his huge efforts in research, testing, and feedback!

Mr Fix-IT
