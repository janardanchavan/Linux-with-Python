# Linux with Python Integration

IIEC RISE ID: RISE2020_71_6_1

## Summary for 10-Feb-2020

## Summary for 11-Feb-2020
we discussed today about installing Oracle virtual box and Red had operating system
various commands like, watch, bash, ^C, ^Z, fg, bg, jobs, echo with various form of string and commands, echo with arguments like, -n, -e, simple while loop

#### Installing Redhat 8

  1. Make sure you have Oracle VM Virtual Box installed
  2. Open Oracle VM Virtual Box installed
  3. Click 'New' button to create new vm machine
  4. Name and Operating System: Provide following details for new virtual Machine <br/>
    - Name : Redhat 8 <br/>
    - Type : Linux <br/>
    - Version : Red Hat (64-bit) <br/>
    If you are not able to select 64-bit version, you need to Enable Virtualization through your laptop's BIOS setting. <br/>
    - Restart your laptop <br/>
    - On restart, press F2/F10 to enter the BIOS <br/>
    - Enable Virtualization <br/>
    - Press F10 to save the changes and exit BIOS
  
  5. Memory Size: Enter 2048 i.e. 2 GB Ram
  6. Hard Disk: Create a Virtual Hard Disk now
  7. Hard Disk File Type: VDI (Virtualbox Disk Image)
  8. Storage on Physical Hard Disk: Dynamically Allocated
  9. File Location and size: 100 GB
  10. Click Create button. Your Virtual Machine / Hardware (RAM/CPU/Harddisk) is up now.

  11. Right Click the VM name and select Settings
  12. Select Storage
  13. At the right side, click the CD icon in front of Optical Drive drop down.
  14. Click Choose Virtual Optical Disk file
  15. Select the Redhat 8 iso file whereever it is downloaded and click OK.

    Now we can start installing OS

  16. Select the VM machine
  17. Click Start button on the top. It will power on you operating syste and start installing Red hat.
  18. On the blank screen, using arrow key select the first option:
      Install Red Hat Enterprise Linux 8.0.0
  19. After installation it will ask few settings:
    - Language: English(United states)
    - Installation Destination (Partition): Select it and click Done
    - Network & Host Name: Open  it and click On against "Ethernet (enp0s3), click Done
    - Software Selection: Select Workstation and click Done
    - Time & Date: As per your country, change the time zone. Click Done
  20. Click Begin Installation
  
    This will take some time.
  
  21. After installation it will ask you to enter <br/>
    - root user password and confirm
    - new user creation
  22. After entering the details continue the installation process. <br/>
     This will create user
  22. Reboot your machine
  
  Note that it will again start the installation, rather power off the machine.
  
  23. On Oracle VM VirtualBox Manager, right click the machine and select Settings.
  24. Move the "Hard Disk" option up at the top so that the installed OS will start next time when you restart the machine.
  
  Thank you.

## Summary for 12-Feb-2020

## Summary for 13-Feb-2020
gnome: how to find all the commands used by a particular program. Simple for loop, and other commands like: ps, kill, mkdir, cd, ls, gedit, cat, touch, REPL, etc.

## Summary for Feb 14, 2020
Commands - useradd, passwd, id, user, whoami, startx, tty, chvt, exit, logout, echo, echo with $, clear, reset, touch, 
cat and > i.e. creating file without any command. Multiple consoles, Shortcut (CTRL+ALT+F1/F2/F3/F4/F5/F6) to switch between consoles, 
shell is required to run any program, creating your own shell is possible, GUI/CLI/WebUI/MobileApp.
-	updated

## Summary for Feb 17, 2020
CAT Command, python data types, slicing strings, jumping indexes, reversing string, escape sequence for new line, tab, etc., interpolation, checking string in string, tuple, list, running python without installation using web site repl.IT.

## Summary for Feb 18, 2020
List and nested lists, I/O redirection & Piping, CAT redirects result to -> Terminal, whatsapp, mail, printer, sms, etc. ‘>’ is output redirection symbol, ‘<’ is input redirection symbol, ‘>>’ is an append symbol, use case of cat command, additional commands, tty, date >, tr ‘a-z’ ‘A-Z’, rm .etc/passwd.lock (to remove unexpected lock)

## Summary for Feb 19, 2020
Linux OS - Package Management, 
Additional Commands:
rpm –q vlc
rpm -1 –a | grep python
which date
rpm –q –f /usr/bin/date
which python3
rpm –q –f /usr/bin/python3 
rpm –e firefox (uninstalling software)
rpm –q fireforx (nothing finds as software is uninstalled)

