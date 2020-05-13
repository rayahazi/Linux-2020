## Increment value

#### Post increment:

Post increment will change the value of the variable only after the line finished executing.

```
x = 1
print(x++) # 1
print(x)   # 2
```

#### Pre increment:

Pre increment will change the value of the variable, and after that, will execute the entire line.

```
x = 1
print(++x) # 2
print(x)   # 2
```

- Example in bash:

```bash
#! /bin/bash

num=1

echo $num 	# 1

num=$(expr $num + 1)
echo $num 	# 2

echo '------- post increment----------'
((num++))
echo $num 	# 3

echo $((num++)) # 3
echo $num 	# 4

echo $[num++]   # 4
echo $num	# 5

echo '------- pre increment-----------'
num=2
((++num))
echo $num 	# 3

echo $((++num)) # 4
echo $num	# 4

echo $[++num]   # 5
echo $num	# 5

```

## Decrement value

#### Post decrement:

Post decrement will change the value of the variable only after the line finished executing.

```
x = 5
print(x--) # 5
print(x)   # 4
```

#### Pre decrement:

Pre increment will change the value of the variable, and after that, will execute the entire line.

```
x = 5
print(--x) # 4
print(x)   # 4
```

- Example in bash:

```bash
#! /bin/bash

num=10

echo $num 	# 10

echo '------- expr: ----------'

num=$(expr $num - 1)
echo $num 	# 9

echo '------- post decrement----------'
((num--))
echo $num 	# 8

echo $((num--)) # 8
echo $num 	# 7

echo $[num--]   # 7
echo $num	# 6

echo '------- pre decrement-----------'
num=8
((--num))
echo $num 	# 7

echo $((--num)) # 6
echo $num	# 6

echo $[--num]   # 5
echo $num	# 5
```
