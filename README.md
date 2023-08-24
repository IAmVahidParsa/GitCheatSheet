# GitCheatSheet
Git is the free and open-source distributed version control system that's responsible for everything GitHub related that happens locally on your computer. This cheat sheet features the most important and commonly used Git commands for easy reference.

### **SETUP**
Configuring user information used across all local repositories  .
One of the ost important concepts is collabration and in order to collabrate you have to identify who you are.  
The way we do that is by modifying **git config**.  
We can look at corrent **config list** by typing:  
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
representing all the files in the corrent working directory or any other files that changed since the last commit.
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
more efficent shortcut if you want to skip the **`add`** command, you can just go straight to **`git commit`** and use **`-a`** flag which will add all the files in the corrent working directory, the add a message after that to wrap-up the entire process in a single command.