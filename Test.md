## Installing Redhat 8

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
  
  5 Memory Size: Enter 2048 i.e. 2 GB Ram
  6 Hard Disk: Create a Virtual Hard Disk now
  7 Hard Disk File Type: VDI (Virtualbox Disk Image)
  8 Storage on Physical Hard Disk: Dynamically Allocated
  9 File Location and size: 100 GB
  10 Click Create button. Your Virtual Machine / Hardware (RAM/CPU/Harddisk) is up now.

  11 Right Click the VM name and select Settings
  12 Select Storage
  13 At the right side, click the CD icon in front of Optical Drive drop down.
  14 Click Choose Virtual Optical Disk file
  15 Select the Redhat 8 iso file whereever it is downloaded and click OK.

  Now we can start installing OS

  16 Select the VM machine
  17 Click Start button on the top. It will power on you operating syste and start installing Red hat.
  18 On the blank screen, using arrow key select the first option:
      Install Red Hat Enterprise Linux 8.0.0
  19 After installation it will ask few settings:
    - Language: English(United states)
    - Installation Destination (Partition): Select it and click Done
    - Network & Host Name: Open  it and click On against "Ethernet (enp0s3), click Done
    - Software Selection: Select Workstation and click Done
    - Time & Date: As per your country, change the time zone. Click Done
  20 Click Begin Installation
  
  This will some time.
  
  21 After installation it will ask you to enter <br/>
    - root user password and confirm
    - new user creation
  22 After entering the details continue the installation process. <br/>
     This will create user
  22 Reboot your machine
  
  Note that it will again start the installation, rather power off the machine.
  
  23 On Oracle VM VirtualBox Manager, right click the machine and select Settings.
  24 Move the "Hard Disk" option up at the top so that the installed OS will start next time when you restart the machine.
  
  Thank you.
    
    

