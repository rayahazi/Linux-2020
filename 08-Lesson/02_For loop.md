# For loop

## Arrays - מערכים

array is a list of many items:
shoppingList = bottle, wine, juice, milk

shoppingList = [bottle, wine, juice, milk]
shoppingList[0] = bottle
shoppingList[1] = wine

Memory: the arrays are stored in the heap, and the address of the first element is stored in the stack.

## Syntax:

```bash
for arg in [list]
do
    commands...
done
```

# Examples:

## 1. Print a list of 5 lessons with their number in for-in loop:

```bash
#! /bin/bash

# for-in: goes on value:

i=1

for lesson in Linux Cyber HTML JavaScript MySql
do
	echo "Lesson $i : $lesson"
	((i++))
done
```

res:

```bash
raya@raya-VirtualBox:~/Desktop/Lesson8$ ./a.bash
Lesson 1 : Linux
Lesson 2 : Cyber
Lesson 3 : HTML
Lesson 4 : JavaScript
Lesson 5 : MySql
```

## 2. Multiple ways to count up to 10:

```bash
#! /bin/bash

# for-in: goes on value:
## ---------- standard syntax ---------------

echo

for num in 1 2 3 4 5 6 7 8 9 10
do
	echo -n " $num"
done

echo
echo

## ---------- count with seq ---------------

echo

for num in `seq 10`
do
	echo -n " $num"
done

echo
echo

## ---------- count with brace expansion ---------------

echo

for num in {1..10}
do
	echo -n " $num"
done

echo
echo

## ---------- C-like syntax ---------------

LIMIT=10

for ((a=1; a <= LIMIT ; a++))
do
	echo -n $a
done

echo
```

- res:

```bash
raya@raya-VirtualBox:~/Desktop/Lesson8$ ./a.bash

 1 2 3 4 5 6 7 8 9 10

```

- Use two values in for-loop:

```bash
#! /bin/bash

## ---------- C-like syntax ---------------

LIMIT=10

for ((a=1, b=1; a <= LIMIT ; a++, b++))
do
	echo -n " $a-$b "
done

echo

# Output:
# 1-1  2-2  3-3  4-4  5-5  6-6  7-7  8-8  9-9  10-10
```

- Print power of numbers from 1 to 10:

```bash
#! /bin/bash

## ---------- C-like syntax ---------------

LIMIT=10

for ((a=1; a <= LIMIT ; a++))
do
	echo -n $(($a*$a)) " "
done

echo

# Output:
# 1  4  9  16  25  36  49  64  81  100
```

## For loop with files:

```bash
#! /bin/bash

i=1

for distro in `cat LinuxDistros.txt`
do
	echo "$i : $distro"
	((i++))
done

echo
```

- res:

```bash
raya@raya-VirtualBox:~/Desktop/Lesson8$ ./a.bash
1 : Ubuntu
2 : Kali
3 : Tails
4 : Parrot
5 : Mint
6 : ElementaryOS


```

## Check for files or directories:

```bash
#! /bin/bash
## ---------- for loop with files ---------------

FILES="
/usr/sbin/accept
/usr/sbin/rmt
/usr/sbin
/usr/sbin
/home/raya/Desktop/Lesson8/LinuxDistros.txt
"
for file in $FILES
do
	if [ -f $file ]
	then
	echo "file: $file"; echo
	# elif - else if
	elif [ -d $file ]
	then
	echo "dir : $file"; echo
	fi
done

exit 0

# echo $?
```

## Check a folder - to see which files in it are files or folders:

```bash
#! /bin/bash

for file in /home/raya/Desktop/Lesson8/*
do
	if [ -f $file ]
	then
	echo "file: $file"; echo
	# elif - else if
	elif [ -d $file ]
	then
	echo "dir : $file"; echo
	fi
done

exit 0

# echo $?

```

## Pyramid:

```bash
#! /bin/bash

# nested for loop:

# *
# * *
# * * *
# * * * *
# * * * * *

LIMIT=8 # constant number

for ((row=1; row<=LIMIT; row++))
do
	for ((col=1; col<=row; col++))
	do
	echo -n "* "
	done
	echo
done
```
