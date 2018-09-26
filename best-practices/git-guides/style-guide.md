# Git Style Guide
Focus on Feature Development

# Table of contents

1. [Branches](#branches)
2. [Commits](#commits)
3. [Pull Requests](#pull-requests)
4. [Code Review](#code-review)

## Branches

There's only one rule: anything in the master branch is always deployable.

Base

* Master branch: `master`
* Testing/QA branch: `stage`
* Development branch: `dev`

Naming

* Feature branch: `feat-*`
* Bug fix branch: `bug-(ticket #)`

Notes 

* Use dashes to separate parts
* Do not use bare numbers
* Avoid long descriptive names

Examples

* `feat-coursework`
* `feat-oauth`
* `bug-1234`

## Commits

* Commit early and often 
* Keep the messages short (30 character soft-limit)
* Prefix all commits with `add, update, remove, fix, refactor`
* Keep your branch up-to-date `git pull --rebase origin dev`
* Only push feature branch
* `feature` branch off `dev` only
* `bug` branch off `master`

##### Autosquash Commits 
1. `git commit --fixup <commit>`
2. `git rebase -i --autosquash HEAD~#`
3. `git push origin +<branch_name>`

## Pull Requests

After you clean & push your feature branch create a Pull Request (PR) and make sure to include a meaningful message about what you did. `feature` branches merge to `dev` and `bug` branches merge to `master`. `dev` merges into `stage `. Once `stage` passes acceptance merge it into `master`. All merges occure in the form of PR.  

[PR Message Template]()
  
## Code Review

Code reviews should:

* Verify code is an effective solution
* Ensure code is maintainable/documented
* Provide constructive feedback
* Not be onerous