# Chmod
*Because you don't want your users deleting /*

[Manual](https://www.gnu.org/software/coreutils/manual/html_node/chmod-invocation.html#chmod-invocation)

**Table of Contents**
- [Chmod](#chmod)
  - [Theory](#theory)
  - [Format](#format)
  - [Overview](#overview)
  - [Modifying Permissions](#modifying-permissions)
    - [Symbolic Syntax](#symbolic-syntax)
    - [Binary References](#binary-references)
  - [Options](#options)
  - [Advanced Permissions](#advanced-permissions)
    - [Special Permissions Flag](#special-permissions-flag)
    - [Setuid/Setguid](#setuidsetguid)
    - [Sticky](#sticky)
  - [*Back to Overview*](#back-to-overview)
## Theory
chmod is designed to change the permissions of a file or directory. Without chmod the world of linux would be exposed to every single security risk known to man.
## Format
```sh
chmod [OPTION] MODE FILE
```
## Overview
Linux permissions are broken down in to three abilities
* read - who can read the contents of a file
* write - who can write or modify a file
* execute - who can execute a file or view the contents of a directory
There are also three user based permission classes
* owner - owner permissions apply to only and owner of the file or directory
* group - group permissions apply to the group assigned to the file or directory
* all users - all users permissions apply to all other users on the system
chmod is designed to manage these permissions
## Modifying Permissions
To modify permissions we use the **chmod** command. There are two ways to use chmod, explicitly defining and using binary references.
### Symbolic Syntax 
Each of the three user based permission classes has a letter assigned to it:
* u - owner
* g - group
* a - all (ugo)
* o - all others
Next use a +, -, or = to denote if you ant to add, remove, or set the class as the same for the permissions

Then state the permission type or types
* r - read
* w - write
* x - execute
* X - execute but only applys to files with a execute permission already set on any class
* s - [setuid/setguid](#setuidsetguid)
* t - [sticky](#sticky)

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
## Options
* -c --changes - prints out changes
* -f --silent --quiet - suppresses most error messages
* -v --verbose - outputs diag file
* --dereference - affects referent of each symbolic link (default)
* -h -no-dereference - affects symbolic link not the referent
* --from=CURRENT_OWNER:CURRENT_GROUP - only changes if the current owner and group equal the one defined
* --no-preserve-root - don't treat / specially (default)
* --preserve-root - do not operate recursively on root /
* --reference=RFILE - use RFILE's owner and group instead of specifying it
* -R --recursive - operate on files and directories recursively
* --help - display help
* --version - display current version

## Advanced Permissions
### Special Permissions Flag
* _ - no special permissions
* d - directory
* l - symbolic link
* s - setuid/setguid permissions (represented as an s in read portion of owner:group permissions)
* t - sticky bit permissions (represented as an t in executable portion of all user permissions)
### Setuid/Setguid 
Setuid/Setguid tells the system to run a program as the owner with their permissions. DON'T SET THIS SPECIAL PERMISSION TO A FILE OWNED BY ROOT, IT OPENS UP A MASSIVE SECURITY HOLE!!!!

To set the setuid/setguid bit you have to use the symbolic syntax mode of chmod. Simply use s in place of a r,w,or x along with a user or group symbol. `chmod u+s file1`
### Sticky 
When the sticky bit is set only the owner can remove or rename files. This is useful when you are in a shared directory. 
## *[Back to Overview](../overview.md)*