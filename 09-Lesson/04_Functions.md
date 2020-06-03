# Functions in bash

why use functions?

- Avoid code repetition.

### Syntax

```bash
function func_name{

}

# or:
func_name(){

}
```

## Examples:

```bash
#! /bin/bash

func(){
	echo
	echo "This is my first func()"
	echo
}

func
```

#### Call function before declaration:

```bash
#! /bin/bash


func1(){
	echo "I am func1"
	func2
}

func1 #- error!

func2(){
	echo "I am func2"
}

func1

```

- Output:

```bash
raya@raya-VirtualBox:~/Desktop/Lesson09$ ./a.bash
I am func1
./a.bash: line 6: func2: command not found
I am func1
I am func2
```

#### Function parameters:

```bash
#! /bin/bash


func1(){
	echo "I am func1"
	echo "My variables: $1"
}

func1 123

# -------------------------------

func2(){
	echo "I am func2"
	echo "Person: $2 is $1 years old"
}

AGE=40
NAME="Bob"

func2 $AGE $NAME
```

- Output:

```bash
raya@raya-VirtualBox:~/Desktop/Lesson09$ ./a.bash
I am func1
My variables: 123

I am func2
Person: Bob is 40 years old
```

#### empty functions

```bash
#! /bin/bash

# empty functions - functions cannot be empty

empty(){}

# ./a.bash: line 5: syntax error near unexpected token `{}'
# ./a.bash: line 5: `empty(){}'

```

- a function with only comments is empty

```bash
#! /bin/bash

# empty functions - functions cannot be empty

empty()
{
	# comment1
	# comment2
	# comment3
}

```

- Use **:** as Null value:

```bash
#! /bin/bash

# empty functions - functions cannot be empty

hasNull()
{
	: # null command
}

hasNull
```

- call nested functions:

```bash
#! /bin/bash

# empty functions - functions cannot be empty

n1()
{
	n2()
	{
		echo "I am n2"
	}
}

# n1 is defined globally. known to all the page.
# n2 is defined locally. known only inside n1()

# n2 - error message.

n1 # empty function.
n2 # I am n2
```
