# seq - sequence

seq - print a sequence of numbers

- Use 1 number: `[end]` returns all the nubmers from 1 - the number.

* default start number: `1`

```bash
raya@raya-VirtualBox:~$ seq 3
1
2
3
```

- Use 2 numbers: `[start] [end]` returns all the numbers from num1 to num2 (including both).

```bash
raya@raya-VirtualBox:~$ seq 2 5
2
3
4
5

```

- Use 3 numbers: `[start] [range] [end]`. returns all the numbers from start number to end number - in range of the middle number.

```bash
raya@raya-VirtualBox:~$ seq 0 5 50
0
5
10
15
20
25
30
35
40
45
50
```

- `seq -s` - allows to determine which separator will be between the values.

```bash
raya@raya-VirtualBox:~$ seq -s " " 10
1 2 3 4 5 6 7 8 9 10
raya@raya-VirtualBox:~$ seq -s ", " 10
1, 2, 3, 4, 5, 6, 7, 8, 9, 10
```

- `seq -w` - adds padding to the numbers with 0 prefix.

```bash
raya@raya-VirtualBox:~$ seq -w 5 10
05
06
07
08
09
10
```
