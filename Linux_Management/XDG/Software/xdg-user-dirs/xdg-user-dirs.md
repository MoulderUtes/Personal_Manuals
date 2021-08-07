# xdg-user-dirs
*Because organization is best*

[https://www.freedesktop.org/wiki/Software/xdg-user-dirs/](https://www.freedesktop.org/wiki/Software/xdg-user-dirs/)
## Theory 
When a new user logs in they do not have a home directory file structure. This tool will create that structure. When they have that structure they will be much more likely to use it and organize.
## Installation
Package is avable on most repos. 
1. Install via package manager with name xdg-user-dirs
    * Debian 
    ```shell
    sudo apt install xdg-user-dirs
    ```
    * Arch 
    ```shell
    sudo pacman -S xdg-user-dirs
    ```
## Configuration
### System wide 
located at `/etc/xed/user-dirs.conf`
* `enabled={True/False}`
    * Enables or disables the program at login
* `filename_encoding={charset encoding}`
    * what language the files will be written in (UTF-8 for english american)
### Per User
located at `$HOME/.config/user-dirs.dirs` with key value pairs
* XDG_XXX_DIR="$HOME/YYY"

## *[Back to Overview](../overview.md)*