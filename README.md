# git-tutorial
Git tutorial

[![git](https://github.com/mohbou/git-tutorial/edit/master/git.PNG)]

follow tutorial on : https://www.youtube.com/watch?v=j1oFazXrzN4

git tutorial

- create a directory and open a git in folder created

- init the project to create a repo  using the command : git init


$ git init
Initialized empty Git repository in C:/androidDev3/project1/.git/

- create your files in your directory

- to add your files to your local repo (staging area) use the command : git add homepage.html

- now git is tracking homepage.html

- now you want to commit in order to have the file stored in local repo by running the command :

git commit -m " added homepage file"  

every time you  do commit you leave a message so you commit all files in staging area


MINGW64 /c/androidDev3/project1 (master)
$ git commit -m "added home page file"
[master (root-commit) ad2f280] added home page file
 1 file changed, 7 insertions(+)
 create mode 100644 homepage.html

insertions are number of line added/updated.

- to stage all files new/ that has changes use the command : git add --all

- to add a remote repo to your local repo :

- create your project on your remote repo ( github ,bitbucket,...)

- link your local repo with your remote using the command :

 git remote add origin https://github.com/mohbou/git-tutorial.git

- you can check using the command : git remote

- now you can push to the remote repo : 

git push origin master 

$ git push origin master
Counting objects: 6, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (5/5), done.
Writing objects: 100% (6/6), 542 bytes | 0 bytes/s, done.
Total 6 (delta 0), reused 0 (delta 0)
To https://github.com/mohbou/git-tutorial.git
 * [new branch]      master -> master

- to make a branch ( create variations/fork of your code) to merge it later :
git branch contact-changes

- to swicth to the specific branch you use the command : 

git checkout contact-changes

You can add new files and commit changes on the new branch

-  to switch back to the main ( master) branch use the command :

git checkout master

- to merge your branch with the master branch use the command  :

git merge contact-changes

$ git merge contact-changes
Updating 87f3e00..9efa3e5
Fast-forward
 contact.html | 2 +-
 1 file changed, 1 insertion(+), 1 deletion(-)

- to get rid of a branch use the command :

git branch -D contact-changes

$ git branch -D contact-changes
Deleted branch contact-changes (was 9efa3e5).

- to push a branch on remote use the command :

git push origin home-changes

$ git push origin home-changes
Counting objects: 6, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 651 bytes | 0 bytes/s, done.
Total 6 (delta 0), reused 0 (delta 0)
To https://github.com/mohbou/git-tutorial.git
 * [new branch]      home-changes -> home-changes


- to recover a deleted branch on local repo, we can get it back from the remote :

git fetch origin home-changes:home-changes

MINGW64 /c/androidDev3/project1 (master)
$ git fetch origin home-changes:home-changes
From https://github.com/mohbou/git-tutorial
 * [new branch]      home-changes -> home-changes

- to check available branches locally use the command : git branch

$ git branch
  home-changes
* master


- to delete a remote branch use the command :

MINGW64 /c/androidDev3/project1 (master)
$ git push origin :home-changes


- in order to ignore files in your project to be added to your repo use the .gitignore file :

- first create the file using the command : touch .gitignore

- edit the file and add all files / folders that need to be ignored

- commit your project : git add --all and git commit -m " changes"

- copy to remote using push : git push origin master


 MINGW64 /c/androidDev3/project1 (master)
$ git push origin master
Counting objects: 3, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 321 bytes | 0 bytes/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/mohbou/git-tutorial.git
   765b43e..39fdc8e  master -> master


