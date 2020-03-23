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
