# Chown
*Because you don't want your users deleting /*

[Manual](https://www.gnu.org/software/coreutils/manual/html_node/chown-invocation.html#chown-invocation)

**Table of Contents**
- [Chown](#chown)
  - [Theory](#theory)
  - [Format](#format)
  - [Overview](#overview)
  - [Options](#options)
  - [*Back to Overview*](#back-to-overview)
## Theory
Chown is used to change the owner and or group ownership of a file, requires root permissions
## Format
```sh
sudo chown [OPTION] [OWNER][:[GROUP]] FILE
```
## Overview
1. replace [\[OPTION\]](#options) with any of the options (optional)
2. replace \[OWNER] with the user id of the new owner (optional)
3. replace [:\[GROUP]] with the guid id of the new group (optional)
4. select the file or directory to change
5. to use reference file use `--reference=RFILE` option where RFILE is the file or directory whose ownership you want to copy (leave owner and group sections empty)

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
* -H - if recursive(-R) is set and the file/directory chown is pointed to is a symbolic link transverse it
* -L - recursive transversal traverses every symbolic link to a directory that is encountered
* -P - do not transverse any symbolic links (default)

## *[Back to Overview](../overview.md)*