# Git Guide
### 1. Config user
```
git config --global user.name "Your Full Name"
git config --global user.email "your-email-address"
git config --list
```
### 2. Init git
```
mkdir "Repository Name"
cd ".\Repository Name"
git init
dir -hidden
```
### 3. First Commit
```
git status
git add ".\readme.md"
git status
git commit -m "Commit message: brief description"
git status
```
### 4. Create branch dir/branch-name
```
git branch dir/branch-name
git branch
```
### 5. Checkout branch
```
git checkout dir/branch-name
git status
```
### 6.  Merge to master
```
git checkout master
git status
git merge dir/branch-name
git status
git log
```
### 7. Create stash
```
git status
git stash
git status
```
### 8. Apply stash
```
git stash list
git stash Apply
git status
```
### 9. Drop stash 
```
git stash list
git stash drop 1
git stash list
```
### 10. Pop stash
``` 
git stash list
git stash Pop
git stash list
```
### 11. Revert Commit
```
git log --oneline
git revert [COMMIT_ID]
```
### 12. Cherry Pick
```
git log --oneline
git cherry-pick [COMMIT_ID]
```
### 13. Reset
```
git log --oneline
git reset --soft HEAD~1
git reset --mixed <commit>
git reset --hard <commit>
git reset --keep <commit>
git reset --merge <commit>
git reset <commit>
```
### 14. Create Patch
```
git diff HEAD > <file>
git diff <commit_id>^ <commit_id> > my_patch.diff

git format-patch -3
git format-patch <commit_range> --stdout > my_patch.diff

git cherry-pick <commit_id>
git diff HEAD^ > my_patch.diff
```
### 15. Apply Patch
```
git apply <file>
```
### 16. Init GitHub
```
git remote add origin [REMOTE-URL]
git push -u origin master
git push origin --all
```