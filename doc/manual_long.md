| /do/git/create                              |                                                                      |
|:--------------------------------------------|:---------------------------------------------------------------------|
| Info                                        | [beta] [interactive]                                                 |
| Description                                 | Create a repo on github (you need to create it on github.com before) |
| Usage                                       | /do/git/create myusername/repo                                       |
| Example                                     | /do/git/create pigetnet/core                                         |
| Arguments                                   | 1:repo,                                                              |
| Variables                                   | repo=$1, remoteErr=$?, pushErr=$?,                                   |
| System                                      | /system/logInit $0,                                                  |
| 1. LOCAL: $repo ---> [NEW] GITHUB: $repo    |                                                                      |
| 1. $repo created                            |                                                                      |
| 2. https://github.com/$repo                 |                                                                      |
| 3. $repo already created                    |                                                                      |
| 4. https://github.com/$repo                 |                                                                      |
| 5. Failed to create $repo                   |                                                                      |
| 6. Check if https://github.com/$repo exists |                                                                      |

| /do/git/forcesave                            |                                                         |
|:---------------------------------------------|:--------------------------------------------------------|
| Info                                         | [beta] [danger]                                         |
| Description                                  | Force push to github (this will erase change on github) |
| Usage                                        | /do/git/forcesave                                       |
| Variables                                    | repoName=$(/do/git/name), pushErr=$?,                   |
| Modules                                      | repoName=$(/do/git/name),                               |
| System                                       | /system/logInit "$0 $repoName",                         |
| File exists                                  | ".git/config"                                           |
| 1. LOCAL:$repoName -FORCE-> GITHUB:$repoName |                                                         |
| 1. Repo saved                                |                                                         |
| 2. Repo not saved                            |                                                         |
| 3. This is not a git repo                    |                                                         |

| /do/git/forceupdate                          |                                                                  |
|:---------------------------------------------|:-----------------------------------------------------------------|
| Info                                         | [beta] [danger]                                                  |
| Description                                  | Force Update current folder (this will erase all local changes!) |
| Usage                                        | /do/git/forceupdate                                              |
| Variables                                    | repoName=$(/do/git/name),                                        |
| Modules                                      | repoName=$(/do/git/name),                                        |
| File exists                                  | ".git/config"                                                    |
| 1. GITHUB:$repoName -FORCE-> LOCAL:$repoName |                                                                  |
| 1. $repoName has been updated                |                                                                  |
| 2. Not a git repo                            |                                                                  |

| /do/git/generateReadMe                   |                                                                 |
|:-----------------------------------------|:----------------------------------------------------------------|
| Info                                     | [alpha] [wip]                                                   |
| Description                              | Analyse scripts on current directory and generate a readme file |
| Usage                                    | /do/git/generateReadMe                                          |
| Variables                                | currentDir=$(/show/dir),                                        |
| System                                   | /system/makedir ./doc,                                          |
| 1. Generate readme for current directory |                                                                 |
| 1. Erase previous manual.md              |                                                                 |
| 2. Scanning $currentDir/$scripts         |                                                                 |
| 3. manual.md finished                    |                                                                 |

| /do/git/generateReadMeVerbose            |                                                                         |
|:-----------------------------------------|:------------------------------------------------------------------------|
| Info                                     | [alpha] [wip]                                                           |
| Description                              | Analyse scripts on current directory and generate a verbose readme file |
| Usage                                    | /do/git/generateReadMeVerbose                                           |
| Variables                                | currentDir=$(/show/dir),                                                |
| System                                   | /system/makedir ./doc,                                                  |
| 1. Generate readme for current directory |                                                                         |
| 1. Erase previous manual_long.md         |                                                                         |
| 2. Scanning $currentDir/$scripts         |                                                                         |
| 3. ./doc/manual_long.md finished         |                                                                         |

| /do/git/hash   |                                             |
|:---------------|:--------------------------------------------|
| Info           | [beta] [return]                             |
| Description    | Show git hash of current folder             |
| Usage          | Description Show git hash of current folder |
| File exists    | ".git/config"                               |

| /do/git/name   |                                                       |
|:---------------|:------------------------------------------------------|
| Info           | [beta] [return]                                       |
| Description    | Display current directory Repository name             |
| Usage          | Description Display current directory Repository name |

| /do/git/README.MD   |                        |
|:--------------------|:-----------------------|
| Info                | [alpha] [undocumented] |

