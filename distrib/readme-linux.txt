URDU QWERTY KEYBOARD LAYOUT FOR LINUX

To activate this keyboard, you have to
 
i) add some files from here into the directory 'xkb' in your system, 
ii) execute a compile command, and then 
iii) change some system settings on your machine so that your typed 
input can make use of the new keyboard layout.
 
These actions require superuser priviliges to execute 'su' or
'sudo' command.

The steps needed to install and use Urdu QWERTY keyboard layout are 
the following:

1. Download the file UrduQWERTY-v6linux.zip and unzip it into some 
local directory, e.g. 'UrduQWERTY-v6linux'. 

2. Find the path to 'xkb' in your system. 
The standard path is '/usr/share/X11/xkb'. 
In case it is different in your distribution, you can determine this 
path by executing the 'find' command, as follows:
	find / -name xkb -print
The example commands below assume the path '/usr/share/X11/xkb'.

3. Become a superuser, by executing the command 
	su
It would require you to type in the root password.

4. Backup the four files that are going to be replaced.
	cd /usr/share/X11/xkb/symbols
	mv pk pk.bak
	cd ../rules
	mv base.lst base.lst.bak
	mv evdev.xml evdev.xml.bak
	mv xorg.lst xorg.lst.bak

5. Place the four new files in the system. The example commands below 
assume that the files have been downloaded into a directory called 
'UrduQWERTYlinux' and the path to 'xkb' is '/usr/share/X11/xkb'.
	cd UrduQWERTY-v6linux/symbols
	cp pk /usr/share/X11/xkb/symbols/
	cd ../rules
	cp base.lst evdev.xml xorgs.lst /usr/share/X11/xkb/rules/

6. Execute the following command to compile the changed keyboard 
information into the system:
	setxkbmap -layout pk -variant urd-qwerty -print | xkbcomp -
   (For this command to work, you might need to be in an Xterm
    shell window rather than a regular command window.)

7. Logout and login again (or restart the machine) for the above 
changes to take effect.

8. To make use of the UrduQWERTY keyboard layout in your input, you 
have to change some system settings. Depending on your Linux 
distribution (e.g., Debian, Fedora, OpenSuSE, Ubuntu) and your desktop
environment (e.g., Gnome, KDE, Mate), this might require typing special 
commands or, more conveniently, working with 'System Settings, 
'Control Panel', etc. The following example is for OpenSUSE with KDE.

A. From the 'Application Launcher', start 'Configure Desktop'. 
From the 'Hardware' section, select 'Input Devices'. It will display 
the 'Keyboard - System Settings' panel. 

B. In the lower pane 'Configure Layouts', click on the 'Add' button, 
and from the choices displayed, select Map 'pk', 
Layout 'Urdu (Pakistan)', Variant 'Urdu (Win-Mac-Linux QWERTY)'.

C. Click on the 'Layouts' tab. In the 'Layout indicator', select 
'Show layout indicator' and 'Show flag'. In 'Switching Policy', 
select 'Global'. In 'Shortcuts for Switching Layout', 
select 'Alt+Shift' for 'Main shortcuts'. 
(This --- to get you started --- is just one set of suitable choices 
among several alternatives:)

D. Click on 'Apply'.

