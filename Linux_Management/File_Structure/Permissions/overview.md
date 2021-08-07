# Permissions
*Because you don't want you sys admin finding that "homework" folder*

[Good Reference](https://www.linux.com/training-tutorials/understanding-linux-file-permissions/)
## Theory
File permissions in linux is one of the most important aspects of security. Without permissions any user with local access has the power of root. Every single linux user needs to learn about and how to set permissions.
## Overview
Linux permissions are broken down in to three abilities
* read - who can read the contents of a file
* write - who can write or modify a file
* execute - who can execute a file or view the contents of a directory
There are also three user based permission classes
* owner - owner permissions apply to only and owner of the file or directory
* group - group permissions apply to the group assigned to the file or directory
* all users - all users permissions apply to all other users on the system
## Viewing Permissions
To view permissions either use a GUI file manager or the **ls** command. `ls -l` will display who owns the file or folder of the current working directory (you can specify what directory or file to show by using `ls -l {directory}`). It will display the permissions in the following format:
```sh
_rwxrwxrwx 1 owner:group
```
1. User rights/Permissions
    1. First character  "_" is the special permission flag
    2. following "rwx" is the owner permissions
    3. second set of "rxw" is the group permissions
    4. third set of "rxw" is the All Users permission
2. Following number shows number of hardlinks (alternate names essentially) to the file
3. Finally the owner and group class assignments in `owner:group`
## Modifying Permissions
To modify permissions we use the **chmod** command. There are two ways to use chmod, explicitly defining and using binary references.
### Symbolic Syntax 
Each of the three user based permission classes has a letter assigned to it:
* u - owner
* g - group
* a - all (ugo)
* o - all others
Next use a + or - to denote if you ant to add or remove permission

Then state the permission type or types
* r - read
* w - write
* x - execute

Example: `chmod o-rw file1`

This would remove the read and write permissions for file 1 from all users not included in the owner and group class.  
### Binary References 
This is the faster way of changing permissions. It is done using binary code instead of symbolic letters. Each ability has a number associated with it:
* read = 4
* write = 2
* execute = 1

Each class gets the sum of these abilities i.e; for read write and execute permissions it would be 7 (4+2+1). Then all the class numbers are suck together in the order of user, group, others or ugo. 

Example: for everyone to have read write and execute permissions on a file use `chmod 777 file1`

Heres a handy chart for reference

 | # | Sum | rwx | Permission |
 |  -----------  |  -----------  |  -----------  |  -----------  |
 | 7 | 4(r) + 2(w) + 1(x) | rwx | read, write and execute |
 | 6 | 4(r) + 2(w) | rw- | read and write |
 | 5 | 4(r) + 1(x) | r-x | read and execute |
 | 4 | 4(r) | r-- | read only |
 | 3 | 2(w) + 1(x) | -wx | write and execute |
 | 2 | 2(w) | -w- | write only |
 | 1 | 1(x) | --x | execute only |
 | 0 | 0 |  | --- | none |
