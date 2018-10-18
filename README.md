ANNOUNCING RECALBOX FOR THE ROCKPRO64 - ALPHA RELEASE

After many efforts with much teamwork, collaboration, and testing, we are very excited to provide the ALPHA release of RECALBOX for the ROCKPRO64 board! 

-- The download is located under this repository's releases --
https://github.com/mrfixit2001/recalbox_rockpro64/releases

Details on the ROCKPRO64 SoC can be found here:
https://www.pine64.org/?page_id=61454

For those of you unfamiliar with Recalbox:
https://www.recalbox.com/
"Recalbox offers a wide selection of consoles and game systems. From the very first arcade systems to the NES, the MEGADRIVE, 32-bit platforms (such as the Playstation) and even Nintendo64. With Kodi already included, Recalbox also serves as a Media Center. By connecting it to your home network, you will be able to stream videos from any compatible devices (NAS, PC, External HDD, etc.)."

Please do keep in mind that this is a ALPHA release, which means you should still EXPECT some things not to work quite right. We have done a LOT of testing on our own to try and resolve as many issues as we can before this release, but now you get to help! (Lucky you!) So if/when you do find things that don't work right, please use the link in github to report the issue.

When reporting issues:
 - Provide logs or screenshots of the issue so that we can see the error(s) you are seeing
 - Provide detailed steps for us to follow in order to reproduce the issue

A few things to know about this release:
 -  Remapping the buttons on some controllers, such as 8BitDo, cause the controller to not work in the emulators – use the default keymaps for these
 -  Resolution for Non-Retroarch Emulators and EmulationStation is 1080p, manual config edit will be needed to change: 
    o Mount the BOOT partition and edit /boot/extlinux/extlinux.conf -- look for the following value: video=HDMI-A-1:1920x1080@60. Edit to your desired resolution. 
    o NOTE: Resolution in KODI can be adjusted without any config changes (up to 4k!)
 -  Netflix Kodi app is included – you can login but it does not currently play anything (yet)
 -  When the image first boots, you can expect a delay as the partition is expanded to the full size of your disk. Please be patient and let this complete. It will not happen on every boot, but you should not interrupt this process or you may need to reimage.
 -  N64 has multiple cores, different ROMS work better with different cores! For example, Mario Kart and Perfect Dark both perform very well using the N64 core (which is “GLES2N64”).
  -  Some emulators / cores are highly dependent on a valid BIOS files being installed (Dreamcast, for example). Be sure to read the documents in the system’s ROM folder for details on what BIOS files are needed. Further documentation is available on the Recalbox wiki.
 -  A single ROM not working is not considered a “bug”, it’s often an incompatibility with the ROM and the emulator or core. We have provided multiple cores for some emulators to try and help maximize the number of ROMS that work.
 -  If you are suddenly and unexpectedly thrown into KODI, then that means EmulationStation may have crashed. Please provide your /recalbox/es.log file so we can review.
 -  We STRONGLY recommend that you install a heatsink on the board

Some things we have added to Recalbox that are Exclusive to the Pine64 releases:
 -  Upgraded Kodi (and addons) from version 17 (Krypton) to a July 2018 commit of version 18 (Leia)
 -  InputStream.Adaptive Kodi Addon
 -  Multiple cores for different emulators so that you can select which core works best for you on each ROM!
 -  Slight default overclock
 -  HDR and 4k Media Playback!
 -  Included Wolfenstein 3D (shareware version) in DosBox
 -  CEC working in KODI
 -  IR working in KODI – supports multiple remotes out of the box, including the Pine64 / Rockbox remote
 -  Added some default shader presets and default cores
 -  Updated Library Versions with Buildroot 2018.2-3
 -  Custom patches to ES and Emulators to improve overall stability


"Where's the source code?"
The source is in the final stages of being cleaned up and organized in preparation to be made available for the recalbox team to maintain, instead of having it hosted in this repository. Merging it with the recalbox repo allows them to maintain and update it, which ensures that you will receive their updates as they are made available. 

Lastly, please remember this is a community build, and just something I've worked on in my free time. There's no pressure at all, but if you appreciate the work then feel free to send me a buck on Paypal: mrfixit2001 at gmail.

Special thanks go out to Kwiboo from LibreELEC, Substring at Recalbox, and LukasZ at Pine64 for their efforts in testing and feedback!

- Mr Fix-IT
