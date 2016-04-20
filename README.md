# Git Commands Cheatsheet

Reference list of common git commands.

## Remotes
| Command                                                                                                            | Purpose                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------|
| git remote -v                                                                                                      | show remove repositories for local repo                                                                        |
| git remote rm `<name>`                                                                                             | remove remote repository                                                                                       |
| git remote add `<name>` `<address>`                                                                                | add remote repository                                                                                          |
| git push  -u `<remote>` `<branch>`                                                                                 | push to remote and branch name. after using -u once you can just use `git push` to push to same remote & branch|

## Diffs
| Command                                                                                                            | Purpose                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------|
| git diff                                                                                                           | unstaged differences from last commit                                                                          |
| git diff --staged                                                                                                  | staged differences from last commit                                                                            |

## Commits
| Command                                                                                                            | Purpose                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------|
| git commit -a -m "`<message>`"                                                                                     | Add tracked files to stage and commit                                                                          |
| git commit -ammend -m "`<message>`"                                                                                | Ammend last commit                                                                                             |
| git reset --soft HEAD^                                                                                             | Reset last commit into staging                                                                                 |
| git reset --hard HEAD^                                                                                             | Blow away last commit                                                                                          |
| git reset --hard HEAD^^                                                                                            | Blow away last two commits                                                                                     |