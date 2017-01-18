# Git Pong

* [Makers Academy - Full GitPong Help] (https://github.com/makersacademy/course/blob/61d35818fa65f1e7acbaab634b31b5e78c9b5f13/pills/github_pong.md)

## Initial Local Git Set up
```shell
$ mkdir <New Folder>
$ cd <New Folder>

$ git init
$ touch README.md
$ git add .
$ git commit -m "Initial Commit"
```

## Initial GitHub Set up
* First create a new GitHub repository through the GitHub Website
```shell
$ git remote add origin <Repo URL>
$ git push -u origin master
```

## Setting up other contributors
```shell
$ git remote add <pair-partner> <URL-to-pair-partners-repo>
$ git pull <pair-partner> master
```

## Create a day branch
```shell
$ git checkout -b <Branch>
$ git push origin <Branch>
```

## Different pair partner
```shell
$ git checkout <day-one-branch>
$ git checkout --orphan <day-two-branch-name>
$ git reset --hard
```

## Commit any changes I've done
```shell
$ git add .
$ git commit -m "Commit informaion"
$ git push origin <branch>
```

## Pull any changes pair partner has done
```shell
$ git pull <pair-partner> <Branch>
```
