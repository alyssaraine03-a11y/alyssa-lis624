# alyssa-lis624
**For spring 2026, lis 624**
what you have set up so far,
what this repo will contain,
or what you learned during this process.

This repo will contain
1. important info for my classwork
2. changes made on my server
3. helpful shortcuts, tips, and nano commands

#### I have learned to keep thorough documentation during this process. Each time I work in the server, exit it, then reopen, my history from my last open is not shown. So, I need to make sure to include the changes I used and commands I sent on this repo to keep track of my progress. If I make a mistake, I can easily reference this doc to see where I went wrong.
nano commands
- Ctrl+S   	Save current file
- Ctrl+O	Offer to write file ("Save as")
- Ctrl+R	Insert a file into current one
- Ctrl+X	Close buffer, exit from nano
- Ctrl+L	Refresh the screen
- new file: nano new_filename
  
~2/12/2026~
rebooted system on vm. used 'sudo reboot now' command. 
# grep #
its a searching tool. so grep searches line of code/text and searches for patterns. it is case-sensitive by default, so -i can ignore the case sensitivity. for example: instead of grep "chrome" operating-systems.csv you need to search grep -i "chrome" operating-systems.csv
grep -vi reverse searches 
carat key ^ removes the first line and $ removes the end of the line. 
| key in parenthesis is searching for multiple things. so "(this|that)"
-w results as a complete word so instead of os (like dos or bios) itll just pull up "os"
-A NUM (you gotta insert an actual number) will bring up the context of lines surrounding the matches. 
-n instructs grep to tell you the number for each hit. 

*added 250 documents from web of science called savedrecs.bib*
use less savedrecs.bib to view the whole doc
tried out these commands to specify lines starting with journal (aka only pulling the journal) grep -i "^journal =" savedrecs.bib | cut -d"=" -f2 |\
    sed 's/ {//' | sed 's/},//' | \
    sort | uniq -c | sort -nr
TO EXIT FILE READING MODE IN LESS 'Q' !!!

made a new nano file for the example called "operating-systems.csv"

## week 6
sudo: package manager    root: the superuser/admin
apt does not require sudo! 'apt search' doesnt modify anything, just searches. 
tldr gives common commands and easy explanations!!! apt search tldr
if you want to remove a package and extra stuff, use sudo apt --purge remove tldr
sudo apt autoremove
sudo apt clean when you install packages to free up disk space
to download .deb files (ubuntu) use the dpkg command sudo dpkg -i <file_name.deb>
# to locate and search software:
sudo apt update
apt search <package_name>
apt show <package_name>
sudo apt install <package_name>
# to remove software and purge related files 
sudo apt --purge remove <package_name>
sudo apt autoremove
sudo apt clean
# keep system up to date 
sudo apt update
sudo apt upgrade
sudo apt autoremove
sudo apt clean

