# 2020-04-24: Git Collaboration Notes

Git collaboration workshop

- `git clone <URL>`: downloads the repository from the web to our computer
    - Make sure you don't nest this command in another repository
    - just like `git init` do this only once per repository

## Branches

- `git branch <branch_name>`: create a new branch
- `git switch <branch_name>`: move to a branch
    - `git checkout <branch_name>`: old way of moving to branch

- `git switch -c <branch_name>`: create and move in 1 command
    - `git checkout -b <branch_name>`

- `git stash`: temp saves current state as a commit so you can `checkout` or `switch`
    - `git stash apply` to apply the last stash from the stack

## Pull requests (Online Merge)

- `git push origin <branch_name>`: pushes branch to the remote
    - this is where you will create the PR (online)
    - you merge the PR (and also the branch) by accepting and merging the PR
- don't forget to clean up your branches
- `git fetch --prune`: cleans up the refrences in your `git log --oneline --graph --decorate --all`
- `git branch -d <branch_name>`: delete branch on your local machine
    - it will tell you to move to another branch (e.g., `master`) first

