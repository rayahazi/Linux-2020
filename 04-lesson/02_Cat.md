# Cat 
cat - concatenate files and print on the standard output

`Cat` can open the data in a file. 

### 1. Display the file content using `cat`
```bash
cat /etc/passwd
```
* Create folder `Lesson04`, enter the folder, create file `a.txt`, insert data to it manually. See the data in `a.txt`
```bash
raya@raya-VirtualBox:~/Desktop$ mkdir Lesson04
raya@raya-VirtualBox:~/Desktop$ cd Lesson04/
raya@raya-VirtualBox:~/Desktop/Lesson04$ touch a.txt
raya@raya-VirtualBox:~/Desktop/Lesson04$ ls
a.txt
raya@raya-VirtualBox:~/Desktop/Lesson04$ cat a.txt 
Hello new users in linux
```

## 2. Create a file using `cat` command
```bash
cat > b.txt
```
```bash
raya@raya-VirtualBox:~$ cd Desktop/Lesson04/
raya@raya-VirtualBox:~/Desktop/Lesson04$ ls
a.txt
raya@raya-VirtualBox:~/Desktop/Lesson04$ cat > b.txt
This is a wondeful world
raya@raya-VirtualBox:~/Desktop/Lesson04$ ls
a.txt  b.txt
```
> note: to close the file: `ctrl + d`

## Display line numbers in a file
With `-n` option we can see the line numbers of the file `theRoadNotTaken.txt ` in the output terminal
```bash
raya@raya-VirtualBox:~/Desktop/Lesson04$ cat -n theRoadNotTaken.txt 
     1	 The Road Not Taken
     2	By Robert Frost
     3	Two roads diverged in a yellow wood,
     4	And sorry I could not travel both
     5	And be one traveler, long I stood
     6	And looked down one as far as I could
     7	To where it bent in the undergrowth;
```

## Concatenate output
We can show the data inside 2 files at the same time: 
```bash
raya@raya-VirtualBox:~/Desktop/Lesson04$ cat a.txt 
Hello dear students!
raya@raya-VirtualBox:~/Desktop/Lesson04$ cat b.txt 
This is a wondeful world

raya@raya-VirtualBox:~/Desktop/Lesson04$ cat a.txt b.txt 
Hello dear students!
This is a wondeful world
```

## Add concatenated data to end of file
If we use `>` - it will override the previous data. 
if we use `>>` - it will concatenate data to the end of the file
```bash
raya@raya-VirtualBox:~/Desktop/Lesson04$ cat a.txt 
Hello dear students!
raya@raya-VirtualBox:~/Desktop/Lesson04$ cat > a.txt 
This is a
raya@raya-VirtualBox:~/Desktop/Lesson04$ cat a.txt 
This is a
raya@raya-VirtualBox:~/Desktop/Lesson04$ cat >> a.txt 
Hello dear students! I am concatenated
raya@raya-VirtualBox:~/Desktop/Lesson04$ cat a.txt 
This is a
Hello dear students! I am concatenated
```





