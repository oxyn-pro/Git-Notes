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
git add remote origin <link_to_remote_repo>
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
