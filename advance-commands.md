🐧 Linux Advanced Commands (System, Users, Permissions, Transfer)

1. System-Level Commands

uname: Displays system information (kernel, OS, architecture).
uname -a

uptime: Shows how long the system has been running.
uptime

date: Displays current system date and time.
date

who: Shows logged-in users.
who

whoami: Displays current user.
whoami

which: Shows location of a command.
which python

id: Displays user ID (UID), group ID (GID).
id

sudo: Executes command with admin privileges.
sudo command

shutdown: Shuts down the system.
sudo shutdown

reboot: Restarts the system.
sudo reboot


apt (Ubuntu/Debian): Package management for Ubuntu.
sudo apt update
sudo apt install nginx



yum (RHEL/CentOS): Package manager (older systems).
sudo yum install nginx



dnf: Modern package manager (Fedora).
sudo dnf install nginx



pacman: Package manager for Arch Linux.
sudo pacman -S nginx



portage: Package manager for Gentoo.
emerge nginx



2. User & Group Management
   
useradd: Creates a new user
sudo useradd username


whoami: Displays current user.
whoami


su: Switch user.
su username


passwd: Set/change password.
sudo passwd username


userdel: Deletes a user.
sudo userdel username


groupadd: Creates a group.
sudo groupadd groupname


gpasswd: Adds user to group.
sudo gpasswd -a username groupname


groupdel: Deletes a group.
sudo groupdel groupname


3. File Permission Commands

umask: Displays default permission settings.
umask


ls -l: Shows file permissions.
ls -l


chmod: Changes file permissions.
chmod 755 file.sh


chown: Changes file ownership.
sudo chown user:group file.txt


chgrp: Changes group ownership.
chgrp group file.txt



4. Compression Commands

gzip: Compresses file.
gzip file.txt


gunzip: Decompresses file.
gunzip file.txt.gz


zip: Creates zip archive.
zip archive.zip file.txt


tar: Creates tar archive.
tar -cvzf archive.tar file.txt


untar: Extracts tar archive.
tar -xvzf archive.tar


5. File Transfer Commands
scp: Copies file to remote server via SSH.
scp file.txt user@host:/path


rsync: Efficient file transfer with synchronization.
rsync -av file.txt user@host:/path
