# Echo - הד

**echo - display a line of text**

```bash
echo [OPTION]... [STRING]...
```

```bash
raya@raya-VirtualBox:~$ echo hello students
hello students
raya@raya-VirtualBox:~$ echo "hello students"
hello students
raya@raya-VirtualBox:~$ echo some text #this is a comment
some text
```

- Create `.sh` file, and run it in the terminal:

```bash
echo "Hello students # a comment"
echo 'Hello students # a comment'
echo Hello stundets # a comment
echo Hello students \# a comment


# Result:
# -------------------------
# Hello students # a comment
# Hello students # a comment
# Hello stundets
# Hello students # a comment
```

### echo -n

> -n do not output the trailing newline

```bash
raya@raya-VirtualBox:~$ echo "Hello"
Hello
raya@raya-VirtualBox:~$ echo -n 'Hello'
Helloraya@raya-VirtualBox:~$
```

### echo -e

> -e enable interpretation of backslash escapes

```bash
raya@raya-VirtualBox:~$ echo "This is a \tnice day"
This is a \tnice day
raya@raya-VirtualBox:~$ echo -e "This is a \tnice day"
This is a 	nice day
raya@raya-VirtualBox:~$ echo "This is a \nbeautiful day"
This is a \nbeautiful day
raya@raya-VirtualBox:~$ echo -e "This is a \nbeautiful day"
This is a
beautiful day
```

### Exit code: `$?`

show the exit code of the last command. If last command was successful - it will be 0.

```bash
raya@raya-VirtualBox:~/Desktop/Lesson06$ dfkljs
dfkljs: command not found
raya@raya-VirtualBox:~/Desktop/Lesson06$ echo $?
127
raya@raya-VirtualBox:~/Desktop/Lesson06$ echo hello
hello
raya@raya-VirtualBox:~/Desktop/Lesson06$ echo $?
0
```

### Path

```bash
raya@raya-VirtualBox:~/Desktop/Lesson06$ echo $PATH
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin
```

### echo as ls
echo can be used as `ls` command:
```bash
raya@raya-VirtualBox:~$ ls
Desktop    Downloads         Music     Public     Videos
Documents  examples.desktop  Pictures  Templates
raya@raya-VirtualBox:~$ echo *
Desktop Documents Downloads examples.desktop Music Pictures Public Templates Videos
raya@raya-VirtualBox:~$ echo D*s
Documents Downloads
```
