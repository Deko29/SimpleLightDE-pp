###### FORKED FROM https://github.com/Sterophonick/omega-de-kernel

# SimpleLightDE++ (EZ Flash Omega DE)
###### *If you're looking for SimpleLight++ for the **original** EZ Flash Omega, check here: https://github.com/Deko29/SimpleLight-pp*

This is SimpleLightDE++, a small Fork of the SimpleLightDE CFW aimed to introduce new QoL features and to fix various bugs.

Huge thank you to all authors of the original FW and the SimpleLightDE CFW, without you this project wouldn't be possible!

## New Features
- New Boot Options:
  
  - MENU: Standard booting behavior. If L is pressed, boot into the first NOR game
  - NOR: Boot into first NOR game. If L is pressed, boot into the EZ-Menu
  - LAST: Boot into your last recent game/software (also takes NOR Games into account). If L is pressed, boot into the EZ-Menu
    
- Overhauled Settings and re-added the extra Settings window! Extra Settings can be opened with SELECT and are now controllable via arrow and L/R keys

## Bug Fixes:
* Cursor of file explorer will not reset anymore when opening expanded settings via SELECT
* The Save backup folder is correctly initialized if it does not exist
* Restored old extra settings window
* Various other minor tweeks

## Known Issues
* Chinese Language Option is broken

## Notes
* DO NOT alter the "RECENT.TXT" file! This is used for the "LAST" boot option and can otherwise lead to undefined behaviour
* DO NOT create a folder/file called "NOR" on root level! The card should throw an error and lifelock itself, but still, don't do this!

If you have any feature requests or issues, please let me know :)

# Original ReadMe...

###### FORKED FROM https://github.com/ez-flash/omega-de-kernel

Hello all!

I have been working on a new theme for the EZ-Flash Omega, and I call it Simple.

It is a nice rounded theme with both light and dark options, and allows for many, many more file types to be used, such as Master System and ZX Spectrum ROMs to be launched, along with the ability to view bitmap images, read text documents, and play music. (shoutouts to Kuwanger for PogoShell)

I completely redid all of the graphics, along with using a different font.

It also uses the 2019-05-04 version of Goomba Color, and has a save backup feature (shoutouts to Veikkos)

Hope everyone likes it!

Official forum thread:
https://gbatemp.net/threads/new-theme-for-ez-flash-omega.520665/

## Installation instructions:

_**Be sure you're using the most recent version, and follow the installation instructions in the !!!!!!!!!IMPORTANT!!!!!!!!!!!.TXT file in the GBAtemp package before reporting issues.**_

_**ALSO YOU MUST USE THE OFFICIAL KERNEL TO UPDATE THE FIRMWARE; THIS DOES NOT APPLY TO THE BASE OMEGA :(**_

1. Copy the SYSTEM and BACKUP folder to the root of the SD Card.
2. Move your IMGS, SAVER, RTS, and PATCH folders to SYSTEM.
3. If you want the light theme, copy ezkernel-light.bin to the root of the SD Card. If you want the dark thing, do the same with ezkernel-dark.bin
4. Rename the new kernel file to ezkernel.bin
5. You're done!

## Registered file types:
### Game ROMs
    .gba - GBA ROM
    .bin - GBA ROM
    .mb - GBA Multiboot ROM
    .agb - GBA ROM
    .col - ColecoVision ROM (Requires Cologne) *
    .gb - Game Boy ROM (Jaga's Goomba Color)
    .gbc - Game Boy Color ROM (Jaga's Goomba Color)
    .gg - Game Gear ROM (SMSAdvance)
    .rom - MSX Cartridge ROM (MSXAdvance) **
    .ngp - Neo Geo Pocket ROM (NGPAdvance)
    .ngc - Neo Geo Pocket ROM (NGPAdvance)
    .ngpc - Neo Geo Pocket Color ROM (NGPAdvance)
    .nes  - NES ROM File (PocketNES)
    .pce - PC-Engine ROM File (PCEAdvance)
    .sms - Sega Master System ROM File (SMSAdvance)
    .sg - Sega SG-1000 ROM File (SMSAdvance)
    .sv - Watara Supervision ROM File (Wasabi)
    .ws - WonderSwan ROM File (SwanAdvance)
    .wsc - WonderSwan Color ROM File (SwanAdvance)
    .z80 - 48k ZX-Spectrum Z80 ROM (ZXAdvance)
    .c8 - Chip-8 ROM (Chip8Adv (My First Emulator! :D))
    .arc - 4kb Emerson Arcadia 2001 ROM File

### Media
    .jpg - JPEG Image
    .jpeg - JPEG Image
    .mod - ProTracker Module file
    .bmp - Bitmap Image
    .pcx - ZSoft Paintbrush PCX image
    .mid - MIDI sequence
    .nsf - NES Music file (Nintendo Sound File)
    .vgm - SMS/GG music file
    .vga - aPlib Compressed SMS/GG music file
    .vgl - LZ77 Compressed SMS/GG music file
    .txt - Text Document
    .wav - Wave Sound (formatted in GSM 6.10)
    .k3m - Krawall Advance Sound
    .sb - MaxMod sound bank
    .lz - LZ77 Compressed Image
    .raw - Uncompressed Mode 3 Bitmap
    .ap - aPlib compressed Mode 3 Bitmap
    .bgf - BoyScout module
    .mda - Sharp X68000 Music
    .cwz - CWZ Music (IDK what exactly it is, but it was included with PogoShell 1.2)

*\* For Cologne, you have to make the ROM yourself.*\
*\*\* MSXAdvance uses the C-BIOS, so I can redistribute the emulator.*

##### Cologne Emulator Guide:
1. Download the latest version of Cologne.
2. Open the EXE file.
3. Take a blank file, and also add the Official Colecovision BIOS.
4. Create col.gba in the PLUG folder.

### This ZIP file contains some tech demos/games:
* XBill (SG-1000)
* Sega Tween (SMS)
* WinGG (Game Gear)
* HuZERO (PC-Engine)
* 1968 (ZX-Spectrum)
* Adventures Of Gus and Rob (Neo Geo Pocket)
* Kaboom! (Homebrew) (ColecoVision)
* Motkonque (MSX)
* SwanDriving (WonderSwan)
* F8Z (Chip-8)

### How to build 
1. Install [devkitPro](https://devkitpro.org/)
2. Set the following environment variables to their correct directories: `DEVKITPRO, DEVKITARM, LIBGBA`
3. Comment or uncomment the `#define DARK` line in `draw.h`. If uncommented, a dark theme is generated.
4. Run the command `make`. If done successfully, this should give you an `ezkernel.bin` file.
5. Follow the installation instructions above.
4. Update your flashcart and enjoy! :)

### Special Greetz & Contributors:
Sasq\
Moonlight\
Kuwanger\
veikkos\
DarkFader\
CoolHJ\
Let's Emu!\
Izder456\
NuVanDibe\
SLKun\
Mintmoon\
hitsgamer\
Rocky5

### Credits
[EZ-FLASH](https://www.ezflash.cn/) - The original firmware & hardware creators\
Kuwanger - PogoShell plugin integration\
Sterophonick - SIMPLE theme for EZO & EZODE\
fluBBa - SMSAdvance, MSXAdvance, Cologne for GBA, Goomba for GBA (Original), PCEAdvance, PocketNES, SNESAdvance, Wasabi, NGPAdvance, SwanAdvance\
[Jaga](https://github.com/EvilJagaGenius) - [Jaga's Goomba Color fork](https://github.com/EvilJagaGenius/jagoombacolor)\
...and others!

