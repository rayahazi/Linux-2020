# Grep

> grep, egrep, fgrep, rgrep - print lines matching a pattern
> grep searches for PATTERN in each FILE. A FILE of “-” stands for standard input.

```
grep [OPTIONS] pattern [FILE...]
```

### Simple grep

- Search for `L` in `a.txt`.

```bash
raya@raya-VirtualBox:~/Desktop/Lesson05$ cat a.txt
Bob
Alice
Root
User
Linux is great
raya@raya-VirtualBox:~/Desktop/Lesson05$ grep L a.txt
Linux is great
```

- Search for `root` in file `/etc/passwd`

```bash
raya@raya-VirtualBox:~/Desktop/Lesson05$ grep root /etc/passwd
root:x:0:0:root:/root:/bin/bash
```

- Search for more than one word - we must add `""`

```bash
raya@raya-VirtualBox:~/Desktop/Lesson05$ grep "Speech Dispatcher" /etc/passwd
speech-dispatcher:x:111:29:Speech Dispatcher,,,:/var/run/speech-dispatcher:/bin/false
```

### invert match (exclude)

> **-v** or **--invert-match**

display lnes that do not match a pattern.

```bash
raya@raya-VirtualBox:~/Desktop/Lesson05$ cat a.txt
Bob
Alice
Root
User
Linux is great
raya@raya-VirtualBox:~/Desktop/Lesson05$ grep -v User  a.txt
Bob
Alice
Root
Linux is great

raya@raya-VirtualBox:~/Desktop/Lesson05\$ grep --invert-match User a.txt
Bob
Alice
Root
Linux is great
```
### Search for a pattern using pipe

```bash
raya@raya-VirtualBox:~/Desktop/Lesson05$ ps awx | grep update
 2243 tty1     Sl+    0:00 update-notifier
 6081 tty1     SNl+   0:09 /usr/bin/python3 /usr/bin/update-manager --no-update --no-focus-on-map
 6260 pts/0    S+     0:00 grep --color=auto update
raya@raya-VirtualBox:~/Desktop/Lesson05$ ps awx | grep root
  618 ?        S      0:00 avahi-daemon: chroot helper
 6262 pts/0    S+     0:00 grep --color=auto root
 raya@raya-VirtualBox:~/Desktop/Lesson05$ ps awx | grep root | grep avahi
  618 ?        S      0:00 avahi-daemon: chroot helper

```

### Recursive search

> grep -r [Pattern][name_of_folder]

> -r, --recursive
> Read all files under each directory, recursively, following symbolic links only if they are on the
> command line. Note that if no file operand is given, grep searches the working directory. This is
> equivalent to the -d recurse option.

Search for each folder and file in a chosen folder.
note: here we search for `passwd` in `/usr/bin` folder. Binary files cannot show their content. only one file had a match.

```bash
raya@raya-VirtualBox:/usr/bin$ grep -r passwd /usr/bin
Binary file /usr/bin/ubuntu-report matches
/usr/bin/migrate-pubring-from-classic-gpg:GHD=${GNUPGHOME:-${HOME:-$(getent passwd "$(id -u)" | cut -f6 -d:)}/.gnupg}
```

## Show only file name

> -l

- Create 3 files of `c` extention. In two of then "Hello world", and in one of them: "hello world".

```bash
raya@raya-VirtualBox:~/Desktop/Lesson05/c$ cat file01.c
#include <stdio.h>
void main(){
	printf("Hello world");
}
```

- Search for some patterns:

```bash
raya@raya-VirtualBox:~/Desktop/Lesson05/c$ grep Hello file01.c
	printf("Hello world");
raya@raya-VirtualBox:~/Desktop/Lesson05/c$ grep "Hello world" file01.c
	printf("Hello world");
```

- `*.c` - search for each file that ends with `.c`.

```bash
raya@raya-VirtualBox:~/Desktop/Lesson05/c$ grep "Hello world" *.c
file01.c:	printf("Hello world");
file03.c:	printf("Hello world");
```

- `-l` - returns only the file name.

```bash
raya@raya-VirtualBox:~/Desktop/Lesson05/c$ grep -l "Hello world" *.c
file01.c
file03.c
raya@raya-VirtualBox:~/Desktop/Lesson05/c$ grep -l "hello world" *.c
file02.c
```

- Search recursively in the folder `c` and all the subfolders.

```bash
raya@raya-VirtualBox:~/Desktop/Lesson05/c$ grep -rl "Hello world"
secondC/secondDir.c
file01.c
file03.c
```

## Case insensitive search

> -i

- Search for "Hello world" both for uppercase and lowecase in file `file02.c`

```bash
raya@raya-VirtualBox:~/Desktop/Lesson05/c$ grep -i "Hello world" file02.c
	printf("hello world");
```

## Search for full words

> -w (word)

- Select the pattern only when it is not inside another word.

```bash
raya@raya-VirtualBox:~/Desktop/Lesson05$ cat a.txt
ubuntu
Ubuntu
Linuxubuntu
GNUubuntulinux
ubu
linux
raya@raya-VirtualBox:~/Desktop/Lesson05$ grep ubuntu a.txt
ubuntu
Linuxubuntu
GNUubuntulinux
raya@raya-VirtualBox:~/Desktop/Lesson05$ grep -w ubuntu a.txt
ubuntu
```

## Show line numbers

> -n (number)

- Select all the lines that math the pattern `ubuntu`, and show the line numbers.

```bash
raya@raya-VirtualBox:~/Desktop/Lesson05$ cat a.txt
ubuntu
Ubuntu
Linuxubuntu
GNUubuntulinux
ubu
linux

raya@raya-VirtualBox:~/Desktop/Lesson05$ grep -n ubuntu a.txt
1:ubuntu
3:Linuxubuntu
4:GNUubuntulinux
```
## Count matches
> -c --count 

* Select the amount of matches `ubuntu` has in `a.txt`
```bash
raya@raya-VirtualBox:~/Desktop/Lesson05$ grep -c ubuntu a.txt 
3
```
