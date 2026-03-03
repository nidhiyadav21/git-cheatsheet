1️⃣ Basic Commands
Configure Git
git config --global user.name "Your Name"
git config --global user.email "your@email.com"

Configure locally:

git config --local user.name "Your Name"
git config --local user.email "your@email.com"
Initialize Repository
git init

Creates a .git folder to track history.

Check Status
git status

Shows:

Untracked files

Modified files

Staged files

Add Files

Add specific file:

git add file1 file2

Add all files:

git add .
Commit

Open editor:

git commit

Inline message:

git commit -m "Commit message"

Commit & stage together:

git commit -a -m "Message"

Amend previous commit:

git commit --amend
View Logs
git log
git log --oneline
2️⃣ Branch Commands
View Branches
git branch
git branch -v
Create Branch
git branch branch_name
Switch Branch
git switch branch_name

Old way:

git checkout branch_name
Create & Switch
git switch -c branch_name
Delete Branch
git branch -d branch_name
git branch -D branch_name   # force delete
Merge Branch
git merge branch_name

⚠ Be on the branch where you want to merge.

3️⃣ Git Diff
View Unstaged Changes
git diff
View Staged Changes
git diff --staged
Compare Branches
git diff branch1 branch2
Compare Commits
git diff commit1..commit2
4️⃣ Git Stash
Save Changes
git stash
View Stash List
git stash list
Apply Stash
git stash apply
Pop Stash
git stash pop
Delete Stash
git stash drop stash@{0}
git stash clear
5️⃣ Time Travel
Checkout Old Commit
git checkout commit_hash

⚠ Detached HEAD state

Return back:

git switch main
Move Back Using HEAD
git checkout HEAD~1
6️⃣ Reset & Revert
Soft Reset
git reset --soft commit_hash

Keeps changes staged.

Hard Reset
git reset --hard commit_hash

Deletes commits & changes permanently.

Revert Commit
git revert commit_hash

Creates new commit that undoes changes.

7️⃣ Remote Repository
Check Remote
git remote -v
Add Remote
git remote add origin https://github.com/username/repo.git
Remove Remote
git remote remove origin
8️⃣ Push, Pull & Fetch
Push
git push origin branch_name

Set upstream:

git push -u origin branch_name
Pull
git pull origin branch_name
Fetch
git fetch
git fetch --prune
9️⃣ Git Rebase
git switch feature_branch
git rebase main

Abort:

git rebase --abort

Continue:

git rebase --continue

Interactive rebase:

git rebase -i HEAD~3
🔟 Git Tags

Create tag:

git tag v1.0

Annotated tag:

git tag -a v1.0 -m "Version 1.0"

Push tag:

git push origin v1.0

Push all tags:

git push origin --tags
1️⃣1️⃣ GitFlow

Initialize:

git flow init

Start Feature:

git flow feature start feature_name

Finish Feature:

git flow feature finish feature_name

Release:

git flow release start 1.0.0
git flow release finish 1.0.0

Hotfix:

git flow hotfix start bug_name
git flow hotfix finish bug_name
1️⃣2️⃣ SSH Setup

Generate SSH Key:

ssh-keygen -t ed25519 -C "your_email@example.com"

Add to SSH agent:

eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519

Copy public key:

cat ~/.ssh/id_ed25519.pub