---
permalink: /vhbl-psvimgtools.html
title: Installing VHBL ePSP Homebrew Launcher
author_profile: true
---
{% include toc title="Разделы" %}

Vita Half Byte Loader is a homebrew loader for the PSP emulator (ePSP) within the Vita. The exploit used by ARK for 3.61-3.63 was patched in 3.65, so all we can gain access to is ePSP Homebrew. {: .notice--info}

On this page we will install VHBL. {: .notice--info}

#### What you need

* A PSP game downloaded on your Vita.
* The latest release of [QCMA](https://codestation.github.io/qcma/) for your OS.
* The latest release of [psvimgtools](https://github.com/yifanlu/psvimgtools/releases/latest) for your OS.
* The [VHBL files archive](https://mega.nz/#!4QoVGDRD!mx7_kCQ83-GKlrGrN8rUl5hpYQAlI1Pl7gWm2lsPeuQ).

#### Instructions

##### Section I - Installing VHBL

1. Download and Install QCMA and set up the connection between QCMA and your Vita.
2. Get your PSN AID. By default, on Windows it will be located in `C:/Users/Username/Documents/PS Vita/PGAME/xxxxxxxxxxxxxxxx/`. `xxxxxxxxxxxxxxxx` (will be a bunch of characters) is your PSN AID.
3. Go to <http://cma.henkaku.xyz/> and paste your PSN AID into the box.
4. Copy the Key it's spits out and put it into a safe place. (Preferably in a text document called "AID KEY")
5. Extract the psvimgtools archive for your OS. (Make sure to put the files somewhere where you'll remember them!)
6. Backup a PSP game with QCMA.
7. Find the game backup in /PSvita/PGAME/xxxxxxxxxxxxxxxx/[GAMEID]/game/game.psvimg
8. Copy the game.psvimg to the psvimgtools folder.
9. Open Command Prompt (Windows) or Terminal (macOS/Linux).
10. Navigate to the psvimgtools folder using `cd`
11. Type `psvimg-extract -K YOUR-KEY game.psvimg` (Windows) or `./psvimg-extract -K YOUR-KEY game.psvimg game` (macOS/Linux), replacing `YOUR-KEY` with the key you got from http://cma.henkaku.xyz/.
12. You will get a folder with the name of `ux0_pspemu_temp_game_PSP_GAME_ID`, `PSP_GAME_ID` will be the GAME ID of your PSP game.
13. Extract the VHBL PBOOT bubble archive and find the PBOOT.PBP
14. Replace the PBOOT.PBP file in the folder of your extracted game (`ux0_pspemu_temp_game_PSP_GAME_ID`) with the VHBL PBOOT.PBP
15. Type `psvimg-create -n game -K YOUR-KEY game game` (Windows) or `./psvimg-create -n game -K YOUR-KEY game game` (macOS/Linux), again replacing `YOUR-KEY` with the key you got from http://cma.henkaku.xyz/. This command will output a `game.psvimg` and a `game.psvmd` in the `ux0_pspemu_temp_game_PSP_GAME_ID` folder.
16. Overwrite the files in the files in the QCMA Backup folder with these ones that you just generated.
17. Restore the QCMA Backup of your PSP game after pasting the files.
18. Copy the VHBL01234 folder from the VHBL files archive to /PSvita/PSAVEGAME/xxxxxxxxxxxxxxxx/. (xxxxxxxxxxxxxxxx is your PSN AID).
19. Restore the VHBL PSP SAVEDATA from your pc to your Vita using QCMA.

* * *

Continue to [Finalizing Setup (VHBL)](finalizing-setup(VHBL)) {: .notice--primary}