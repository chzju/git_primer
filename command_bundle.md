#### 初始化 ####
```
mkdir test_git_flow
cd test_git_flow
git init
touch README
git add README
touch version.properties
echo '1.0' > version.properties
git add version.properties
git commit -m 'first commit'
git remote add origin ssh://git@gitlab.lab.infra.mail:1046/chenhui/test_git_flow.git
git push -u origin master

git tag -a 0.1
git push origin 0.1

# 创建一个develop分支
git checkout -b develop master
git push origin develop

git checkout develop
touch a.js
echo '1' > a.js
git add a.js
git commit -m  "d1"
git push

echo '2' > a.js
git add a.js
git commit -m  "d2"
git push

```

#### feature for future release ####
```
git checkout -b myfeature develop
touch b.js
echo '1' > b.js
git add b.js
git commit -m  "myfeature1"
echo '2' > b.js
git add b.js
git commit -m  "myfeature2"
# merge back
git checkout develop
git merge --no-ff myfeature
git branch -d myfeature
git push origin develop

```

#### release branch ####
```
git checkout -b release-1.1 develop
echo '1.1' > version.properties
git commit -a -m "Bumped version number to 1.1"
git push origin release-1.1
# bugfix
echo '3' > b.js
git commit -a -m "bugfix:xxxxx"
git push
# 使用release branch发布到线上

# merge to master
git checkout master
git merge --no-ff release-1.1
git push
git tag -a 1.1
git push origin 1.1

git checkout develop
git merge --no-ff release-1.1
git push

git branch -d release-1.1
# 删除远程分支
git push origin --delete release-1.1
```


#### Hotfix branches 全部在本地修改 ####
```
git checkout -b hotfix-1.1.1 master
echo '1.1.1' > version.properties
git commit -a -m "Bumped version number to 1.1.1"
# fix bug
echo '4' > b.js
git add b.js
git commit -m "Fixed severe production problem"
# 发布到线上

# merge back
git checkout master
git merge --no-ff hotfix-1.1.1
git push
git tag -a 1.1.1
git push origin 1.1.1

git checkout develop
git merge --no-ff hotfix-1.1.1
git push
```