| /do/git/restore                                      |                                         |
|:-----------------------------------------------------|:----------------------------------------|
| Info                                                 | [beta] [interactive] [danger]           |
| Description                                          | Restore git repo to last remote state   |
| Usage                                                | /do/git/restore                         |
| Variables                                            | repoName=$(/do/git/name), commitErr=$?, |
| Modules                                              | repoName=$(/do/git/name),               |
| System                                               | /system/logInit "$0 $repoName",         |
| File exists                                          | ".git/config"                           |
| 1. GITHUB:$repoName [RESTORE] ----> GITHUB:$repoName |                                         |
| 1. Repo restored                                     |                                         |
| 2. Repo not restored                                 |                                         |
| 3. This is not a git repo                            |                                         |

| /do/git/save                                                                              |                                                      |
|:------------------------------------------------------------------------------------------|:-----------------------------------------------------|
| Info                                                                                      | [beta] [interactive]                                 |
| Description                                                                               | Add all, commit and push current directory to Github |
| Usage                                                                                     | /do/git/save                                         |
| Variables                                                                                 | repoName=$(/do/git/name), commitErr=$?, pushErr=$?,  |
| Modules                                                                                   | repoName=$(/do/git/name),                            |
| System                                                                                    | /system/logInit "$0 $repoName",                      |
| File exists                                                                               | ".git/config"                                        |
| 1. LOCAL:$repoName ----> GITHUB:$repoName                                                 |                                                      |
| 1. Repo saved                                                                             |                                                      |
| 2. Repo not saved                                                                         |                                                      |
| 3. You can force this (this will erase any change on Github) by typing: /do/git/forcesave |                                                      |
| 4. Nothing to save                                                                        |                                                      |
| 5. This is not a git repo                                                                 |                                                      |

| /do/git/saveDoc   |                                                                      |
|:------------------|:---------------------------------------------------------------------|
| Info              | [alpha] [undocumented]                                               |
| Modules           | /do/git/generateReadMe, /do/git/generateReadMeVerbose, /do/git/save, |

| /do/git/settings                                        |                                           |
|:--------------------------------------------------------|:------------------------------------------|
| Info                                                    | [beta]                                    |
| Description                                             | Display git configuration (git config -l) |
| Usage                                                   | /do/git/settings                          |
| 1. ~~~~~~~~~~~~~ Git configuration ~~~~~~~~~~~ $PICOLOR |                                           |
| 2. ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ $PICOLOR          |                                           |

| /do/git/setup                                                             |                                   |
|:--------------------------------------------------------------------------|:----------------------------------|
| Info                                                                      | [beta] [interactive]              |
| Description                                                               | Configure git client (name/email) |
| Usage                                                                     | /do/git/setup                     |
| Softwares                                                                 | git,                              |
| Variables                                                                 | name=$ASKUSER, email=$ASKUSER,    |
| System                                                                    | /system/install git,              |
| 1. Git Client Setup                                                       |                                   |
| 2. -- Ask user: Github nickname (not your email)                          |                                   |
| 3. -- Ask user: Github email                                              |                                   |
| 4. Password is now cached for 15 minutes                                  |                                   |
| 5. http://stackoverflow.com/questions/5343068/is-there-a-way-to-skip-pass |                                   |

| /do/git/undo               |                                                           |
|:---------------------------|:----------------------------------------------------------|
| Info                       | [beta] [interactive] [danger]                             |
| Description                | Erase last commit on github (use it only on last resort!) |
| Usage                      | /do/git/undo                                              |
| Modules                    | /do/git/forcesave,                                        |
| 1. Undo last commit ?      |                                                           |
| 1. Are you really sure ?   |                                                           |
| 2. git reset --hard HEAD~1 |                                                           |

| /do/git/update                            |                                                                |
|:------------------------------------------|:---------------------------------------------------------------|
| Info                                      | [beta]                                                         |
| Description                               | Update current folder                                          |
| Usage                                     | /do/git/update                                                 |
| Variables                                 | repoName=$(/do/git/name), pullMessage=$(git pull), pullErr=$?, |
| Modules                                   | repoName=$(/do/git/name),                                      |
| File exists                               | ".git/config"                                                  |
| 1. GITHUB:$repoName ----> LOCAL:$repoName |                                                                |
| 1. $repoName is already up-to-date        |                                                                |
| 2. $repoName has been updated             |                                                                |
| 3. $repoName was not updated              |                                                                |
| 4. Not a git repo                         |                                                                |

