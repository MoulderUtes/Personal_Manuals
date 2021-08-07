# Base Directory Specification
*Because who loves a clean home directory*

[https://specifications.freedesktop.org/basedir-spec/latest/index.html#introduction](https://specifications.freedesktop.org/basedir-spec/latest/index.html#introduction)
## Introduction
>Various specifications specify files and file formats. This specification defines where these files should be looked for by defining one or more base directories relative to which files should be located.
## Environment Variables
 * \$XDG_DATA_HOME - \$HOME/.local/share
    * User specific data files
* \$XDG_CONFIG_HOME - \$HOME/.config
    * Configuration files
* **\$XDG_STATE_HOME - \$HOME/.local/state**
    * Data persistent between application restarts but not \$XDG_DATA_HOME important
* User-Specific executable files - \$HOME/.local/bin
    * Reserved for user specific binaries or other tools (NOT AppImages)
* \$XDG_DATA_DIRS - /usr/local/share/:/usr/share/
    * Order of data directories to look in for data files
* **\$XDG_CONFIG_DIRS - /etc/config:/etc/xdg**
    * Order of data directories to look for config files
* \$XDG_CACHE_HOME - \$HOME/.cache
    * User specific non-essential data files
* \$XDG_RUNTIME_DIR - /run/user/$(id -u)
    * User specific non-essential runtime files


## *[Back to Overview](../overview.md)*