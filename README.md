# Experiments
a/b testing experiments repo

# Contributing to Experiments Repo

## Setting up your local environment

To get started, you will need to have `git` installed locally. Depending on
your operating system, there are also a number of other dependencies required.

Once you have `git` and are sure you have all of the necessary dependencies,
it's time to create a fork.

### Step 1: Clone

Clone the project [from GitHub](git@github.com:EverlyWell/experiments.git)

```text
$ git clone git@github.com:username/node.git
$ cd node
$ git remote add upstream https://github.com/nodejs/node.git
$ git fetch upstream
```

### Step 2: Branch

As a best practice to keep your development environment as organized as
possible, create local branches to work within. These should also be created
directly off of the `master` branch.

```text
$ git checkout -b my-branch
```

## The Process of Making Changes

### Step 3: Commit

It is a recommended best practice to keep your changes as logically grouped
as possible within individual commits. There is no limit to the number of
commits any single Pull Request may have, and many contributors find it easier
to review changes that are split across multiple commits.

Make sure to label your commits of type FRAURD (Fix, Remove, Add, Update, Refactor, Document).
Then provide a summary of the commit. What it does and why it is needed.

```text
$ git add my/changed/files
$ git commit -m "[Add] Summary of change"
```

Multiple commits often get squashed when they are landed. See the
notes about [commit squashing](#commit-squashing).

### Step 4: Rebase

As a best practice, once you have committed your changes, it is a good idea
to use `git rebase` (not `git merge`) to synchronize your work with the main
repository.

```text
$ git pull --rebase origin master
```

This ensures that your working branch has the latest changes from `EverlyWell/experiments`
master.

### Step 5: Push

Once you are sure your commits are ready to go, begin the process of opening a Pull Request by pushing your working branch to GitHub.

```text
$ git push origin my-branch
```

### Step 6: Opening the Pull Request

From within GitHub, open a new Pull Request.

Once opened, Pull Requests are usually reviewed within a few days

If a pull request does not require review, feel free to merge once the test launches and changes are complete.

### Step 7: Updating your local master

Change local development branches back to master.

Then rebase master to include recently merged commits.

```text
$ git checkout master
$ git pull --rebase origin master
```
