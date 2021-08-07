# GNU Core Utilities 
*Because how else am I going to make a directory*

[GNU.org](https://www.gnu.org/software/coreutils/)

[Manual](https://www.gnu.org/software/coreutils/manual/html_node/index.html)

**Table of Contents**
- [GNU Core Utilities](#gnu-core-utilities)
  - [Theory](#theory)
  - [Utilities](#utilities)
    - [Output of entire files](#output-of-entire-files)
    - [Formatting File Contents](#formatting-file-contents)
    - [Output of Parts of Files](#output-of-parts-of-files)
    - [Summarizing Files](#summarizing-files)
    - [Operating on Sorted Files](#operating-on-sorted-files)
    - [Operating on Fields](#operating-on-fields)
    - [Operating on characters](#operating-on-characters)
    - [Directory Listing](#directory-listing)
    - [Basic Operations](#basic-operations)
    - [Special File Types](#special-file-types)
    - [Changing File Attributes](#changing-file-attributes)
    - [Disk Usage](#disk-usage)
    - [Printing Text](#printing-text)
    - [Conditions](#conditions)
    - [Redirection](#redirection)
    - [File Name Manipulation](#file-name-manipulation)
    - [Working Context](#working-context)
    - [User Information](#user-information)
    - [System Context](#system-context)
    - [SELinux Context](#selinux-context)
    - [Modified Command Innovation](#modified-command-innovation)
    - [Process Control](#process-control)
    - [Delaying](#delaying)
    - [Numeric Operations](#numeric-operations)
## Theory
GNU has created these core utilities in order to manage *nix operating systems. When most people create a linux operating system they really create GNU/Linux. Which is the linux kernel with the utilities stolen from the GNU operating system.
## Utilities
### Output of entire files
* cat - concatenate and write files
* tac - concatenate and write files in reverse
* nl - number lines and write files
* od - write files in octal or other formats
* base32 - transform data into printable data
* base64 - transform data into printable data
* basenc - transform data into printable data
### Formatting File Contents
* fmt - reformat paragraph text
* pr - paginate or columnate file for printing
* fold - wrap input lines to fit in specified width
### Output of Parts of Files
* head - output the first part of files
* tail - output the last part of files
* split - split a file into pieces
* csplit - split a file into context-determined pieces
### Summarizing Files
* wc - print newline, word, and byte counts
* sum - print checksum and block counts
* cksum - print CRC checksum and byte counts
* b2sum - print or check BLAKE2 digests
* md5sum _ print or check MD5 digests
* sha1sum - print or check SHA-1 digests 
* sha2 utilities - print or check SHA-2 digests
### Operating on Sorted Files
* sort - sort text files
* shuf - shuffling text
* uniq - uniquify files
* comm - compare two sorted files line by line
* ptx - produce permuted indexes
* tsort - topological sort
### Operating on Fields
* cut - print selected parts of lines
* paste - merge lines of fields
* join - join lines on a common field
### Operating on characters
* tr - translate, squeeze, and/or delete characters
* expand - convert tabs to spaces
* unexpand - convert spaces to tabs
### Directory Listing
* ls - list directory contents
* dir - briefly list directory contents
* vdir - verbosely list directory contents
* dircolors - color setup for ls
### Basic Operations
* cp - copy files and directories
* dd - convert and copy a file
* install - copy files and set attributes
* mv - move (rename) files
* rm - remove files or directories
* shred - remove files more securely
### Special File Types
* link - make a hard link via the syscall
* ln - make links between files
* mkdir - make directories
* mkfifo - make FIFOs (named pipes)
* mknod - make block or character special files
* readlink - print value of a symlink or canonical file name
* unlink - remove files via the unlink syscall
### [Changing File Attributes](Changing_File_Attributes)
* [chown](Changing_File_Attributes/chown.md) - change file and owner group
* [chgrp](Changing_File_Attributes/chgrp.md) - change group ownership
* [chmod](Changing_File_Attributes/chmod.md) - change access permissions
* touch - change file timestamps
### Disk Usage
* df - report file system disk space usage
* du - estimate file space usage
* stat - report file or file system status
* sync - synchronize cached writes to persistent storage
* truncate - shrink or extend the size of a file
### Printing Text
* echo - print a line of text
* printf - format and print data
* yes - print a string until interrupted
### Conditions
* false - do nothing, unsuccessfully
* true - do nothing, successfully
* test - check file types and compare values
* expr - evaluate expressions
### Redirection
* tee - redirect output to multiple files or processes
### File Name Manipulation
* basename - strip directory and suffix from a file name
* dirname - strip last file name component
* pathchk - check file name validity and portability
* realpath - print the resolved file name
### Working Context
* pwd - print working directory
* stty - print or change terminal characteristics
* printenv - print all or some environment variables
* tty - print file name of terminal on standard input
### User Information
* id - print user identity
* logname - print current login name
* whoami - print effective user ID
* groups - print group names a user is in
* users - print login names of user currently logged in
* who - print who is currently logged in
### System Context
* date - print or set system data and time
* arch - print machine hardware name
* nproc - print number of available processors
* uname - pint system information
* hostname - print or set system name
* hostid - print numeric host identifier
* uptime - print system uptime and load
### SELinux Context
* chcon - change SELinux context of file
* runcon - run a command in specified SELinux context
### Modified Command Innovation
* chroot - run a command with a different root directory
* env - run a command in a modified environment
* nice - run a command with modified niceness
* nohup - run a command immune to hangups
* stdbuf - run a command with modified I/O stream buffering
* timeout - run a command with a time limit
### Process Control
* kill - send a signal to processes
### Delaying
* sleep - delay for a specified time
### Numeric Operations
* factor - print prime factors
* numfmt - reformat numbers
* seq - print numeric sequences


