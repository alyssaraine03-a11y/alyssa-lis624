# helpful tips will be added here for troubleshooting or common questions #
## nano commands ##
- Ctrl+S Save current file
- Ctrl+O Offer to write file ("Save as")
- Ctrl+R Insert a file into current one
- Ctrl+X Close buffer, exit from nano
- Ctrl+L Refresh the screen
new file: nano new_filename
## grep commands/usage ##
*grep is a placeholder for search, so when you say grep "chrome" operatingsystems.csv, you're saying search (for) "chrome" (in) this file*
- -i: ignore case sensitivity (-v is the inverse)
- ^ removes first line of text, $ removes last
- | is an boolean or search, you can search for a or b like "a|b"
- -w will turn up the exact word, not just parts of words
*q is a quick exit*
## using sudo/apt ##
- 'apt search' is a searching tool. using 'apt search tldr' filters out extra info, only gives cut and dry
- 'sudo reboot now' if it says your system needs a reboot.

*to locate and search software*
- apt search <package_name>
- apt show <package_name>
- sudo apt install <package_name>

*to remove software and purge related files*
- sudo apt --purge remove <package_name>
- sudo apt autoremove
- sudo apt clean

*to keep system up to date*
- sudo apt update
- sudo apt upgrade
- sudo apt autoremove
- sudo apt clean

## mysql

to login to the database: 
- sudo mysql -u root
- /c clears current input

user_name@computer_name:path$ is what you use so lyssaraine03@spring624alyssa:path$

*mysql always needs to end commands w semicolon;* 

use a forward slash!!!! copy this

\q

to exit mysql

if you get stuck ctrl + c

