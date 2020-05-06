# Regular expression

Regular expressions are special characters which help search data, matching complex patterns.
Regular expressions are shortened as `regexp` or `regex`

> Note: we can use `grep -E` instead of `egrep`

### Basic Regular expressions

1. `^` - match start of a string

```bash
raya@raya-VirtualBox:~/Desktop/Lesson05$ cat a.txt | egrep ^u
ubuntu
ubu
```

2. `$` - match end of a string

```bash
raya@raya-VirtualBox:~/Desktop/Lesson05$ cat a.txt | egrep u$
Ubuntu
Linuxubuntu
ubu
```

3. `*` - match up zero or more times the preciding character.

```bash
raya@raya-VirtualBox:~/Desktop/Lesson05/c$ grep "Hello world" *.c
file01.c:	printf("Hello world");
file03.c:	printf("Hello world");
```

4. `.` - replace any character

```bash
raya@raya-VirtualBox:~/Desktop/Lesson05$ cat a.txt | egrep "l.n"
GNUubuntulinux
linux
lanox
```