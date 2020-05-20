# File or directory:

#### `-f` = file, `-d` = directory, `-e` = file or directory

- Syntax:

```bash
if [[ -f <file> ]]
then
	echo "<file> exists as a file!"
fi
```

- Check if "/etc/passwd" exists, and a file:

```bash
#! /bin/bash

if [[ -f "/etc/passwd" ]] # return boolean value
then
	echo "/etc/passwd - exists as a file!"
fi

```

- Short check:

```bash
#! /bin/bash

[[ -f "/etc/passwd" ]] && echo "/etc/passwd - exists as a file!"

[ -f "/etc/passwd" ]   && echo "/etc/passwd - exists as a file!"

```

- Check multiple files:

```bash
#! /bin/bash

File1="check1.txt"
File2="check2.txt"

if [ -f $File1 ] && [ -f $File2 ]
then
	echo "Both exists and are files"
fi
```

- Check with `not` gate = !

```bash
#! /bin/bash


# Check multiple files:

File1="check1.txt"
File2="check2.txt"

if [ ! -f $File1 ] && [ ! -f $File2 ]
then
	echo "Both do not exist!"
fi


[ ! -f $File1 ] && echo "file does not exists"
```

- Check for directories

```bash
#! /bin/bash

# Check if a file exists, and a directory:

D1="/etc"

if [ -d $D1 ]
then
	echo "$D1 exists and a directory"
fi


D2="/home"
[ -d $D2 ] && echo "$D2 exists and a directory"
```

- `-e` - check if file or folder exists:

```bash
#! /bin/bash

File="/home"

if [ -e $File ]
then
	echo "Exists! can be both file and dir."
fi
```
