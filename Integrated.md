<!-- Head -->

# Integrated

### Connection with Cmder, vscode, Github

**Often used command with Cmder**
|Command|Description|
|--|--|
|Connection between git and vscode using comder|git config --global core.editor "code --wait"|
|Open vscode(Mac OS)|code .|
|Open vscode(Android OS)|git config --global -e|
|Open Directory|explorer ."Directory name"|
|move to Child Directory|cd "Directory name"|
|move to Parent Directory |cd ..|
|Make Directory|mkdir "Directory name"|
|Delete Directory|rm -rf "Directory name"|
|Delete file|rm file name.txt|
|Initialize git|git init|
|Check git status|git status|
|Summary git status|git status -s|
|Write comment in file(untracked) and creat the file|echo comment >file name.txt|
|Make file from untracked to tracked|git add .|
|Make file from tracked to untracked|git rm --cached \*.txt|
|Read comment in file|cat file name.txt|
|Open text file in staged area with vscode|git difftool --staged|
|Move file from staged area to git repository|git commit|
|git commit with message|git commit -m "message"|
|Check git history|git log|
|Clone github repository from remote area to local area|git clone "github address"|
|Upload file from staged area to remote area named "github"|git push|

**Sequence**

- Make user.name in github
  `git config --global user.name "github ID"`
- Make user.email in github
  `git config --global user.email "github email"`

* Initialize .git hidden folder
  `git init`
* Write comment in text file
  `echo "comment" > name.txt`
* Make file from untracked to tracked
  `git add .`
* Move file from staged area to git repository
  `git commit -m "Message"`
* Clone github to local area
  `git clone "github address"`
* Upload code in github
  `git push`

**Resolve failure**

- Fatal : authentication failed error when git push after git commit.
  - occurred in creating new repository first time and I didn't change information of user.
  - This situation normally occurred when changed information of user.
  - In my case, this situation maybe occurred when creating and deleting repository several times.
  - I guess crashing between Windows credential manager and saved credentials from my local git configuration.
- Countmeasure : input code below for clearing failed credentials.
  `git config --unset-all credential.helper` : reset credentials at the repository level.
  `git config --global --unset-all credential.helper` : reset credentials at user level.
  `git config --system --unset credential.helper` : reset credentials at system level.
- It would also be helpful to see output of `git config --list --show-origin` when run in the repository directory I am trying to connect to.
