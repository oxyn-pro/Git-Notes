# Git-Notes

### Create directory and setup git:
```
git init .
```
- Create a git repository in directory

```
git status
```
- Check status in order to understand which files are added to staging area and which are not, see branch and etc.

## Staging Area

#### Add to staging area:
```
git add <file_name>
```
- Add a specific file into staging area

```
git add .
```
- Add all files into staging area

```
git add -A
```
- Add every single file into staging area regardless of their location in git repository directory

#### Remove from staging area:
```
git rm --cached <file_name>
```
- Remove a specific file from staging area

```
git rm -r --cached .
```
- Remove all files from staging area

## Commits

#### Make commits:

```
git commit -m "Any message"
```
- Make a commit with message

```
git commit -a
```
- Make a commit with message

```
git log
```
- See commits history

```
git log --oneline
```
- See commits history (oneline: id of commit, name of commit)

#### Show difference
```
git show <commit_id>
```
- Show what kind of changes were added to the last commit comparing to before the previous commit.

```
git diff
```
- Show what the difference between current directory changes and what has been commit.

#### Discard changes

```
git restore <file_name>
```
- Discard all changes until the last commit in a specific file.

#### Change message of the last commit:

```
git commit --amend -m "Any message"
```
- Amend - make change in message (text) with given message and commit to the last commit.

## Remote repository (GitHub)

#### Mapp remote repo with local repo

```
git remote add origin <link_to_remote_repo>
```
- To connect local repository with remote repository (created repository)

#### Change branch from one branch to another

```
git branch -M main
```
- Change the name of the current branch (master) to main

#### Git Push to remote repository

```
git push -u origin main
```
- Pushing local repository commits to remote repository

```
git remote remove origin
```
- Removing an origin

```
git pull origin
```
- Pull changes from remote repository to local repository

## Configure SSH keys in order to permit access to change repository from a specific device.

#### 1) Generating the SSH key:
```
ssh-keygen -t ed25519 -C "your_email_address"
```
OPTIONAL: you can add passphrase (recommended)

#### 2) Adding the SSH key to the ssh-agent:
```
$ eval "$(ssh-agent -s)"
```
This means, start the ssh-agent in the background

- #### Adding the SSH private key to the ssh-agent:
```
ssh-add ~/.ssh/id_ed25519
```
#### 3) Adding the SSH key to GitHub account:
```
clip < ~/.ssh/id_ed25519.pub
```
Copies the contents of the id_ed25519.pub file to your clipboard

#### The next step is just inserting copied SSH to SSH section in GitHub account.

## Branches

#### Check branches

```
git branch
```
- To see current branch

```
git branch -r
```
- To see current remote branches

```
git branch -a
```
- To see all branches

#### Create, switch, delete branches

```
git branch <branch_name>
```
- Create a branch with particular name

```
git checkout <branch_name>
```
- Switch to a particular branch

```
git checkout -
```
- Switch to previous branch

```
git checkout -b <new_branch_name>
```
- It will create a new branch and automatically switch to that new branch

```
git delete -D <branch_name>
```
- Delete a particular branch

```
git merge <branch_name>
```
- Delete a particular branch

#### Rebase is useful when for example main branch was uptaded but the branch that you are working is not updated with main branche's commits, here rebase pulls main branch's changes into your working branch and the commits of your current branch stores in the top of the commit history when commits of main stores in buttom of history.

```
git pull --rebase origin main
```
- Pull and rebase main branch to current branch

```
git rebase --continue
```
- Continues rebase after fixing a conflict

#### NOTE: all commits with changes created in different branch will not be added/included in main branch
#### NOTE: In a company, the programmer never pushes to the main branch first, usually the programmer creates a new branch, adds all the features and creates a pull request, then someone reviews those changes, and then decides whether to push programmer's changes to the main branch or not.


#### Basic writing and formating syntax
https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax

#### Necessary guidline
https://github.com/git-guides/
