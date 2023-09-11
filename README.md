# My favorite Git and GitHub terminal commands (incl. basic navegation)

https://git-scm.com/

Don't forget to create a .gitignore before anything else!

git --version

https://git-scm.com/download/mac
binary installer

CMND + SHIFT + V (README preview on VSC)

## SHORTCUTS

- CMND + K (clear terminal)
- CTRL + C (leave live servers)

## NAVEGATION COMMANDS

```
$ ls
$ ls folderName
$ ls folderName/secondFolder
$ open .
$ cd
$ cd ..
```
Opens the path you are in with VSC.
```
$ code .
```

#### Show hidden files

```
$ ls -a
```

#### Quit

```
$ q
```

#### Tells you where you are

```
$ pwd
```

## CREATION/DELETE COMMANDS

#### Create files

```
$ touch <noteFiles.txt>
```

#### Create more files

```
$ touch <noteFiles.txt> <list.txt>
```

#### Create files somewhere else

```
$ touch <folderName>/<noteFiles.txt> <list.txt>
```

#### Create folder

```
$ mkdir folderName
```

#### Remove files or folders

```
$ rm <file.txt>
$ rm -rf <folderName>
$ rm -rf .git
```

## GIT SETUP

```
$ git config user.name
$ git config --global user.name "My Name"
```

Put your email:

- Same as above but with .email

## CREATE REPO

Creates .git hidden folder. Never create repos inside repos!

```
$ git status
$ git init
```

## LOG COMMITS/CHECKPOINTS (one task as a time!)

```
$ git add <file1> <file2>
$ git add .
```

#### It is doable to stage and commit some files and not others

#### This commits what's staged but you can still have other unmodified files

```
$ git commit -m "start project"
```

## COMMIT REPORTS

This is for the branch you are in:
```
$ git log
$ git log --oneline
```

You can also check others:
```
$ git log <branch>
$ git log --oneline <branch>
```

## BRANCHES

#### Shows what branches do you have. From the upcoming list, HEAD will appear with a \*

```
& git branch
```

#### Creates new branch but HEAD doesn't move

```
& git branch <branch-name>
```

#### List + last commit from each

```
& git branch -v
```

#### Removes branch

```
& git branch -d <branch-name>
```

Sometimes it asks for the D to be capital as a double check.

## HEAD

This is the commit you are in, working on or pointing to. Always the last unless you change.

#### Change HEAD to another branch (and last commit of it)
NOTE: This is also the way to access a branch that's only on the Remote Tracking Branch.

```
& git switch <branch-name>
```
You also use the above to get the head back to normal after you do the below.
#### Change HEAD to another commit
```
& git checkout <commit-hash>
```

## REPORT CHANGES
Check differences between unstaged changes and last commit. It doesn't include new files.
```
& git diff
```
Check differences between changes (staged or unstaged) and HEAD incl new files.
```
& git diff HEAD
```
...or specific files
```
& git diff HEAD <file1>
& git diff HEAD <file1> <file2>
```
Check differences between branches and commits
```
& git diff <branch1>..<branch2>

& git diff <commit1>..<commit2>
```
Check differences between HEAD and staged changes.
```
& git diff --staged
& git diff --cached
```

## MERGING

What you merge are branches, not commits. So it makes sense to some degree to remove the merged branch after the merging.

#### HEAD has to be on branch you want to merge changes to

```
$ git merge <second-branch>
```

## GITHUB

 NOTE: When the remote is updated on GitHub and you check the status of the local repo, it will tell you that you are up to date with the remote, even if you are not. It's only after you fetch the changes that your computer knows about the new stuff. This is because the reference to the remote on your computer (called Remote Tracking Branch) doesn't update automatically. In other words, the remote is not what's on GitHub but what's on the Remote Tracking Branch. This one only updates by fetching or pulling (I think).

 NOTE2: When you click on "This branch is X commits behind Y:<_branch>.", the commits show backwards in time!

#### Clones project folder where you are locally

```
$ git clone <github-repo-url>
```

#### You see the remote (url reference); normally called "origin"

```
$ git remote
```

#### The above plus the url

```
$ git remote -v
```

#### Sets up a remote (collab tip: you normall do it from your fork)

```
$ git remote add origin <github-repo-url(yours)>
```

If you want a remote just to get updates, convention is to call it upstream:

```
$ git remote add upstream <github-repo-url(original)>
```

#### Removes a remote
```
$ git remote remove <remote(origin)>
```

#### Pushes a branch to github

```
$ git push <remote(origin)> <branch>
```

#### Fetches changes from github (you can also use it without the branch) / Updates Remote Tracking Branch

```
$ git fetch <remote(origin)> <branch>
```

#### Fetches changes from github and merges it to the local repo. So it matters where the head is!

```
$ git pull <remote(origin)> <branch>
```

#### Check Remote Tracking Branch

```
$ git branch -r
```

Origin (a.k.a github-repo-url or remote or anotherhub-website) is the conventional name for the url. You can have more than one if you want to.

## OTHER POSSIBLE OPTIONS

- There's a way to add files that you forgot in the last commit (amend).
- You can create a huge message with an editor insted of using the -m on logs