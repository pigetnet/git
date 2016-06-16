| /do/git/create   |                                                                      |
|:-----------------|:---------------------------------------------------------------------|
| Description      | Create a repo on github (you need to create it on github.com before) |
| Example          | /do/git/create pigetnet/core                                         |
| Info             | [beta] [interactive]                                                 |
| Arguments        | 1:repo,                                                              |

| /do/git/forcesave   |                                                         |
|:--------------------|:--------------------------------------------------------|
| Description         | Force push to github (this will erase change on github) |
| Info                | [beta] [danger]                                         |

| /do/git/forceupdate   |                                                                  |
|:----------------------|:-----------------------------------------------------------------|
| Description           | Force Update current folder (this will erase all local changes!) |
| Info                  | [beta] [danger]                                                  |

| /do/git/generateReadMe   |                                                                 |
|:-------------------------|:----------------------------------------------------------------|
| Description              | Analyse scripts on current directory and generate a readme file |
| Info                     | [alpha] [wip]                                                   |

| /do/git/generateReadMeVerbose   |                                                                         |
|:--------------------------------|:------------------------------------------------------------------------|
| Description                     | Analyse scripts on current directory and generate a verbose readme file |
| Info                            | [alpha] [wip]                                                           |

| /do/git/hash   |                                 |
|:---------------|:--------------------------------|
| Description    | Show git hash of current folder |
| Info           | [beta] [return]                 |

| /do/git/name   |                                           |
|:---------------|:------------------------------------------|
| Description    | Display current directory Repository name |
| Info           | [beta] [return]                           |

| /do/git/restore   |                                       |
|:------------------|:--------------------------------------|
| Description       | Restore git repo to last remote state |
| Info              | [beta] [interactive] [danger]         |

| /do/git/save   |                                                      |
|:---------------|:-----------------------------------------------------|
| Description    | Add all, commit and push current directory to Github |
| Info           | [beta] [interactive]                                 |

| /do/git/saveDoc   |                        |
|:------------------|:-----------------------|
| Info              | [alpha] [undocumented] |

| /do/git/settings   |                                           |
|:-------------------|:------------------------------------------|
| Description        | Display git configuration (git config -l) |
| Info               | [beta]                                    |

| /do/git/setup   |                                   |
|:----------------|:----------------------------------|
| Description     | Configure git client (name/email) |
| Info            | [beta] [interactive]              |

| /do/git/undo   |                                                           |
|:---------------|:----------------------------------------------------------|
| Description    | Erase last commit on github (use it only on last resort!) |
| Info           | [beta] [interactive] [danger]                             |

| /do/git/update   |                       |
|:-----------------|:----------------------|
| Description      | Update current folder |
| Info             | [beta]                |

