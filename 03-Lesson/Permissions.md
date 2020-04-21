# Permissions - הרשאות 

<img src="https://www.guru99.com/images/PermissionsConcept.png"/>

## Ownership of Linux files
Every file and directory on your Unix/Linux system is assigned 3 types of owner, given below.

#### User
A user is the owner of the file. By default, the person who created a file becomes its owner. Hence, a user is also sometimes called an owner.

#### Group
A user- group can contain multiple users. All users belonging to a group will have the same access permissions to the file. Suppose you have a project where a number of people require access to a file. Instead of manually assigning permissions to each user, you could add all users to a group, and assign group permission to file such that only this group members and no one else can read or modify the files.

#### Other
Any other user who has access to a file. This person has neither created the file, nor he belongs to a usergroup who could own the file. Practically, it means everybody else. Hence, when you set the permission for others, it is also referred as set permissions for the world.

----
## Permissions

<img src="https://www.guru99.com/images/permission(1).png">

Every file and directory in your UNIX/Linux system has following 3 permissions defined for all the 3 owners discussed above.

#### Read:
This permission give you the authority to open and read a file. Read permission on a directory gives you the ability to lists its content.
#### Write: 
The write permission gives you the authority to modify the contents of a file. The write permission on a directory gives you the authority to add, remove and rename files stored in the directory. Consider a scenario where you have to write permission on file but do not have write permission on the directory where the file is stored. You will be able to modify the file contents. But you will not be able to rename, move or remove the file from the directory.
#### Execute: 
In Windows, an executable program usually has an extension ".exe" and which you can easily run. In Unix/Linux, you cannot run a program unless the execute permission is set. If the execute permission is not set, you might still be able to see/modify the program code(provided read & write permissions are set), but not run it.

<img src='https://qph.fs.quoracdn.net/main-qimg-0f76c00cf97852795a234a730bf9e4fd' height=250/>



### Example:
<img src='https://www.guru99.com/images/FilePermissions(1).png'>

'764' absolute code says the following:

* Owner can read, write and execute
* Usergroup can read and write
* World can only read
This is shown as -rwxrw-r-

### Chmod

#### example:
```sh
chmod o+rwx b.txt 

or: chmod u=rwx
chmod u+rwx
chmod 147
```

