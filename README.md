
# Learn basic to intermediate Git


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

![App Screenshot]()


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

## git commit command

If you want to commit for particular change to track run

```bash
  git commit -m "Your message"
```

If you want to add and commit together then run

```bash
  git commit -am "Commit message"
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
## Screenshots

![App Screenshot]()

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

## git diff command

If we want to see the all changes under a commit than run

```bash
  git show hash_id
```

## git delete or remove files and folder

To delete or remove file thne run

```bash
  rm -r file_name
```
To delete or remove folder thne run

```bash
  rm -r folder_name
```
