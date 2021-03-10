# UltiFlash

I am designing a bash-based flashing utility (called UltiFlash) that will leave all others behind in the dust, in terms of speed and flexibility.  
![2021-03-06-090329_1920x1080_scrot](https://user-images.githubusercontent.com/54716352/110555837-eeb9be00-8102-11eb-8463-dcc9bcd86a92.png)  
It will do everything RPi Imager does, everything Etcher does, everything SD Card Copier does, everything RonR's `image-backup` does, and much more. It will be both GUI and CLI.  
In addition, it will support file conversions (.img, .zip, and .xz), incremental backups, have the most informative progress bar, verifying capabilities, and multiple download connections for maximum speed. Despite all these features, it'll be very easy to use.

Plans began forming around May 2020, after the general public was dismissive to [Pi Power Tools' flashing benchmarks](https://www.raspberrypi.org/forums/viewtopic.php?f=63&t=272365) and pointed out its shortcomings. Originally I planned to *improve* Pi Power Tools's Flash tool, but as the list of necessary changes got longer and longer, I realized a **full rewrite** was required.  
[Development began](https://github.com/ptitSeb/box86/issues/296#issuecomment-783524463) on Feb 22 2021 after I was introduced to the `aria2c` download utility and realized its usefulness for a flash utility.

## Combinations available:

Input -> Output|UltiFlash|Raspberry Pi Imager|balenaEtcher
--- | --- | --- | ---
SD card -> SD card|✔️|❌|✔️
SD card -> SD card (file-based)|✔️|❌|❌
SD card -> file.img|✔️|❌|❌
SD card -> file.img (file-based)|✔️|❌|❌
SD card -> file.zip|✔️|❌|❌
SD card -> file.xz|✔️|❌|❌
SD card -> file.gz|✔️|❌|❌
file.img -> SD card|✔️|✔️|✔️
file.img -> SD card (file-based)|✔️|❌|❌
file.img -> file.img|✔️|❌|❌
file.img -> file.img (file-based)|✔️|❌|❌
file.img -> file.zip|✔️|❌|❌
file.img -> file.xz|✔️|❌|❌
file.img -> file.gz|✔️|❌|❌
file.zip -> SD card|✔️|✔️|✔️
file.zip -> file.img|✔️|❌|❌
file.zip -> file.zip|✔️|❌|❌
file.zip -> file.xz|✔️|❌|❌
file.zip -> file.gz|✔️|❌|❌
file.xz -> SD card|✔️|✔️|✔️
file.xz -> file.img|✔️|❌|❌
file.xz -> file.zip|✔️|❌|❌
file.xz -> file.xz|✔️|❌|❌
file.xz -> file.gz|✔️|❌|❌
file.gz -> SD card|✔️|✔️|✔️
file.gz -> file.img|✔️|❌|❌
file.gz -> file.zip|✔️|❌|❌
file.gz -> file.xz|✔️|❌|❌
file.gz -> file.gz|✔️|❌|❌
url.img -> SD card|✔️|✔️|✔️
url.img -> file.img (aria2c)|✔️|❌|❌
url.img -> file.zip|✔️|❌|❌
url.img -> file.xz|✔️|❌|❌
url.img -> file.gz|✔️|❌|❌
url.zip -> SD card|✔️|✔️|✔️
url.zip -> file.img|✔️|❌|❌
url.zip -> file.zip (aria2c)|✔️|❌|❌
url.zip -> file.xz|✔️|❌|❌
url.zip -> file.gz|✔️|❌|❌
url.xz -> SD card|✔️|✔️|✔️
url.xz -> file.img|✔️|❌|❌
url.xz -> file.zip|✔️|❌|❌
url.xz -> file.xz (aria2c)|✔️|❌|❌
url.xz -> file.gz|✔️|❌|❌
url.gz -> SD card|✔️|✔️|✔️
url.gz -> file.img|✔️|❌|❌
url.gz -> file.zip|✔️|❌|❌
url.gz -> file.xz|✔️|❌|❌
url.gz -> file.gz (aria2c)|✔️|❌|❌
