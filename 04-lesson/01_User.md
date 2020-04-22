# User in linux

### whoami
whoami - print effective userid

```bash
raya@raya-VirtualBox:~$ whoami
raya
```

### Sudo -i / su / sudo su
`sudo -i` will change the user to a `root` user.

That will give us the permissions of a super-user (Similar to Administrator in windows)

sudo, sudoedit — execute a command as another user
```bash
raya@raya-VirtualBox:~$ sudo -i
[sudo] password for raya: 
root@raya-VirtualBox:~# whoami
root
```
---
# Add a new user:
### useradd
* Try to add a user to the system, but we have no permissions: 
```bash
raya@raya-VirtualBox:~$ useradd john
useradd: Permission denied.
useradd: cannot lock /etc/passwd; try again later.
```
* Use `sudo` before a command, and we can add a user. 
```bash
raya@raya-VirtualBox:~$ sudo useradd john
[sudo] password for raya: 
```
### passwd
passwd - change user password

```
raya@raya-VirtualBox:~$ sudo passwd john
Enter new UNIX password: 
Retype new UNIX password: 
passwd: password updated successfully
```
##### see the user in `/etc/passwd` file. 

```sh
passwd (1ssl)        - compute password hashes
```
* Open the file `/etc/passwd`
```bash
cat /etc/passwd
```
* This is the output from `/etc/passwd` for user `john`
```bash
john:x:1002:1002::/home/john:/bin/sh
```
```sh
root:x:0:0:root:/root:/bin/bash
```
#### Structure of `/etc/passwd`
We have 7 columns, and each one has a meaning:
* **Username** - user login name used to login into a system. It could be between 1 to 32 character long. 
* **Password** - User password (or x character) stored in `/etc/shadow` file in encrypted format
* **User ID (UID)** - every user must have UID. By default UID 0 is reserved for `root` user
* **Group ID (GID)** - The primary gorup id is stored in `/etc/group` file
* **User info** - this field is optional and allow you to define extra information about the user. For example: user full name. 
* **Home directory** - The absolute path to the user's home direcory
* **Shell** - The absolute location of a user's shell. `/bin/sh`

---

#### Add user with specific `UID`

```bash
raya@raya-VirtualBox:~$ man useradd

 -u, --uid UID
           The numerical value of the user's ID. This value must be unique, unless the -o option is used. The value must be non-negative. The default
           is to use the smallest ID value greater than or equal to UID_MIN and greater than every other user.

```
* The command:
```bash
sudo useradd -u 555 paul
```

* in `/etc/passwd` we can see that the `UID` is 555 
```bash
paul:x:555:1003::/home/paul:/bin/sh
```

### Userdel
userdel - delete a user account and related files

```bash
sudo userdel paul 
[sudo] password for raya: 
```

## Structure of `/etc/shadow` file
`/etc/shadow` file stores the actuall passwords in encrypted format. (The hash of a password). 

```bash
raya:$6$oloCWpfW$q4beNkhVne7Bzy67kt8dkC83JfPG2LjauphiIWFFTz8q58QYsDq//e8psyTdjJhHsV8kTDjqPIkzp6I5N6QRv0:18342:0:99999:7:::
```
* **Username** - it is the login name of a user. 
* **Password** - it is the encrypted password. The password should be minimum 8-12 digits(there are other linux distributions that allow less than 8 digits)
Usually password format is set to `$id$salt$hashed`. 

    the `id`:
    
        1. `$1$` is MD5
        
        2. `$2a$`, `$2y$` is Blowfish
        
        3. `$5$` is SHA-256
        
        4. `$6$` is SHA-512

```
$6$oloCWpfW$q4beNkhVne7Bzy67kt8dkC83JfPG2LjauphiIWFFTz8q58QYsDq//e8psyTdjJhHsV8kTDjqPIkzp6I5N6QRv0
```
