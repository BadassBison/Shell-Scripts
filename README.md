# Bash Scripts

This is a directory to store Bash Scripts. To use this directory effectively, 
make sure to update your PATH with the location of this diretory. If you are 
unsure how to update your PATH, follow the steps below

1. In terminal, `cd` into the directory
2. type `pwd` into the terminal (save this, I'll refer to this as $dirPath)
3. Open your .bashrc file in an editor > `nano ~/.bashrc`
    - If none exists this will create it
4. On the top line add `PATH="$dirPath:$Path"`
5. type `ctrl-x`
6. type `y` to save
7. in terminal, type `source ~/.bashrc`

Once you have this on your PATH, bash will be able to locate the file names and
run them with the name of the file. This is most effective if you leave off the
`.sh` from the file names. Everything at the root level of this directory can 
now be called by simply typing the name of the file into your terminal. You can 
keep any or all of the scripts you want to use. Simply delete all others.


## Table of Contents

**Information**
* About
* References
* Colors
* Conditional Expressions
* Debugging Scripts

**Scripts**
* clean-docker
* create-api
* helloworld
* list
* newgame
* newscript
* note
* scripts
* trash


## Information

***
### About
This is a bash library for people who want a much better user experience
when it comes to using the terminal. This project will continue to grow as
I do as a developer. This project is completely open source, so please message
me if you would like to contribute. 


***
### References
Latest publication
https://www.gnu.org/software/bash/manual/bash.pdf

Colors
https://misc.flogisoft.com/bash/tip_colors_and_formatting


***
### Colors
Black \e[30m
Red \e[31m


***
### Conditional Expressions
These are wrote as follow `[[ Expression ]]` with 2 brackets.


***
### Debugging Scripts
To have the entire script show its output in the terminal, append `-x`
to the first line `#!/bin/bash -x`. If you want more limited output, put
`set -x` where you want to start debugging and `set +x` where you want 
it to stop.


## Scripts

***
### clean-docker
This script is for stoping and removing all docker containers, 
then removing the images


***
### create-api (unfinished)
This script is for building a .NET core 2.1 API to be used with
AWS. The build has a dependency in the directories folder and is
unfinished at this point


***
### helloworld
This is the most basic script, there as an entry point and for
others to use if they are unfamiliar with using bash scripts


***
### list
This script overrides the previous ls command providing much 
better viewing in the terminal


***
### newgame (unfinished)
This is a directory builder for simple 2D games. The use of this
was initially to clone a Github template and pull it down, but I've
since changed directions and feel it would be better to have a
custom directory get build and create a new Github repo when initialized


***
### newscript
This script is used to provide the basic template when writing scripts.
There are a few lines of code that are needed in every script and 
permission changes for executable. It is better to just have them generated 
so they are not forgotten.


***
### note
This script will keep track of notes storing them in the notes directory.
If you simply call `note` it will prompt you to add a note, then append it
to notes.txt. If you provide a name `note <name>` then it will create a new
file with that name and note


***
### scripts
This script allows you to view what scripts are available


***
### trash
This script will move a file to the trach opposed to removing it permanently