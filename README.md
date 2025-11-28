# Arch Jonux is an Arch(btw)-based GNU/Linux distro.
At this point in time, it is pretty much just the archiso https://archlinux.org with an easy arch install script based on this script: https://github.com/classy-giraffe/easy-arch/tree/main



## Features

**LUKS2-encryption**: Your files will be protected with a password (das cool)

**btrfs-snapshots**: Automatic snapshots of your system probably, I haven't tested yet.

**ZRAM**: Some cool swap alternate thingy I dunno.

**Predefined Finnish language**: If you don't want this, then I guess you are gonna have to fork this.


## What is modified?

Very little has been modified from the official archiso.

When booting the archiso, it will say Arch Jonux instead of Arch Linux (btw). I don't remember all the files which were modified to change this, but it was at least the grub files.

The packages.x86_64 includes some additional packages (eg. fastfetch).

airootfs/root/.automated_script.sh runs loadkeys fi and the archjonux-install.sh



## Building your own ISO
Check this page: https://wiki.archlinux.org/title/Archiso

Just modify what you want in the arch jonux folder.

The installation script is in airootfs/root/archjonux-install.sh

Building the ISO only requires you to be on an arch-based distro and install the archiso package with **sudo pacman -S archiso**

archiso package contains mkarchiso command which is used to build the ISO.

I use **sudo mkarchiso -v -r -w /tmp/archiso-tmp -o ~/ ./** to build it.

This will put the ISO inside your home directory and needs to be run from inside /archjonux for it to work (or just change the last ./ to the correct directory)


> [!NOTE]
> When using virtualbox, remember to choose UEFI


> [!TIP]
> Bro, just use Arch Linux (btw), it's way better


> [!WARNING]
> Do NOT use this on any important system because at this stage it has not been tested on anything but virtualbox.
