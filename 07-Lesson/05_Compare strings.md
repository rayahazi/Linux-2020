# Compare strings

- `=` - equal (use with test command [ ] )
- `==` - equal (use with pattern matching command [[ ]] )
- `!=` - not equal
- `>` - greater than
- `<` - smaller than

```bash
#! /bin/bash

str1="Hello"
str2="Hello user"

if [ "$str1" = "$str2" ]; then
	echo "Equal"
else
	echo "Not equal"
fi
```

```bash
#! /bin/bash

read -p "Enter first string: " str1
read -p "Enter second string: " str2

if [[ "$str1" == "$str2" ]]; then
	echo "Equal"
else
	echo "Not equal"
fi
```

- This code will be short check to compare two strings:

```bash
#! /bin/bash

read -p "Enter first string: " str1
read -p "Enter second string: " str2

# Shorter if:
[[ $str1 == $str2 ]] && echo "Equal" || echo "Not equal"

# true && true  -> true.
# false && true -> false
# false || true -> true
```
