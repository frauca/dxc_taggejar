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