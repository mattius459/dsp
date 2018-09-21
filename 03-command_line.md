# Learn command line

Please follow and complete the free online [Bash Scripting Tutorial](https://ryanstutorials.net/bash-scripting-tutorial/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. You should be able to go through these in a couple of hours.

**Note:** Bash is not installed on a PC. Rather, PC users must install Cygwin. Once Cygwin has been installed, the command line interface witll _emulate_ bash. You can find all information regarding Cygwin [here](https://www.cygwin.com/).

---

### Q1.  Cheat Sheet of Commands  


Here's a list of items with which you should be familiar:  
* show current working directory path
* creating a directory
* deleting a directory
* creating a file using `touch` command
* deleting a file
* renaming a file
* listing hidden files
* copying a file from one directory to another

Make a cheat sheet for yourself: a list of at least **ten** commands and what they do.  (Use the 8 items above and add a couple of your own.)  

`ls` shows files in current directory.
`ls -a` shows all files, including hidden files
`pwd` shows which directory you are currently in (as well as the file path)
`cd` changes directory if followed by the name of another directory. If only `cd` is entered, takes you up one directroy.
`mkdir` creates a new directory inside of current directory.
`rm -r` removes directory
`rm` removes file
`cp` copies a file
`pico` brings up my text editor of choice
`chmod` allows user to adjust read/write access to given file
`date` shows current date
`mv` moves file to desired directory, if the second argument is another filename, changes the original filname to the new filename.

---

### Q2.  List Files in Unix   

What do the following commands do:  
`ls`  *shows files in current directory*
`ls -a`  *shows files in current directory, including hidden files*
`ls -l`  *shows files in current directory with additional information*
`ls -lh`  *shows files in current directory with additional information, including file size*
`ls -lah`  *shows all files, including hidden files, with additional information, inlcuding file size.
`ls -t`  *sorts files by time and date*
`ls -Glp`  *not noticable difference*

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

`ls -d` is handy if you only want to look at directories and don't want your screen to be cluttered with filenames
`ls -t` is handy if you want to see the most recent files first.
`grep` allows you to search a file for a string of characters.
`man` allows to yo figure out what a command does.
`kill` stops an operation which can be helpful if things are frozen.

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

`xargs` allows you to execute a command against multiple items.

__Example:__

`ls | xargs rm` will remove all files in a given directory.

 

