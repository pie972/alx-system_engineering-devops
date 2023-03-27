# System engineering & DevOps - Bash
# Shell Basics


# Resources
--------------------------------------------------------------------------
## Read or watch:
[What Is “The Shell”?](http://linuxcommand.org/lc3_lts0010.php) <br />
[Navigation](http://linuxcommand.org/lc3_lts0020.php) <br />
[Looking Around](http://linuxcommand.org/lc3_lts0030.php) <br />
[A Guided Tour](http://linuxcommand.org/lc3_lts0040.php) <br />
[Manipulating Files](http://linuxcommand.org/lc3_lts0050.php) <br />
[Working With Commands](http://linuxcommand.org/lc3_lts0060.php) <br />
[Reading Man pages](http://linuxcommand.org/lc3_man_pages/man1.html) <br />
[Keyboard shortcuts for Bash](https://www.howtogeek.com/181/keyboard-shortcuts-for-bash-command-shell-for-ubuntu-debian-suse-redhat-linux-etc/) <br />
[LTS](https://wiki.ubuntu.com/LTS) <br />
[Shebang](https://en.wikipedia.org/wiki/Shebang_%28Unix%29) <br />

## man or help:
* cd <br />
* ls
* pwd
* less
* file
* ln
* cp
* mv
* rm
* mkdir
* type
* which
* help
* man



# Learning Objectives
--------------------------------------------------------------------------
## General
* What does RTFM mean?
* What is a Shebang
<br />

## What is the Shell
* What is the shell
* What is the difference between a terminal and a shell
* What is the shell prompt
* How to use the history (the basics)
<br />

## Navigation
* What do the commands or built-ins ***cd***, ***pwd***, ***ls*** do 
* How to navigate the filesystem
* What are the . and .. directories
* What is the working directory, how to print it and how to change it
* What is the root directory
* What is the home directory, and how to go there
* What is the difference between the root directory and the home directory of the user root
* What are the characteristics of hidden files and how to list them
* What does the command ***cd*** - do
<br />

## Looking Around
* What do the commands ***ls***, ***less***, ***file*** do
* How do you use options and arguments with commands
* Understand the ls long format and how to display it
* [A Guided Tour](http://linuxcommand.org/lc3_lts0040.php)
* What does the ***ln*** command do
* What do you find in the most common/important directories
* What is a symbolic link
* What is a hard link
* What is the difference between a hard link and a symbolic link
<br />

## Manipulating Files
* What do the commands ***cp***, ***mv***, ***rm***, ***mkdir*** do
* What are wildcards and how do they work
* How to use wildcards
<br />

## Working with Commands
* What do ***type***, ***which***, ***help***, ***man*** commands do
* What are the different kinds of commands
* What is an alias
* When do you use the command help instead of man
<br />

## Reading Man Pages 
* How to read a man page
* What are man page sections
* What are the section numbers for User commands, System calls and Library functions
<br />

## Keyboard Shortcuts for Bash
* Common shortcuts for Bash
<br />

## LTS
* What does ***LTS*** mean?
<br />

# Requirements
--------------------------------------------------------------------------
## General
* Allowed editors: vi, vim, emacs
* All your scripts will be tested on Ubuntu 20.04 LTS
* All your scripts should be exactly two lines long ($ wc -l file should print 2)
* All your files should end with a new line ([why?](https://unix.stackexchange.com/questions/18743/whats-the-point-in-adding-a-new-line-to-the-end-of-a-file/18789))
* The first line of all your files should be exactly #!/bin/bash
* You are not allowed to use backticks, &&, || or ;
* All your scripts must be executable. To make your file executable, use the chmod command: chmod u+x file.
<br />

## More Info
Example of line count and first line
```bash
pie@ubuntu:/tmp$ wc -l 12-file_type 
2 12-file_type
pie@ubuntu:/tmp$ head -n 1 12-file_type 
#!/bin/bash
pie@ubuntu:/tmp$ 
```
In order to test your scripts, you will need to use this command: chmod u+x file. 
Example
```bash
pie@ubuntu:/tmp$ ls
12-file_type
lll
pie@ubuntu:/tmp$ ls -la lll
-rw-rw-r-- 1 pie pie 15 Mar 23 21:05 lll
pie@ubuntu:/tmp$ cat lll
#!/bin/bash
ls
pie@ubuntu:/tmp$ ls -l lll
-rw-rw-r-- 1 pie pie 15 Mar 23 21:05 lll
pie@ubuntu:/tmp$ chmod u+x lll
pie@ubuntu:/tmp$ ls -l lll
-rwxrw-r-- 1 pie pie 15 Mar 23 21:05 lll
pie@ubuntu:/tmp$ ./lll
12-file_type
lll
pie@ubuntu:/tmp$ 
```
<br /><br />


# Tasks
--------------------------------------------------------------------------
## 0. Where am I?
Write a script that prints the absolute path name of the current working directory.
Example:
```bash
$ ./0-current_working_directory
/root/alx-system_engineering-devops/0x00-shell_basics
$
```
Repo:
- GitHub repository: [alx-system_engineering-devops](https://github.com/pie972/alx-system_engineering-devops)
- Directory: [0x00-shell_basics](https://github.com/pie972/alx-system_engineering-devops/tree/master/0x00-shell_basics)
- File: [0-current_working_directory](https://github.com/pie972/alx-system_engineering-devops/blob/master/0x00-shell_basics/0-current_working_directory)



## 1. What’s in there?
Display the contents list of your current directory.
Example:
```bash
$ ./1-listit
Applications    Documents   Dropbox Movies Pictures
Desktop Downloads   Library Music Public
$
```
Repo:
- GitHub repository: [alx-system_engineering-devops](https://github.com/pie972/alx-system_engineering-devops)
- Directory: [0x00-shell_basics](https://github.com/pie972/alx-system_engineering-devops/tree/master/0x00-shell_basics)
- File: [1-listit](https://github.com/pie972/alx-system_engineering-devops/blob/master/0x00-shell_basics/1-listit)



## 2. There is no place like home
Write a script that changes the working directory to the user’s home directory.
* You are not allowed to use any shell variables
```bash
pie@ubuntu:/tmp$ pwd
/tmp
pie@ubuntu:/tmp$ echo $HOME
/home/pie
pie@ubuntu:/tmp$ source ./2-bring_me_home
pie@ubuntu:~$ pwd
/home/pie
pie@ubuntu:~$ 
```
Repo:
- GitHub repository: [alx-system_engineering-devops](https://github.com/pie972/alx-system_engineering-devops)
- Directory: [0x00-shell_basics](https://github.com/pie972/alx-system_engineering-devops/tree/master/0x00-shell_basics)
- File: [2-bring_me_home](https://github.com/pie972/alx-system_engineering-devops/blob/master/0x00-shell_basics/2-bring_me_home)



## 3. The long format
Display current directory contents in a long format
Example:
```bash
$ ./3-listfiles
total 32
-rwxr-xr-x@ 1 sylvain staff 18 Mar 23 00:19 0-current_working_directory
-rwxr-xr-x@ 1 sylvain staff 19 Mar 23 00:23 1-listit
-rwxr-xr-x@ 1 sylvain staff 18 Mar 23 00:29 2-bring_me_home
-rwxr-xr-x@ 1 sylvain staff 18 Mar 23 00:39 3-listfiles
$
```
Repo:
- GitHub repository: [alx-system_engineering-devops](https://github.com/pie972/alx-system_engineering-devops)
- Directory: [0x00-shell_basics](https://github.com/pie972/alx-system_engineering-devops/tree/master/0x00-shell_basics)
- File: [3-listfiles](https://github.com/pie972/alx-system_engineering-devops/blob/master/0x00-shell_basics/3-listfiles)



## 4. Hidden files
Display current directory contents, including hidden files (starting with .). Use the long format.
Example:
```bash
$ ./4-listmorefiles
total 32
drwxr-xr-x@ 6 sylvain staff 204 Mar 23 00:29 .
drwxr-xr-x@ 43 sylvain staff 1462 Mar 23 00:19 ..
-rwxr-xr-x@ 1 sylvain staff 18 Mar 23 00:19 0-current_working_directory
-rwxr-xr-x@ 1 sylvain staff 19 Mar 23 00:23 1-listit
-rwxr-xr-x@ 1 sylvain staff 18 Mar 23 00:29 2-bring_me_home
-rwxr-xr-x@ 1 sylvain staff 18 Mar 23 00:39 3-listfiles
-rwxr-xr-x@ 1 sylvain staff 18 Mar 23 00:41 4-listmorefiles
$
```
Repo:
- GitHub repository: [alx-system_engineering-devops](https://github.com/pie972/alx-system_engineering-devops)
- Directory: [0x00-shell_basics](https://github.com/pie972/alx-system_engineering-devops/tree/master/0x00-shell_basics)
- File: [4-listmorefiles](https://github.com/pie972/alx-system_engineering-devops/blob/master/0x00-shell_basics/4-listmorefiles)



## 5. I love numbers
Display current directory contents.
* Long format
* with user and group IDs displayed numerically
* And hidden files (starting with .)
Example:
```bash
$ ./5-listfilesdigitonly
total 32
drwxr-xr-x@ 6 501 20 204 Mar 23 00:29 .
drwxr-xr-x@ 43 501 20 1462 Mar 23 00:19 ..
-rwxr-xr-x@ 1 501 20 18 Mar 23 00:19 0-current_working_directory
-rwxr-xr-x@ 1 501 20 18 Mar 23 00:23 1-listfiles
-rwxr-xr-x@ 1 501 20 19 Mar 23 00:29 2-bring_me_home
-rwxr-xr-x@ 1 501 20 20 Mar 23 00:39 3-listfiles
-rwxr-xr-x@ 1 501 20 18 Mar 23 00:41 4-listmorefiles
-rwxr-xr-x@ 1 501 20 18 Mar 23 00:43 5-listfilesdigitonly
$
```
Repo:
- GitHub repository: [alx-system_engineering-devops](https://github.com/pie972/alx-system_engineering-devops)
- Directory: [0x00-shell_basics](https://github.com/pie972/alx-system_engineering-devops/tree/master/0x00-shell_basics)
- File: [5-listfilesdigitonly](https://github.com/pie972/alx-system_engineering-devops/blob/master/0x00-shell_basics/5-listfilesdigitonly)



## 6. Welcome
Create a script that creates a directory named 'my_first_directory' in the /tmp/ directory.
Example:
```bash
$ ./6-firstdirectory
$ file /tmp/my_first_directory/
/tmp/my_first_directory/: directory
$
```
Repo:
- GitHub repository: [alx-system_engineering-devops](https://github.com/pie972/alx-system_engineering-devops)
- Directory: [0x00-shell_basics](https://github.com/pie972/alx-system_engineering-devops/tree/master/0x00-shell_basics)
- File: [6-firstdirectory](https://github.com/pie972/alx-system_engineering-devops/blob/master/0x00-shell_basics/6-firstdirectory)



## 7. Betty in my first directory
Move the file ***betty*** from /tmp/ to /tmp/my_first_directory.
Example:
```bash
$ ./7-movethatfile
$ ls /tmp/my_first_directory/
betty
$
```
Repo:
- GitHub repository: [alx-system_engineering-devops](https://github.com/pie972/alx-system_engineering-devops)
- Directory: [0x00-shell_basics](https://github.com/pie972/alx-system_engineering-devops/tree/master/0x00-shell_basics)
- File: [7-movethatfile](https://github.com/pie972/alx-system_engineering-devops/blob/master/0x00-shell_basics/7-movethatfile)



## 8. Bye bye Betty
Delete the file ***betty***.
* The file betty is in /tmp/my_first_directory
Example:
```bash
$ ./8-firstdelete
$ ls /tmp/my_first_directory/
$
```
Repo:
- GitHub repository: [alx-system_engineering-devops](https://github.com/pie972/alx-system_engineering-devops)
- Directory: [0x00-shell_basics](https://github.com/pie972/alx-system_engineering-devops/tree/master/0x00-shell_basics)
- File: [8-firstdelete](https://github.com/pie972/alx-system_engineering-devops/blob/master/0x00-shell_basics/8-firstdelete)



## 9. Bye bye My first directory
Delete the directory my_first_directory that is in the /tmp directory.
Example:
```bash
$ ./9-firstdirdeletion
$ file /tmp/my_first_directory
/tmp/my_first_directory: cannot open `/tmp/my_first_directory' (No such file or directory)
$
```
Repo:
- GitHub repository: [alx-system_engineering-devops](https://github.com/pie972/alx-system_engineering-devops)
- Directory: [0x00-shell_basics](https://github.com/pie972/alx-system_engineering-devops/tree/master/0x00-shell_basics)
- File: [9-firstdirdeletion](https://github.com/pie972/alx-system_engineering-devops/blob/master/0x00-shell_basics/9-firstdirdeletion)



## 10. Back to the future
Write a script that changes the working directory to the previous one.
```bash
pie@ubuntu:/tmp$ pwd
/tmp
pie@ubuntu:/tmp$ cd /var
pie@ubuntu:/var$ pwd
/var
pie@ubuntu:/var$ source ./10-back
/tmp
pie@ubuntu:/tmp$ pwd
/tmp
```
Repo:
- GitHub repository: [alx-system_engineering-devops](https://github.com/pie972/alx-system_engineering-devops)
- Directory: [0x00-shell_basics](https://github.com/pie972/alx-system_engineering-devops/tree/master/0x00-shell_basics)
- File: [10-back](https://github.com/pie972/alx-system_engineering-devops/blob/master/0x00-shell_basics/10-back)



## 11. Lists
Write a script that lists all files (even ones with names beginning with a period character, which are normally hidden) in the current directory and the parent of the working directory and the /boot directory (in this order), in long format.
Repo:
- GitHub repository: [alx-system_engineering-devops](https://github.com/pie972/alx-system_engineering-devops)
- Directory: [0x00-shell_basics](https://github.com/pie972/alx-system_engineering-devops/tree/master/0x00-shell_basics)
- File: [11-lists](https://github.com/pie972/alx-system_engineering-devops/blob/master/0x00-shell_basics/11-lists)



## 12. File type
Write a script that prints the type of the file named ***iamafile***. The file ***iamafile*** will be in the /tmp directory when we will run your script.
Example
```bash
ubuntu@ip-172-31-63-244:~$ ./12-file_type
/tmp/iamafile: ELF 64-bit LSB  executable, x86-64, version 1 (SYSV), dynamically linked (uses shared libs), for GNU/Linux 2.6.24, BuildID[sha1]=bd39c07194a778ccc066fc963ca152bdfaa3f971, stripped
```
Note that depending on the file, the output of your script will be different.
Repo:
- GitHub repository: [alx-system_engineering-devops](https://github.com/pie972/alx-system_engineering-devops)
- Directory: [0x00-shell_basics](https://github.com/pie972/alx-system_engineering-devops/tree/master/0x00-shell_basics)
- File: [12-file_type](https://github.com/pie972/alx-system_engineering-devops/blob/master/0x00-shell_basics/12-file_type)



## 13. We are symbols, and inhabit symbols
Create a symbolic link to /bin/ls, named __ls__. The symbolic link should be created in the current working directory.
```bash
ubuntu@ip-172-31-63-244:/tmp/sym$ ls -la
total 144
drwxrwxr-x  2 ubuntu ubuntu   4096 Mar 23 03:24 .
drwxrwxrwt 12 root   root   139264 Mar 23 03:24 ..
ubuntu@ip-172-31-63-244:/tmp/sym$./13-symbolic_link
ubuntu@ip-172-31-63-244:/tmp/sym$ ls -la
total 144
drwxrwxr-x  2 ubuntu ubuntu   4096 Mar 23 03:24 .
drwxrwxrwt 12 root   root   139264 Mar 23 03:24 ..
lrwxrwxrwx  1 ubuntu ubuntu      7 Mar 23 03:24 __ls__ -> /bin/ls
```
Repo:
- GitHub repository: [alx-system_engineering-devops](https://github.com/pie972/alx-system_engineering-devops)
- Directory: [0x00-shell_basics](https://github.com/pie972/alx-system_engineering-devops/tree/master/0x00-shell_basics)
- File: [13-symbolic_link](https://github.com/pie972/alx-system_engineering-devops/blob/master/0x00-shell_basics/13-symbolic_link)



## 14. Copy HTML files
Create a script that copies all the HTML files from the current working directory to the parent of the working directory, but only copy files that did not exist in the parent of the working directory or were newer than the versions in the parent of the working directory.
You can consider that all HTML files have the extension .html
Repo:
- GitHub repository: [alx-system_engineering-devops](https://github.com/pie972/alx-system_engineering-devops)
- Directory: [0x00-shell_basics](https://github.com/pie972/alx-system_engineering-devops/tree/master/0x00-shell_basics)
- File: [14-copy_html](https://github.com/pie972/alx-system_engineering-devops/blob/master/0x00-shell_basics/14-copy_html)



## 15. Let’s move
Create a script that moves all files beginning with an uppercase letter to the directory /tmp/u.
You can assume that the directory /tmp/u will exist when we will run your script
```bash
ubuntu@ip-172-31-63-244:/tmp/sym$ ls -la
total 148
drwxrwxr-x  3 ubuntu ubuntu   4096 Mar 23 03:33 .
drwxrwxrwt 12 root   root   139264 Mar 23 03:26 ..
-rw-rw-r--  1 ubuntu ubuntu      0 Mar 23 03:32 My_file
lrwxrwxrwx  1 ubuntu ubuntu      7 Mar 23 03:24 __ls__ -> /bin/ls
-rw-rw-r--  1 ubuntu ubuntu      0 Mar 23 03:32 Elif_ym
-rw-rw-r--  1 ubuntu ubuntu      0 Mar 23 03:32 random_file
ubuntu@ip-172-31-63-244:/tmp/sym$ ls -la /tmp/u
total 8
drwxrwxr-x 2 ubuntu ubuntu 4096 Mar 23 03:33 .
drwxrwxr-x 3 ubuntu ubuntu 4096 Mar 23 03:33 ..
ubuntu@ip-172-31-63-244:/tmp/sym$ ./100-lets_move
ubuntu@ip-172-31-63-244:/tmp/sym$ ls -la
total 148
drwxrwxr-x  3 ubuntu ubuntu   4096 Mar 23 03:33 .
drwxrwxrwt 12 root   root   139264 Mar 23 03:26 ..
lrwxrwxrwx  1 ubuntu ubuntu      7 Mar 23 03:24 __ls__ -> /bin/ls
-rw-rw-r--  1 ubuntu ubuntu      0 Mar 23 03:32 random_file
ubuntu@ip-172-31-63-244:/tmp/sym$ ls -la /tmp/u
total 8
drwxrwxr-x 2 ubuntu ubuntu 4096 Mar 23 03:33 .
drwxrwxr-x 3 ubuntu ubuntu 4096 Mar 23 03:33 ..
-rw-rw-r-- 1 ubuntu ubuntu    0 Mar 23 03:32 My_file
-rw-rw-r-- 1 ubuntu ubuntu    0 Mar 23 03:32 Elif_ym
```
Repo:
- GitHub repository: [alx-system_engineering-devops](https://github.com/pie972/alx-system_engineering-devops)
- Directory: [0x00-shell_basics](https://github.com/pie972/alx-system_engineering-devops/tree/master/0x00-shell_basics)
- File: [100-lets_move](https://github.com/pie972/alx-system_engineering-devops/blob/master/0x00-shell_basics/100-lets_move)



## 16. Clean Emacs
Create a script that deletes all files in the current working directory that end with the character ~.
```bash
ubuntu@ip-172-31-63-244:/tmp/sym$ ls
main.c  main.c~  Makefile~
ubuntu@ip-172-31-63-244:/tmp/sym$ ./101-clean_emacs
ubuntu@ip-172-31-63-244:/tmp/emacs$ ls
main.c
ubuntu@ip-172-31-63-244:/tmp/emacs$
```
Repo:
- GitHub repository: [alx-system_engineering-devops](https://github.com/pie972/alx-system_engineering-devops)
- Directory: [0x00-shell_basics](https://github.com/pie972/alx-system_engineering-devops/tree/master/0x00-shell_basics)
- File: [101-clean_emacs](https://github.com/pie972/alx-system_engineering-devops/blob/master/0x00-shell_basics/101-clean_emacs)



## 17. Tree
Create a script that creates the directories welcome/, welcome/to/ and welcome/to/school in the current directory.
You are only allowed to use two spaces (and lines) in your script, not more.
```bash
pie@ubuntu:/tmp/h$ ls -l
total 4
-rwxrw-r-- 1 pie pie 44 Mar 23 12:09 102-tree
pie@ubuntu:/tmp/h$ wc -l 102-tree 
2 102-tree
pie@ubuntu:/tmp/h$ head -1 102-tree 
#!/bin/bash
pie@ubuntu:/tmp/h$ tr -cd ' ' < 102-tree | wc -c # you do not have to understand this yet, but the result should be 2, 1 or 0
2
pie@ubuntu:/tmp/h$ ./102-tree 
pie@ubuntu:/tmp/h$ ls
102-tree  welcome
pie@ubuntu:/tmp/h$ ls welcome/
to
pie@ubuntu:/tmp/h$ ls -l welcome/to
total 4
drwxrwxr-x 2 julien julien 4096 Mar 23 12:11 school
pie@ubuntu:/tmp/h$ 
```
Repo:
- GitHub repository: [alx-system_engineering-devops](https://github.com/pie972/alx-system_engineering-devops)
- Directory: [0x00-shell_basics](https://github.com/pie972/alx-system_engineering-devops/tree/master/0x00-shell_basics)
- File: [102-tree](https://github.com/pie972/alx-system_engineering-devops/blob/master/0x00-shell_basics/102-tree)



## 18. Life is a series of commas, not periods
Write a command that lists all the files and directories of the current directory, separated by commas (,).
* Directory names should end with a slash (/)
* Files and directories starting with a dot (.) should be listed
* The listing should be alpha ordered, except for the directories . and .. which should be listed at the very beginning
* Only digits and letters are used to sort; Digits should come first
* You can assume that all the files we will test with will have at least one letter or one digit
* The listing should end with a new line
```bash
ubuntu@ubuntu:~/$ ls -a

.  ..  0-commas  0-commas-checks  1-empty_casks  2-gifs  3-directories  4-zeros  5-rot13  6-odd  7-sort_rot13  Makefile  quote  .test  test_dir  test.var

ubuntu@ubuntu:~/$ ./103-commas

./, ../, 0-commas, 0-commas-checks/, 1-empty_casks, 2-gifs, 3-directories, 4-zeros, 5-rot13, 6-odd, 7-sort_rot13, Makefile, quote, .test, test_dir/, test.var

ubuntu@ubuntu:~/$
```
Repo:
- GitHub repository: [alx-system_engineering-devops](https://github.com/pie972/alx-system_engineering-devops)
- Directory: [0x00-shell_basics](https://github.com/pie972/alx-system_engineering-devops/tree/master/0x00-shell_basics)
- File: [103-commas](https://github.com/pie972/alx-system_engineering-devops/blob/master/0x00-shell_basics/103-commas)



## 19. File type: School
Create a magic file school.mgc that can be used with the command file to detect School data files. School data files always contain the string SCHOOL at offset 0.
```bash
ubuntu@ip-172-31-63-244:/tmp/magic$ cp /bin/ls .
ubuntu@ip-172-31-63-244:/tmp/magic$ ls -la
total 268
drwxrwxr-x  2 ubuntu ubuntu   4096 Mar 23 02:44 .
drwxrwxrwt 11 root   root   139264 Mar 23 02:44 ..
-rw-r--r--  1 ubuntu ubuntu    496 Mar 23 02:42 school.mgc
-rwxr-xr-x  1 ubuntu ubuntu 110080 Mar 23 02:43 ls
-rw-rw-r--  1 ubuntu ubuntu     50 Mar 23 02:06 thisisaschoolfile
-rw-rw-r--  1 ubuntu ubuntu     30 Mar 23 02:16 thisisatextfile
ubuntu@ip-172-31-63-244:/tmp/magic$ file --mime-type -m school.mgc *
school.mgc:         application/octet-stream
ls:                    application/octet-stream
thisisaschoolfile: School
thisisatextfile:       text/plain
ubuntu@ip-172-31-63-244:/tmp/magic$ file -m school.mgc *
school.mgc:         data
ls:                    data
thisisaschoolfile: School data
thisisatextfile:       ASCII text
ubuntu@ip-172-31-63-244:/tmp/magic$
```
Repo:
- GitHub repository: [alx-system_engineering-devops](https://github.com/pie972/alx-system_engineering-devops)
- Directory: [0x00-shell_basics](https://github.com/pie972/alx-system_engineering-devops/tree/master/0x00-shell_basics)
- File: [school.mgc](https://github.com/pie972/alx-system_engineering-devops/blob/master/0x00-shell_basics/school.mgc)


















