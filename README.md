# Git Commands Cheatsheet

A list of common git commands

## Remotes
| Command                                                                                                            | Purpose                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------|
| git remote -v                                                                                                      | show remove repositories for local repo                                                                        |
| git push  -u [remote] [branch]                                                                                     | push to specific remote and branch name                                                                        |

## Diffs

| Command                                                                                                            | Purpose                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------|
| git diff                                                                                                           | unstaged differences from last commit                                                                          |
| git diff --staged                                                                                                  | staged differences from last commit                                                                            |

## Reset commits

| Command                                                                                                            | Purpose                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------|
| git reset --soft HEAD^                                                                                             | Reset last commit into staging                                                                                 |
| git reset --hard HEAD^                                                                                             | Blow away last commit                                                                                          |
| git reset --hard HEAD^^                                                                                            | Blow away last two commits                                                                                     |
