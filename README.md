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
Note that secondary is now on a newer version of origin

### Second person starts working on the project

User 2 start working in the project

```shell
git clone https://github.com/frauca/dxc_taggejar.git
cd dxc_taggejar
git config user.name "roger2"
git config user.email "rfrauca@dxc.com"
git branch feature/user2
git checkout feature/user2
git add .
git commit -m "I have make something diferent from user 1"
```

User2 finish before the feature and merge to master

### Second user ends before its feature and commit to master

Look for changes on master

```shell
git checkout master
git pull origin
git checkout feature/user2
git merge master
```

Easy no changes.
```shell
git checkout master
git merge feature/user2
```

Another easy. A fast fordward merge.

upload and remove branch

```shell
git push origin master
git branch -d feature/user2
```

### Second person starts working on the project

User 1 is now on a previus release and a merge will be needed

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
### Modify on a report and push to server

git add .
git commit -m "send to server"
git push origin master

# Diferent branches 

Some changes for f4Changes on this one but not on the base one