Wellcome to Chi Tang V.Q

[TOC]

# Basic Git
## Clone Database
``` bash
git clone <your_git_link>
```
Download all the Database in master branch from server to your computer.
> git clone https://github.com/at-chitang/summer-inter-2017.git
## Make default folder
``` bash
git init
```
Make your folder you stay become default folder for your Github
## Upload file
### Add file
``` bash
git add "name_of_file" "name_of_another_file"
git add -A	# Add all
git add *	# Add all
git add .	# Add new and modified, without deleted
git add -u	# Add modified and deleted, without new
```
It make your file ready for commit, first step for push file on server
> git add "develop.txt" "hello_world.txt" 

Check out what file had add:
``` bash
git status
```
### Commit file
``` bash
git commit
git commit -m "name_of_commit"
git commit -am "name_of_commit"	# Don't need to add, it will help you add all file had modified
```
Add your file to a queue and ready for upload to server
> git commit -m "first_up"

Check out your commit:
``` bash
git log
```
### Push file
``` bash
git push -u <your_server_link> <name_brand>
```
Push all file you had commit on server
> git push https://github.com/at-chitang/summer-inter-2017.git master

Easier way to do every thing without a long link, that is you assign a variable for that link:
``` bash
git remote add <variable_name> <link>
```
> git remote add sumint https://github.com/at-chitang/summer-inter-2017.git
> git push -u sumint master

## Branch
### Check your branch
``` bash
git branch
```
Show all branch in your Github and show where is your branch

### Create new branch
``` bash
git checkout -b <name_branch>
```
Create new branch from branch you are staying
> git checkout -b featureA

### Change branch
``` bash
git checkout <name_branch>
```
Change branch you stay at become branch you choose
> git checkout master

### Delete old branch
``` bash
git branch -D <name_branch>
```
Delete branch you choose
> git branch -D featureA

## Update a branch
``` bash
git pull <variable> <name_branch>
```
Update branch you choose
> git pull sumint master

## Pull requests
First, you go to your Github and choose tab "Pull requests".
Second, choose "New pull request".
Then, choose Base and Compare and choose "Create pull request".
Finally, type your comment and choose "Create pull request".
Now, we wait for who have responsibility accept it.

# Advance Git

## Merge branch at local
``` bash
git merge <name_branch>
git rebase <name_branch>
```
You merge 2 branch at local and if you have conflict then you have to fix it before push it on server

## Stash
``` bash
git stash
```
When you are working at a branch and you want to change to another branch. You should put your code to a stack by use this code.

## Cherry-pick
``` bash
git cherry-pick
```
Choose some update to add to another branch

## Reset --soft/--hard
``` bash
git reset <id>
git reset --soft <id>
git reset --hard <id>
```
Undo summit to older summit
--soft: just undo in log
--hard: delete and modify file

## Tag
``` bash
git tag <version_number>
```
You can go back to older version easier by tag

## Merge commit
``` bash
git rebase -i HEAD ~<number_of_summit>
```
You can merge a number of summit that they modify same file

## Fix conflict
You 'll meet conflict when you try to merge 2 branch have at least 1 same file with difference content.
1. When ever you have a conflict, you have to fix it at local.
2. First, you update main branch by "git pull".
3. Second, choose branch you want to merge by "git checkout".
4. Third, merge 2 branch by "git merge" and you will get a list of conflict.
5. Then, you have to fix all conflict by delete what you don't need in your file before you can push it again on server.
 







[toc]
