---
title: Git/GitHub Hands-On
output: pdf_document
fontsize: 12pt
---

We'll work in pairs: **User A** and **User B**

## 1. User A

- Go to your GitHub account (let's assume it's
  `https://github.com/userA`) and create a new repository (let's call
  it "TestRepo")

- In the project you've been working so far, connect your local
  repository to GitHub. In shell, run:

        git remote add origin https://github.com/userA/TestRepo

- Push your local repository to GitHub

        git push -u origin master


## 2. User B

- Log into your GitHub account (let's assume it's `https://github.com/userB`)

- Fork user A's repository on GitHub: go to
  `https://github.com/userA/TestRepo` and click the "Fork" button.

- Clone _your_ version of that repository locally:

    1. in RStudio, "create a project" and choose "version control"

    2. choose "Git: clone a project from a Git repository"

    3. enter repository URL: `https://github.com/userB/TestRepo`


- Change a file, and another file

- Add and commit your changes

- Push the changes to GitHub: click on "up arrow" in the Git tab

- Make a pull request:

    - Go to _your_ version of the repository on GitHub
      (`https://github.com/userB/TestRepo`)
    - Click "Pull requests"
    - Click "New pull request"
    - Click "Create pull request"
    - Optionally add a comment
    - Click "Create pull request"


## 3. User A

- Connect to User B's repository:

        git remote add userBrepo https://github.com/userB/TestRepo

- Fetch the changes from User B:

        git fetch userBrepo

- Create their version of the repository as a local branch:

        git branch userB userBrepo/master

- In RStudio, switch to branch "userB" and check that you like the changes

- Switch back to your master branch

- Note that the files are in the state that _you_ left them.

- Merge their work into your master branch:

        git merge userB

- Push the work to GitHub.

- Make another change to the file; then add, commit, and push.
