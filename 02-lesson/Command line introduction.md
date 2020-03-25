### How to make ubuntu full screen
devices -> insert guest additions

# Command Line Interface

Command Line Interface (CLI) allows us interact with computer using text commands

For example: the `cd` command would help navigating to a particular directory and `ls` command to view contents of a directory. In GUI, you'd use an explorer for directory navigation by point and click, directory contents are shown by default

### PWD 
pwd - print name of current/working directory

```sh
raya@raya-VirtualBox:/$ pwd 
/
```

### Man
man - an interface to the on-line reference manuals
press `q` to quit. 
```sh
man man 
```

### whatis
whatis - display one-line manual page descriptions
```sh
raya@raya-VirtualBox:/$ whatis clear
clear (1)            - clear the terminal screen
```

### Clear
clear - clear the terminal screen
`clear` is similar to `cls` in windows. 
```sh
raya@raya-VirtualBox:/$ clear
```

### Top
top - display Linux processes

### df -h
df - report file system disk space usage

### LS
ls - list directory contents
```sh
raya@raya-VirtualBox:/$ pwd
/
raya@raya-VirtualBox:/$ ls
bin   cdrom  etc   initrd.img      lib    lost+found  mnt  proc  run   snap  swapfile  tmp  var
boot  dev    home  initrd.img.old  lib64  media       opt  root  sbin  srv   sys       usr  vmlinuz

```
##### Show hidden files
-a, --all : do not ignore entries starting with .
```sh
raya@raya-VirtualBox:~$ ls -a
.              .config           .ICEauthority  Public                       .vboxclient-seamless.pid
..             Desktop           .local         .sudo_as_admin_successful    Videos
.bash_history  Documents         .mozilla       Templates
.bash_logout   Downloads         Music          .vboxclient-clipboard.pid
.bashrc        examples.desktop  Pictures       .vboxclient-display.pid
.cache         .gnupg            .profile       .vboxclient-draganddrop.pid

```
-l     use a long listing format

* d = directory (תקייה)
```sh
drwxr-xr-x 3 raya raya 4096 Mar 25 11:34 Desktop
```
* `-` is file
```sh
-rw-r--r-- 1 raya raya 8980 Mar 22 00:46 examples.desktop
```
```sh
raya@raya-VirtualBox:~$ ls -l
total 44
drwxr-xr-x 3 raya raya 4096 Mar 25 11:34 Desktop
drwxr-xr-x 2 raya raya 4096 Mar 22 00:57 Documents
drwxr-xr-x 2 raya raya 4096 Mar 22 00:57 Downloads
-rw-r--r-- 1 raya raya 8980 Mar 22 00:46 examples.desktop
drwxr-xr-x 2 raya raya 4096 Mar 22 00:57 Music
drwxr-xr-x 2 raya raya 4096 Mar 22 00:57 Pictures
drwxr-xr-x 2 raya raya 4096 Mar 22 00:57 Public
drwxr-xr-x 2 raya raya 4096 Mar 22 00:57 Templates
drwxr-xr-x 2 raya raya 4096 Mar 22 00:57 Videos

```
##### Combine the two commands: 
```sh
raya@raya-VirtualBox:~$ ls -la
total 108
```

## cd 
cd - change direcory. 
```sh
raya@raya-VirtualBox:~$ ls
Desktop  Documents  Downloads  examples.desktop  Music  Pictures  Public  Templates  Videos
raya@raya-VirtualBox:~$ cd Desktop/
raya@raya-VirtualBox:~/Desktop$ 
```
Go back: 
```sh
raya@raya-VirtualBox:~/Desktop$ pwd
/home/raya/Desktop
raya@raya-VirtualBox:~/Desktop$ cd ..
raya@raya-VirtualBox:~$ pwd
/home/raya
```


#### Update packages:
Sudo - Super User. 
```sh
raya@raya-VirtualBox:/$ sudo apt update
[sudo] password for raya: 
```

### tree
tree - list contents of directories in a tree-like format.

```sh
raya@raya-VirtualBox:/$ sudo apt-get install tree
```
```sh
raya@raya-VirtualBox:~$ tree
.
├── Desktop
│   └── 02
├── Documents
├── Downloads
├── examples.desktop
├── Music
├── Pictures
├── Public
├── Templates
└── Videos

9 directories, 1 file
```












