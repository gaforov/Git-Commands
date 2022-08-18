Git Commands
============

## Translated Versions

- [Versão em português](READMEpt.md)
- [Versión en español](READMEes.md)
- [Türkçe versiyon](READMEtr.md)
- [বাংলা সংস্করণ](READMEbn.md)

___

_A list of my commonly used Git commands_

_I copied this file from @joshnh and improved it with my own commands. If you want to see original you can view it
here: https://github.com/joshnh/Git-Commands_

*If you are interested in his Git aliases, have a look at his `.bash_profile`, found
here: https://github.com/joshnh/bash_profile/blob/master/.bash_profile*

--

### Getting & Creating Projects

| Command                                                           | Description                                 |
|-------------------------------------------------------------------|---------------------------------------------|
| `git init`                                                        | Initialize a local Git repository           |
| `git clone ssh://git@github.com/[username]/[repository-name].git` | Create a local copy of a remote repository  |

### Basic Snapshotting

| Command                                   | Description                                                         |
|-------------------------------------------|---------------------------------------------------------------------|
| `git status`                              | Check status (Detailed status)                                      |
| `git status -s`                           | Short status (Summarized status)                                    |
| `git add [file-name.txt]`                 | Add a file to the staging area                                      |
| `git add -A` OR `git add .`               | Add all new and changed files to the staging area                   |
| `git commit -m "[commit message]"`        | Commit changes                                                      |
| `git commit -a -m "[commit message]"` OR `git commit -am "[commit message]"` | Combine add all & commit changes together. This skips staging area. |
| `git rm [file-name.txt]`                  | Remove a file (or folder)                                           |
| `git rm [file1.txt file2.txt *.txt]`      | Remove multiple files (or folder)                                   |
| `git rm --cached -r [file1.txt]`          | Remove a file (or folder) from staging area                         |

### Branching & Merging

| Command                                              | Description                                             |
|------------------------------------------------------|---------------------------------------------------------|
| `git branch`                                         | List branches (the asterisk denotes the current branch) |
| `git branch -a`                                      | List all branches (local and remote)                    |
| `git branch [branch name]`                           | Create a new branch                                     |
| `git branch -d [branch name]`                        | Delete a branch                                         |
| `git push origin --delete [branch name]`             | Delete a remote branch                                  |
| `git checkout -b [branch name]`                      | Create a new branch and switch to it                    |
| `git checkout -b [branch name] origin/[branch name]` | Clone a remote branch and switch to it                  |
| `git branch -m [old branch name] [new branch name]`  | Rename a local branch                                   |
| `git checkout [branch name]`                         | Switch to a branch                                      |
| `git checkout -`                                     | Switch to the branch last checked out                   |
| `git checkout -- [file-name.txt]`                    | Discard changes to a file                               |
| `git merge [branch name]`                            | Merge a branch into the active branch                   |
| `git merge [source branch] [target branch]`          | Merge a branch into a target branch                     |
| `git stash`                                          | Stash changes in a dirty working directory              |
| `git stash clear`                                    | Remove all stashed entries                              |

### Viewing the staged/unstaged changes

| Command                                    | Description            |
|--------------------------------------------|------------------------|
| `git diff`                                 | Shows unstaged changes |
| `git diff --staged` OR `git diff --cached` | Shows staged changes   |

### Sharing & Updating Projects

| Command                                                              | <div style="width:400px">Description</div>                  |
|-------------------------------------------|-------------------------------------------------------------|
| `git push origin [branch name]`           | Push a branch to your remote repository                     |
| `git push -u origin [branch name]`        | Push changes to remote repository (and remember the branch) |
| `git push`                                | Push changes to remote repository (remembered branch)       |
| `git push origin --delete [branch name]`  | Delete a remote branch                                      |
| `git pull`                                | Update local repository to the newest commit                |
| `git pull origin [branch name]`           | Pull changes from remote repository                         |
| `git remote add origin ssh://git@github.com/[username]/[repository-name].git` | Add a remote repository                                     |
| `git remote set-url origin ssh://git@github.com/[username]/[repository-name].git` | Set a repository's origin branch to SSH                     |

### Viewing the History & Changes

| Command                                    | Description                                      |
|--------------------------------------------|--------------------------------------------------|
| `git log`                                  | Show full history of commits                     |
| `git log --oneline`                        | Show history (summarized version)                |
| `git log --summary`                        | Show history (detailed version)                  |
| `git log --reverse`                        | Lists the commits from the oldest to the newest  |
| `git log --oneline --reverse`              | Show summarized history in reverse order         |
| `git diff [source branch] [target branch]` | Preview changes before merging                   |

### Setup & Configurations

| Command                                      | Description                                                                                               |
|----------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| `git config --global -e`                     | Edit global configuration settings                                                                        |
| `git config --global diff.tool vscode`       | Use VS Code as a diff tool                                                                                |
| `git config --global difftool.vscode.cmd "code --wait --diff $LOCAL $REMOTE"` | VS Code waits and performs diff action on old and new copies of the file |
| `git difftool`                               | Show unstaged changes                                                                                     |
| `git difftool --staged`                      | Show staged changes                                                                                       |
