# string length

```bash
#! /bin/bash

# string length:

str="This is a linux course"

len=${#str}

echo "str: $str, len: $len"
```

- Use `expr`:

```bash
#! /bin/bash

str="This is a linux course"

len=`expr length "$str"`

echo "str: $str, len: $len"
```
