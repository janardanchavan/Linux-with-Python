IIEC RISE ID: RISE2020_71_6_1
## Redhat & Python Summary for 31-Mar-2020:
#### 1st topic:  create a login and password.
IIEC RISE ID: RISE2020_71_6_1
Redhat & Python Summary for 23-Mar-2020:
Project Work:
- take user input to capture value for local or remote location to be run the command
- conditional statements for checking if user wants to run the command on local machine or remote machine based on user input value
- running dates and creating users on local as well as remote machine

Tasks: 
1. Check if the connectivity to the ip is valid or not?
2. If remote machine is required, then username and pass should not be asked again and again i.e. ask once only and refer it further.
--------------------------------------------------------
What is data center?



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



use "vim python.py" command to edit file as it gives proper colors.
use "id tom1" command to check if tom1 user exist.

remote input?
socket programming?
sub-process?
past wd - using standard input.
kickstart - way to install unix system automatically.


Redhat & Python Summary for 24-Mar-2020:
Holiday

IIEC RISE ID: RISE2020_71_6_1
Redhat & Python Summary for 25-Mar-2020:
Project Work:While loop
- While loop vs if statement
- While with a condition
- While with True
- Exiting the programm with True and Exit()
- Indentation with while loop, best practice to use spaces.
- Repeating menu to avoid running program again and again un-necessarily.

IIEC RISE ID: RISE2020_71_6_1
Redhat & Python Summary for 26-Mar-2020:
Preparation for coming 2-day workshop:
- On VM Machine, create a new machine with existing Hard Disk with preinstalled Redhat 7 OS and other necessary environment.
- Connect your local machine's web cam to RHEL 7
- Devices => WebCam => (By Default WebCam option is not available, to enable WebCam option, use  extension provided, Oracle_VM_,
- Install this extension in Oracle VM Machine,
File, preferences, extensions, Add)

IIEC RISE ID: RISE2020_71_6_1
Redhat & Python Summary for 31-Mar-2020:
1st topic:  create a login and password.

vim menu.py

before where to run,
passwd = input("Enter ur password: ")
---------------------------------
apass = "lw"
if passwd != apass:
    print("Auth incorrect")
    exit()
else
    your code
---------------------------------
2nd topic: stop echo back.

Due to 'echo back', character is displayed on the screen
telnet	X
http	X

use getpass() for entering password as it takes the input but doesn't echo back.
import getpass
	x = getpass.getpass()

	x = getpass.getpass("Enter your string: ")

store password in : database,
compile program and convert into binary.

3rd topic: Avoid typing password for ssh agian and again:
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

IIEC RISE ID: RISE2020_71_6_1
Redhat & Python Summary for 01-Apr-2020:
Global exam for RHCSA-8 (30-40 ques)
Partition:

Q. how many partition can be created for 100 GB hard disk?

step1: create a partition -> creating a drive -> then format

Q. after re-formatting hard disk or pend drive? do we loose data or it is there?

Q what is the minimum size of the partition / drive in windows or linux?

Q4. In 1 MB, how much kilobyte you have?
1. < 999 KB
2. 1000 KB
3. 1024 KB
4. NOT

1000 KB in human language/Decimal
1024 KiB in Computer lang/Binary

- lvdisplay -> shows partition size in GiB

HD/Floppy/Pen/DvD = Storage (needed to store data permanent)
We cannot store data on storage.

Data need File need Directory need partition/drive

Q5. Why we need to create multiple partitions?

(electro mechanical hard disk)
Ex. SATA HARD DISKS (Aluminium)
	platter
		trackers
			sectors

A converted into asci (065) converted into binary (01000001)

head / hole on plates

shred remove drive

1 sector = 512 bytes

- fdisk -l

sda / hda / vda => Hard Disk
sdb / hdb / vdb => for second HD
all the devices are in dev folder, eg. /dev/sda

sector range 0-209715199
2048-209919


init 0 -> shut down operating system

right click -> go to settings -> storage -> Add a new virtual Hard Disk.

Questions:
There are two type of partitions avaible 1. fixed size 2. variable size ???

dynamic and static hard disk?

Redhat examination?

how to check the ip is valid or not through linux and python in a program?