Attach the ISO file to access firefox installation package
If menu not visible press right CTRL+C to activate top menu

Then iso image can be shown as a dvd in redhat.
Package can be  available in AppStream or BaseOS folder.

Open terminal in that folder.
To  list rpm file name type -> ls fire <<tab, tab>> - this lists all the files starting with fire word
(press tab  once if you have only one file starting with given  word)

For installation: rpm –I firefox-60.5.1-1.e18.x86_64.rpm
Check file with below command: rpm –q firefox

Use –i option for additional information while installation
Use -v option for verbose mode while installation
Use –h option to see the installation progress while installation
Use -l for long list, eg. ls -l vimal.txt (for long list)
command name, more options with or without hyphen (option/field/switch), argument(s)

man rpm - to  check the manual  for  the given command

additional details about the software can be viewed using –i command like:
rpm –q –i firefox
rpm –q –I coreutils

Not all the command's source code is available.

multiple options can be given with single hyphen as well.
rpm –q i coreutils

EOG to  open image in terminal. image can be  replaced with our phone but with same name.
Commands from q&a section : Dig, ping, where, which, etc.

## Summary for Feb 20, 2020
Printing column from List is Not Possible...
- type(name)
- array(name) <br/>
+ import numpy <br/>
'Error:' No module named 'numpy'

module comes from library and it is not installed
- pip3 list - to list out all the libraries installed in python
- pip3 install numpy - to install numpy library

- import numpy - to import the numpy module (please restart the python program)
- a = numpy.array(name)
- print(a)
- a[0:2] 	- print first and second rows
- a[:2, 1]	- print first 2 rows and second column
- a[:]	- print entire  array
- a[:, 1]	- print all rows and second column

How can we prove that the output given by date or cal is the right output.
For this  we need exit code which is in shell variable (?)
- echo $?

xyz 1> f1.txt
There are  two channels 1 and 2 to redirect the output. 1 goes to the standard output i.e. console and can be redirected to file.
And second if error occurs then it goes to standard output.
If we combine both the channels - errors can be also send to the file.

Question: when we write following command, where the output is send? How can  we send the output  of cmd 
xyz 2> f1.txt
it will go to the screen as no command exist.

5 switches available - 1>, 1>>, <, 2>, 2>>

0 - STDIN <BR/>
1 - STDOUT <BR/>
2 - STDERR

## Summary for Feb 21, 2020 : Holiday
## Summary for Feb 24, 2020
Announcement of Docker training for professionals
Commands run:
- tr 'a-z' 'a-z'

piping explained:
- DATE | tr 'a-z' 'A-Z'

- rpm -m

-gedit f.txt
- cat f.txt

- wc f.txt
- wc < f.txt

- wc 
.................
... ...... .... ....
... .. .. ..... ........... ... (left control)^D

Que: How OS come to know where my file starts and where my file ends
Ans: EOF

- wc -w f.txt
- wc -c f.txt
- wc -l f.txt

- rpm -qa | wc -l

- vim f1.txt
- cat f1.txt

- grep linux f1.txt
- rpm -qa | grep python
- rpm -qa | grep python | wc -l

Small into to mapReduce

- ls
- ls -l

- unalias ls (remove colors for now)
- ls
- ls -f
- ls -l
- ls -l | grep d
- ls -l | grep ^d
- ls -l | grep ^d | we ^l
- ls -l | grep -n ^d (show line number using -n)
- grep -n linux f1.txt
- grep -v linux f1.txt
- grep -n -v linux file.txt

tee
- date | tee
- date | tee fz.txt

## Summary for Feb 25, 2020
Networking concept
Accessing another machine (cli/gui) from another laptop/desktop/mobile
running commands from another machine on different machine

Running commands on localhost and remote host

In Networking world, all the processes are know as protocol.

creating your own protocol.
every task, usage there is a protocol, accessing file on ftp, send email, etc.
rsh, telnet, very secured one is ssh (secured shell).

For networking purpose, below three things are required:
1. A and B should be physically connected (wired or wireless)
2. both the system should have ip address
3. Ping to each other

start mobile hotspot and connect through laptop.
in vm enable bridging adapter.
In VM:
	 ifconfig will show you network card in vm
	on the  top of vm machine, click devices option.
	go to network -> network  settings
		Network  option, changed attached to Bridged Adapter.

	reboot vm machine,
	then ifconfig command will show the ip address.
	to check ip address of your mobile phone from vm machine, run command : route -n

	then you can ping this ip address to check  connectivity with mobile phone.

