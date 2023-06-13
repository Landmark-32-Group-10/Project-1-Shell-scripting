# Project-1-Shell-scripting
Class Projects
What is Shell?
A shell is an interface to the Unix system in which we can run our commands, programs & shell scripts

How to check how many shells that Linux/Unix server will support
	$ cat/etc/shells

What are the different shell types? 
Bourne shell
C shell

 How many types of comments does shell script support? 
Single line comment
Multi line comments

 What is command line arguments? 
An argument also called a command line argument, can be defined as the input given to a command line to process that input with the help of given command. Arguments can be in the form of a file or directory. 
Arguments are entered in the terminal or console after entering the command.

 What is the difference between $* and $@ ?
Both are the parameters that specify the command line argument; however, all are command line arguments. They are often used to pass all arguments to another program

Write down the syntax for if condition?
sudo service sshd 
cat deploy.sc     
if [ $?==0 ] 
then
echo "We succeeded" 
else  
echo "We failed, please troubleshoot" 
fi  

cat deploy.sc     
if [ $#==3 ] 
then
echo "We succeeded" 
else  
echo "Please pass 3 arguments with your script" 
fi

Write down the syntax for for-loop? 
The syntax for a for-loop is: 
for < variable name> in <directory>; do <command> $ <Variable name>; done:

Write down the syntax for a function and write one function and call that function? 
The syntax for a function is: 
function_name () {list of commands} 
An example of a function is: 
!/bin/sh 
hello() {
 Echo “Hello World”} 
Hello world or introduction function. 

What is the difference between > and >> and < and what is the standard output and standard error codes? 
The differences between > and >> is shell scripting is, > is used to either create a file not present in the directory or to overwrite an existing file in the directory. 
Whereas >> is used to attach functions or commands to an existing file. Lastly < is used for file redirection within the directory. 
The standard output code in shell scripting is stdout and the standard error code is stderr. 
The syntax for standard output numerical value of 0 
> output.file.name 
The syntax for error code numerical value of 2 
2> errors.txt

11. How to display one variable (take variable name as technology) value?
    	echo $technology

12  How many types of variables are in Shell scripting?
   	 2 types of variables,
       a. User defined variable, e.g., variables defined by the user while creating a shell script.
       b. System defined variables, these are variables that are defined by the system.

13. Write some System defined variables?
     with env tool, you can display all system defined variables as below,
       SHELL=/bin/bash
       HISTCONTROL=ignoredups
       SYSTEMD_COLORS=false

14. What is String? 

Strings are scalar and there is no limit to the size of a string. Any characters, symbols, or words can be used to make up your string.

15. How to find the length of the given string? 
using expr - length or echo command length $ (expr length "$ str" ) echo "length of my string is $length" example: Please enter your name angel angel, please enter your date of birth april 29 How can we help you today [ec2-user@try2 ~]$ expr length "$ str" 5 3.

16. Write a shell script to accept the name and age from the user and display that back to the user.
echo "Please enter your name" 
read name 
echo "$name, please enter your date of birth" 
read date of birth echo 
"How can we help you today" 
[ec2-user@try2 ~]$ sh test2.sh 
Please enter your name 
Angel 
Angel, please enter your date of birth 
April 29 
How can we help you today

17. Write a shell script to accept a file name from the user and make a copy of that file
#!/bin/bash

# Interactive Script to backup user file
clear
echo "INTERACTIVE SCRIPT TO COPY USER FILE"
echo "======================================"
echo
read -p "Enter file name to copy - absolute path: " filename
echo
echo "The file name you enter is :" $filename
echo
echo " Copying in progress . . . ."
 cp  $filename "$filename"_copy
echo
 echo " The name of the copy file is: $filename"_copy

18. Write a shell script to accept file name from the user and display the contents of file. If the file doesn't exist then try curbing the error and display a user friendly error to user. 
#!/bin/bash

# Interactive Script to display content of an existing file
clear
echo "INTERACTIVE SCRIPT TO CHECK FILE TYPE"
echo "====================================="
echo
read -p "Enter file name  - (absolute path): " filename
echo
if [ -f $filename ]
then
	echo "displaying file content .  .  ."
	echo
        cat $filename
elif
[ -d $filename ]
then

	echo " `ls $filename | wc -l` files and directories counted"
else
	echo
	echo "File does not exist"
fi
echo
echo " Script completed"

19.  Write a shell script to accept a file name from user and check whether its anordinary file or a directory. In case of file show the contents of file and if it’s a directory show number of files in that directory
#!/bin/bash

# Interactive Script to display content of an existing file
clear
echo "INTERACTIVE SCRIPT TO DISPLAY CONTENT OF AN EXISTING FILE"
echo "========================================================="
echo
read -p "Enter file name to copy - (absolute path): " filename
echo
if [ -f $filename ]
then
	echo "displaying file content .  .  ."
	echo
        cat $filename
else
	cat $filename 2> /dev/null
	echo "File does not exist"
Fi
echo
echo " Script completed"

20. Write a shell script to accept a file name from user. Check whether file has allthe permissions if not assign the respective permissions to that file.
 
#!/bin/bash

# Author: GROUP 10
# This script prompt user for a file name and assign full permission if not already have
#  Date June 6th, 2023

clear
echo
echo "Script to set full permission to a file if not already set"
echo
read -p "Enter file name (absolute path) :" filename

if [ -f $filename ]
then
	echo " file name is " $filename
else
	echo "File does not exist"
	echo
	echo "Script completed . . . ."
        echo 

	exit
fi


21. Write a shell script to accept a file name from the user and sort the file. If the file doesn’t exist curb the error message and show the user-friendly message

#!/bin/bash
# Author: Group 10
# Date: June 5th  2023


# Script to sort the content of a file
clear
echo "SCRIPT TO SORT CONTENT OF A FILE"
echo "================================"
echo
read -p "Enter file name to copy - (absolute path): " filename
echo
if [ -f $filename ]
then
	echo "displaying file content .  .  ."
	echo
        cat $filename
	echo
	echo "Sorting in progress . . . ."
	echo
	sort $filename  
	echo
else
	echo "File does not exist"
fi
echo
echo " Script completed"
echo










