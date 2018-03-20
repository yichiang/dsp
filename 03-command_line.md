# Learn command line

Please follow and complete the free online [Bash Scripting Tutorial](https://ryanstutorials.net/bash-scripting-tutorial/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. You should be able to go through these in a couple of hours.

**Note:** Bash is not installed on a PC. Rather, PC users must install Cygwin. Once Cygwin has been installed, the command line interface witll _emulate_ bash. You can find all information regarding Cygwin [here](https://www.cygwin.com/).

---

### Q1.  Cheat Sheet of Commands  

Here's a list of items with which you should be familiar:  
* show current working directory path 
* creating a directory ``
* deleting a directory
* creating a file using `touch` command
* deleting a file
* renaming a file
* listing hidden files
* copying a file from one directory to another

Make a cheat sheet for yourself: a list of at least **ten** commands and what they do.  (Use the 8 items above and add a couple of your own.)  

> > 
show current working directory path `pwd`
creating a directory `mkdir <foldername>`
deleting a directory `rmdir <foldername>`
deleting a directory along with all files and directories within that directory, would be deleted with no prompt or message `rm -rf <foldername>`
creating a file using touch command  `touch`
deleting a file `rm <fileName>`
renaming a file `mv file1 file2`
listing hidden files `ls -ld .?* `
copying a file from one directory to another `cp file1 folder1`

---

### Q2.  List Files in Unix   

What do the following commands do:  
`ls`  
`ls -a`  
`ls -l`  
`ls -lh`  
`ls -lah`  
`ls -t`  
`ls -Glp`  

> > 
`ls` Displays all of the files in the directory.
`ls -a`  Displays all files.
`ls -l`  Displays the long format listing.

`ls -lh`  list long format with readable file size
`ls -lah`  list long format with readable file size including hidden files
`ls -t`  Displays newest files first. (based on timestamp)
`ls -Glp`  Displays the long format listing, but exclude the owner name.
Displays the long format listing.
Displays directories with /


source: https://www.techonthenet.com/unix/basic/ls.php
---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > 
`-p` Displays directories with /
`-a` Displays all files.
`-d` Displays only directories.
`-m` Displays the names as a comma-separated list.
`-r` Displays files in reverse order.


---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > 
The xargs command in UNIX is a command line utility for building an execution pipeline from standard input. Whilst tools like grep can accept standard input as a parameter, many other tools cannot. Using xargs allows tools like echo and rm and mkdir to accept standard input as arguments.

`echo 'one two three' | xargs mkdir`
`find /tmp -mtime +14 | xargs rm`
source: https://shapeshed.com/unix-xargs/#what-is-the-xargs-command-in-unix
 

