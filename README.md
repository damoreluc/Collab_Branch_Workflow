# Collab_Branch_Workflow

Esercizio sul workflow collaborativo

## The problem

While it's nice and easy to onlt work on the master branch, this leads to some serious issues on teams!

* Lots of time spent resolving conflicts and merging code, especially as team size scales up

* No one can work on anything without disturbing the main codebase. How do you try adding something radically different in? How do you experiment?

* The only way to collaborate on a feature together with another teammate is to push incomplete code to master/main. Other teammates now have broken code...

## Feature Branches

Rather than working directly on master/main, all new development should be done on separate branches.

* Treat master/main branch as the official project history

* Multiple teamates can collaborate on a single feature and share code back and forth without polluting the master/main branch

* Master/main branch won't contain broken code, or at least, it won't unless someone messes up.

## Merging in Feature branches

At some point the new work on feature branches will need to be merged in to the master branch.

There are a couple of options for how to do this:

1. Merge _at will_ without any sort of discussion with teammates. Just _do it whenever you want_ .

2. Send an email or chat message or something to your team to discuss if the changes should be merged in.

3. **Pull Request!**

## Pull Requests

Pull Requests are a feature built in to products like Github % Bitbucket. **They are not native to Git itself**.

They allow developers to alert team-members to new work that needs to be reviewed. They provide a mechanism to approve or reject the work on a given branch. They also help facilitate discussion and feedback on the specified commits.

> I have this new stuff I want to merge in to the master branch... what do you think about it?

## The Workflow

1. Do some work locally on a feature branch
2. Push up the feature branch to Github
3. Open a pull request (or **PR**) using the feature branch just pushed up to Github
4. Wait for the **PR** to be approved and merged. Start a discussion on the **PR**. This part depends on the team structure.

## Merging PR with conflicts

Just like any other merge, **sometimes there are conflicts** that need to be solved when merging a pull request. This is fine. Don't panic.

You can perform the merge and fix the conflicts on the command line like normal, or you can use Github's interactive editor.

### On my Boss's local machine

My boss can merge the branch and solve the conflicts locally...

1. switch to the branch in question, say for example `my-new-feature`. Merge into it the `main` branch and resolve conflicts:

    ```
    > git pull origin main
    > git fetch origin
    > git switch my-new-feature
    > git merge main
    > fix manually conflicts!
    > commit all changes
    ```

2. switch to `main`. Merge into it the `my-new-feature` branch (now with **no** conflicts) and push changes up to Github:

    ```
    > git switch main
    > git merge --no-ff my-new-feature
    > git push origin main
    ```
