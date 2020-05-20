# If statement

If statement gives a condition - that returns only boolean value - true / false.

## Numbers:

- `-gt` - greater than
- `-ge` - greater equal
- `-lt` - less than
- `-le` - less equal
- `-ne` - not equal
- `-eq` - equal

```bash
#! /bin/bash

Num1=10

if [ $Num1 -ge 10 ]
then
	echo "Num1: $Num1 is greater than 10"
fi
```

## Strings

- `=` - equal
- `!=` - not equal
- `>` - greater than
- `<` - smaller than

```bash
#! /bin/bash


if [ "Hello world" = "hello world" ]
then
	echo "Hello world" = "Hello world"
fi

```
