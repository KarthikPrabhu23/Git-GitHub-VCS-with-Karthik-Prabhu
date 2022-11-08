# Git, GitHub & Version control with Karthik Prabhu
Tutorial for Git, Github &amp; VCS for workshop at CEC.

## Chapter 1 :- ***Git*** set go 

**1. Downloading Git for Windows :-**

 [Git windows](https://gitforwindows.org/)
 
  Accept the options as they are, default settings are good enough.
  
  Before we start make sure `git --version` command successfully returns. If the output is something like **command not found** then please make sure Git is properly installed on your machine. My machine output is shown below. **Output on your machine might be different.**

```bash
git --version 
```
Output should be similar to:-
```
git version 2.36.1.windows.1
```

> **Commands that a user should type on his/her terminal are prefixed with the shell prompt symbol `$`. The output of command follows the command. Also, you don't have to type `$` on your terminal.**

  
 **2. Starting with Git :-**
 
 Once you have installed Git,
- Create a folder . Eg :- folder1
- Create a text file inside the created folder   
          E.g:- File1.txt
- Type something in the text file ‘File1’
- Save the file

- Right click on folder , select `Git Bash here`.
- The Git terminal will then open.

**2a. Configuring name & E-mail**

To configure your name & email to the folder , use 

```
git config --global user.name (your_name)
```

```
git config --global user.email (your_email)
```

Followed by your name & email

The command shown above populates a file named `.gitconfig` in your user home directory with configuration information.

```bash
$ cat ~/.gitconfig
```
```
[user]
	name = Karthik Prabhu
	email = karthikprabhu23223@gmail.com
[push]
	default = simple
```

**2b. init command & other basics**

   the `git init` command initializes your folder to the Git.
```
 git init
```
`ls` command lists all the files in the computer’s folder
```
 git ls
```

git status command provides the overview of the git

Time and again we will need to know status of our Git repository. By status what we mean is the current state of the repository. E.g., what needs to be added to the index, what needs to be committed, if there is any change that we have to commit, etc., This is the command that you will use the most.


Use `git status` to list all new or modified files that haven't yet been committed.
```
git status
```
`touch <filename>` command creates new files in the folder using git
```
touch file1.txt
```
**2C. Adding files to staging area**

`git add -A` command is used to add all files of the folder to the staging area.
```
git add -A
```
**2D. Commit files to Git**

`git commit -m “your message”` command commits your files from stage to Git

Once you have a smallest working change, you should commit it to your version control system. Smallest working change could be a test case, a small piece of functional code, a line or paragraph in your text file, etc. **You should commit often and daily.** Also, every commit should strive to do exactly one change.

After staging your changes, next step is to commit them into your local Git repository. To do that, we will use commit command as shown below.

```bash
 git commit -m "first commit"
```
Staging and committing are two different steps in Git. You can't commit a change until it has been staged. If you are working with a tracked file, then you can do both of these steps in a single command.

Edit your git file

Check the status of your repository. This time it will say it is a **modified** change.

