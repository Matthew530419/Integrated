# Integrated

### Connection with Cmder, vscode, Github

**Often used command Using Cmder**
|Command|Descriotion|
|--|--|
|Connection between git and vscode using comder|git config --global core.editor "code --wait"|
|Open vscode(1)|code .|
|Open vscode(2)|git config --global -e|
|Open folder|explorer .folder name|
|move to subfolder|cd folder name|
|Go up one folder level|cd ..|
|Make folder|mkdir folder name|
|Delete folder|rm -rf folder name|
|Delete file|rm file name.txt|
|Initialize git|git init|
|Check git status|git status|
|Summary git status|git status -s|
|Write comment in file(untracked)|echo comment >file name.txt|
|Make file from untracked to tracked|git add .|
|Make file from tracked to untracked|git rm --cached \*.txt|
|Read comment in file|cat file name.txt|
|Launch text file in staged area with vscode|git difftool --staged|
|Move file from staged area to git repository|git commit|
|git commit with comment|git commit -m "message"|
|Check git history|git log|
|Clone github to local area|git clone "github address"|
|Upload code in github|git push|

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
  `git commit`
* Clone github to local area
  `git clone "github address"`
* Upload code in github
  `git push`

**Resolve failure**

- Fatal : authentication failed error when git push after git commit
  - occured in creating new repository first time and I didn't change information of user
  - This situation maybe occured when creating and deleting repository several times 
- Countmeasure : input code below
  `git config --system --unset credential.helper`