configuring your system as a web server.

Need ssh app for  android, eg. JuiceSSH, Termius
need to provide following things to the ssh app:
1. ip address of remote host 
2. User Name
3. password

- ifconfig enp0s3
- killall firefox

Que: How to start any gui based command from local host to remote host?
Ans:
$ ssh tim
$ export DISPLAY=:0 (or whatever the remote display is numbered as)
$ firefox

## Summary for Feb 26, 2020
Need to purchase wireless access point (hub)
Other solution: use your mobile phone; enable hotspot (wireless access point)
Use only one mobile phone to connect all the machines.

We can clone the red hat operating system 
-	First power off then only clone,
-	Also check the “Reinitialize the MAC address of all network cards” checkbox while cloning.
-	Full Clone
o	In Order to remove OS, right click and select ‘remove’

On both the VMs, NIC card, put it on host only mode. This is called as Virtual Wire.
No access to Internet.

Hence put it on Bridged Adapter mode. This way can ping each other and can access internet but require outside wireless Hub / Hotspot (DHCP)

Ifconfig enp0s3 – to check all network card details (if not working enable wireless connectivity on vm machine)
To run date command on 162 machine run following command from 124 machine:
-	ssh 192.168.0.162 date (provide password of root account of 162 machine)

creating a folder on our machine:
-	mkdir zz

creating a directory on another vm machine:
-	ssh 192.168.0.162 mkdir zz11111

This way we have crated our own N/W / Lab / LAN

1.	RAM + CPU = compute unit
2.	Storage Unit
3.	 

