# ultiflash

I am designing a bash-based flash utility (called UltiFlash) that will leave all others behind in the dust, in terms of speed and flexibility.  
![screenshot.png](https://cdn.discordapp.com/attachments/752577535375704224/817546525302587402/2021-03-05-174312_1920x1080_scrot.png)  
It will do everything RPi Imager does, SD Card Copier does, and RonR's `image-backup` does. It will be both GUI and CLI.  
In addition, it will support file conversions (.img, .zip, and .xz), incremental backups, have the most informative progress bar, verifying capabilities, artificial intelligence, and multiple download connections for maximum speed. Despite all these features, it'll be very easy to use.

## Combinations available:

Input -> Output|UltiFlash|Raspberry Pi Imager|balenaEtcher
--- | --- | --- | ---
SD card -> SD card|✔️|❌|✔️
SD card -> SD card (file-based)|✔️|❌|❌
SD card -> file.img|✔️|❌|❌|❌
SD card -> file.img (file-based)|✔️|❌|❌
SD card -> file.zip|✔️|❌|❌
SD card -> file.xz|✔️|❌|❌
SD card -> file.gz|✔️|❌|❌
file.img -> SD card|✔️|✔️|✔️
file.img -> SD card (file-based)|✔️|❌|❌
file.img -> file.img|✔️|❌|❌|❌
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
