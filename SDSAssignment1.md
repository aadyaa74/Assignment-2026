## 1.commit-one-file
git add A.txt
git commit -m "commit A.txt"

## 2.commit-one-file-staged
git reset --soft HEAD~1
git add B.txt
git reset A.txt
git commit -m "commit B.txt"

## 3.ignore-them
touch .gitignore
# add the file names in .gitignore file
git add .gitignore
git commit -m "commit .gitignore"

## 4.chase-branch
git checkout chase-branch
git merge escaped

## 5.merge-conflict
git checkout merge-conflict
git merge another-piece-of-work
# manually make changes in file
git add .
git commit

## 6.save-your-work
git stash
# fix bug
git commit -am "remove bug"
git stash apply

## 7.change-branch-history
git checkout change-branch-history
git rebase hot-bugfix   

## 8.remove-ignored
git rm --cached ignored.txt
git commit -am "untrack ignored.txt"

## 9.case-sensitive-filename
git mv File.txt file.txt
git add file.txt
git commit -m "file renamed in lowercase"

## 10.fix-typo
# correct typo in file
git commit --amend -m "corrected message"

## 11.forge-date
git commit --amend --no-edit --date="27-02-1987"

## 12.fix-old-typo
git rebase -i HEAD^2
# change pick to edit and fix typo in file
git add file.txt
git rebase --continue
# fix conflict
git add file.txt
git rebase --continue