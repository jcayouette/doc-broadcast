# suse-publisher
Publishes documentation sources from remote repository branches to a local gh-pages branch.

Initial testing version

1. git clone <repo-a-url> tmp-repo
2. cd tmp-repo
3. git checkout <branch-in-repo-a>
4. git remote rm origin # not really needed
5. git filter-branch --subdirectory-filter <directory-to-move> -- --all
6. mkdir -p <target-path in="" repo-b="">
7. git mv -k * <target-path in="" repo-b="">
8. git commit
9. cd <path-to-local-repo-b> # clone it, if you didn't do already
10. Create a new branch and check it out
11. git remote add origin-tmp-repo <path to="" tmp-repo="">
12. git pull origin-tmp-repo <branch-in-repo-a>
13. rm -rf <path to="" tmp-repo="">
