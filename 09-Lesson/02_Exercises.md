# Exercises

### Program to swap two numbers:

```bash
#! /bin/bash

# swapping of two numbers:

read -p "Enter num1: " num1
read -p "Enter num2: " num2

echo "Before swap: num1: $num1, num2: $num2"

# num1 = 5, num2 = 7

temp=$num1	# num1 = 5, num2 = 7, temp = 5
num1=$num2	# num1 = 7, num2 = 7, temp = 5
num2=$temp      # num1 = 7, num2 = 5, temp = 5

echo "After  swap: num1: $num1, num2: $num2"

```

- output:

```bash
raya@raya-VirtualBox:~/Desktop/Lesson09$ ./a.bash
Enter num1: 5
Enter num2: 7
Before swap: num1: 5, num2: 7
After swap: num1: 7, num2: 5
```

### Palindrome

```bash
#! /bin/bash

# Palindrome - 12321, 1221

num=12345
remainder=0
revNum=""

temp=$num # here: num=373, temp=373

while [ $num -gt 0 ]
do
	remainder=$(( $num % 10 ))
	num=$(( $num / 10 ))
	revNum=$( echo ${revNum}${remainder} )
done

if [ $temp -eq $revNum ]
then
	echo "Number is palindrome!"
else
	echo "Number is not palindrome!"
fi
```

## Fibonacci series:

<img height=400 src="https://i.pinimg.com/originals/98/82/d5/9882d569f7e0b5665fe3b2edd5069b06.png"/>

```bash
#! /bin/bash

# Fibonacci series -
# * the two first numbers are always 1.
# * ask from the user the limit digits to print.
# * use a for loop (optional)

# 1 1 2 3 5 8 13

LIMIT=10

a=0
b=1

echo "Fibonacci series: "

for (( i=0; i<LIMIT; i++ ))
do
	fib=$((a+b))
	a=$b
	b=$fib
	echo -n "$a "
done
echo

```

- output:

```bash
raya@raya-VirtualBox:~/Desktop/Lesson09$ ./a.bash
Fibonacci series:
1 1 2 3 5 8 13 21 34 55
```

- Repeat password:

```bash
#! /bin/bash

# enter a password twice, and check if equal.

read -p "Enter your password:    " pass1
read -p "Repeat password:    " pass2

echo

if [ $pass1 == $pass2 ]
then
	echo "Success!"
else
	echo "Fail!"
fi
```

- Output:

```bash
raya@raya-VirtualBox:~/Desktop/Lesson09$ ./a.bash
Enter your password:    1234
Repeat password:    1234

Success!
```
