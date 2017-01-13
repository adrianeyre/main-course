# Git Pong

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
