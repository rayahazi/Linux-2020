# Linux file system
<img src="https://www.rs-online.com/designspark/rel-assets/dsauto/temp/uploaded/linux-filesystem.png?w=815"/>

1. The entire Linux directory structure starting at the top (/) root directory.

2. In linux, everything is represented by a file or a folder!

## /bin
The /bin directory contains user executable files.

## /boot	
Contains the static bootloader and kernel executable and configuration files required to boot a Linux computer.

## /dev
This directory contains the device files for every hardware device attached to the system. These are not device drivers, rather they are files that represent each device on the computer and facilitate access to those devices.

## /etc	
Contains the local system configuration files for the host computer.

## /home	
Home directory storage for user files. Each user has a subdirectory in /home.

## /lib	
Contains shared library files that are required to boot the system.

## /media	
A place to mount external removable media devices such as USB thumb drives that may be connected to the host.

## /mnt	
A temporary mountpoint for regular filesystems (as in not removable media) that can be used while the administrator is repairing or working on a filesystem.

## /opt	
Optional files such as vendor supplied application programs should be located here.

## /root	
This is not the root (/) filesystem. It is the home directory for the root user.
## /sbin	
System binary files. These are executables used for system administration.
## /tmp	
Temporary directory. Used by the operating system and many programs to store temporary files. Users may also store files here temporarily. Note that files stored here may be deleted at any time without prior notice.
## /usr	
These are shareable, read-only files, including executable binaries and libraries, man files, and other types of documentation.
## /var	
Variable data files are stored here. This can include things like log files, MySQL, and other database files, web server data files, email inboxes, and much more.

# <a name="absolute-and-relative-paths"></a>Absolute and Relative paths

>An **absolute or full path** points to the same location in a file system regardless of the current working directory. To do that, it must contain the root directory.

>By contrast, a **relative path** starts from some given working directory, avoiding the need to provide the full absolute path. A filename can be considered as a relative path based at the current working directory. If the working directory is not the file's parent directory, a file not found error will result if the file is addressed by its name.

* `/home/learnbyexample` absolute path
* `../design` relative path
