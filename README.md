
# Learn basic to intermediate Git

![App Screenshot](https://github.com/alaminbhuyan/Instruction-of-Git/blob/main/Images/img.png)

## Generating SSH key for git-hub: (Best way to follow the git-hub SSH key generating process)

- At first, open "git besh" command prompt.

- ssh-keygen -t ed25519 -C "your_email@example.com" [ then press Enter ]
	
	- Enter passphrase (empty for no passphrase): [Type a passphrase] { you can skip it press Enter }
	- Enter same passphrase again: [Type passphrase again] { you can skip it press Enter }

- eval "$(ssh-agent -s)" [ then press Enter ]

- ssh-add ~/.ssh/id_rsa [ then press Enter ]

- cat ~/.ssh/id_rsa.pub [ then press Enter ]

- Then copy the Key and paste it git-hub ssh-key add settings.

## Screenshots

![App Screenshot](https://github.com/alaminbhuyan/Instruction-of-Git/blob/main/Images/ssh.jpg)


## Installation

Download Git from below link

```bash
  https://git-scm.com/download/win
```

## To check version and upgrade version

To check Git version

```bash
  git --version
```

To upgrade Git version

```bash
  git update-git-for-windows
```
## To set git configuration in local machine

To set username and email in locally

```bash
  git config user.name "your name"
  git config user.email "your email"
```

To set username and email in globally

```bash
  git config --global user.name "your name"
  git config --global user.email "your email"
```

To see which Email and Username used

```bash
  git config --list
```

## To create or initialize git repository

Run the below command and it will create .git folder by default

```bash
  git init
```
If you want to create a project folder and inside project folder you want to create .git folder then run this command.

```bash
  git init "project_folder_name"
```

## git status command

If you want to see the status files and folder then run

```bash
  git status
```

## git add command

If you want to take all the files and folder in staging area then run

```bash
  git add .
```
If you want to take a particular files in staging area then run

```bash
  git add file_name

  Ex: git add test.py
```
You can also use directory wildcard and directory and subdirectory wildcard

```bash
  git add *.file_extension

  Ex: git add *.js

  git add **/*.file_extension

  Ex: git add **/*.js
```
If you want unstag from staged then run
```bash
git restore --staged "file_name"
or
git rm --cached fileName
```
## git commit & uncommit command

Move the file to local repository from stagging area

```bash
  git commit -m "Your message"
```

If you want to add and commit together then run

```bash
  git commit -am "Commit message"
```
## Uncommit
If all you want to do is undo the act of committing, leaving everything else intact, run
```bash
   git reset --soft HEAD^
```
If we want to delete 'n' number of commit then run
```bash
   git reset --soft HEAD-num
   Ex: git reset --soft HEAD-3
```
If all you want to do is undo the act of committing, and also removing from the stagging area then run
```bash
   git reset HEAD^
```
And if you actually want to completely undo it, throwing away all uncommitted changes, resetting everything to the previous commit then run
```bash
   git reset --hard HEAD^
```
![App Screenshot](https://github.com/alaminbhuyan/Instruction-of-Git/blob/main/Images/git-level.png)

## git HEAD and undo theory
If you want to go back a particular previous commit
```bash
   git checkout commit_hash_id
   or
   git checkout HEAD-NUM
   EX: git checkout HEAD-3 (that means I want to back in third number commit)
```
If you want to go back a particular previous commit and then If we want to back at the last commit then run
```bash
   git checkout master or main
```

## git log command

If you want to see all the commit that you have done till then run.

```bash
  git log
```

If you want to see all the commit that you have done till in short way then run.

```bash
  git log --oneline
```
If you want to see a particuler number of commit then run

```bash
  git log -num
  Ex: git log -3
```

## Screenshots

![App Screenshot](https://github.com/alaminbhuyan/Instruction-of-Git/blob/main/Images/gitLog.jpg)

## git diff command

Shows the differences between the current state of your files and the last commit.


If you want to see all the commit that you have done till then run.

```bash
  git diff
```

For particular file

```bash
  git diff file_name
```

If we want to see the new add data after (add .) command than run

```bash
  git diff --staged [ Risk ]
```

If we want compare two commit than run

```bash
  git diff hash_id_of_first_commit hash_id_of_second_commit
```

## git show command

If we want to see the all changes under a commit than run

```bash
  git show hash_id
```

## git delete or remove files and folder

if you want to delete .git folder then run

```bash
  rm -rf .git
```

To delete or remove file thne run

```bash
  rm -r file_name
```
To delete or remove folder thne run

```bash
  rm -r folder_name
```
## git branch command

To create a branch

```bash
  git branch branch_name
```
To see all the branch

```bash
  git branch
```
To go one branch to another branch

```bash
  git checkout branch_name
```

To create a branch and go that branch at once run

```bash
  git checkout -b branch_name
```
To delete a branch run

```bash
  git branch -D branch_name
```
If we want to see last commit for all the branchs than run

```bash
  git branch -v
```
If we want to see list all remote branches

```bash
  git branch -r
```
If we want to see list all local & remote branches

```bash
  git branch -a
```

If we want to connect a branch with master branch or one branch to another branch than run

```bash
  git merge brance_name
```
If we want to delete any branch from GitHub then run

```bash
  git push origin --delete branch_name

  or

  git push origin --d branch_name
```
## Git branch practice link

[Click Here](http://git-school.github.io/visualizing-git/)

## git pull command

If you change anything on GitHub and you want to fetch those change in your local machine then run

```bash
  git pull

  or,

  git pull origin master or main
```
## git clone command

If you want to clone any repository then copy the repository link and open terminal then run

```bash
   git clone repository_link 
```
If you want to give new name of the project that you are going to download in your local machine then run

```bash
   git clone repository_link new_project_name
```

## git push command

If you want to push any change or repository then run

```bash
   git push origin branch_name
   or
   git push -u origin branch_name
```
If you want to push all branch then run

```bash
   git push --all
```
If you want to see git remote link then run

```bash
   git remote -v
```

## git --pretty=format command

In Git, you can use the --pretty=format option to specify the output format for various Git commands, such as git log or git show. This option allows you to customize the output and display the information in a specific format.

Here are a few commonly used placeholders that you can include in the format string:
```bash
	%H: Commit hash (full SHA-1)
	%h: Abbreviated commit hash
	%an: Author name
	%ae: Author email
	%ad: Author date (format respects the --date option)
	%s: Subject
```
```bash
	git log --pretty=format:"%h - %an, %ad : %s"
```
