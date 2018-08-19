# git-workflow

This is my personal git workflow; it might not be a good one; please help to improve it

## 0. What is origin, upstream?

**repo** is from repository, in git world it means the place we keep code.

**origin** is an alias name, we use to call the repo on the server which we clone it.

**upstream** is an alias name, we use to call the repo on the server where the main project is.

**local**, or **local repo** is the way we call the repo (folder) on our working folder's local machine.

## 1. Fork a project
when we would like to contribute on a project we start by forking it

<p align="center">
  <img width="800" src="https://raw.githubusercontent.com/VaultExpress/git-workflow/master/img/1-git-workflow.png">
</p>

after fork the project, you will have a new repo in your github. this repo will have a reference back to the upstream repo where you forked from.

<p align="center">
  <img width="800" src="https://raw.githubusercontent.com/VaultExpress/git-workflow/master/img/2-git-workflow.png">
</p>

## 2. Prepare local repo
On your machine, you need to prepare your local repo for further work
```
git clone https://github.com/<YOUR NAME HERE>/vault-express.git
cd vault-express
git remote add upstream https://github.com/VaultExpress/vault-express.git
```
check it by
```
git remote -v
```
it should displays similar to this
<p align="center">
  <img width="800" src="https://raw.githubusercontent.com/VaultExpress/git-workflow/master/img/3-git-workflow.png">
</p>

## 3. Create a working branch
On your machine, in your local repo directory. When we start to work/edit on something, we start by creating a new branch
```
git branch work
```
This will create a new branch name 'work'. You may use any words as you like
and then we check the branch in local repo by
```
git branch
```
You will notice ***master** and **work** on your terminal
the * mark means you are on that branch, in this case it means you are on master branch
then we need to change to our new **work** branch by enter
```
git checkout work
```
check with **git branch** again, you will see the star mark move to ***work**

There is a shortcut for above command by
```
git checkout -b work
```
it will create **work** branch and also move you to that specific branch

## 4. Editing and Commit the changes
Make sure you are on your **work** branch by issuing **git checkout work**
From here, you may create/edit/delete as you like. Once you have done, you can save your changes to **local repo**, **work** branch by
```
git add .
git commit -m "YOUR COMMENT MESSAGE"
```
**notice** that with old git version, we might need to use **git add . --all**, if you delete some files

From this point, your **work** branch will have your changes **BUT** your **master** branch still have old code before changes

if you checkout **master** branch by **git checkout master**, you will see your old code in your local repo directory, you can move back and forth between branch anytime you like
