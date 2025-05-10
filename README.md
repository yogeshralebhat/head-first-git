# To be sorted into chapters

git branch -m [branch-name] <new-branch-name>

git branch -d <branch-name>

git commit --amend -m <commit-message>

git diff

git diff --staged

git diff <branch-1-name> <branch-2-name>

git diff <old-commit-id> <new-commit-id>

git diff HEAD~n HEAD

git log

git log --all --pretty=oneline --abbrev-commit --graph

--pretty=oneline --abbrev-commit = --oneline

git merge <branch-name>

git mv <file-name> <new-file-name>

git mv <file-path> <new-file-path>

git reset --soft | --mixed | --hard <commit-id>

git restore <file-name>

git restore --staged | --cached <file-name>

git revert <commit-id>

git rm <file-name>

git rm -r <directory-name>

# Chapter 01

git init

git config [--global] --list

git config [--global] user.name <user-name>

git config [--global] user.email <user-email>

git add <file-name>

git commit -m <commit-message>

git status

# Chapter 02

git branch

git branch <new-branch-name>

git swith <branch-name>

git switch [-c | --create] <branch-name>

# Chapter 05
git clone <remote-repository-url>

git push

git config [--global] push.default simple

git remote

git remote -v

git remote -r

git push --set-upstream | -u remote-alias local-branch-name

# Chapter06

git clone URL folder-name

git pull

git fetch
- This command fetches all the new commits and branches from the remote repository
into the local repository. It also updates the remote tracking branches.
This command, however, does not make any changes to the local branches.

git branch -a | --all
- Lists all the branches including local branches and remote tracking branches
