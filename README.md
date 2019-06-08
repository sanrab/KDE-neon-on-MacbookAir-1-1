# KDE-neon-on-MacbookAir-1-1

KDE neon installation on a 2008 MacbookAir 1,1

hardware : MacBookAir 1,1, Core 2 Duo 1.6 13" Original, RAM 2 GB, late 2008

Last possible OS X : Mac Os X Snow Leopard 10.6.8  = too old !

notice : UEFI 32 bit !!

Download KDE Neon latest

from https://mattgadient.com/2016/07/11/linux-dvd-images-and-how-to-for-32-bit-efi-macs-late-2006-models/

How-to: Making a standard Linux distro ISO compatible with 32-bit EFI Macs 

search "Converting the ISO"; 
follow instructions for the ISO conversion

convert KDE Neon ISO

Make USB with Balena-etcher

boot from USB (alt/option + power on);
install (very slow at the beginning due to to drm_kms_helper errors); wait

reboot

in Konsole:

sudo nano /etc/default/grub

change the line GRUB_CMDLINE_LINUX_DEFAULT="quiet video=SVIDEO-1:d"

sudo update-grub

sudo reboot

now it boots much faster

for BCM4321 wifi:

in Konsole:

sudo apt purge bcmwl-kernel-source

sudo apt install b43-fwcutter firmware-b43-installer

sudo reboot

working:

external monitor

battery indicator

keyboard backlight function key

brightness function key

internal wi-fi (BCM4321)



