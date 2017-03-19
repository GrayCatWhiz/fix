-----------------------------------------------
	[TROUBLESHOOT]
-----------------------------------------------		

# Check GPU VRAM

command:  `dmesg | grep drm`

# Check GPU information

command: `lshw -C Video`

# Check 3D Acceleration

command: `/usr/lib/nux/unity_support_test -p`
		    `glxinfo | grep direct`
		    `glxgears`
		    
# Netbeans Errors

locate: /usr/local/netbean-XX/etc/netbeans.conf "Where xx is the Netbeans version "
command: `netbeans_jdkhome=/usr/lib/jvm/java-8-oracle`

# Chromium cannot run as root

Edit file /etc/chromium-browser/default

Add line CHROMIUM_FLAGS=" --user-data-dir"

# Clean Uninstall Application

command: apt-get autoremove, apt-get remove apt autoremove, apt remove, apt autoremove purge [application name]-data

# Run VLC as Root

command: `sed -i 's/geteuid/getppid/' /usr/bin/vlc`

# No Mechanize on Python

apt-get install python-mechanize
		    
# Run Steam as Root

after updating it.
edit bin_steam.sh - this is the binary launcher of steam

comment : # Don't allow running as root
if [ "$(id -u)" == "0" ]; then
	show_message --error $"Cannot run as root user"
	exit 1
fi

or change "0" to 1

# Check PHP error

`tail -f /var/log/apache2/error.log`

or

`php -l <filename.php>`

# Fix Virtualbox Error for kernel module issue (dkms) and modprobe vboxdrv

apt-get install virtualbox ; from repository of ubuntu and not on vbox site does not include virtualbox-dkms and other vbox essentials

disable secureboot on your computer if you were running UEFI.

---------------------------------------------
	[INSTALL SECTION]
---------------------------------------------

# GIMP Image Manipulator

command: apt-get install gimp

# Steam

command: apt-get install steam

# Apache Web Server

apt-get install apache2

# PHP (Hypertext Preprocessor)

apt-get install php

# Mysql GUI (Mysql Workbench)

apt-get install mysql-workbench

# Arc theme Linux

apt-get install arc-theme

# MYSQL Database and Web 

apt-get install mysql-server
apt-get install apache2
apt-get install php7 or php7.0-cli
apt-get install php-mysql // For mysqli extensions

# Programmers Stuffs

Java JDK 8 PPA
GIMP
Android Studio PPA
Sublime-text 3 PPA with Material Theme
Brackets PPA
Netbeans.sh
MysqlWorkbench
Steam

./[compilation of errors: -> compiled by GrayCat]
	
