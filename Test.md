IIEC RISE ID: RISE2020_71_6_1
## Redhat & Python Summary for 01-Apr-2020:
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

1000 KB in human language/Decimal <br/>
1024 KiB in Computer lang/Binary

	lvdisplay -> shows partition size in GiB

HD/Floppy/Pen/DvD = Storage (needed to store data permanent) <br/>
We cannot store data on storage.

Data need File need Directory need partition/drive

Q5. Why we need to create multiple partitions?

(electro mechanical hard disk) <br/>
Ex. SATA HARD DISKS (Aluminium) <br/>
        platter <br/>
            trackers <br/>
                sectors <br/>

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

