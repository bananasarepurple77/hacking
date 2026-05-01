# Git
Git allows you to save your code, as well as the history and changes you have done to your code. It also makes collaboration and working in teams on the same code simpler.

The Git system contains a lot of commands. Some of the most essential commands are:
```
git init    to create a new Git repository/project
git clone   to copy an existing git repository
git push    updates remote repository
git pull    get updates from remote repository
```
It is also possible to use a Git client that has a GUI for easier interaction (https://git-scm.com/downloads/guis).

### .git directory
Contains all information that is required for version control. It contains information about:
* commits
* the remote repository address
* a log and more.

A README file may contain a short explanation of the project, configuration and installation instructions, licensing information and more.

Example of git clone:
`git clone ssh://bandit27-git@bandit.labs.overthewire.org:2220/home/bandit27-git/repo`
Notice the port is specified.

### Finding information with a repository
`git log` shows us the commit log
`git show <commit>` will show us the content of a commit (When creating a public repository it is important to be aware of the information you push to it since changes and previous versions are saved. So sensitive data, like passwords, could still be retrieved).
