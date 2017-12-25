---
title: "SD Card formatting with Linux"
---

#### Required Reading
This page is for Linux users only. If you are not on Linux, check out the corresponding [Windows](sd-format-windows) and [MacOS](sd-format-macos) pages.

#### Overview of steps

During this process, we will setup your SD Card to get it working with your SD2Vita Adapter in your PS Vita:

#### What you need

* [exfat-utils](https://github.com/relan/exfat) on your Linux distribution to format your SD Card. Maybe it's in your package manager. Search for it
* [fuse-exfat](https://github.com/relan/exfat) on your Linux distribution to mount your SD Card with exFAT filesystem. Maybe it's in your package manager. Search for it.
* The [zzBlank.img]({{ base_path }}/files/zzBlank.img) file 

#### Instructions

1. Put your SD Card into your Computer. For example with an SD Card adapter or built-in SD Card reader.
1. Find the whole-device node for the SD Card (usually **/dev/sdX** or **/dev/mmcblkX**.
1. Unmount all partitions, but don't eject the microSD. Replace the X with the actual device name. 
{% highlight bash %}
root# umount /dev/sdX1
{% endhighlight %}
1. Use the `dd` command to write zzBlank.img to the card
{% highlight bash %}
root# dd if=/path/zzBlank.img of=/dev/sdX
{% endhighlight %}
1. Take out the micro SD card and put it in again
1. Create a new exFAT filesystem on the whole SD Card
{% highlight bash %}
root# mkfs.exfat /dev/sdX
{% endhighlight %}
1. mount your SD Card on your system. Use the uid of your user name. You can find it with the comman `id`. Replace the **1000** with your current uid
{% highlight bash %}
root# mount -o uid=1000 /dev/sdX /mnt/
{% endhighlight %}
1. Go back to the [SD2Vita Setup Page](sd2vita-info-setup) and proceed with Section III

