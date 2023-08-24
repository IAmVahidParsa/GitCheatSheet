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

