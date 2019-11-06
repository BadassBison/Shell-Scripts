# Bash Scripts

This is a directory to store Bash Scripts. To use this directory effectively, 
make sure to update your PATH with the location of this directory. If you are 
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
* Aliases
* Color Codes
* Conditional Expressions
* Debugging Scripts
* Git Commands
* Dotnet Commands
* Docker Commands

**Scripts**
* docker_clean
* dotnet_create_api
* git_change_authorship
* my_create_new_game
* my_helloworld
* my_ls
* my_ls_scripts
* my_mkdir
* my_mv_file_to_trash
* my_new_script
* my_take_note


## Information

***
### About
This is a bash library for people who want a much better user experience
when it comes to using the terminal. This project will continue to grow as
I do as a developer. This project is completely open source, so please 
message me if you would like to contribute. 


***
### References
Latest publication
https://www.gnu.org/software/bash/manual/bash.pdf

Terminal color codes
https://misc.flogisoft.com/bash/tip_colors_and_formatting

Docker documentation
https://docs.docker.com/v17.12/edge/engine/reference/commandline/docker/#description

***
### Aliases
For better script names, you should alias the scripts to something of your
choosing, here is a list of my aliases. Add these to your ~/.bash_profile.
You can call the script `my_add_aliases` to have them added for you.

```
alias newscript=my_new_script               # Bash script template
alias scripts=my_ls_scripts                 # List scripts
alias trash=my_mv_file_to_trash             # Move file to trash
alias note=my_take_note                     # Add a note 
```


***
### Color Codes
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


***
### Git Commands
```
git status                                  # show status of all modified files
git diff                                    # inspect changes in working directory
git diff --staged                           # inspect changes on files in staging area
git add <filename>                          # adds specified files to the staging area
git add .                                   # adds all modified files to the staging area
git commit -m "<comment>"                   # commits changes with added message
git log                                     # shows log of recent commits
git stash                                   # stash changes made on current branch
git remote add origin                       # add URL to Github repo
git push -u origin master                   # push commits to Github repo
git push -u origin <branchname>             # push commits to specified branch
git branch                                  # lists all branches or creates a new branch
git branch -d <branchname>                  # deletes specified branch
git checkout <branchname>                   # checks out specified branch
git checkout -b <branchname>                # creates a new branch and checks it out
git merge <branchname>                      # merges specified branch to master
git reset --hard                            # undo all changes since last commit
git reset --hard HEAD~3                     # reset 3 commits
git reset --soft HEAD~1                     # reset to right before prior commit
git rebase (more research needed)
```

***
### Dotnet Commands
dotnet                                      # list of basic entry commands
dotnet --help                               # list help for using dotnet cli
dotnet -all                                 # see full SDK command list


***
### Docker Commands
```
docker ps                                           (View running containers)
docker ps -a                                        (View all container instances)
docker start <container name or id>                 (Start a container instance)
docker stop <container name or id>                  (Stop a container instance)
docker rm <container name or id>                    (Remove a stopped container instance)
docker rmi <image name or id>                       (Remove an image that has zero instances)
docker pull <repo name>                             (Pulls the repo and creates the image without a container instance)
docker run <image name or id>                       (Creates an instance of the image. Pulls the repo if it doesn't exist)
docker run -d <image name or id>                    (Creates a detached instance)
docker attach <container name or id>                (Attaches to a detached container)
docker run <name>:<tag>                             (Creates an instance of the image with the same tag)
docker run -it <name>                               (Interactive & Sudo Terminal)
docker run -p <host>:<mapped>                       (Map dockers exposed ports to different local ports)
docker inspect <container name or id>               (More detail about the container)
docker logs <container name or id>                  (Log information for the container)
docker history <image name or id>                   (Shows image build history)
docker rename <old container name> <new name>       (Renames containers)
docker network ls                                   (Shows all networks. Defaults: bridge, host, none)
docker build Dockerfile -t <image name> <path>      (Build a new image from a Dockerfile)
```

## Scripts

***
### docker_clean
This script is for stoping and removing all docker containers, 
then removing the images


***
### dotnet_create_api (unfinished)
This script is for building a .NET core 2.1 API to be used with
AWS. The build has a dependency in the directories folder and is
unfinished at this point


***
### git_change_authorship
This script changes the git author and committer information


***
### my_add_aliases
This script adds the default aliased to the .bash_profile


***
### my_create_new_game (unfinished)
This is a directory builder for simple 2D games. The use of this
was initially to clone a Github template and pull it down, but I've
since changed directions and feel it would be better to have a
custom directory get build and create a new Github repo when initialized


***
### my_helloworld
This is the most basic script, there as an entry point and for
others to use if they are unfamiliar with using bash scripts


***
### my_ls
This script overrides the previous ls command providing much 
better viewing in the terminal


***
### my_ls_scripts
This script shows the available scripts


***
### my_mkdir
This script provides better UX for the mkdir command


***
### my_mv_file_to_trash
This script allows for files to be moved to the trash opposed to
just deleting them with rm

***
### my_new_script
This script is used to provide the basic template when writing scripts.


***
### my_take_note
This script will keep track of notes storing them in the notes directory.
If you simply call `note` it will prompt you to add a note, then append it
to notes.txt. If you provide a name `note <name>` then it will create a new
file with that name and note

