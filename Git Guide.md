**Case Study 1: Start a New Project \& Push to Remote**

Scenario



You are starting a backend project and need to push it to GitHub.



**Steps \& Commands**

git init

git status

git add .

git commit -m "Initial project setup"

git branch -M main

git remote add origin https://github.com/user/project.git

git push -u origin main



Key Commands Explained

**Command**			**Purpose**

git init			Initialize repository

git add .		Stage all files

git commit		Save snapshot

git push -u		Link local \& remote branch



**Case Study 2: Feature Development Using Branching**

Scenario



You are adding login functionality without disturbing main code.



Steps

git checkout -b feature/login

\# code changes

git add .

git commit -m "Added login feature"

git checkout main

git merge feature/login



Best Practice



1. &nbsp;Always create feature branches
2. &nbsp;Merge only tested code



 **Case Study 3: Sync Local Code With Remote (Team Collaboration)**

Scenario



Team members pushed changes; your local repo is outdated.



**Steps**

git fetch origin

git pull origin main



**Difference**

Command			Description

git fetch			Downloads changes only

git pull				Fetch + merge

 **Case Study 4: Undo Last Commit (Safe \& Unsafe)**

Scenario



You committed wrong code.



Options



Keep Changes



git reset --soft HEAD~1



Remove Changes

git reset --hard HEAD~1





⚠ Warning: --hard deletes work permanently



 **Case Study 5: Fix Mistakes Using git stash**

Scenario



Urgent bug fix needed but you have unfinished work.



Steps

git stash

git checkout main

\# fix bug

git commit -m "Hotfix"

git checkout feature/login

git stash pop



Utility



Temporarily saves working directory

Very useful during production issues



 **Case Study 6: Resolve Merge Conflict**



Scenario



Two developers changed the same file.



Steps

git pull origin main





Git shows conflict:



<<<<<<< HEAD

Your code

=======

Other developer code

>>>>>>> branch-name



Resolution



Open file



Choose correct code



Save file



git add .

git commit -m "Resolved merge conflict"



 **Case Study 7: Cherry-Pick Specific Commit**

Scenario



You want only one commit from another branch.



git cherry-pick <commit-hash>





1. Ideal for hotfixes
2. Avoids full branch merge



 **Case Study 8: View History \& Debug Issues**



**Useful Commands**

git log --oneline

git log --graph --all

git blame filename

git diff



**Command**					**Use**

git blame				Who changed what

git diff					File changes

git log --graph			Branch visualization

&nbsp;



**Case Study 9: Rename \& Delete Branches**



git branch -m old-name new-name

git branch -d feature/login

git push origin --delete feature/login



 **Case Study 10: Revert a Commit (Safe for Production)**

Scenario



Bad commit already pushed.



git revert <commit-hash>





1. Does not rewrite history
2. Best for production systems



&nbsp;Case Study 11: Clean Untracked Files

git clean -n   # preview

git clean -f   # delete





**Removes build/cache files**



&nbsp;Case Study 12: Tagging for Releases

git tag v1.0.0

git push origin v1.0.0





**Useful for production releases**



&nbsp;Case Study 13: Squash Commits Before Merge



git rebase -i HEAD~3





Change:



pick → squash





1. Clean commit history
2. Preferred in teams



&nbsp;Case Study 14: Clone Specific Branch

git clone -b develop https://github.com/user/repo.git



 **Case Study 15: Recover Lost Commit**



git reflog

git checkout <commit-hash>





**Lifesaver command**



 **Most Important Git Utility Commands (Quick Cheat Sheet)**

git status

git log --oneline

git diff

git stash

git reset

git revert

git cherry-pick

git rebase

git reflog

