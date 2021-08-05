# File Structure
*Grep does not work for everything*
---
## Theory
The method outlined here is going to be Hierarchical. That means organized by topic or project with sub folders further breaking it down. Some exceptions will be made in regards to things like photos which will be organized via date or as specified.
## Rules to follow
1. When in doubt make a new topic
2. Follow the naming conventions outlined in style guide
2. If a standard exists already use that standard (naming conventions/ file structure/ XDG)
2. Use a archive folder/partition/drive don't be looking through last years school work
3. Try to limit the depth of folders to 6 
3. Try to limit the breadth of folders to 12 (Some exceptions for things like /home)
## Examples
School Work would be broken up as follows
* School
    * Class
        * Project
            * For larger projects by file type (i.e. Images, PDF, src, docs)
                * End file

Computer Projects should all be set up in git repos (even if they arn't going to be published). 

Mandatory 
* README
* CHANGELOG
* LICENSE,
* .gitignore

Structure

* data
* legacy (optional)
* tests
* thirdparty (for external libraries)
* tools
    * data_integration
    * data_scraping
    * development
* ui (optional)
* wiki