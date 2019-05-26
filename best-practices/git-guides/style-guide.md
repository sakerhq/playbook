# Git Style Guide
Focus on Feature Development

# Table of contents

1. [Branches](#branches)
2. [Commits](#commits)
3. [Pull Requests](#pull-requests)
4. [Code Review](#code-review)

## Branches

The `master` branch always stands as a branch that is production ready. Do not provision a `master` branch during initial stages of development.

Base

* Master branch: `master`
* Testing/QA branch: `stage`
* Development branch: `dev`

Naming

* Feature branch: `feat-*`
* Refactor branch: `refactor-*`
* Bug fix branch: `bug-(ticket #)`

Examples

* `feat-auth`
* `refactor-auth`
* `bug-42`

## Commits
 
* Keep the messages short (30 character soft-limit)
* Prefix all commit messages with `add, update, remove, fix, refactor`
* Keep your branch up-to-date `git pull --rebase origin dev`

##### Autosquash Commits 
1. `git commit --fixup <commit>`
2. `git rebase -i --autosquash HEAD~#`
3. `git push origin +<branch_name>`

## Pull Requests

After you clean & push your feature branch create a Pull Request (PR) and make sure to include a meaningful message about what you did. `feature` branches merge to `dev` and `bug` branches merge to `master`. `dev` merges into `stage`. Once `stage` passes acceptance merge it into `master`. All merges must occur in the form of PR.  

[PR Message Template]()
  
## Code Review

Code reviews should:

* Verify code is an effective solution
* Ensure code is maintainable/documented and follows basic architectural principles
* Provide constructive feedback
* Not be onerous