Example setup to reproduce an issue when using lint-staged with git worktrees.

To reproduce:

  * Clone this repo, install deps (via yarn or npm)
  * Edit the abc.js file and commit the change -- note that lint-staged successfully runs
  * Create a git worktree: `git worktree add ../some-other-path`
  * cd into worktree: `cd ../some-other-path`
  * install deps (`npm install` or `yarn install`)
  * Edit the abc.js file and commit the change -- note that now lint-staged fails in "prepare" step
