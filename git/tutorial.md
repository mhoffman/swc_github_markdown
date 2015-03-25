# Git Tutorial

## Create and Use a Repository

1. create a repository

    mkdir my_git_project
    cd my_git_project
    git init

1. create some files

    touch README.md LICENSE setup.py

1. add those files

    git add README.md LICENSE setup.py

1. make a commit

    git commit -m'Initial checkin of project files'

1. check that commit worked.

    git log


## Connecting with other repos

1. Head over to http://github.com and click on '+' in upper RHS to create new repository

1. git remote add github https://github.com/<username>/new_repo.git

1. git pull

1. git push


## A Stable workflow

1. Checkout http://nvie.com/posts/a-successful-git-branching-model/

- two branches **master** and **develop**

- Version number chages whenever **develop** merges into **main**

- feature_\* branches merge into **master** and hotfix_\* branches merge into **master**

- always merge with --no-ff

- use `git tag` to mark set version numbers
