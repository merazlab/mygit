# GitHub

## Lecture - 01

What is **git** or **github** ?

    Git is a version Control

## Install Git

https://git-scm.com/

https://training.github.com/downloads/github-git-cheat-sheet.pdf

## Check version

    git --version

---
## Setup git in Linux

    git config --global user.name "merazlab"   

    git config --global user.email "merazlab"  

Check about git configration

    git config --list

Git Help

    git help <verb>
    git <verb> --help

    EX-
    git add --help
---

# Use git in local code base

Your project dir- **my_project**

Check list of file in a directory

    ls -la

Now Inside project directory run

    git init #a new file .git it is added

Check project file list

    ls -la

    #Stop tracking by removing
    rm -rf .git

Check staus of the file 

    git status

For ignore any file or folder

    #create file
    touch .gitignore

Write ignore file name in **.gitignore**

    test
    *.py
    .proj
---
## Add file git stagging area

    git add filename    

    git add filename #add specific file
        or
    git add -A  #add all file 
        or
    git add .   #add all file


## Our First commit

    git commit -m "..commit meaasage.."

    git status  #for checking status

## See Graph of all commit or branch

    git log --all --decorate --oneline --graph

    #create alias or shortcut
    alias graph="git log --all --decorate --oneline --graph"

    graph   #draw graph


    

## Remove file from staging area

    git reset filename
    git reset       #removing all

    git status #check status


For viewing commit details

    git log

------

# Now work with GitHub repository

    git clone <url> <where to clone>  #it works for cloning locally or globaly

    git clone https://github.com/merazlab/bash.git

---

## Git branch

List of branches

    git branch
Create branch

    git branch branch_name
Shift to the branch

    git checkout branch_name

Create branch and move to branch

    git checkout -b branch1

### Delete branch
    
    #first move from the branch
    git checkout master

    #Now delete the branch
    git branch -d branch name  
