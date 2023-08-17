## My favorite terminal commands

https://git-scm.com/

Don't forget to create a .gitignore before anything else!

git --version

https://git-scm.com/download/mac
binary installer

### SHORTCUTS

- CMND + K (clear)

### PUT YOUR NAME

```
$ git config user.name
$ git config --global user.name "My Name"
```

### PUT YOUR EMAIL

- Same as above but with .email

### NAVEGATION COMMANDS

```
$ ls
$ ls folderName
$ ls folderName/secondFolder
$ ls -a (show hidden files)
$ open .
$ pwd (where are you)
$ cd
$ cd ..
$ q (when it gets crazy)
```

### CREATION/DELETE COMMANDS

```
$ touch noteFiles.txt (create files)
$ touch noteFiles.txt list.txt (create more files)
$ touch folderName/noteFiles.txt list.txt (create files somewhere)
$ mkdir folderName (create folder)
$ rm file.txt
$ rm -rf folderName
```

### CREATE REPO (creates .git hidden folder) don't create repos inside repos

```
$ git status
$ git init
```

### LOG COMMITS/CHECKPOINTS (one task as a time!)

```
$ git add file1 file2 (you can stage and commit some files and not others)
$ git add .
$ git commit -m "start project" (this commits what's staged but you can still have other unmodified files)
```

### COMMIT REPORTS

```
$ git log (each has an ID)
$ git log --oneline (gets a shorter ID)
```

### BRANCHES

You always start in MASTER branch; on GITHUB it is called MAIN

```
& git branch (from the upcoming list, the HEAD will appear as *)
& git branch branch-name (creates new branch but HEAD doesn't move)
& git branch -v (list + last commit from each)
```

### BRANCHES.HEAD

This is the commit you are in, working on or pointing to. Always the last unless you change.

```
& git switch branch-name (change HEAD to another branch)
```

### MERGING (branches, not commits. So it makes sense to some degree to remove the merged branch)

```
$ git merge secondBranch (HEAD has to be on branch you want to merge changes to)
```

$
$

### GITHUB

```
$ git clone <gitHubRepoUrl> (creates the project folder where you are locally)
$ git remote (you see the reference (origin) of github)
$ git remote -v (the above plus the url)
$ git remote add origin <gitHubRepoUrl> (sets up a remote)
$ git push <remote> <branch>
```

- Origin (my gitHubRepoUrl) is the conventional name for the url. You can have more than one

### OTHER OPTIONS THAT I WON'T USE AT THE MOMENT

- There's a way to add files that you forgot in the last commit (amend)
- You can create a huge message with an editor insted of using the -m on logs
- You can delete and rename branches
- You can delete and rename remote names (which is typically origin)
  $
$
