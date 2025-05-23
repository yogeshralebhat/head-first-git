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

# Chapter 06

git clone URL folder-name

git pull

git fetch
- This command fetches all the new commits and branches from the remote repository
into the local repository. It also updates the remote tracking branches.
This command, however, does not make any changes to the local branches.

git branch -a | --all
- Lists all the branches including local branches and remote tracking branches

git push -d remote-name branch-name
- This command will push the branch deletion.
This will first delete the remote branch and then delete the remote tracking brach.

git fetch -p | --prune
- In addition to what **git fetch** does, adding the -p (shorthand for --prune) flag
deletes the remote tracking branches if their remote counterpart branches are deleted.

# Chapter 07

* git blame file-name
This command helps to find the information related to changes made to the file.
The information includes who made the change, to what line, on which date, the message
used during commit and the id of the commit that introduced this change.

* git blame -s | --supress file-name
If you don't want to see author and timestamp information then use -s or --supress flag.

* git blame commit-id file-name
The git blame command, by default, will show changes to the file till the commit where
HEAD is pointing at.
For example:
git blame test.md
is similar to
git blame HEAD test.md

If you want to find the changes to the from a perticular commit then provide the ID
of that commit.
For example:
git blame b993dc7 test.md

* git grep search-string
The git grep command is used to search a given string in all the files that are
"tracked" by git. The git grep command will search the files in index and object database.

The git grep will not search in the files outside the repository or any untracked files
in the working directory.

Each line from the output of the git grep command will show the name of the file and 
the line that contains the given search string.
If the file contains more than one occurance of the search string then output will
list the file name multiple times along with the matching line.

* git grep "search string"
If the search string contains any spaces then enclose the whole search string in either
dobule quotes or single quotes.

* git grep -i | --ignore-case search-string
If you want to search the given string irrespictive of the case then use -i (or the
lognhand --ignore-case) flag.

* git grep -n | --line-number search-string.
If you want to see the line number along with the file name then use -n (or the
longhand --line-number) flag.

* git grep -l | --name-only search-string
If you want only the name of the files that contain the given search string then
use -l (or the longhand --name-only) flag.
When this flag is used, a file name will be listed only once even if the file 
contains multiple occurances of the search string.

You can ofcourse make use of different combinations of these flags based on 
your needs.

* git log -S search-string

* git log -S search-string file-name

* git log -p | --patch 

* git log -S search-string -p

* git log -S search-string -p --word-diff

* git log -S search-string -p --word-diff --oneline --graph

* git log -G search-string

* git log -G search-string -p --word-diff --oneline --graph

* git log --grep search-string

* git checkout commit-id

* git bisect start

* git bisect bad commit-id

* git bisect good commit-id

* git bisect reset

# Chapter 08

* git config --local section.key value

* git config --global --unset section.key

* git config --local --unset section.key

* git config --list

* git config --list --show-origin

* git config --global --list

* git config --local --list

* git config --global --list --show-origin

* git config --local --list --show-origin

* git config --global alias.name "expands to what"

# Appendix

- git tag command:
Tags, like branches, are also a named references to commits,
except that once they are created, they **never** move.
They are also stored as git's commit history.

Tags are created to make a note of "landmarks" in a project history.
For example:
    To mark a specific version of the software.
    To mark the fix of a particularly nasty bug.


- git tag tag-name
To create a tag provide a name to the git tag command.

The tag name rules are same as that of branch.
Tag name cannot have a space. If required replace with hyphen (-).
Tag name can also a forward slash (/) and / or a period (.).
Avoid creating tags with the name of branches. Instead use
names which signify the milestone.
For example:
    git tag v1.0.0

Creating a tag by providing only the tag name will create
a tag on the commit which HEAD is currently pointing to.

- git tag tag-name commit-id
If tag needs to be created for a perticular commit then
provide the id of that commit to git tag command.
For example:
    git tag v1.5.3 b3fc8de

- git tag -l | --list
To see all the tags from the commit history use -l
(shorthand for --list) flag.

**Synchronize tags with remote**
To push the tags to the remote use --tags flag
with the git push command.

To retrieve the tags from the remote use --tags
flg with git fetch / pull command.

**Serious Coding**
When a tag is created for a perticular commit then
that commit becomes reachable even if there is no
child commit or branch referring to that commit.


