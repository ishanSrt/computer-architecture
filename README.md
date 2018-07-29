# computer-architecture
Course Assignments for CS 301/311

# Setting up your fork
### Clone the repository
```
git clone https://github.com/ishanSrt/computer-architecture.git
```
### Fork the repository
Go to the link https://github.com/ishanSrt/computer-architecture and click on `fork this repo`

### Setup your fork locally
```
git remote add myfork <link to your fork>
```

# Pushing changes
### Set up a new branch
```
git checkout -b <new branch name>
```
### Add the required files
Whatever is needed for the assignment

### Commit
Write a commit description. The last line of the commit should be
```
Closes <full link to the issue>
```

### Pushing changes
Use
```
git push -f myfork <branch name>
```
to push the changes. Go to github, your fork and open a Pull Request first time you do this.

# Additional info
### Amending commit message
```
git commit --amend
```
### Squashing commits
Make only one commit for closing one issue.
If you already added one commit and then did additonal changes, then after adding the required
files, use this to squash the changes into previous commit
```
git commit -a --allow-empty-message -m '' && git reset --soft HEAD~2 &&
git commit --edit -m"$(git log --format=%B --reverse HEAD..HEAD@{1})"
```
This will squash the current changes with the previous one. Use `HEAD~3` to squash the current changes
and 2 previous commits. This will open an editor window with all your commit messages concatenated
and you can edit the commit message over here for the final squashed commit.

# Checking out other persons PR
Use https://www.google.com/search?client=safari&rls=en&q=git+checkout+a+pull+request&ie=UTF-8&oe=UTF-8

# Rebasing
Always do `git pull` on `master` branch and then checkout your branch, then `git rebase master` to
avoid merge commits as they are confusing.
