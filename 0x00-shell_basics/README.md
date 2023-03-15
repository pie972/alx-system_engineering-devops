# RTFM
--------------------------------------------------------------------------


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
--------------------------------------------------------------------------
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
--------------------------------------------------------------------------


# Learning Objectives
--------------------------------------------------------------------------
## General
* What does RTFM mean?
* What is a Shebang
--------------------------------------------------------------------------
## What is the Shell
* What is the shell
* What is the difference between a terminal and a shell
* What is the shell prompt
* How to use the history (the basics)
--------------------------------------------------------------------------
## Navigation
* What do the commands or built-ins 'cd', 'pwd', 'ls' do 
* How to navigate the filesystem
* What are the . and .. directories
* What is the working directory, how to print it and how to change it
* What is the root directory
* What is the home directory, and how to go there
* What is the difference between the root directory and the home directory of the user root
* What are the characteristics of hidden files and how to list them
* What does the command 'cd' - do
--------------------------------------------------------------------------
## Looking Around
* What do the commands 'ls', 'less', 'file' do
* How do you use options and arguments with commands
* Understand the ls long format and how to display it
* [A Guided Tour](http://linuxcommand.org/lc3_lts0040.php)
* What does the 'ln' command do
* What do you find in the most common/important directories
* What is a symbolic link
* What is a hard link
* What is the difference between a hard link and a symbolic link
--------------------------------------------------------------------------
## Manipulating Files
* What do the commands 'cp', 'mv', 'rm', 'mkdir' do
* What are wildcards and how do they work
* How to use wildcards
--------------------------------------------------------------------------
## Working with Commands
* What do 'type', 'which', 'help', 'man' commands do
* What are the different kinds of commands
* What is an alias
* When do you use the command help instead of man
--------------------------------------------------------------------------
## Reading Man Pages 
* How to read a man page
* What are man page sections
* What are the section numbers for User commands, System calls and Library functions
--------------------------------------------------------------------------
## Keyboard Shortcuts for Bash
* Common shortcuts for Bash
--------------------------------------------------------------------------
## LTS
* What does 'LTS' mean?
--------------------------------------------------------------------------


# Tasks
--------------------------------------------------------------------------
## 0. Where am I?
Write a script that prints the absolute path name of the current working directory.
```bash
$ ./0-current_working_directory
/root/alx-system_engineering-devops/0x00-shell_basics
$
```

## 1. What’s in there?
```bash
$ ./1-listit
Applications    Documents   Dropbox Movies Pictures
Desktop Downloads   Library Music Public
$
```

## 2. There is no place like home
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

## 3. The long format
```bash
$ ./3-listfiles
total 32
-rwxr-xr-x@ 1 sylvain staff 18 Mar 23 00:19 0-current_working_directory
-rwxr-xr-x@ 1 sylvain staff 19 Mar 23 00:23 1-listit
-rwxr-xr-x@ 1 sylvain staff 18 Mar 23 00:29 2-bring_me_home
-rwxr-xr-x@ 1 sylvain staff 18 Mar 23 00:39 3-listfiles
$
```

## 4. Hidden files
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

## 5. I love numbers
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

## 6. Welcome
```bash
$ ./6-firstdirectory
$ file /tmp/my_first_directory/
/tmp/my_first_directory/: directory
$
```

## 7. Betty in my first directory
```bash
$ ./7-movethatfile
$ ls /tmp/my_first_directory/
betty
$
```

## 8. Bye bye Betty
```bash
$ ./8-firstdelete
$ ls /tmp/my_first_directory/
$
```

## 9. Bye bye My first directory
```bash
$ ./9-firstdirdeletion
$ file /tmp/my_first_directory
/tmp/my_first_directory: cannot open `/tmp/my_first_directory' (No such file or directory)
$
```

## 10. Back to the future
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

## 11. Lists


## 12. File type
```bash
ubuntu@ip-172-31-63-244:~$ ./12-file_type
/tmp/iamafile: ELF 64-bit LSB  executable, x86-64, version 1 (SYSV), dynamically linked (uses shared libs), for GNU/Linux 2.6.24, BuildID[sha1]=bd39c07194a778ccc066fc963ca152bdfaa3f971, stripped
```

## 13. We are symbols, and inhabit symbols
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

## 14. Copy HTML files


## 15. Let’s move
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

## 16. Clean Emacs
```bash
ubuntu@ip-172-31-63-244:/tmp/sym$ ls
main.c  main.c~  Makefile~
ubuntu@ip-172-31-63-244:/tmp/sym$ ./101-clean_emacs
ubuntu@ip-172-31-63-244:/tmp/emacs$ ls
main.c
ubuntu@ip-172-31-63-244:/tmp/emacs$
```

## 17. Tree
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























