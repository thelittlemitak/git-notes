# My favorite terminal commands

https://git-scm.com/

Don't forget to create a .gitignore before anything else!

git --version

https://git-scm.com/download/mac
binary installer

## SHORTCUTS

- CMND + K (clear)

## PUT YOUR NAME

```
$ git config user.name
$ git config --global user.name "My Name"
```

## PUT YOUR EMAIL

- Same as above but with .email

## NAVEGATION COMMANDS

```
$ ls
$ ls folderName
$ ls folderName/secondFolder
$ open .
$ cd
$ cd ..
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
```

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

```
$ git log
$ git log --oneline
```

## BRANCHES

You always start in/with MASTER branch; on GITHUB it is called MAIN

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

## HEAD

This is the commit you are in, working on or pointing to. Always the last unless you change.

#### Change HEAD to another branch

```
& git switch <branch-name>
```

## MERGING

What you merge are branches, not commits. So it makes sense to some degree to remove the merged branch after the merging.

#### HEAD has to be on branch you want to merge changes to

```
$ git merge <secondBranch>
```

## GITHUB

#### Creates project folder where you are locally

```
$ git clone <gitHubRepoUrl>
```

#### You see the remote (url reference); normally called "origin"

```
$ git remote
```

#### The above plus the url

```
$ git remote -v
```

#### Sets up a remote

```
$ git remote add origin <gitHubRepoUrl>
```

#### Pushes a branch to github

```
$ git push <remote> <branch>
```

Origin (a.k.a github-repo-url or remote) is the conventional name for the url. You can have more than one if you want to.

## OTHER POSSIBLE OPTIONS

- There's a way to add files that you forgot in the last commit (amend)
- You can create a huge message with an editor insted of using the -m on logs
- You can delete and rename branches
- You can delete and rename remote names (which is typically origin)