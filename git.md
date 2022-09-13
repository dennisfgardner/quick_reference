# Git Quick Reference

Sometimes I want to add an empty directory to a repo, for example a data directory.
I want the empty folder to be created when the repo is cloned but the the content inside.
To accomplish this I create the directory and create a `.gitignore` file inside with the following content:

```sh
# Ignore everything in this directory
*
# Except this file
!.gitignore
```
