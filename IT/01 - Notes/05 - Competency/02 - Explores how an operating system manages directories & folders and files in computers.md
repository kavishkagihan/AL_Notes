# Explores how an operating system manages directories/folders and files in computers.

## Files Management 

### Files
- File is a named collection of data stored in secondary storage
- There are 2 views of a file.
	1. Logical View (User's view) - As a collection of records
	2. Physical View (OS's view) - Whether blocks of secondary storage space either allocated or not 

### Directories

- A directory is **a special type of file** that contains other files

### File Management System

```
A File Management System is a system that allows you to create, delete, move, rename and other actions to manage files properly.
```
### File Systems

```
A file system is used to control how data is stored and retrieved
```

- There are different types of file systems
	1. FAT (File Allocation Table)
	2. NTFS (New Technology File System)
	3. ReFS file system (Resilient File System)
		- developed by Microsoft as a **new generation file system** and it requires Windows 8 or Windows server 2012 

#### FAT

##### Features of FAT file system
- inherited from old DOS
- can only have a filename up to 8 characters
- can only have portions of size 4 GB
- Disk can get fragmented
- Two types of FAT file systems
	- FAT32
		- FAT32 can be read in just about any OS
	- exFAT
		- Microsoft file systems (**proprietary** and **patented**)

#### NTFS

##### Features of NTFS file system

- It provides security for both local and remote users. 
- It supports 255 characters long file name. 
- Partition size can be up to 16 Exabyte. 
- Supports file compression. 
- Lesser possibility of fragmentation. 
- **proprietary file system** developed by Microsoft. This is improvement of FAT. 


![](../../../assets/Images%201/Pasted%20image%2020221112124509.png)


### File Storage Management

- On secondary storage, stored data is organised using
	- Tracks - rings on platters
	- Sectors - tracks are devided into sectors
	- Cluster - a group of sectors, the smallest unit (512 bytes) allocated to store a file

![](../../../assets/Images%201/Pasted%20image%2020221112124843.png)

• OS uses a data structure called **File Allocation Table** (FAT) to keep the track of allocated and free blocks.

### File Allocation Methods

There are 3 main methods.
	1. Contiguous Allocation
	2. Linked Allocation
	3. Indexed Allocation

#### Contiguous Allocation

- A single contiguous set of blocks is allocated to a file at the time of file creation. All the blocks are allocated closer to each other

![](../../../assets/Images%201/Pasted%20image%2020221112125254.png)

##### Strengths
- Simple
- Easy Access

##### Weaknesses
- File size should be known at the time of file creation.
- Extending file size is difficult
- External fragmentation(unusable free blocks between allocation)
	- This can be resolved by using defragmentation, but that results in system overhead (using the other resources unwantedly)

#### Linked Allocation
- This is kinda the opposite of the contiguous allocation.
- Inside each block, 
	- the contents of the relevant file,
	- a link maintained to point to where the next block of the file is present.

![](../../../assets/Images%201/Pasted%20image%2020221112125905.png)

##### Strength
- No need to know the file size at the time of creation
- No external fragmentation to worry about because block by block is allocated at a time as needed.
- Files can grow dynamically and easily

##### Weaknesses
- Slow, many seeks  to access the file 
- Periodic consolidation can solve this but adds system overhead

![](../../../assets/Images%201/Pasted%20image%2020221112130214.png)

By doing this, we can access the file fast. Even if its edited and the size gets large, that extended content can be saved in some place else and then again can be defragmented to make them closer in order.

#### Indexed Allocation

- FAT contains entry to index block of each file.
- The index block has entries for each block allocated to file
- The index table is also saved in a block/s
- Example:
	- UNIX file system - used indexed allocation with contiguous blocks
	- NTFS – used indexed allocation method

![](../../../assets/Images%201/Pasted%20image%2020221112131127.png)

##### Features
- No need to know the file size at the time of creation
- Files can grow dynamically, and the index is updated accordingly
- File ends at nil pointer (empty index block)
- No external fragmentation
- Each index block contains 2 data
	- indexes of the blocks that contain the contents of the relevant file 
	- pointer to next index block
- Using contiguous blocks in combination with this can **save the seek time**

### The Secondary storage

This storage is typically used to store
- Source programs
- Executable programs
- Temporary data

#### Maintenance of Secondary storage

##### Defragmentation

```
This is a **process that reduces the amount of fragmentation.**
```
- Simply said, removing the spaces between the saved files.

##### Disk Cleanup

- Removing unnecessary files, including temporary internet files
- Allows you to empty the Recycle Bin, delete temporary files, and delete thumbnails

##### Disk formatting

```
Formatting is the process of preparing a data storage device for initial use, which may also create one or more new file systems.
```
> As file deletion is done by the operating system, data on a disk are not fully erased during every high-level format. Instead, links to the files are deleted and the area on the disk containing the data is retains until it is overwritten
