# git-branching-practice
Practice Git branching, merging, rebasing, reverting, cherry-picking, and remote repository operations using a personal GitHub repository.
#commands
git branch
git branch
git checkout -b feature/login
git checkout main
git checkout -b feature/register
git branch
git checkout feature/login
git checkout feature/register
git checkout feature/register
git checkout main
git checkout
git checkout feature/register
git checkout main
git checkout feature/login
git checkout main
## Creating branches (feature/login, feature/register) and switching between them throughout the session
##

GIT MERGE
git merge feature/login
git merge feature/register
git merge main          # (run multiple times, from feature/register)
git merge origin/feature/register
## Combining branches — merging feature/login and feature/register into main, and later merging main's new commits back into feature/register ##

GIT REBASE
git rebase feature/register
git rebase feature/register   # run a second time later
## Reapplying main's commits on top of feature/register to create a linear history — done twice in your session ##

GIT REVERT
git revert 7479def
## Undid the "hii team" commit (which had added ccp.txt) by creating a new commit (cda0ae3) that deleted the file — while keeping the original commit in history.##

GIT CHERRY-PICK
git cherrypick dc58fc3      # (typo — command not found)
git cherry-pick dc58fc3     # first attempt — caused a conflict
git cherry-pick dc58fc3     # second attempt — blocked by uncommitted local changes
git cherry-pick dc58fc3     # third attempt — succeeded after committing local changes
## Copying the single commit dc58fc3 ("1", which modified ccp.txt) from main onto feature/register without merging the whole branch. Took three attempts due to a conflict and uncommitted changes getting in the way.##

git push origin feature/login
git push origin feature/register
git push origin main
git push origin
git push origin main
git push origin main
git push origin feature/register
## Uploading local commits/branches to GitHub at various points — after initial commits, after merges, and after the cherry-pick.##

GIT PULL
git pull origin main
git pull origin feature/register
## Fetching + merging remote changes into your local branch — used once to sync main, and once to bring down a teammate's/your own remote update to feature/register (the ccp.txt edit that came from GitHub directly, likely edited via GitHub web UI).##

GIT FETCH
git fetch origin feature/register
git fetch origin
git fetch
git fetch
git fetch
## Checking for new remote commits without merging them — run repeatedly to detect updates on origin/feature/register ##



