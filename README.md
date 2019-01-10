ANNOUNCING RECALBOX FOR THE RK3399 ROCKPRO64 - BETA RELEASE

After many efforts with much teamwork, collaboration, and testing, we are very excited to provide the BETA release of RECALBOX for the ROCKPRO64 board!
-- The download is located under this repository's releases -- 
https://github.com/mrfixit2001/recalbox_rockpro64/releases

Details on the ROCKPRO64 SoC can be found here: https://www.pine64.org/?page_id=61454

For those of you unfamiliar with Recalbox: https://www.recalbox.com/ 
"Recalbox offers a wide selection of consoles and game systems. From the very first arcade systems to the NES, the MEGADRIVE, 32-bit platforms (such as the Playstation) and even Nintendo64. With Kodi already included, Recalbox also serves as a Media Center. By connecting it to your home network, you will be able to stream videos from any compatible devices (NAS, PC, External HDD, etc.)."

Please do keep in mind that this is a BETA release, which means you should still EXPECT some things not to work quite right. We have done a LOT of testing on our own to try and resolve as many issues as we can before this release, but now you get to help! (Lucky you!) So if/when you do find things that don't work right, please use the link in github to report the issue.

When reporting issues:
- Provide logs and/or screenshots of the issue so that we can see the error(s) you are seeing
- Provide detailed steps for us to follow in order to reproduce the issue

We STRONGLY recommend that you install a heatsink on the board
CPU intensive tasks, such as 4K playback and demanding emulators, can create a substantial amount of heat. You can monitor your board's temperature and stats by enter it's IP address in a browser.

Improvements Since the Alpha Release:
Kernel Updates:
- Updated to version 4.4.169
- Various custom kernel fixes, mainline backports, stability and other enhancements
- 4K Playback @ 60fps is now smooth and Audio/Video are synced

Emulator Updates:
- Updated versions of many emulators and cores
- Buggy button re-mapping issue is resolved
- PPSSPP now performs at 100% speed for most games
- Customizable "max fps" setting in PPSSPP to fine tune your experience - set to 30fps to play GOW nice and smooth!
- PSP video scenes now play perfectly
- VirtualJaguar is now fixed and playable
- NEOGEO Core Fixed
- Bluetooth Controllers Reconnect After Reboot

Rockpro Specific Updates:
- WIFI and Bluetooth Module working (https://www.pine64.org/?product=rockpro64-2x2-mimo-dual-band-wifi-802-11acbluetooth-4-1-module)
- RTL8812EU USB Wifi adapter working (https://www.pine64.org/?product=rock64-usb-3-0-dual-band-1200mbps-wifi-802-11abgnac-rtl8812au-adapter)
- eMMC boot issues resolved
- Headphone / Audio-Out (ES8316) Fixed
- PCIe is enabled and connected storage devices have been confirmed to work correctly
- Improved Gigabit Ethernet performance
- Custom optimized resolutions for Mupen, PSP, and Reicast to hit 100% emulation speeds!
- EmulationStation menu music always playing


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


"Where's the source code?" The source is being cleaned up and organized in preparation to be made available for the recalbox team to maintain, instead of having it hosted in this repository. Merging it with the recalbox repo allows them to maintain and update it, which ensures that you will receive their updates as they are made available.

Lastly, please remember this is a community build, and just something I've worked on in my free time. There's no pressure at all, but if you appreciate the work then feel free to send me a buck on Paypal: mrfixit2001 at gmail.

Special thanks go out to the LibreELEC and Recalbox teams, as well as LukasZ at Pine64 for his huge efforts in research, testing, and feedback!

Mr Fix-IT
