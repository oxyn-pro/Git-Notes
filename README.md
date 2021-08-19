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

