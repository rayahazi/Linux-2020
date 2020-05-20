# Class task

## 1. Median number:

- Get three variables from the user, and find the median amoung the 3.
  example: 1,5,8: we get 5

```bash
#! /bin/bash

echo "Enter num1:"
read num1

echo "Enter num2:"
read num2

echo "Enter num3:"
read num3

echo "$num1, $num2, $num3"

# num1 = 5, num2 = 7, num3 = 3

# get num1 if it is the middle number:
if [ $num1 -gt $num2 ] && [ $num1 -lt $num3 ]
then
	echo "Num1 = $num1 is the middle number"
fi

if [ $num1 -gt $num3 ] && [ $num1 -lt $num2 ]
then
	echo "Num1 = $num1 is the middle number"
fi
```

## 2. Biggest number:

- Get three variables from the user, and find the biggest amoung the 3.
  example: 1,5,8: we get 8.

```bash
#! /bin/bash

echo "Enter num1:"
read num1

echo "Enter num2:"
read num2

echo "Enter num3:"
read num3

echo "$num1, $num2, $num3"

# num1 = 10, num2 = 7, num3 = 3

# get num1 if max:
if [ $num1 -gt $num2 ] && [ $num1 -gt $num3 ]
then
	echo "Num1 = $num1 is max"
fi
```
