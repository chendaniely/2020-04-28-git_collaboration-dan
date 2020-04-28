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

