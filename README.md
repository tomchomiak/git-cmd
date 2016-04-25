# Git Commands Cheatsheet

Reference list of common git commands. 

`<remote>` remote repository name (i.e. Github automatically adds `origin` remote to your repo)

`<address>` canonical url for remote repository

`<branch>` branch name

`<message>` commit message

## Remotes
| Command                                                                                                            | Purpose                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------|
| git remote -v                                                                                                      | show remove repositories for local repo                                                                        |
| git remote rm `<remote>`                                                                                             | remove remote repository                                                                                       |
| git remote add `<remote>` `<address>`                                                                                | add remote repository                                                                                          |
| git push  -u `<remote>` `<branch>`                                                                                 | push to remote and branch name.                                                                                |
| git remote show `<remote>`                                                                                 | show status of all remote and local branches

## Diffs
| Command                                                                                                            | Purpose                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------|
| git diff                                                                                                           | unstaged differences from last commit                                                                          |
| git diff --staged                                                                                                  | staged differences from last commit                                                                            |

## Commits
| Command                                                                                                            | Purpose                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------|
| git commit -a -m "`<message>`"                                                                                     | Add tracked files to stage and commit                                                                          |
| git commit -amend -m "`<message>`"                                                                                 | Amend last commit                                                                                              |
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
| git checkout master; git merge `<branch>`                                                                     | merge branch with master                                                                      |
| git push `<remote>` master `<branch>`                                                                     | make local branch a remote branch on master  
| git push `<remote>` :`<branch>`                                                                    | adding colon deletes remote branch, not the local branch though |

  
| git branch -d `<branch>` | remove local branch (will warn if have uncommited work) |
| git branch -D `<branch>` | remove local branch and blow away any uncommited work |
  
| git push `<remote>` :`<branch>`                                                                    | adding colon deletes remote branch, not the local branch though |