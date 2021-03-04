# ultiflash

I am designing a bash-based flash utility (called UltiFlash) that will leave all others behind in the dust, in terms of speed and flexibility.

It will do everything RPi Imager does, SD Card Copier does, and RonR's `image-backup` does. It will be both GUI and CLI.  
In addition, it will support file conversions (.img, .zip, and .xz), incremental backups, have the most informative progress bar, verifying capabilities, artificial intelligence, and multiple download connections for maximum speed. Despite all these features, it'll be very easy to use.

## Combinations available:

Input|Output
--- | --- 
SD card|SD card
SD card|file.img (can be incremental)
SD card|file.zip
SD card|file.xz
-|
file.img|SD card (can be incremental)
file.img|file.img (can be incremental)
file.img|file.zip
file.img|file.xz
file.zip|SD card
file.zip|file.img
file.zip|file.zip
file.zip|file.xz
file.xz|SD card
file.xz|file.img
file.xz|file.zip
file.xz|file.xz
-|
url.img|SD card
url.img|file.img (aria2c)
url.img|file.zip
url.img|file.xz
url.zip|SD card
url.zip|file.img
url.zip|file.zip (aria2c)
url.zip|file.xz
url.xz|SD card
url.xz|file.img
url.xz|file.zip
url.xz|file.xz (aria2c)

