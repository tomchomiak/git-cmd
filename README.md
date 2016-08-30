# Git Commands Cheatsheet

Reference list of common git commands. Bug fix

* [Glossary](#dynamic-targets)
* [Help](#help)
* [Git Config](#configuration)
* [Starting a repo](#starting-a-repo)
* [Tracking and Staging Files](#tracking-and-staging-files)
* [Git History](#git-history)
* [Remotes](#remotes)
* [Diffs](#diffs)
* [Commits](#commits)
* [Branching](#branching)


## Dynamic Targets

`<remote>` remote repository name (i.e. Github automatically adds `origin` remote to your repo)

`<address>` canonical url for remote repository

`<branch>` branch name

`<message>` commit message

`<file>` path to a file

`HEAD` refers to the last commit on the current branch you are on

## Help

| Command | Purpose |
| -------- | ------ |
| git help |  will return a list of commands |
| git help `<command>` | will return info about that command|

## Configuration

| Command | Purpose |
| -------- | ------ |
| git config --global user.name "Tom Chomiak" | globally set your user name |
| git config --global user.email "youremail@email.com" | globally set your email |
| git config --global color.ui true | enable colors in git command line |

## Starting a Repo

Create local git directory

```bash
mkdir test
cd test
git init
```

## Tracking and Staging Files

| Command | Purpose |
| ------- | ------ |
| git add `<file>` | add file to staging area for commit |
| git add `<file>` `<file>` | add multiple files to staging area for commit |
| git add --all | Adds all **tracked files** that have changed to staging area|
| git add *.txt | Adds all text files in current directory |
| git add app/ | Adds all files in app directory |
| git add app/*.txt | Adds all text files in app directory|
| git add "*.txt" | Adds all text files in the entire project |

## Unstaging Files
| Command | Purpose |
| ------- | ------ |
| git reset HEAD `<file>` | Unstage a file |
| git checkout `<file>`| reset unstaged file to the state it was in in last commit |


## Git History

| Command | Purpose |
| ------- | ------ |
| git log | list git timeline history|
| | |

## Remotes
| Command                                                                                                            | Purpose                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------|
| git remote -v | show remove repositories local repo knows about |
| git remote rm `<remote>` | remove remote repository |
| git remote add `<remote>` `<address>`                                                                                | add remote repository                                                                                          |
| git push  -u `<remote>` `<branch>`                                                                                 | push to remote and branch name.                                                                                |
| git push heroku `<branch>`:`master` | push branch to heroku. heroku only deploys master|
| git remote show `<remote>` | show status of all remote and local branches|
| git remote prune `<remote>` | remove stale branches|

## Diffs
| Command                                                                                                            | Purpose                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------|
| git diff                                                                                                           | unstaged differences from last commit                                                                          |
| git diff --staged                                                                                                  | staged differences from last commit                                                                            |

## Commits
| Command                                                                                                            | Purpose                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------|
| git commit -m "`<message>`" | Make a commit with message |
| git commit -a -m "`<message>`"                                                                                     | Add tracked files to stage and commit                                                                          |
| git commit --amend -m "`<message>`"                                                                                 | Amend last commit                                                                                              |
| git reset --soft HEAD^                                                                                             | Reset last commit into staging                                                                                 |
| git reset --hard HEAD^                                                                                             | Blow away last commit                                                                                          |
| git reset --hard HEAD^^                                                                                            | Blow away last two commits                                                                                     |

## Branching
| Command                                                                                                            | Purpose                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------|
| git branch                                                                                                         | show current branch along with available local branches                                                                                            |
| git branch -r                                                                                               | list all remote branches branch                                                                                      |
| git branch `<branch>`                                                                                                | create new feature branch                                                                                      |
| git checkout `<branch>`                                                                                       | switch timelines to branch                                                                                     |
| git checkout -b `<branch>`                                                                                    | shortcut that creates branch and then checks it out                                                            |
| git checkout master; git merge `<branch>` | merge branch with master |
| git push `<remote>` master `<branch>`  | make local branch a remote branch on master |
| git push `<remote>` :`<branch>` | adding colon deletes remote branch, not the local branch though |
| git branch -d `<branch>` | remove local branch (will warn if have uncommited work) |
| git branch -D `<branch>` | remove local branch and blow away any uncommited work |
