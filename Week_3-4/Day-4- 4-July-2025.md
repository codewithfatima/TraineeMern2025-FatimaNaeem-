###  # Git Branching, Merge, Rebase & Conflict Resolution – Quick Notes

## 🧠 Branching Basics

-   Create a new branch:
    
    bash
    
    CopyEdit
    
    `git checkout -b feature/my-feature` 
    
-   List all branches:
    
    bash
    
    CopyEdit
    
    `git branch` 
    
-   Switch branches:
    
    bash
    
    CopyEdit
    
    `git checkout main` 
    
-   Delete local branch:
    
    bash
    
    CopyEdit
    
    `git branch -d feature/my-feature` 
    

## 🔀 Merge vs Rebase (TL;DR)

Merge

Rebase

Combines histories

Rewrites history

Keeps full history

Makes history linear

Good for preserving context

Good for clean commit history

### 🔁 Merge

bash

CopyEdit

`# Merge feature branch into main git checkout main
git merge feature/my-feature` 

### 🔄 Rebase

bash

CopyEdit

`# Rebase your branch onto main git checkout feature/my-feature
git rebase main` 

> 🔥 Fireship Tip: Rebase before merging for cleaner history (especially in PRs).

----------

## ⚔️ Merge Conflict Resolution

1.  Git will show conflicted files:
    
    bash
    
    CopyEdit
    
    `git status` 
    
2.  Open file and resolve conflict markers:
    
    txt
    
    CopyEdit
    
    `<<<<<<< HEAD
    your current branch changes
    =======
    incoming branch changes
    >>>>>>> feature/my-feature` 
    
3.  After editing, mark as resolved:
    
    bash
    
    CopyEdit
    
    `git add <file>` 
    
4.  Continue merge or rebase:
    
    bash
    
    CopyEdit
    
    `# If merging git commit # If rebasing git rebase --continue` 
    

----------

## 💡 Pro Tips

-   Always pull with rebase to avoid messy merge commits:
    
    bash
    
    CopyEdit
    
    `git pull --rebase` 
    
-   Abort merge or rebase if things go wrong:
    
    bash
    
    CopyEdit
    
    `git merge --abort
    git rebase --abort` 
    
-   Use visual tools:
    
    -   `git log --graph --oneline --all` – see branching tree
        
    -   VSCode Git UI or `GitKraken` for visual conflict resolution
        

----------

## 🧼 Clean Up

-   Delete merged branches:
    
    bash
    
    CopyEdit
    
    `git branch -d feature/my-feature` 
    
-   Clean stale remote branches:
    
    bash
    
    CopyEdit
    
    `git remote prune origin`
