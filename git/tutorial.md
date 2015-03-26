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

        git remote add github https://github.com/<username>/new_repo.git

        git pull github master

        git push github master


   The command `git push` is a combination of `git fetch` and `git merge`
   Usually it is a good idea 


## A Pragmatic Workflow : Git Flow

1. Checkout http://nvie.com/posts/a-successful-git-branching-model/

- two branches **master** and **develop**

- Version number chages whenever **develop** merges into **main**

- feature_\* branches merge into **master** and hotfix_\* branches merge into **master**

- always merge with --no-ff

- use `git tag` to mark set version numbers


## Git further hints

- git has a lot of advanced commands

        blame, bisect, stash, branch

- a git aware prompt

        export GIT_PS1_SHOWDIRTYSTATE=true
        export export GIT_PS1_SHOWSTASHSTATE=true

- aliases for your ~/.gitconfig

        pl = pull
        ps = push
        ci = commit
        co = checkout
        st = status
        sy = !"git pl; git ps"

## Merging conflicts

- Check git status.
  Open files marked as conflicting.
  Inside the file check for `<<<<` markers.
  Resolve merge conflict by manually editing the text.
  Afterwards `git add` all conflicting files again.
  Finish conflict resolution with `git commit`.


