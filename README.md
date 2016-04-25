# Git Commands Cheatsheet

Reference list of common git commands. 

`<remote>` remote repository name (i.e. Github automatically adds `origin` remote to your repo)

`<branch>` branch name

`<message>` comit message

## Remotes
| Command                                                                                                            | Purpose                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------|
| git remote -v                                                                                                      | show remove repositories for local repo                                                                        |
| git remote rm `<remote>`                                                                                             | remove remote repository                                                                                       |
| git remote add `<remote>` `<address>`                                                                                | add remote repository                                                                                          |
| git push  -u `<remote>` `<branch>`                                                                                 | push to remote and branch name.                                                                                |
| git remote show `<remote>`                                                                                 | shows all remote branches and local branches (and whether local is up to date) 

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
| git checkout master; git merge `<branch>`                                                                     | merge branch with master                                                                                       |
| git checkout master; git merge `<branch>`                                                                     | remove branch (do this after merge)                                                                            |
| git push `<remote>` master `<branch>`                                                                     | make local branch a remote branch on master  
| git push `<remote>` :`<branch>`                                                                    | adding colon deletes remote branch, not the local branch though
                                                                          |