---
title: "SD2Vita Information and Setup"
---

#### Overview of steps

During this process, we will setup your SD2Vita Adapter to get it working with your PS Vita:

#### What you need

* The latest release of [GameSD](https://github.com/xyzz/gamecard-microsd/releases/) (the .skprx file)
* The [zzBlank.img]({{ base_path }}/files/zzBlank.img) file 
* An FTP Client such as [FileZilla](https://filezilla-project.org/download.php)

#### Instructions

##### Section I - Prep Work

1. Launch VitaShell on your Vita and press Select to start the built-in FTP Server.
1. Connect to your Vita using your FTP Client.
1. Copy `gamesd.skprx` to the `ur0:tai` folder on your vita
1. Copy all files from `ux0:tai` to `ur0:tai`
1. Add the following line to ``ur0:tai/config.txt`` under the line ``*KERNEL``:
 + ``ur0:tai/gamesd.skprx``.
1. Backup your Vita Memory Card to your computer via VitaShell using USB or FTP
 + If you're using USB, make sure you have hidden files enabled and hidden operating system files enabled
1. Put your microSD card into your computer

##### Section II - Format SD card

In case which operating system you have, do the following steps:
[Windows](sd-format-windows), [Linux](sd-format-linux) or [MacOS](sd-format-macos).

##### Section III - Restore files from Backup

1. Copy the backup you made earlier to the SD Card
1. Put the SD Card into the SD2Vita adapter and reboot your PS Vita

---

The PS Vita should boot as usual. Every Software already installed should be listed. You do not need
the Memory Card anymore. Don't forget to change `USB Device` to `sd2vita` in `VitaShell`
{: .notice--success}
