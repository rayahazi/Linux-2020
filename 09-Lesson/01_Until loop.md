# until loop

**Until** loop is the oppsite of **while** loop.
As long as the condition is false - the loop will continue running.

### Syntax

```bash
until [ condition ]
do
    # commands to execute
done
```

#### Example:

```bash
#! /bin/bash

read -p "Enter a number: " num

i=0

until [ $i -eq 11 ]
do
	echo "$num * $i = $((num*i))"
	i=$((i+1))
done

echo "i = $i"

```

- output

```bash
raya@raya-VirtualBox:~/Desktop/Lesson09$ ./a.bash
Enter a number: 4
4 * 0 = 0
4 * 1 = 4
4 * 2 = 8
4 * 3 = 12
4 * 4 = 16
4 * 5 = 20
4 * 6 = 24
4 * 7 = 28
4 * 8 = 32
4 * 9 = 36
4 * 10 = 40
i = 11
```
