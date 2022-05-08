# What to do after a fresh linux install

Privilège 2
Upgrade & Update 2
Create User & Groups 2
Install Applications 2
Create Aliases 3
Application 3
Files 3
Commands 3
Logs 3
Configuration and Resources 4

Privilège
su -

apt-get install sudo -y

usermod -aG sudo $USER

Check sudoers file
Visudo

# Allow members of group sudo to execute any command

%sudo ALL=(ALL:ALL) ALL
You need to relogin or reboot device completely for changes to take effect

Upgrade & Update

Keyboard Layout

sudo dpkg-reconfigure keyboard-configuration
Create User & Groups

adduser sammy

groups sammy

Install Applications

Git
Curl

Ranger
Tmux
Htop
Vim

Zsh
Oh my zsh
https://github.com/robbyrussell/oh-my-zsh
Reload the bash
Create Aliases
edit zsh
update/upgrade/dist upgrade/install package
pupdate / pupgrade / pdupgrade / pinstall

Application

Ranger
http://ranger.carina.uberspace.de/qa/723/how-to-open-a-selected-file-in-root-privillege

Tail
Files

OS release
Ubuntu /etc/lsb-release

Commands

OS release uname -a

Restart
http://www.binarytides.com/linux-command-shutdown-reboot-restart-system/

Quit ctrl+c
Clean screen ctrl+l
Show IP ip addr show
Logs

https://help.ubuntu.com/community/LinuxLogFiles
http://www.cyberciti.biz/faq/linux-log-files-location-and-how-do-i-view-logs-files/

Configuration and Resources
