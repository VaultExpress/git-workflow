# git-workflow

This is my personal git workflow; it might not be a good one; please help to improve it

## What is origin, upstream?

**repo** is from repository, in git world it means the place we keep code.

**origin** is an alias name, we use to call the repo on the server which we clone it.

**upstream** is an alias name, we use to call the repo on the server where the main project is.

**local**, or **local repo** is the way we call the repo (folder) on our working folder's local machine.

## Fork a project
when we would like to contribute on a project we start by forking it

<p align="center">
  <img width="800" src="https://raw.githubusercontent.com/VaultExpress/git-workflow/master/img/1-git-workflow.png">
</p>

after fork the project, you will have a new repo in your github. this repo will have a reference back to the upstream repo where you forked from.

<p align="center">
  <img width="800" src="https://raw.githubusercontent.com/VaultExpress/git-workflow/master/img/2-git-workflow.png">
</p>

## Prepare local repo
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
