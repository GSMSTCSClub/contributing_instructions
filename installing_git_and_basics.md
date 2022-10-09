# What is Git Anyways?

Git is version control software. It basically allows you to keep track of your code at different points in time (like Google Docs edit history). Git (in combination with other tools like GitHub) allows developers to work together in codebases.

Each saved snapshot of your code is called a commit. Frequent commits allow developers to navigate their codebases at different points in time, which can be very useful. For example, let's say some new code introduced a bug into a program. Developers can compare their current code with the code in previous commits to figure out what caused the bug and can even choose to rollback to a previous version (like Ctrl-Z but on steroids).

# Installing Git

Go to this website and download the installer for your OS
Click through each step, leaving the default options
Open up command prompt (windows) or terminal (Mac/Linux) and type in `git --version` (without the quotation marks). You should see something like `git version 2.25.1`.

If you see “command not found” or a similar error message, refer to
this [link](https://techdirectarchive.com/2022/07/12/git-command-not-found-how-to-fix-git-is-not-recognized-as-an-internal-or-external-command/#:~:text=If%20you%20opened%20Command%20Prompt,reopening%20it%20as%20an%20administrator.)

# Git Basics

### Initializing the repository
In your terminal, navigate to the directory with your code (use the `cd` command)
Initialize a git repository using the `git init` command

## Commiting
When you make changes to your code, you can commit (you don't have to commit too frequently, but more frequent commits are usually better)

First, add the changed files. You can figure out what files have been
changed by using the command `git status`

```bash
foo@bar:~$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        test.txt

nothing added to commit but untracked files present (use "git add" to track)
```

In this case, I've create the file `test.txt` but haven't added it yet.
To add it, I run `git add test.txt`.

```bash
foo@bar:~$ git add test.txt
```
Now, I can finally commit. Use the following command
`git commit -m "Commit message"`. Include a short commit message
to describe the changes.

```bash
foo@bar:~$ git commit -m "Add test.txt"
[master (root-commit) 61d527b] Add test.txt
 1 file changed, 1 insertion(+)
 create mode 100644 test.txt
```

**NOTE**: You may have to run the following commands before commiting:
```bash
foo@bar:~$ git config --global user.email "your email"
foo@bar:~$ git config --global user.name "your name"
```
