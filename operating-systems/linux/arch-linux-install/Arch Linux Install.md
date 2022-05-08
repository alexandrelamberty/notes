# Arch Linux installation

Pre-installation
Language and keymap
Partition disks
Ethernet and wireless connection
Installation
Download and install the base system
Enter root and create a password
Set locales
Set your timezone
Install boot loader
Set hostname and configure ethernet and wireless connection
Unmount disk and reboot
Package manager
Create root password, users
Improve bash
Configure Network
fplug for laptop
Optimize Pacman
Mirrors
Arch User Repository
Install Yaourt
Test yaourt
Install Pacaur
Install packages
Install GUI
Install video driver
Install display-server
Login Manager
Desktop environment
Awesome Window Manager
Install more
Bash
Tmux
Text editor
Sublime text
File Manager
Thunar
Image Viewer
Audio Player
Video player
Web browser
References
Customize your environment
Pre-installation
Language and keymap
Change your keyboard layout
[root@archiso] loadkeys /usr/share/kbd/keymaps/…
Edit the locale
[root@archiso] nano /etc/locale.gen
[root@archiso] locale-gen
Partition disks
[root@archiso] fdisk -l
[root@archiso] cfdisk /dev/sda
[root@archiso] mkswap /dev/sda1
[root@archiso] mkfs.ext4 /dev/sda2
[root@archiso] mkfs.ext4 /dev/sda3

Mount disk
[root@archiso] swapon /dev/sda1
[root@archiso] mount /dev/sda2 /mnt
[root@archiso] mkdir /mnt/home
[root@archiso] mount /dev/sda3 /mnt/home
Ethernet and wireless connection
[config sample] /etc/netctl/examples/
[config folder] /etc/netctl/

[root@archiso] ip link set wlan0 down
[root@archiso] netctl start wlan0-ssid
[root@archiso] wifi-menu

Your are ready to install the base system now.

Installation
Download and install the base system
[root@archiso] pacstrap -i /mnt base base-devel sudo
[root@archiso] genfstab -U /mnt >> /mnt/etc/fstab
Enter root and create a password
[root@archiso] arch-chroot /mnt
Set locales
[sh-4] nano /etc/locale.gen
[sh-4] locale-gen
[sh-4] echo LANG=fr_BE.UTF-8 > /etc/locale.conf
[sh-4] export LANG=fr_BE.UTF-8
Set your timezone
[sh-4] cd /usr/share/zoneinfo/Europe/...
[sh-4] ln -sf /usr/share/zoneinfo/Europe/… /etc/localtime
hwclock --systohc --utc

[sh-4] mkinitcpio -p linux

Install boot loader
[sh-4] pacman -s grub-bios
[sh-4] grub-install --recheck /dev/[DISK]
[sh-4] grub-mkconfig -o /boot/grub/grub.cfg

Set hostname and configure ethernet and wireless connection
$ sudo systemctl start dhcpcd@eth0.service
$ sudo systemctl enable dhcpcd@eth0.service
Set hostname
[sh-4] echo [HOSTNAME] > /etc/hostname
Unmount disk and reboot
[sh-4] passwd
[sh-4] exit
[root@archiso] umount -R /mnt
[root@archiso] reboot

Package manager
Edit pacman conf. Core extra and community repo must be uncommented.
[sh-4] nano /etc/pacman.conf
Create root password, users
useradd -m -G USERGROUP USERNAME
Improve bash
Edit .bashrc
autocomplete
complete -cf sudo
complete -cf man
Configure Network
fplug for laptop

Optimize Pacman
Update pacman mirrors list and install yaourt to use the AUR repository
Mirrors
Optimize mirrors
pacman-optimize

Edit mirror list
sudo cp -vf /etc/pacman.d/mirrorlist /etc/pacman.d/mirrorlist.bak
sudo nano /etc/pacman.d/mirrorlist

Rank mirrors
sudo rankmirrors /etc/pacman.d/mirrorlist

Reflector
sudo pacman -S reflector
sudo reflector --verbose -l 10 -p http --sort rate --save /etc/pacman.d/mirrorlist

Update pacman
[user@host] sudo pacman -Syy sudo pacman -Syu
Arch User Repository
Create builds directory in home
mkdir ~/builds

Go into builds directory in home
cd builds
Install Yaourt
Create acces to the AUR (Arch User Repository)
Download package
Build package

Test yaourt
Search and install Archey
sudo yaourt -Ss archey
sudo yaourt -S archey

Install Pacaur
sudo yaourt -S pacaur
Install packages
Wget
Curl
Git
Ranger
Zsh
Vim
Ssh
Mysql

Install GUI
Edit .bashrc
export EDITOR=”nano”
archey
Install video driver
lspci | grep VGA
Install display-server
xorg-server xorg-xinint -xorg-server-utils
Xinitrc
Login Manager
Desktop environment
Awesome Window Manager
Install awesome and dependepencies
Add awesome to xinitrc
exec awesome
Donwload themes

sudo cp -r /usr/share/awesome/themes/\* ~/.config/awesome/themes/

Edit awesome
sudo nano ~/.config/awesome/rc.lua

Start X

Install more
Bash
Tmux
Text editor
Sublime text
sudo pacaur -S gnome-terminal sublime-text
File Manager
Thunar
Image Viewer
Audio Player
Video player
Web browser

References

Customize your environment
Awesome WM libraries and widgets
Vicious
Beautiful
http://awesome.naquadah.org/wiki/widgets

gksu

## References

https://www.youtube.com/playlist?list=PLj97-HQdMXyZSvMD1xRTqPEeh4nSA6dpC
