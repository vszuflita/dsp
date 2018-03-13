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

**Task** | **Command**
--- | ---
Show current working directory path | pwd
Change directory you're in | cd (directory)
Show the type of file | file (filepath)
Access the manual | man (thing you want to search)
Creating a directory | mkdir (directory name)
Deleting a directory | rmdir (directory name)
Creating a file | touch (file name)
Deleting a file | rm (filename)
Renaming a file | mv (original file name) (new file name)
Listing hidden files | ls -a
Copying a file from one directory to another | cp (source) (destination)

---

### Q2.  List Files in Unix   

What do the following commands do:  

**Command** | **What they do**
--- | ---
`ls`  | Lists what's in the directory
`ls -a`  | Lists what's in the directory including hidden items
`ls -l`  | "Long List". Gives you information on the file type, permission, owner of the file, and file name)
`ls -lh`  | "Long List" in human form. Gives you all the information from -l, but with a readable file size). 
`ls -lah`  | "Long List" with hidden files shown.
`ls -t`  | List sorted by time and date. 
`ls -Glp` | Long list formatting, excluding the owner's name, displaying directories with "/". 


---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

**Command** | **What they do**
--- | ---
`ls -s`  | Lists file size
`ls -S`  | Sorts by file size
`ls -R`  | Displays subdirectories as well
`ls -1`  | Displays on it's own line
`ls -r`  | Displays in reverse order

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

xargs allows you to do the same command for every item in a series. 

 

