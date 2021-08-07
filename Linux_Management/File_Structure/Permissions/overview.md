# Permissions
*Because you don't want you coworkers finding that "homework" folder*

[Good Reference](https://www.linux.com/training-tutorials/understanding-linux-file-permissions/)

**Table of Contents**
- [Permissions](#permissions)
  - [Theory](#theory)
  - [Overview](#overview)
  - [Viewing Permissions](#viewing-permissions)
  - [Modifying Permissions](#modifying-permissions)
  - [Changing Owner/Group](#changing-ownergroup)
    - [Chgrp](#chgrp)
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
To modify permissions we use the **chmod** command. Refer to [chmod](../../GNU/Core_Utils/Changing_File_Attributes/chmod.md)
## Changing Owner/Group
Use `chown` command to modify owner or group. (requires root privileges). See [chown](../../GNU/Core_Utils/Changing_File_Attributes/chown.md)
### Chgrp
se `chgrp` command to modify the group. See [chgrp](../../GNU/Core_Utils/Changing_File_Attributes/chgrp.md)

UMASK