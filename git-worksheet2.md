---
title: "Git/GitHub Hands-On: Part 2"
output: pdf_document
fontsize: 12pt
---

Continuing where we left off...

## 4. User B

- Add a connection to User A's repository:

        git remote add userArepo git://github.com/userA/TestRepo

- Fetch User A's latest

        git fetch userArepo

- Create their version of the repository as a local branch:

        git branch userA userArepo/master

- In RStudio, switch to branch "userB" and test things

- Switch back to your master branch

- Merge the change from User A

        git merge userA

- Push to GitHub


## 5. Users A and B

- Make simulateneous changes, then add, commit, and push.

## 6. User B

- Switch to branch "userA"

- Pull User A's change from GitHub

        git pull userArepo master

- Go back to your master branch

- Merge the change from User A.

        git merge userA

- Fix the merge conflict; then add, commit, push.

- Make another pull request


## 7. User A

- Switch to branch "userB"

- Pull User B's changes

        git pull userBrepo master

- Review the changes

- Go back to your master branch

- Merge their changes your master branch

        git merge userB

- Push back to GitHub
