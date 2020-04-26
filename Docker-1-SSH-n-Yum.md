# 1. SSH & Yum
```
To install the OpenSSH client:

Run the following command to install the OpenSSH client on your computer: sudo apt-get install openssh-client
Type in your superuser password when asked.
Hit Enter to complete the installation.
You are now able to SSH into any machine with the server-side application on it, provided that you have the necessary privileges to gain access, as well as the hostname or IP address.


Configuring yum:
Create a new repo file in the following folder:
/etc/yum.repos.d/

# gedit myrepo.repo
==================================================================
[dvd1]
baseurl=file:///run/media/root/RHEL-8-0-0-BaseOS-x86_64/AppStream
gpgcheck=0
==================================================================
[dvd1]
This is an unique name of the path

file://
This is to mention that the software is locally available

gpgcheck=0
This is to disable the check that whether this software belongs to Oracle or any other vendor.
This also help us to be safe from hackers.

After creating a report check or validate with following command:
# yum repolist

if you have numbers understatus column, it means yum is properly installed as there are items to be  installed in the mentioned repository. Else check the path, symbol in repo file.


Now check if firefox is installed
# rpm -q firefox
firefox-60.5.1-1.el8.x86_64

Now uninstall firefox
# rpm -e firefox

Again check if firefox is available
# rpm -q firefox
package firefox is not installed

Now we don't have to go to the dvd. Just  following command to check the new compatible version and install it.
# yum install firefox

Now check if firefox is installed
# rpm -q firefox
firefox-60.5.1-1.el8.x86_64

Check if python2 software is installed
# rpm -qa | grep python2

You can also check / confirm which repo contains python2 command:
# yum list python2

If not you can install it with following command
# yum install python2
Note that if  you use rpm command, it will fail as there might be some dependency.	


Still there are lots of issue with yum command, hence, we use dnf which is more advanced and supports all the yum commands.
User dnf from Redhat8 onwards, before that use yum.

to check available repo list:
# yum repolist
# dnf repolist

E.g. if yum doesn't file any repo link, on ^C it takes time to close the command, but dnf immediately closes it.

additional examples:
# yum remove firefox
yum command will first remove dependencies then firefox which rpm command will not.
you can also use dnf here.

dnf is more powerfull
# dnf install firefox
enter y, if asked.

Get online yum repo:
https://download1rpmfusion.org/free/el/rpmfusion-free-release-8.noarch.rpm
https://dl.fedoraproject.org/pub/repl/epel-release-latest-8.noarch.rpm

wget command: We can download any file from any url.

# wget https://dl.fedoraproject.org/pub/repl/epel-release-latest-8.noarch.rpm

Now you can install it using rpm command as this is a single program and no dependency.
# rpm -i epel-release-latest-8.noarch.rpm

this is two-step right?
you can install in one command also:
# dnf install https://dl.fedoraproject.org/pub/repl/epel-release-latest-8.noarch.rpm

another url:
#dnf install https://download1.rpmfusion.org/free/el/rpmfusion-free-release-8.noarch.rpm

this downloads the file and automatically configures yum.repos.d and creates new repo files

Web source Link: https://linuxconfig.org/how-to-install-vlc-player-on-centos-8-rhel-8-linux

if vlc player not available in above link, refer fusion link: https://download1.rpmfusion.org/free/el/

https://download1.rpmfusion.org/free/el/rpmfusion-free-release-8.noarch.rpm

this downloads the file and automatically configures yum.repos.d and creates new repo files

Note that  VLC is not supposed to be run as  root.
Hence, create a new user account.
# useradd John
# passwd John

List out all the user details which is saved in passwd file:
# cat /etc/passwd

list user names only
# cat /etc/passwd | cut -d: -f1
OR
# awk -F':' '{ print $1}' /etc/passwd

We can use pagers such as more/less command as follows to view /etc/passwd file

# more /etc/passwd
# less /etc/passwd

# tail -5 /etc/passwd
# head -5 /etc/passwd	

Ideally we cannot install docker-c (community version) in Redhat  8, however we have a trick for  this.
-----------------------------------------
Session 18: dated 12-Mar-2020:

Client Side software:
---------------------
note that ssh is by default installed in Redhat OS.

to check which file contains software "openssh-clients":
# rpm -q openssh-clients
openssh-clients-7.8p1-4.el8.x86_64

to check where ssh command is located:
# which ssh
/usr/bin/ssh

to check the installation file
# rpm -qf /usr/bin/ssh
openssh-clients-7.8p1-4.el8.x86_64

'ssh' to login to another machine:
# ssh -l root 172.20.10.11

Session20: Linux Networking Core:
How to change the port number of openssh-server
step 1: view the file
# rpm -q openssh-server
openssh-server-7.8p1-4.el18.x86_64

step 2: edit the file sshd_config
# vim /etc/ss
ssh/ ssl/ sssd/
# vim /etc/ssh/sshd_config

uncomment and update the needed port number.
Note before that check if anyother  program is using that new port number:
#netstat -tnlp | grep 26
#netstat -tnlp | grep 27

Note to restart the service / program / daemon
# systemctl restart sshd
It may fail. check log by command:
# journalctl -xe

Validation/check if you can access this  server from client side:
1. ping
# ping 172.20.10.13
Yes, this is working

2. try to log in with root login
# ssh -l root 172.20.10.13
ssh: connect to host 172.20.10.13 port 22: Connection refused
It failed because client doesn't know port number changed.
Here you have to inform the client and provide port number with command:
# ssh -l root -p 27 172.20.10.13
This works.
------------------------------------
Running the output at server side:
# date > /dev/pts/2

# date > /dev/tty4

Running client side graphical program at client side:
# ssh -l root -X 172.20.10.13 firefox
This will open the firefox application on client machine but application from server.

# check  how many consoles you have and accessing:
example1:
# tty

exaple2:
# w
This command shows details of how many users are logged in and from where they are logged in.

Note:
1. All tty starting with : is for graphical ui
2. All tty starting with tty is for cli
3. All tty with From (ip address) is for external login.

Check for  :1 TTY  and set it to DISPLAY variable, for example:
# DISPLAY=:1

This will run the graphical program on that window.

If you want the graphical program to run to the another program, export it:
# export DISPLAY=:1
We have to enable the xhost.
# xhost +
No SELinux imapct.


set the terminal font color to red
# tput setaf 1  => Red
# tput setaf 0  => Black
```
