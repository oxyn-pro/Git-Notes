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
