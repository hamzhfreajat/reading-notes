# Practice in the Terminal

## The Command Line

The command line is text base inteface to the system which mean you can do a command by typing it in the keyboard . 



## Basic Navigation

### How to know where we are ? 

`pwd` which stands for Print Working Directory , this command will show the working directory or where we are. 

    pwd
    /home/hamzh

### What's in Our Current Location?
`ls` which will list the files in the directory that you are in .

    ls
    bin Documents public_html

###  Move Around `cd`
This command able us to move around throug directory 
    cd directory-name


## More About Files
In linux system the extension is not important , Linux the system actually ignores the extension and looks inside the file to determine what type of file it is. 

The command file will help us to find the extension 

    file [path]

## Hidden Files and Directories

This command will help us to show hidden files and directories

    ls -a directory-name

## Manual Pages

This command like help to let remember what the command is talking about . 

    man <command to look up>

## File Manipulation
### Making a Directory 

This command will help you to make directory 

    mkdir [options] <Directory>

### Removing a Directory
This command will help you to remove directory 

    rmdir [options] <Directory>

### Creating a Blank File
This command will help you to create empty file
    
    touch [options] <filename>

## Cheet Sheet 
[Cheet sheet](https://ryanstutorials.net/linuxtutorial/cheatsheet.php)

