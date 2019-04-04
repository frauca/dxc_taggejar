# Test with git hub operations


## Operations performed


### Init project

init project

```shell
git init taggejar
git config user.name "roger"
gti config user.email "mi@mail.com"
```

### Add readme and put it on github

```shell
git add .
git commit -m "Adding a README.md before going to remote"
git remote add origin git@github.com:frauca/dxc_taggejar
git push -u origin master
```
### Add second remote


```shell
git remote add secondary git@github.com:frauca/dxc_taggejar_secondary
git push -u secondary master
```

### Make origin newer than secondary

```shell
git add .
git commit -m "make origin newr"
git push -u origin master
```

### Second person starts working on the project

Now we will work on features each one will work on its featrue

User 1

```shell
git branch feature/user1
git checkout feature/user1
git commit -m "This text will not be present on user 2"
```

### User 1 try to merge

User 1 will merge but it will have problems as the other user has make changes

Make changes and commit htem

```shell
git checkout feature/user1
git add .
git commit -m "user 1 make changes"
```
Try again the master checkout and the merge

```shell
git checkout master
git pull
```
No problems here

```shell
git checkout feature/user1
git merge master
```

resolve problems commit and hten merge an upload

```shell
git add .
git commit -m "resolve conflicts"
git checkout master
git merge feature/user1
git branch -d feature/user1
```