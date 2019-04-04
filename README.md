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


