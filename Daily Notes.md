# Linux with Python Integration

## Summary for 10-Feb-2020

## Summary for 11-Feb-2020
we discussed today about installing Oracle virtual box and Red had operating system
various commands like, watch, bash, ^C, ^Z, fg, bg, jobs, echo with various form of string and commands, echo with arguments like, -n, -e, simple while loop

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
