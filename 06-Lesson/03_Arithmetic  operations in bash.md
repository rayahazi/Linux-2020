# Arithmetic operations in bash

### First way: `[ ]`

```bash
#! /bin/bash

echo Enter num1
read n1

echo Enter num2
read n2

echo "The numbers are:"
echo n1 = $n1
echo n2 = $n2

# Arithmetic first way:
echo 'n1 + n2 =' $[$n1+$n2]
echo 'n1 - n2 =' $[$n1-$n2]
echo 'n1 * n2 =' $[$n1*$n2]
echo 'n1 / n2 =' $[$n1/$n2]
echo 'n1 % n2 =' $[$n1%$n2]
```

- Result:

```bash
Enter num1
5
Enter num2
7
The numbers are:
n1 = 5
n2 = 7
n1 + n2 = 12
n1 - n2 = -2
n1 * n2 = 35
n1 / n2 = 0
n1 % n2 = 5
```

### Second way: `(( ))`

```bash
#! /bin/bash

echo Enter num1
read n1

echo Enter num2
read n2

echo "The numbers are:"
echo n1 = $n1
echo n2 = $n2


echo -e "\nArithmetic operations:"
# Arithmetic second way:
echo 'n1 + n2 =' $(($n1+$n2))
echo 'n1 - n2 =' $(($n1-$n2))
echo 'n1 * n2 =' $(($n1*$n2))
echo 'n1 / n2 =' $(($n1/$n2))
echo 'n1 % n2 =' $(($n1%$n2))

```

- Boolean expressions:

```bash
#! /bin/bash

echo Enter num1
read n1

echo Enter num2
read n2

echo "The numbers are:"
echo n1 = $n1
echo n2 = $n2

echo -e "\nBoolean operations:"

echo 'n1==n2: ' $(($n1==$n2))
echo 'n1!=n2: ' $(($n1!=$n2))
echo 'n1>=n2: ' $(($n1>=$n2))
echo 'n1>n2: '  $(($n1>$n2))
echo 'n1<=n2: ' $(($n1<=$n2))
echo 'n1<n2: '  $(($n1<$n2))
```

### third way: `expr`

> expr (1) - evaluate expressions

```bash
#! /bin/bash

echo Enter num1
read n1

echo Enter num2
read n2

echo "The numbers are:"
echo n1 = $n1
echo n2 = $n2

echo -e "\nexpr operations:"

echo 'n1 + n2 = ' $(expr $n1 + $n2)
echo 'n1 - n2 = ' $(expr $n1 - $n2)
echo 'n1 * n2 = ' $(expr $n1 \* $n2)
echo 'n1 / n2 = ' $(expr $n1 / $n2)
echo 'n1 % n2 = ' $(expr $n1 % $n2)

```
* Boolean expressions with `expr`:
```bash
#! /bin/bash

echo Enter num1
read n1

echo Enter num2
read n2

echo "The numbers are:"
echo n1 = $n1
echo n2 = $n2

echo -e "\nBoolean operations:"

echo 'n1==n2: ' $(expr $n1 = $n2)
echo 'n1!=n2: ' $(expr $n1 != $n2)
echo 'n1>=n2: ' $(expr $n1 \>= $n2)
echo 'n1>n2 : '  $(expr $n1 \> $n2)
echo 'n1<=n2: ' $(expr $n1 \<= $n2)
echo 'n1<n2 : '  $(expr $n1 \< $n2)
```

