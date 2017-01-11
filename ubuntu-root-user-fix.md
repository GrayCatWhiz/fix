#								[UBUNTU 16.10 Yakkety] 

		How to unlock root on ubuntu
	1. Change root password by executing command: 
	sudo passwd root
	(Enter new root password: )
	(Re-enter new root password: )

	2. Unlock the root user by executing command:
	(sudo) usermod -U root

	3. Edit "/usr/share/lightdm/50-ubuntu.conf" and add the following:
	greeter-show-manual-login=true

 ----------------------------------------------------

		How to fix error after unlocking root user
	1. Add the following line of codes on .profile
	(you should edit ./profile by executing  `nano ./profile` command)

	if `tty -s`; then
	mesg n
	fi
	
	NOTE: You should enable "show hidden items on your nautilus"
 ----------------------------------------------------

		How to fix sound issue after unlocking root user
		
	1. Open "Startup Application" on dash.
	2. Click add.
	3. Add "/usr/bin/pulseaudio" to command.
	4. Add Title and Description onto it.
	5. Save.
	
------------------------------------------------------	
