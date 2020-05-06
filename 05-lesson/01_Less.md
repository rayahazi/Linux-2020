# Less

Show large files in nice window. (From begining to end, and not the oopsite).

> Less  is  a  program similar to more, but it has many more features.

- Enter the folder:

```bash
cd /usr/share/common-licenses/
```

- Show the content of `GPL-3`

```bash
cat GPL-3
```

- Show the content using `less` command

```bash
less GPL-3
```

- Simple way:

```bash
less /usr/share/common-licenses/GPL-3
```

### PIPE - `|`

Pipe - can redirect the output from the first command to the second command.

```bash
[Command 1] | [Command 2]
```

- `ps aux` will output all the proceses. we redirect the output to the command `less`, so we can see the output in a better way.

```bash
ps aux | less
```

### less -N

- Show the output with line numbers.

```bash
less -N /usr/share/common-licenses/GPL-3
```

### less +(number)

This command will start the output from the requsted line. (in this example: 10).

```bash
less -N +10 /usr/share/common-licenses/GPL-3
```
