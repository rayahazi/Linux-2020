# Lesson 03 commands


### Mkdir
mkdir (1) - make directories
```
mkdir [name of folder]
```
```bash
raya@raya-VirtualBox:~/Desktop$ mkdir Dir01
raya@raya-VirtualBox:~/Desktop$ cd Dir01/
```

### Touch 
touch (1) - change file timestamps
```
touch [name of file]
```

```bash
raya@raya-VirtualBox:~/Desktop/Dir01$ touch a.txt
raya@raya-VirtualBox:~/Desktop/Dir01$ ls
a.txt
```

### Rmdir 
rmdir (1)  - remove empty directories
```bash
raya@raya-VirtualBox:~/Desktop$ mkdir stam
raya@raya-VirtualBox:~/Desktop$ rmdir stam/
```
If we try to delete not an empty folder: 
```bash
raya@raya-VirtualBox:~/Desktop$ rmdir Lesson\ 03/
rmdir: failed to remove 'Lesson 03/': Directory not empty
```
### Rm
rm (1) - remove files or directories
```bash
raya@raya-VirtualBox:~/Desktop$ cd Dir01/
raya@raya-VirtualBox:~/Desktop/Dir01$ ls
a.txt  b.txt
raya@raya-VirtualBox:~/Desktop/Dir01$ rm a.txt 
raya@raya-VirtualBox:~/Desktop/Dir01$ ls
b.txt
raya@raya-VirtualBox:~/Desktop/Dir01$ touch a.txt
raya@raya-VirtualBox:~/Desktop/Dir01$ ls
a.txt  b.txt
raya@raya-VirtualBox:~/Desktop/Dir01$ rm a.txt b.txt 
raya@raya-VirtualBox:~/Desktop/Dir01$ ls
raya@raya-VirtualBox:~/Desktop/Dir01$ 
```

* Delete a folder that is not empty:
`-r` : recursively 
```bash
rm -r [name of folder]
```

```bash
raya@raya-VirtualBox:~/Desktop/Dir01$ ls
raya@raya-VirtualBox:~/Desktop/Dir01$ touch a.txt b.txt 
raya@raya-VirtualBox:~/Desktop/Dir01$ ls
a.txt  b.txt
raya@raya-VirtualBox:~/Desktop/Dir01$ cd ..
raya@raya-VirtualBox:~/Desktop$ ls
 02   Dir01  'Lesson 03'
raya@raya-VirtualBox:~/Desktop$ rmdir Dir01/
rmdir: failed to remove 'Dir01/': Directory not empty
raya@raya-VirtualBox:~/Desktop$ rm -r Dir01/
raya@raya-VirtualBox:~/Desktop$ ls
'Lesson 03'
```

### Mv
mv (1) - move (rename) files

```bash
raya@raya-VirtualBox:~/Desktop/newFolder$ ls
b.txt  newA.txt
raya@raya-VirtualBox:~/Desktop/newFolder$ mv b.txt newB.txt
raya@raya-VirtualBox:~/Desktop/newFolder$ ls
newA.txt  newB.txt
```

