# GitCheatSheet
Git is the free and open-source distributed version control system that's responsible for everything GitHub related that happens locally on your computer. This cheat sheet features the most important and commonly used Git commands for easy reference.

### **SETUP**
Configuring user information used across all local repositories  .
One of the ost important concepts is collabration and in order to collabrate you have to identify who you are.  
The way we do that is by modifying **git config**.  
We can look at current **config list** by typing:  
```
git config --list
```
This list should have "user.name" and "user.email".  
```
git congif --global user.name "firstname lastname"
```
Set a name that is identifiable for credit when review version history.
```
git config --global user.email "valid-email"
```
Set an email addresses that will be associated with each history marker.
```
git config --global color.ui auto
```
set automatic command line coloring for git for easy reviewing.  
If you stuck in this screen hit `:q` to quit. 

---
### **SETUP & INIT**
Configuiring user information, initializing and cloning repositories.
```
git init
```
initialize an existing directory as a Git repository.  
```
git clone [url]
```
retrieve an entire repository from a hosted location via URL.  

---

### **STAGE & SNAPSHOT**
Working with snapshots and the Git staging area.    
```
git status
```
show modified files in working directory, staged for your next commit.  
```
git add [file]
```
add a file as it looks now to your next commit (stage).  
```
git add .
```
representing all the files in the current working directory or any other files that changed since the last commit.
```
git reset [file]
```
unstage a file while retianing the changes in working directory.
```
git reset .
```
unstage all files.
```
git diff
```
diff of what is changed but not staged.
```
git diff --staged
```
diff of what is staged but not yet committed.
```
git commit -m "descriptive message"
```
commit your staged content as a new commit snapshot.
```
git commit -a -m "descriptive message"
```
more efficent shortcut if you want to skip the **`add`** command, you can just go straight to **`git commit`** and use **`-a`** flag which will add all the files in the current working directory, the add a message after that to wrap-up the entire process in a single command.

---

### **CONNECT TO REPOSITORY FROM LOCAL**
from your GitHub account create a new repository and give it a name of what ever you like, once you create it, GitHub will initializing an empty **remote** repository and give you some instruction how to connect it localy.
the only thing you need is the [URL] to the repository, so go ahead and copy it. 
```
git remote
``` 
this will tell you which remote repositories you have linked to your local project.  
to connect our local code to GitHub we're going to run **`git remote add`** followed by two values, the first value is the name of the remote repository which tipically has the name of **origin** because it will serve as the main source of truth of our code, and the second value is the [url] to it that we copied from GitHub.

```
git remote add origin [url]
```
now our local code is linked up to that remote repository, and if we run **`git remote`** again it should list out **origin** and if you type **`-v`** after that it will provide **url** as well.
```
git remote -v
```
and if you want more information you can use:
```
git remote show [repository name]
```
which show additional informations like **branches** and things like that.  
Now that we have remote repo on GitHub we're going to sync-up our local code with it.

---

### **SHARE & UPDATE**
Retrieving updates from another repository and updating local repos.  
```
git remote add [alias] [url]
```
add a git **URL** as an alias.
```
git fetch [alias]
```
fetch down all the branches from that Git remote.
```
git merge [alias]/[branch]
```
merge a remote branch into your current branch to bring it up to date.

```
git push [alias] [branch]
```
Transmit local branch commits to the remote repository branch.  
You can also add a **`-u`** flag at the end of this command and set the repo that mentioned to upstream remote in that git config file. It's allow us to use the command **`git pull`** without the requiring in any additional arguments.  

>**Note:** you wanna use **`-u`** flag when the remote repository is the final source of trouth (origin).
```
git pull
```
fetch and merge any commits from the tracking remote branch.

---
### **BRANCH & MERGE**
Isolating work in branches, changing context, and integrating changes.
```
git branch
```
list your branches. a __*__ will appear next to the currently active branch.
```
git branch -M [new-name]
```
you can rename your active branch by this command.
```
git branch [branch-name]
```
create new branch at the current commit.
```
git branch -d [branch-name]
```
**delete** a branch by using a lower-case **`-d`** flag, it will do it in a safe manner and only deleted the branch if it merged to the **main** branch and if it has no changes on it.
```
git branch -D [branch-name]
```
forcing to delete a branch, so be careful with it 😁.
```
git checkout -b [branch-name]
```
if you are in the **main** branch and you want to create and switch to a new branch at the same time.  
kinda like **`git pull`** that just combinds two commands into one.
```
git checkout -
```
returns you to the previous branch.
```
git checkout [branch-name]
```
switch to another branch and check it out into your working directory.
```
git merge [branch]
```
merge the specified branch's history into the current one.
```
git log
```
show all commits in the current branch's history.

---
