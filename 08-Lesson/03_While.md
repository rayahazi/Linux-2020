# While

### Basic while

- loop over counter 4 times, and increment the conuter in 1 each round, using `expr` - to convert the conuter to a number:

```bash
#! /bin/bash

counter=0

while [ "$counter" -lt 4 ]
do
	echo "Round number: $counter"
	counter=`expr $counter + 1`
done

echo "Finished while loop: counter =  $counter"

# Round number: 0
# Round number: 1
# Round number: 2
# Round number: 3
# Finished while loop: counter =  4
```

### Multiplication table (for a given number):

```bash
#! /bin/bash

read -p "Enter a number: " number

i=0

while [ $i -le 10 ]
do
	echo "$number * $i =  " $((number*i))
	((i++))
done
```

- res

```
raya@raya-VirtualBox:~/Desktop/Lesson8$ ./a.bash
Enter a number: 3
3 * 0 =   0
3 * 1 =   3
3 * 2 =   6
3 * 3 =   9
3 * 4 =   12
3 * 5 =   15
3 * 6 =   18
3 * 7 =   21
3 * 8 =   24
3 * 9 =   27
3 * 10 =   30
```

### run while loop with command:

```bash
#! /bin/bash

# can be installed: sudo apt-get install xterm

i=0

while [ $i -lt 3 ]
do
	xterm & ((i++))
done

# Open 3 x terminals.


i=0

while [ $i -lt 3 ]
do
	touch $i.txt & ((i++))
done

# Result:
# 0.txt  1.txt  2.txt
```

### User writes many words, end to exit:

```bash
#! /bin/bash



while [ "$var" != "end" ]
do
	echo "Write something (end to exit) "
	read var
	echo "variable: $var"
	echo
done

exit 0
```

- res

```bash
raya@raya-VirtualBox:~/Desktop/Lesson8$ ./a.bash
Write something (end to exit)
banana
variable: banana

Write something (end to exit)
computer
variable: computer

Write something (end to exit)
end
variable: end

```

### Program to create endless images(until we stop the execution):

```bash
#! /bin/bash

# %s - seconds since 1970-01-01 00:00:00 UTC


while true # infinity - endless loop
do
	touch image-`date +%s`.jpg
	sleep 3
done

exit 0
```

- res:

```
raya@raya-VirtualBox:~/Desktop/Lesson8$ ls
a.bash                image-1590578328.jpg  image-1590578343.jpg
image-1590578316.jpg  image-1590578331.jpg  image-1590578346.jpg
image-1590578319.jpg  image-1590578334.jpg  image-1590578349.jpg
image-1590578322.jpg  image-1590578337.jpg
image-1590578325.jpg  image-1590578340.jpg

```
