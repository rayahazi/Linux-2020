# Nano

nano - Nano's ANOther editor, an enhanced free Pico clone

Nano is a text editor

#### 1. `nano --version` will output the current version of nano. 
```bash
raya@raya-VirtualBox:~/Desktop/Lesson04$ nano --version
 GNU nano, version 2.9.3
 (C) 1999-2011, 2013-2018 Free Software Foundation, Inc.
 (C) 2014-2018 the contributors to nano
 Email: nano@nano-editor.org	Web: https://nano-editor.org/
 Compiled options: --disable-libmagic --disable-wrapping-as-root --enable-utf8
```

#### 2. Edit file with nano

```bash
raya@raya-VirtualBox:~/Desktop/Lesson04$ cat a.txt 
This is a
Hello dear students! I am concatenated
raya@raya-VirtualBox:~/Desktop/Lesson04$ nano a.txt 
raya@raya-VirtualBox:~/Desktop/Lesson04$ cat a.txt 
This is a
Hello dear students! I am concatenated

This line was added by nano
```

> save & exit: press `ctrl + o`(save changes), press enter, press `ctrl + x`(exit)
