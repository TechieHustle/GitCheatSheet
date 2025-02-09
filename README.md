# GitCheatSheet
Contains Quick Reference for general Git tasks.

- `-u` or `--set-upstream`: `-u origin a_branch` or `--set-upstream origin a_branch` flags in any of the commands mean that we are setting the upstream reference branch for the current brach to `a_branch`.\\
  NOTE: `a_branch` branch can be a different name from the local branch name, but local will follow `a_branch` as the reference branch. 

#### Config
- List all the users: `git config -l` or `git config --list`.
- Set username and email: `git config user.name "Anurag Chandra"` and `git config user.email techiehustle.dev@gmail.com`
- After setting username and email, check `cat .git/config`.


#### Rebase
```
--- mainline 
             \ 
               --- feature-branch --- commit1 --- commit2 --- commit3
```
- Rebase everything in `feature-branch` to exact one commit:
  - Switch to `feature-branch`
  - `git rebase -i origin/mainline` it'll rebase it to remote mainline branch. `git rebase -i mainline` will rebase to mainline on local branch.
- Rebase such that we have last two commits (commit2 and commit3 in this case) as combined, `git rebase -i HEAD~2`.
- Rebase evenrything after commit1 `git rebase -i commit1`.
- The above two commands will result in `-- feature-branch --- commit1 --- commit-X`, commit-X has commit2 and commit3 in single one commit.

#### Revert
- `git revert --no-commit a69a6f0 d309de1 # revert in reverse order`
- `git commit -m "Revert GFD configs and QueueToEventListMap changes"`
