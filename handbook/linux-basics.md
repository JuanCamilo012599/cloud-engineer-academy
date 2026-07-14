# Linux Basics

## Commands Learned

### pwd
Shows the current directory I am working in.

### ls
Shows the files and folders inside the current directory.

### cd
Changes the current directory.

### cd ~
Takes me to my personal Linux home directory: /home/juan.

### cd ..
Takes me one level up to the parent directory.

### mkdir
Creates a new folder.

### touch
Creates a new empty file.

## Important Concepts

### Home Directory
My personal folder inside Linux.

Example:

/home/juan

### Absolute Path
A complete path starting from the root of the system.

Example:

/home/juan/cloud-engineer-academy

### Relative Path
A path based on where I am currently located.

Example:

If I am inside:

/home/juan/cloud-engineer-academy

Then:

cd journal

takes me to:

/home/juan/cloud-engineer-academy/journal

### Parent Directory
The folder that contains the folder I am currently inside.

It is represented by:

..

## Mistakes I Made

- I typed 1s instead of ls.
- I used cd - before having a previous directory.
- I tried to enter projects from inside journal, but projects was not inside journal.
- I accidentally created notes and projects inside /home/juan instead of inside cloud-engineer-academy.

## Lesson of the Day

Before running commands, I should ask myself:

1. Where am I?
2. What is inside this directory?

Useful commands:

pwd
ls

## File Commands

### touch
Creates a new empty file.

Example: touch notes.txt

### cat
displays the content of a file in the terminal.

Example: cat notes.txt

### echo
Prints text to the terminal. It can also write text into a file.

Example: echo "Hello Linux" > notes.txt

### >
Writes outpot into a file and overwrites the previous content.

### >>
Adds outpot to the end of a file without deleting the previous content.

### cp
Copies a file.

Example: cp notes.txt notes-backup.txt

### mv
Moves or renames a file.

Example: mv notes-backup.txt backup-notes.txt

### rm
Deletes a file

Example: rm delete-me.txt
Important: rm can permanently delete files, so I should use it carefully

### nano
A terminal-based text editor.

Save in nano: 
Ctrl + O
Enter

Exit nano:
Ctrl + X

## Git Notes From Day 2

### git add .
Stages all changes inside the current repository.

Example: git add .

### git add ..
Tries to stage the parent directory.

This failed because the parent directory was outside my Git repository.

### git commit -am
Stages and commits changes only for files that Git is already tracking.

Important:

git commit -am does not add brand-new files.

For new files, I need to use git add firts.

## Git Fundamentals

### git status
Shows the current state of the repository.

It tells me:
- What files changed
- What files are staged
- What files are untracked
- Whether the working tree is clean

### git diff
Shows the exact changes made before the staging.

### git diff --staged
Shows the exact changes that are staged and ready to be committed.

### git add
Stages files for the next commit.

Example: git add README.md

### git add .
Stages all changes inside the current repository.

### git commit -m
Creates a saved checkpoint with a message.

Example: git commit -m "add academy readme"

### git log --oneline --graph
Shows commit history in a short visual format.

### git restore
Discard unwanted local changes and returns a file to the last committed version.

Example: git restore README.md

### .gitignore
Tells Git which files or patterns to ignore.

Example:

*.log
.env

Before comitting, I should review my changes with:

git status
git diff
git diff --staged

This helps prevent bad commits and accidental mistakes.

## GitHub Connection

### Local Repository
A local repository is the Git project stored on my computer.

Example:
/home/juan/cloud-engineer-academy

### Remote Repository
A remote repository is the Git project stored on my computer.

Example:
github.com/JuanCamilo012599/cloud-engineer-academy

### origin
origin is the default name Git uses for the remote repository.

### git remote -v
Shows the remote repositories connected to my local project.

Example:
git remote -v

### git remote add origin
Connects a local repository to a remote repository for the first time.

Example:
git remote add origin git@github.com:username/repo.git

### git remote set-url origin
Changes the URL of an existing remote

I used this when my origin was set to HTTPS and I wanted to switch it to SSH

Example:
git remote set-url origin git@github.com:JuanCamilo012599/cloud-engineer-academy.git

### SSH Authentication
SSH allows my computer to authenticate with GitHub using a key pair.

Private key: id_ed25519

Public key: id_ed25519.pub

Important:

The private key should never be shared.
The public key is safe to add to GitHub.

### ssh -T git@github.com
Test if my SSH connection on GitHub works.

### git push -u origin main
Pushes my local main branch to GitHub and sets it to track origin/main

### origin/main
origin/main represents the main branch that lives on GitHub

## GitHub Lesson

A professional Git workflow is:

1. Make changes locally
2. Review changes with git status and git diff
3. Commit changes locally
4. Push commits to GitHub

After the first push, I can usually use:

git push

## GitHub Workflow and Sync

### git pull
Downloads new commits from the remote repository and updates my local branch.

I should usually run this before starting work.

Example:

git pull

### git push
Uploads my local commits to the remote repository on GitHub

Example:
git push

### Local branch
The branch on my computer

Example:

main

### Remote branch
The branch on GitHub

Example: origin/main

### Up to date
When Git says my branch is up to date with origin/main, it means my local branch and GitHub are both synchronized

### Ahead of origin/main
When Git says my branch is ahead of origin/main, it means I have local commits that have not been pushed to GitHub yet

### Behind origin/main
When Git says my branch is behind origin/main, it means GitHub has commits that my local machine does not have yet

### Sync Workflow

Before working:

git pull

After working:

git status
git diff
git add .
git diff --staged
git commit -m "clear message"
git push