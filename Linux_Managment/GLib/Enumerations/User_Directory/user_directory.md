# User Directory
*Because who wants your downloads in your raw home directory*

[https://docs.gtk.org/glib/enum.UserDirectory.html](https://docs.gtk.org/glib/enum.UserDirectory.html)
## Theory
These enumerations as GLib calls it or environment variables, can be used in programs to find the location of common locations for folders. This way programs know where to place or look for files across operating systems.
## Description 
>These are logical ids for special directories which are defined depending on the platform used. You should use g_get_user_special_dir() to retrieve the full path associated to the logical id.

>The GUserDirectory enumeration can be extended at later date. Not every platform has a directory for every logical id in this enumeration.
## Members
* G_USER_DIRECTORY_DESKTOP - \$HOME/Desktop
    * The user’s Desktop directory
* G_USER_DIRECTORY_DOCUMENTS - \$HOME/Documents
    * The user’s Documents directory
* G_USER_DIRECTORY_DOWNLOAD - \$HOME/Downloads
    * The user’s Downloads directory
* G_USER_DIRECTORY_MUSIC - \$HOME/Music
    * The user’s Music directory
* G_USER_DIRECTORY_PICTURES - \$HOME/Pictures
    * The user’s Pictures directory
* G_USER_DIRECTORY_PUBLIC_SHARE - \$HOME/Public
    * The user’s shared directory
* G_USER_DIRECTORY_TEMPLATES - \$HOME/Templates
    * The user’s Templates directory
* G_USER_DIRECTORY_VIDEOS - \$HOME/Videos
    * The user’s Movies directory
* G_USER_N_DIRECTORIES - 8
    * The number of enum values


#### *[Back to Overview](../overview.md)*