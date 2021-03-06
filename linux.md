<h1 align="center">
  Cheat Sheet - <a href="https://en.wikipedia.org/wiki/Linux" target="_blank"> #Linux </a>
</h1>
<p align="center">
  My most used Linux commands
<p/>

## Indice

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [Subtitle](#subtitle)
- [Subtitle Example](#subtitle-example)
- [File Editing](#file-editing)
- [Wildcard Example](#wildcard-example)
- [File info](#file-info)
- [File / Folder Creation](#file--folder-creation)
- [Command Info](#command-info)
- [SSH Key for Remote Access](#ssh-key-for-remote-access)
- [Network Troubleshooting](#network-troubleshooting)
- [Process Management](#process-management)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Subtitle

Input             | Description
------------------|------------
**[ ]**           | Brackets only represent a user input (what you have to type)
**[file]**        | Type a file name + extension (".txt", ".css", ".js", etc)
**[folder]**      | Type a folder name
**[directory]**   | Type a directory path
**[word]**        | Type a Word
**[host]**        | Type a remote computer name + IP address (example: peterComputer@178.68.xx.x)
**[PID]**         | Type a process ID. It's a number listed in "top" or "ps" command and identifies the process
**[site]**        | Type a site name or IP address


## Subtitle Example 

* Command description: ```touch [file]```
* Desired input #1: ```touch myFile.html```
* Desired input #2: ```touch hello.txt```

Below, the commands are organized in groups:

## File Editing

Command                                 | Description 
----------------------------------------| -------------
nano **[file]**                         | Open file to edit
mv **[file]** **[file / directory]**    | Rename/move file
cp [file] **[directory]**               | Copy to directory
rm -rf **[file]**                       | Remove file (r = recursive, f = force)
rm ***[file]**                          | Wildcard: remove all files with same letter combination or extension 

## Wildcard Example

rm *[file]  | Description
------------|-------------
rm *        | Remove all files
rm *.js     | Remove all javascript files
rm a*.txt   | Remove all text files beginning with the letter "a"


## File info


Command                                 | Description 
----------------------------------------| -------------
list -l                                 | List files with detailed info (l = long)
list -a                                 | List visible & insisible files (a = all)
cat **[file]**                          | Concatenate: print file content
head **[file]**                         | Print file's first 10 lines 
tail **[file]**                         | Print file's last 10 lines
less **[file]**                         | Print file with navigation
grep **[word]** **[file]**              | Search word in file and print corresponding line
find -name **[file]**                   | Find file directory

## File / Folder Creation

Command                                 | Description 
----------------------------------------| -------------
touch **[file]**                        | Create file
mkdir **[folder]**                      | Create folder
echo **[word]** > **[file]**            | Write word inside file

## Command Info

Command                                 | Description 
----------------------------------------| -------------
man **[command]**                       | Get documentation about command
history **[command]**                   | Get the list of all typed commands
CTRL + R **[command]**                  | Reverse i-search: find command from history, based on typed input
cd ~/.bash_history                      | Go to invisible file in the HOME directory, which contains command history log

## SSH Key for Remote Access 

Command                                 | Description 
----------------------------------------| -------------
ssh-keygen                              | Create SSH key pair
ls .ssh                                 | Confirm if SSH key was created
ssh-copy-id **[host]**                  | Copy SSH key to remote computer
ssh **[host]**                          | Login remote computer with SSH

## Network Troubleshooting

Command                                 | Description 
----------------------------------------| -------------
ifconfig                                | Get network info
hostname -I                             | Get IPV4 & IPV6 info
route                                   | Check if "default" line has IP, and if so, you can contact servers outside the local network
ping **[site]**                         | Check "packet loss" summary to see if you have a good internet connection
whois **[site]**                        | Get all info about domain names registered on the Internet
whois **[site]** \| grep **[word]**     | Search for word inside "whois" command (\| = group commands together)
whois **[site]** \| head                | Get first 10 lines of "whois" command

## Process Management 

Command                                 | Description 
----------------------------------------| -------------
top                                     | List processes executing in the computer
ps                                      | Similar to "ls" command, but for processes
ps aux                                  | More detailed info to "ps" command
kill **[PID]**                          | Kill process
