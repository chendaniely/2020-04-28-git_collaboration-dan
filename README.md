# 2020-04-28: Git Collaboration

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

## Rebaseing or incorporating branch updates

- `git rebase <branch>`: if `branch` is `master` replay the current branch off of master
    - will auto merge if possible
    - potentially deal with conflicts

## Add collaborators

in the settings

## Additional Notes and links:

- Software Carpentry notes on basic git: https://swcarpentry.github.io/git-novice/
    - The setting up git has the commands to setup your name/email/editor: https://swcarpentry.github.io/git-novice/02-setup/index.html

- Git workflow notes and commands (to paste on your wall)
    - https://chendaniely.github.io/training_ds_r/help-faq.html

- Atlassian page on git workflows: https://www.atlassian.com/git/tutorials/comparing-workflows
    - The one we covered today was mainly the "Feature Branch Workflow": https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow

## Question from after the class:

- How to look at just the files that changed from a branch
    - One way is to push the branch to GitHub and create the PR. You can use the "files changed" tab to look at the files and the differences
    - On your computer you can use `git diff <commit hash>` to look at the diff locally (it will show the files changed and the diff)
    - `git diff --name-only master` will list files changed from current branch to master
        - You can also use `git diff --name-only <SHA1> <SHA2>` to get the files from any 2 places in history (using `git log --oneline` to get the SHA values)

- Getting your (bash) terminal to show current path and other things:
    - Use this to create your PS1 variable: http://bashrcgenerator.com/

- Show git branch in terminal:
    - In addition you can write a function and put that in your PS1 to also show git branch
    - https://gist.github.com/joseluisq/1e96c54fa4e1e5647940
