# While

- loop over counter 4 times, and increment the conuter in 1 each round, using `expr` - to convert the conuter to a number:

```bash
#! /bin/bash

counter=0

while [ "$counter" -lt 4 ]
do
	echo "Round number: $counter"
	counter=`expr $counter + 1`
done

echo "Finished while loop: counter =  $counter"

# Round number: 0
# Round number: 1
# Round number: 2
# Round number: 3
# Finished while loop: counter =  4
```
