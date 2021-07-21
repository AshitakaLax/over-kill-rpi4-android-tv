# over-kill-rpi4-android-tv
A low cost rpi4 Android TV setup instructions that destroys weak sauce "Smart" tv's.

## Overview

 * Update a rpi4(8Gb Model) to use PXE Network boot.
 * Setup a PXE Network Boot Server.
 * Configure the bootloader to load into 4Gb partitioned ramdisk.
 * Boot the latest Android 11 TV konstakang image into 4Gb Ramdisk.
 *  Install [OpenGApps](https://sourceforge.net/projects/opengapps/files/arm/test/20210130/) for Google play access.
 * Gigabit network file system for apps and persistent data storage.
 * Slightly overclock CPU for burst performance improvements while maintaining below 50C temperature(Note: temp throttling takes place at 80C).
 * Attach network drive that contains the android /sdcard items
   *  

## OS Performance Goals

With the SDCard throughput throttling the OS speeds to ~20MB/S. The next upgrade would be a SSD USB drive with ~40MB/S. The Network I/O speeds can get up to around ~110 MB/s. With the known performance king ramdisk at about 300MB/s.
We should be able to out perform most Raspberry pi Android TV setups.


## Benchmarks

Read Speed
| Device | SDCard | SSD(USB) | M.2 | Command | Source|
|:------:|:------:|:------:|:------:|:------:|:------:|
| Read speed | 44.53 MB/sec | 108.56 MB/sec | 347.06 MB/sec | hdparm -t | [Raspberry Pi 4 Boot from USB:14 minutes into it](https://www.youtube.com/watch?v=nFM01mQ9qrk) |