Create a file on 124 machine.
Gedit my.py
Cat my.py
Python3 my.py
ssh 192.168.0.162 python3 my.py (will generate an error as my.py file does not exist on 162 machine.

Transfer / upload of the file is require, this can be done using scp as below:
<<< NEVER SHARE YOUR PASSWORD >>>

-	Pwd
Copying file:
-	scp my.py 192.168.0.162:/root (enter root password of 162 machine)
Running program:
-	ssh 192.168.0.162 python3 /root/my.py
Copying file from another machine to current machine:
-	scp 192.168.0.162:/root/z1234.txt /root/

-	touch a b c (creating all three files together)
How to login into other’s facebook or linkedIn account without using password.

ssh with –X – if we need to run gui in the remote machine.

MOSS protocol – not part of this training.

## Red Hat & Python: Summary for Mar 02, 2020: 

Server-Client concept
Server -> who gives the service / server can give or deny the service.
Client -> who takes the service / client is the one who goes to the server.

- pwd

If ssh access has been given to anyone, they can do anything on your machine.
ssh 192.168.0.162 cat /root/vimal.html

Creating and configuring a server both are different things.
Today we will see configuring a server: (This is without ssh)

For different server, we have different protocols <br/>
3-Steps Process:
1.	Install software (for us using rpm)
2.	Setup (look and feel)
3.	Execute

HTTPD (Apache) – Apache Webserver: (Configuring Apache webserver)

This is web hosting in other words.

-	Ifconfig enp0s3
-	Check : rpm –q httpd
-	Dnf install httpd
-	Check: dnf list httpd
-	pwd
-	cd var/www/html/
-	ls

copy / webhosting / deploy - all these terms are same.

To start web services:
-	Systemctl start httpd

Web server -> web client

Two steps at client side:
1.	Software called client side software e.g. browser
2.	Connectivity
3.	IP address of server
4.	Three things (which comprise the URL)
a.	How client wants to connect / protocol
b.	Where i.e. ip address
c.	Page name

Network packets / traffic : rhcl firewall is not allowing to access any folder:
Let us temporary disable firewall. Note that this is not a best practice.
-	systemctl stop firewalld

The place where we save our file, is called as documentRoot

## Red Hat & Python: Summary for Mar 03, 2020: 

## Red Hat & Python: Summary for 05-Mar-2020: 

-	systemctl status httpd (d stands for  daemon)

Service failed because: SELinux security was prohibiting the out of range port number

SELinux is a one of linux security.

SELinux alter:
Check current status:
-	getenforce <BR/>
Enforcing
-	setenforce 0 <BR/>
Permissive
-	setenforce 1 <BR/>
Enforcing

Nmap is a scanning tool to scan open ip addresses.
-	Yum install nmap
-	nmap -sP 192.168.0.162
-	nmap -sT 192.168.0.162
-	nmap -sT 1111 192.168.0.162

Check port

-	nmap -sT p 1111 192.168.0.162

Webserver can read from vimal folder not from html folder.
Priority goes to latest included files: 

Same way yum.conf is original file and not yum.repos.d:

Default directory index: 

Que: How to change the  document folder.

Firewall security -> network level <BR/>
SELinux security -> File system and processes

## Red Hat & Python: Summary for Mar 20, 2020: 
IIEC RISE ID: RISE2020_71_6_1
- Conditional statements
- checking if applicant have greater than 2 years of experience or not
- indentation required for any block related codes
- comparing values
- type casting variables
- Nested if statements
- additional topics on project

if exp <= 2:
	print("Hi")
else:
	print("Bye")

- Nested if statements
- useradd pop1 - command to create a new user
- id pop1 - check if pop1 user is available
- 

Some examples as 

>>> x = 5
>>> y = 10
>>> print("this is {}".format(x))
this is 5
>>> print("this is {} and {}".format(x,y))
this is 5 and 10
>>> print("this is {1} and {0}".format(x,y))
this is 10 and 5
>>> 

## Redhat & Python Summary for Mar 23, 2020:
Project Work:
- take user input to capture value for local or remote location to be run the command
- conditional statements for checking if user wants to run the command on local machine or remote machine based on user input value
- running dates and creating users on local as well as remote machine

Tasks: 
1. Check if the connectivity to the ip is valid or not?
2. If remote machine is required, then username and pass should not be asked again and again i.e. ask once only and refer it further.

```
print("Where you would like to perform your job (local/remote) : ", end"")
location = input()

if location == "remote"
	remoteIP = input("Enter ur IP : ")

print("""Press 1: to see date
Press 2: to check  cal
Press 3: conf we server
Press 4: to create user
Press 5: create file
Press 6: to setup n/w
Press 7: to exit
""")

Print("Enter your choice : ", end="")
ch=input()
print(ch)

if location == "local":
	if int(ch) == 1:
		os.system("date")
	elif int(ch) == 2:
		os.system("cal")
	elif int(ch) == 3:
		os.system("yum install httpd")
	elif int(ch) == 4:
		print("Please enter user name : ", end="")
		create_user = input()
		os.system("useradd {}".format(create_user))
	elif int(ch) == 5:
		os.system("date")
	elif int(ch) == 6:
		os.system("date")
	elif int(ch) == 7:
		os.system("date")
	else:
		print("Option not supported.")
else:
	print("location doesn't support")
```
use "vim python.py" command to edit file as it gives proper colors. <br/>
use "id tom1" command to check if tom1 user exist. <br/>

remote input? <br/>
socket programming? <br/>
sub-process? <br/>
past wd - using standard input. <br/>
kickstart - way to install unix system automatically.
## Redhat & Python Summary for Mar 24, 2020:
Holiday
## Redhat & Python Summary for Mar 25, 2020:
Project Work:
- While loop
- While loop vs if statement
- While with a condition
- While with True
- Exiting the programm with True and Exit()
- Indentation with while loop, best practice to use spaces.
- Repeating menu to avoid running program again and again un-necessarily.

## Summary for 26-Mar-2020:
Preparation for coming 2-day workshop:
- On VM Machine, create a new machine with existing Hard Disk with preinstalled Redhat 7 OS and other necessary environment.
- Connect your local machine's web cam to RHEL 7
- Devices => WebCam => (By Default WebCam option is not available, to enable WebCam option, use  extension provided, Oracle_VM_,
- Install this extension in Oracle VM Machine, File, preferences, extensions, Add)

## 30-Mar-2020:
Announcement by Preeti about MLOPs internship.


## Redhat & Python Summary for 31-Mar-2020:
#### 1st topic:  create a login and password.

    vim menu.py

before where to run

    passwd = input("Enter ur password: ")

    apass = "lw"
	if passwd != apass:
    print("Auth incorrect")
        exit()
    else
        your code

#### 2nd topic: stop echo back.

Due to 'echo back', character is displayed on the screen
telnet	X
http	X

use getpass() for entering password as it takes the input but doesn't echo back.
        import getpass

	x = getpass.getpass()

	x = getpass.getpass("Enter your string: ")

store password in : database,

compile program and convert into binary.

#### 3rd topic: Avoid typing password for ssh agian and again:
lots of way for authentication:
- password based authentication
- key based authentication (private key)

ssh-keygen command -  to gerate public/private rsa key pair.

command to be typed on A machine from where we are running command for another machine

This is a public key and password-less authentication.

To login to machine B:
- ssh-copy-id root@192.168.0.106

first time you have to type password, later on it is not required.

To check private key:
- cat /root/.ssh/id_rsa
