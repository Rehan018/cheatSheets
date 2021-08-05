# Table of Contents :
- <b>[Setup](#setup)</b>
- <b>[Create](#create)</b>
- <b>[Local Changes](#local-changes)</b>
- <b>[Move or Rename](#move--rename)</b>
- <b>[Branches](#branches)</b>
- <b>[Update & Publish](#update--publish)</b>
- <b>[Merge](#merge)</b>

<hr />

## Setup

<p><b>Show Current Configuration<b></p>

```
git config --list
```

<p><b>Show Global Configuration<b></p>

```
git config --global --list
```

<p><b>Set User name<b></p>

```
git config --global user.name "[user_name]"
```

<p><b>Set User Email<b></p>

```
git config --global user.email "[user_email]"
```

## Create
<p><b>Clone from Sever<b></p>

```
git clone <URL>
```

<p><b>Create Local repo.<b></p>

```
git init
```

<p><b>Create Local repo. in Specific folder<b></p>

```
git init <directory>
```

## Local Changes
<p><b>See Changes in working repo.<b></p>

```
git status
```

<p><b>See Changes tracked files<b></p>

```
git diff
```

<p><b>See Changes of specific file<b></p>

```
git diff <file>
```

<p><b>Add all files to Staging<b></p>

```
git add .
```

<p><b>Add specific files<b></p>

```
git add <file1> <file2>
```

<p><b>Commit with messsages<b></p>

```
git commit -m "[messages here]"
```

<p><b>Commit with skipping Staging area<b></p>

```
git commit -am "[messages here]"
```

## Move || Rename
<p><b>Move or Rename file<b></p>

```
git mv <oldFile.ext> <newFile.etc>
```

## Branches
<p><b>List All Branch<b></p>

```
git branch
```

<p><b>Switch Branch<b></p>

```
git checkout <branch>
```

<p><b>Change Branch Name<b></p>

```
git -m <newName>
```

<p><b>Delete a Branch<b></p>

```
git -d <branch>
```

## Update & Publish
<p><b>List all Remotes<b></p>

```
git remote -v
```

<p><b>Add new Remote<b></p>

```
git remote add <name> <URL>
```

<p><b>Change Remote Name<b></p>

```
git remote rename <remote>
```

<p><b>Remove a Remote<b></p>

```
git remote rm <remote>
```

<p><b>Push to Server<b></p>

```
git push -u <remote> master
```

<p><b>Fetch from Server<b></p>

```
git pull <remote> master
```

## Merge
<p><b>Merge into Current Branch<b></p>

```
git merge <branch>
```

<p><b>List All merged Branches<b></p>

```
git branch --merged
```

