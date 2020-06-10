# Shuf

> shuf - generate random permutations

- Basic random with `a.txt` file:

```bash
raya@raya-VirtualBox:~/Desktop/Lesson10$ cat > a.txt
Hello
Students
Byte
Bye
Linux
OS
raya@raya-VirtualBox:~/Desktop/Lesson10$ shuf a.txt
Bye
Students
OS
Byte
Linux
Hello
```

### shuf -n

> -n, --head-count=COUNT
> output at most COUNT lines

- select three lines randomally from a file:

```bash
raya@raya-VirtualBox:~/Desktop/Lesson10$ shuf -n 3  a.txt
OS
Byte
Students
raya@raya-VirtualBox:~/Desktop/Lesson10$ shuf -n 3  a.txt
Bye
Students
Hello
```

- select one line randomally from a file:

```bash
raya@raya-VirtualBox:~/Desktop/Lesson10$ shuf -n 1  a.txt
Bye
raya@raya-VirtualBox:~/Desktop/Lesson10$ shuf -n 1  a.txt
Linux
raya@raya-VirtualBox:~/Desktop/Lesson10$ shuf -n 1  a.txt
Students

```

### shuf -e

> -e, --echo
> treat each ARG as an input line

- `shuf -e` gets parameters and use the random on them.

```bash
raya@raya-VirtualBox:~/Desktop/Lesson10$ shuf -e A B C D
B
D
C
A
raya@raya-VirtualBox:~/Desktop/Lesson10$ shuf -e A B C D
D
A
C
B
```

- Use both `shuf -n` and `shuf -e`: insert parameters with the command, and show only one random item from them each time.

```bash
raya@raya-VirtualBox:~/Desktop/Lesson10$ shuf -e one two three -n 1
one
raya@raya-VirtualBox:~/Desktop/Lesson10$ shuf -e one two three -n 1
two
raya@raya-VirtualBox:~/Desktop/Lesson10$ shuf -e one two three -n 1
two
```
