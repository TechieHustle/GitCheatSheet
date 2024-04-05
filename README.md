# GitCheatSheet
Contains Quick Reference for general Git tasks.

- `-u` or `--set-upstream`: `-u origin a_branch` or `--set-upstream origin a_branch` flags in any of the commands mean that we are setting the upstream reference branch for the current brach to `a_branch`.\\
  NOTE: `a_branch` branch can be a different name from the local branch name, but local will follow `a_branch` as the reference branch. 

#### Config
- List all the users: `git config -l` or `git config --list`.
- Set username and email: `git config user.name "Anurag Chandra"` and `git config user.email techiehustle.dev@gmail.com`
- After setting username and email, check `cat .git/config`.
