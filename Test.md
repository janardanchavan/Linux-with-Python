IIEC RISE ID: RISE2020_71_6_1

## Docker Summary for 05-Apr-2020:

fdisk -l => to check how many hard disk do we have <br/>
fdisk -l /dev/sda =>To check for the particular hard disk	

Today's topic: how to create partition ourself

3 Step process:
1. how much data you want to store?
2. Format
3. Mount / Activate

Creating a physical partition

fdisk /dev/sdb => to go inside your hard disk:

p => to show detail about hard disk

N => to create new partition

p option => for primary partition <br/>
1 option => first partition <br/>
start of partition <br/>
end of partition

Creating second drive:

Creating third drive

n 1 hard disk, we can create only 4 partitions, i.e. 1 hard disk = max 4 partitions total.

If any space remaining, it is called as un-alloated space / sector, because we cannot create fifth partition.

1 information of 1 partition required 16 bytes. <br/>
This information is stored in the partition table. <br/>
Partitional table size is 64 bytes.

64/16 = 4, hence, we can create 4 partitions only.

To create additional partitions, create 4th partition as extended partion.

We'll have primary and logical (extended) partitional <br/>
enter and enter

5th partition

Que: How many logical partitions we can create in Redhat 8 operating system.

Que: What is the minimum size of 1 partition = 1 sector.

Press q to quit (if you are not sure whatever you have done is correct, this will not save anything)

w => to save partition 

check how many partitions: fdisk -l

lsblk => another command to check drives / partition

Any devices where you store your devices, those devices are called “block devices”, hence lsblk command.

To load drivers, use partprobe command

This command (partprobe) doesn't support properly in Redhat8

In Redhat8 use following command: udevadm settle

```
	┌──────────────────────────────────────────────────────────┐
	│                     Host OS (Linux)                      │
	│                                                          │
	│  ┌───────────────┐ ┌───────────────┐  ┌───────────────┐  │
	│  │ Container OS  │ │ Container OS  │  │ Container OS  │  │
	│  │   (Ubuntu)    │ │   (Ubuntu)    │  │   (Ubuntu)    │  │
	│  │ ┌───────────┐ │ │ ┌───────────┐ │  │ ┌───────────┐ │  │
	│  │ │ Couchbase │ │ │ │ Couchbase │ │  │ │ Couchbase │ │  │
	│  │ │  Server   │ │ │ │  Server   │ │  │ │  Server   │ │  │
	│  │ └───────────┘ │ │ └───────────┘ │  │ └───────────┘ │  │
	│  └───────────────┘ └───────────────┘  └───────────────┘  │
	└──────────────────────────────────────────────────────────┘
```
